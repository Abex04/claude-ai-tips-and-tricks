# Give Claude Examples of What You Want (Few-Shot Prompting)

**Problem:** Written instructions alone often leave room for interpretation. You might describe the tone, format, or style you want in detail, and still get responses that technically follow the instructions but miss the feel you were going for.

**Prompt / Technique:**

Instead of only describing what you want, show Claude 2-3 examples of the input/output pattern you're looking for, then give it the new input to follow the same pattern.

Example prompt:

Rewrite each product description to be short, punchy, and benefit-focused.

Input: "This blender has a 1200-watt motor and 6 speed settings."
Output: "Blend anything, fast. 1200 watts, 6 speeds, zero effort."

Input: "The backpack is made from water-resistant nylon with padded straps."
Output: "Rain-ready and shoulder-friendly. Built to keep up with you."

Input: "The desk lamp has adjustable brightness and a USB charging port."
Output:

**Why it works:** Examples remove ambiguity that words alone can't fully capture -- tone, length, structure, and style are all easier to demonstrate than describe. Claude picks up on the pattern across your examples (length, punctuation style, sentence rhythm) and applies it to the new input, often producing a much closer match to your intent than a written description would on its own.

**Example:**

Asking for "professional but friendly" emails can be interpreted many different ways. Providing one or two sample emails in that exact tone, then asking Claude to write a new one following the same style, produces far more consistent results than describing "professional but friendly" in the abstract.

**Tip:** 2-3 examples is usually the sweet spot. One example may not be enough to establish a clear pattern; more than 3-4 rarely adds much further improvement and just uses up context.
