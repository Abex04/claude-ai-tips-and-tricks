# Use XML Tags to Structure Complex Prompts

**Problem:** When a prompt has multiple parts -- instructions, background context, examples, and the actual question -- Claude can sometimes blend them together or lose track of which part is which, especially in longer prompts. This leads to answers that miss instructions or misread context as part of the question.

**Prompt / Technique:**

Wrap distinct parts of your prompt in simple XML-style tags so each piece is clearly separated:

<context>
You are reviewing a customer support ticket for a software company.
The customer is reporting that their exported CSV file is missing a column.
</context>

<instructions>
1. Identify the likely cause of the issue.
2. Suggest a first troubleshooting step for the support agent to try.
3. Keep the response under 100 words.
</instructions>

<ticket>
"Hi, I exported my report yesterday and the Region column is missing from the file. It was there last week. Can you help?"
</ticket>

**Why it works:** Claude is trained to recognize XML-style structure as a signal of intentional organization, not just prose. Tags like `<context>`, `<instructions>`, and `<ticket>` tell Claude exactly where one part of the prompt ends and another begins -- reducing the chance it treats background info as an instruction, or vice versa. This matters most as prompts grow longer or combine multiple types of content (data, rules, examples, questions) in one request.

**Example:**

Without tags, a long prompt mixing instructions and a document to summarize can cause Claude to accidentally follow instructions embedded in the document, or summarize your instructions along with the content. Wrapping the document in `<document>` tags and instructions in `<instructions>` tags reliably keeps them separate, even in prompts several paragraphs long.

**Tip:** Tag names don't need to be standardized -- `<data>`, `<context>`, `<rules>`, `<examples>` all work. What matters is consistency: use the same tag name when referring back to that section later in the prompt.
