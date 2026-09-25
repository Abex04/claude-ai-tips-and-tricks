# Be Explicit About Output Format

**Problem:** Without clear instructions, Claude has to guess how you want a response structured -- as prose, a list, a table, a specific length, a certain tone. The guess is often reasonable, but reasonable isn't the same as what you actually needed, especially when the output is going straight into a document, email, or another tool.

**Prompt / Technique:**

State the format you want directly, rather than leaving it implied. Be specific about structure, length, and tone where it matters.

Example prompt:

Summarize the key findings from this research paper.

Format:
- 3 bullet points, one sentence each
- No jargon -- write for a general audience
- End with one sentence on why this matters practically

**Why it works:** Claude will follow explicit formatting instructions much more reliably than it can infer implicit ones. "Summarize this" leaves length, structure, and audience all open to interpretation. Specifying bullet count, tone, or audience removes that ambiguity, so the first response is usable rather than something you have to ask Claude to reformat afterward.

**Example:**

Asking "explain how compound interest works" might return a few paragraphs of prose. Adding "explain it in exactly 3 steps, each under 20 words, as if teaching a teenager" produces a response shaped for a specific use case -- far more useful if you're dropping it into a slide, a script, or a short explainer, rather than reading it as-is.

**Tip:** If you're going to reuse a format repeatedly (e.g. always wanting 3 bullets + a takeaway line), save that instruction as a reusable snippet or prompt template rather than retyping it each time. See the `templates` folder for examples.
