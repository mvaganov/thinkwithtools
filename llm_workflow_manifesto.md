# Using LLMs for Software Development

LLMs are the new normal in software development. This is a 3-part guide to develop programming habits for success in this new world, especially for less experienced software developers. This is not a guide to getting hired, it is a guide for how to think about programming with access to LLMs that write code for you.

## LLMs Distort the Importance of Testing
Understanding remains the most important commodity a software developer can have. Understanding in software development comes from testing: start with an expectation for code, and then test the expectation by observing actual behavior.

The experimentation process should be familiar to developers. Make a guess, introduce inputs, observe outputs, and compare the results to expectations. Over time, the cycle of testing builds the practical judgment and intuition that distinguishes programmers. It creates reliable progress. Mastery of this skill is an implicit professional expectation. This is how understanding is earned.

Testing skills are not automatically acquired, and they are not transferred by tools or simple reading material. They are developed through repeated practice and deliberate skepticism of assumptions. For software developers, testing is a core part of thinking, not as a secondary or deferrable step.

**LLMs, by their nature, unintentionally create the impression that testing is optional. This is a mental hazard.** Because software testing is highly situational, often tedious, associated with frustration, it is inconsistently documented. Under-representation in writing leads LLMs to under-represent it in practice. This is not intentional deception, it is a limitation of the medium.

Then, freely acquired working code seems to punish skepticism, further de-emphasizes the need for testing. The habit must be intentionally maintained in spite of that. A developer should not trade their own development of the most distinguishing strengths of a programmer for convenience.

## Use LLMs Early, Before You Code
The earliest phase of software development, gathering requirements, is disproportionately important to success of a software project. <details><summary>Even before any code is written, Understanding the Problem is critical to solving it.</summary> Defining scope is the most costly decision in the process (eg: a bug is about 10x cheaper to fix before the product is released; and it's 10x cheaper than that to design a bug out in the design phase; and it's 10x cheaper than that to eliminate the problem/solution spaces in the conceptual scope phase).</details> Because of this, the LLM should be used early in the process, to help recognize goals and define scope.

Use an LLM to explain things you don't understand. This is one of the highest leverage uses possible for an LLM. The knowledge gained from an LLM can quickly inform decisions, or be turned into real understanding with testing or even existing experience.

The value of understanding compounds over time, increasing your real capabilities. Similarly, the cost of confusion is a "Technical Debt" which also compounds over time, because sub-optimal decisions keep getting made. LLMs can address both of those by providing knowledge. Start accruing value from knowledge early.

## Ownership
You must be aware that LLMs can unintentionally mislead users with bad knowledge. These illusions from the LLM are not malicious. <details><summary>An LLM is a technical artifact that has unknowable and accidental flaws</summary> (eg: architecture of LLMs can cause them to hallucinate, confidently asserting things that are not true. LLMs can be mis-aligned on accident, which can happen with training data, system prompt, tools in the LLM's toolchain, unintentionally distracting context provided by the user, and more)</details>. As an LLM user, you should be skeptical of LLM output. Test it. Use it early. Turn the knowledge into a hypothesis, and test it.

How you respond to the LLMs knowledge is your complete responsibility. When you ask it for code, run the code to make sure it works for your intended purpose. Discuss with the LLM how you think the code works, as a test to verify your understanding. Experiment with refactoring the code. Rename variables, extract methods, change method signatures to fit your purpose.

Once you understand the knowledge, it is yours. It becomes knowledge that you own. That is the basis of the Ownership that senior software developers demand from their teams. Ownership means you can explain, modify, and debug code without the LLM.

Once you hit "Commit", you are the owner of that code. If it breaks in production, "the AI wrote it" is not an acceptable excuse. If you can't explain it, don't commit it. Experiment until you own it.

## Intelligence Augmentation
You can use LLMs to test and experiment on your own thoughts. Another extremely high leverage use of LLMs is getting critiques of your work. Developers of all levels will find value from a prompt like "Review this code as if you were a Senior Developer looking for style inconsistencies, potential bugs and edge cases, readability improvements, and performance bottlenecks."

At the very least, a prompt like that before a pull request can help find mistakes. And at best, the intelligence of millions of source files and technical papers might be distilled into actionable advice that which you would have never discovered otherwise.

It is impossible for a human to keep up with all of the useful knowledge on the internet. That is roughly the training data used by the premier LLM. That is a good source for finding insight that can help you improve.

I recommend that you explicitly ask the LLM to "avoid praise unless it [promotes specific goal of document being critiqued]." LLMs are often tuned to be overly encouraging to users, which can introduce noise into the critique, and guide you down an un-insightful path.

For junior developers, this insight can be overwhelming. When an LLM gives what feels like too much critical feedback, remember that you can read the feedback and apply it at your own pace. Instead of feeling overwhelmed, recognize the value of having clear goals, and context-aware suggestions that you are free to disagree with. Remember that an LLM is not an adversary or boss that is controlling you, it is a tool to help you think.

## Next Steps
The next part is "Software Development Workflow with LLMs", a list of tactics to get value out of LLMs in your programming workflow, while augmenting your intelligence as a developer, and without needing a compute token budget afforded to software professionals.

The last part is "Programming with LLM Gotchas and Anti-patterns", a compendium of perverse incentives and specific warnings to help recognize LLM usage habits that harm software development.

# Software Development Workflow with LLMs

# Programming with LLM Gotchas and Anti-patterns
