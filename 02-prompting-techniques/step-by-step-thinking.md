# Ask Claude to Think Step-by-Step Before Answering

**Problem:** For tasks involving reasoning, math, multi-part logic, or decisions with tradeoffs, Claude can sometimes jump straight to a final answer and skip steps that would have caught a mistake or produced a better-considered result.

**Prompt / Technique:**

Explicitly ask Claude to reason through the problem before giving its final answer. This can be as simple as adding one line to your prompt.

Example prompt:

A company has 3 warehouses. Warehouse A holds 1,200 units, Warehouse B holds 950 units, and Warehouse C holds 1,600 units. If demand this month is 3,000 units total, and shipping costs are lowest from Warehouse C, how should the company allocate shipments to minimize cost while meeting demand?

Think through this step-by-step before giving your final recommendation.

**Why it works:** Asking Claude to work through a problem before answering encourages it to break the task into smaller, checkable steps rather than pattern-matching straight to a plausible-sounding conclusion. This is especially valuable for arithmetic, multi-step logic, comparisons with tradeoffs, or any task where an intermediate mistake would silently produce a wrong final answer. Seeing the reasoning also makes it much easier for you to spot exactly where something went wrong, if it did.

**Example:**

For the warehouse problem above, asking for a direct answer might just return a plausible-sounding allocation. Asking for step-by-step reasoning first will typically show the constraints being checked explicitly (total demand vs. total capacity, cost-minimizing order) before committing to a final number -- making the reasoning visible and the answer more reliable.

**Tip:** For tasks where you only care about the final answer and want a shorter response, you can still ask Claude to "think it through internally, then just give me the final answer" -- getting the benefit of the reasoning without the long explanation in the output.
