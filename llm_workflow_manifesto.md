# Part 1: How LLMs Change What It Means to be a Developer

I'm a software development teacher of over 20 years. I've taught thousands, and brought hundreds on a journey to real software development mastery. And recently, I have noticed young developers falling into dangerous intellectual traps with LLMs. This guide is what I think you need to know to navigate this new world of LLMs while becoming expert software developers.

## LLMs Hurt Understanding by Averting Experimentation
Understanding survives tool changes, failures, and novel problems, making it the most important commodity a software developer can have. Understanding in software development comes from experimentation: start with an expectation for technology, and then test the expectation by observing actual behavior.

The experimentation process should be familiar to developers. Make a guess, introduce inputs, observe outputs, and compare the results to expectations. This cycle of testing builds the practiced judgment and intuition that distinguishes programmers. It creates reliable progress. Mastery of this skill is an implicit professional expectation. This is how understanding is earned.

**LLMs, by their nature, unintentionally deemphasize experimentation. This is a mental hazard.** Little documentation about testing makes LLMs under-represent it in practice. Consistently good code from LLMs punishes user skepticism (because the code does work correctly). The medium makes a choice of convenience for you. It doesn't force understanding, so you must experiment intentionally.

## Use LLMs Early, Before You Code
LLMs are not just vending machines for code. The LLM should be used early, while scope is being defined. The tool can help you discover what you don't know (eg: ask an LLM to explain dense terms from this guide). Confusion is a Technical Debt which compounds over time with repeated sub-optimal decisions.

Explain what you are trying to solve to the LLM, and ask it to help discover blind spots, weakness in expertise, or poor workflow. This could increase your abilities and improve your scope before you consider a line of code.

## Critique as Intelligence Augmentation
LLMs can help you test and experiment on your own thoughts, with critiques. A code review prompt could at the very least point out easy to miss mistakes in your writing. And in the best case, you could get actionable advice, sourced and adapted from intelligent training data you never would have discovered otherwise.

Remember that you can read and apply critical feedback at your own pace. You are free to disagree with any LLM suggestions. You can ignore or reframe any implied goals. You can choose how to use this tool as an engine for growth.

## Ownership
You must be aware that LLMs can unintentionally and confidently mislead users with Hallucination. They optimize for plausible sounding output, not correctness in the real world. Premier LLMs can explain how their own technology necessarily causes this behavior.

As an LLM user, you need to be skeptical of LLM output. Bad advice is possible. Turn a new idea into a hypothesis, and test it early. How you respond to the new knowledge is your complete responsibility. Experiment on the new knowledge to understand it.

Once you understand, it becomes knowledge that you own. This is the basis of the Ownership that senior software developers encourage in their teams. Ownership means you can explain, modify, and debug code without the LLM. Hit "Commit", and you are known to own the code. If it breaks in production, "AI wrote it" is not an excuse. You are expected to want to fix it. If you can't explain it, don't commit it. Experiment until you own it.

## Summary
LLMs can produce code without understanding; growth belongs to developers who choose to earn it.

## Next Steps
"Part 2: Software Development Workflow with LLMs" is a list of strategies and tactics to get value out of LLMs in your programming workflow, while augmenting your intelligence as a developer, without needing a compute token budget afforded to software professionals.

"Part 3: Programming with LLM Gotchas and Anti-patterns" is a compendium of perverse incentives and specific warnings to help recognize LLM usage habits that can harm software development.

---

# Part 2: Software Development Workflow with LLMs

## Have a Note Taking Habit
Practice managing cognitive load for your own mental safety. Interaction with LLMs, like all software development, will push you to Cognitive Overload. You will naturally expand cognitive limits through practicing thinking skills. If you aren't struggling, you aren't learning.

Electronic note taking takes immediate pressure off of your memory, allows you to list and prioritize ideas, supports visibility of goals over time, allows you to audit your own thinking process for improvement, and seamlessly stores information for transfer between LLMs.

When an LLM critique provides too much advice, write meaningful parts of it in your notes, and prioritize it. When you need to craft the perfect prompt for an LLM, write it in your notes where you won't accidentally hit submit before you're done. When you need to find context from something you were doing days ago, check your notes. When you need to refresh your LLM's context because your discussion has become to conceptually noisy, ask the LLM:
```
Please produce a concise summary suitable for pasting into a new chat as fresh context.
```
and save that result into your notes.

Use Markdown Format (*.md) text files for your notes, the simple standard already used by LLMs. Write it in any modern text editor. Other effective electronic note-takers include: private chats with yourself, emails to self, office document processors, and Personal Knowledge Management (PKM) software.

Keep a running list of side project ideas and problems that you wish you could automate. As your software development automation skill improves, these projects will start to look more like low-hanging fruit. A time will come when defining the problem to solve is the hardest part of solving the problem.

## Focus On Your Agency
Context is the greatest source of agency you have as an LLM user to influence the quality of LLM output. When you need results, write your intent, purpose, and goals. Give relevant examples. Keep the signal-to-noise ratio high by avoiding distracting information.

Write down your high level goals, beyond this project. Include these in prompts, to help the LLM craft responses specifically motivating to you. Use these goals to reshape LLM compliments that would otherwise be a distraction:
```
Give no encouraging feedback unless it supports {{my_goals}}.
```

If you need new writing from an LLM, write your own first draft and ask the LLM to critique it. If you ask the LLM to generate the first draft, it will never feel like your work, and that lack of ownership will corrupt the your workflow from the beginning.

When you ask questions, include relevant understanding you have as context. In addition to goals and intent, include: error messages, stack traces, concrete data, personal theories, and expectations. This context improves answer quality, can reduce the LLMs generative compute needs, and helps you learn by keeping your mind engaged.

Articulating your thinking very clearly provides excellent context, and is also an effective debugging technique called Rubber Ducky Debugging. You can discover additional insight through personal reflection, and sometimes answer your own questions before even engaging the LLM.

## Starting By Understanding
* **Try starting a new software project with a prompt** like:
```
I'm starting a new software development project.
{{goals_for_project}}
{{relevant_personal_goals}}
{{relevant_context}}
{{first_draft_high_level_project_plan}}
Ask me questions to help me discover blind spots, weakness in expertise, or poor workflow that I can correct. Help me define a project scope that sets me up for success.
```
* **Ask the LLM for a minimal boiler-plate starting point** if you decide to use a technology stack you are not familiar with. Your power as a developer is expressed in the implementation/testing iterative loop, and LLM automation can help you get into that loop sooner. Read through the starting point code and ask questions about what you don't know, LLMs are well trained on intro tutorials.
* **Ask an LLM for new knowledge** like this:
```
Explain {{this_code_or_concept}} like I'm a junior developer. Give brief, clear answers that include all key details. Be concise but informative.
```
If you don't know the right question to ask, explain your goals to the LLM, and ask it to help you write the correct question.
* **Dramatically increase your comprehension by explaining it back** in your own words:
```
{{explanation_in_your_own_words}}
Is that correct? Prioritize corrective accuracy over conversational politeness.
```
Failure is better for learning than success, so ask the LLM to preserve that signal.
* **Verify critical new facts, now**. Use a web-search to find primary sources, or another LLM to corroborate. If the idea can be experimented on, prioritize testing it soon. You can ask the LLM to help you:
```
I have just learned {{new_concept_or_idea}}. Offer a way that I can quickly verify or practice this understanding.
```
Learning before doing will organize your mind and prepare your awareness, which is required for long-term mastery.
* **Describe the algorithm that you need but don't know**, including relevant context. Method signatures and initial implementation are an excellent starting point. Remember to experiment with the resulting code, to prove it is valid, and take intellectual ownership of it. Once you have clear expectations, consider asking the LLM to help you write Unit Test code, a formal proof of working to expectations.

## Debugging With LLMs
* **Refactor code to use as few dependencies as possible** before giving it to an LLM as example code or context. This is a generally helpful debugging technique called "Minimal Reproducible Example". Extra dependencies/files can distract/confuse the model.
* **Testing code does not mean "it ran once without crashing"**. Deliberately try to falsify expectations, and the expectations of the LLM. Finding and solving bugs is a form of experimentation, an excellent way to develop understanding.
* **More compile time feedback means better context**. Using Strongly Typed Languages and Linters is better for debugging with LLMs.

## Automated Testing
* **LLMs can write unit tests for existing code**, which can help maintain old functionality as you refactor or develop new code. Ask the LLM to help you with generate unit tests for your project.
* **Try Test Driven Development (TDD)** if you don't have a clear path forward for writing code. TDD means writing Unit Tests before functionality. Discuss how to do this with your LLM.
* **LLMs can find some blind-spots in tests** if prompted to do so.
```
Act as a malicious QA engineer. What inputs or failures would break this logic that current tests don't cover?
```

## High Leverage Prompts
* **Ask the LLM to help you understand what code does**. You can always ask `What does this file do?`, and also consider asking `Trace the lifecycle of user data, where does validation happen?` A prompt like this can mitigate hours of manual text searches and focus your experimentation.
* **Ask the LLM for a code review**:
```
Review the attached code as if you were a Senior Developer looking for style inconsistencies, potential bugs and edge cases, readability improvements, and performance bottlenecks.
```
You can also setup smaller coding models on a local computer, to avoid submitting private information to a service on the internet.
```
Guide me through setting up local LLM on my computer, so that I can do code reviews.
```
* **Pre-mortem theory crafting** can inform and improve software design.
```
Where does this design assume latency or user input will stay benign, and in a small range? What circumstances could break those assumptions? How could the software be changed to mitigate these failure cases?
```

### Try Different LLMs
* **Different models have different strengths and weaknesses**, and are worth trying for different purposes. Ask your LLM to tell you about contemporary models:
```
Act as an objective AI analyst. Compare the current leading LLM vendors, highlighting their distinct strengths, known weaknesses, and best-fit use cases.
```
* **Another model may not get stuck in the same way** because of differences in Model Weights.
* **A of habit to trying new LLMs every few weeks will be regularly rewarded** because of how rapidly global industries are advancing LLM technology.

---

# Part 3: Programming with LLM Gotchas and Anti-patterns

## Elevating AI Slop
AI Slop is sloppy content created by generative AI. Slop Code may be functional, but probably not robust or maintainable. A developer elevates LLM output by identifying value in generated code, extracting it, and composing intentional software with it. The capability to do this is rooted in understanding of the problem space, and understanding the generated code.

## Outsourcing Understanding
* **Don't assume LLM generated code is production ready**, certainly not in the first pass. LLMs often prioritize functionality over security and maintainability. Review it like any other code. Take responsibility to start improving it yourself, as soon as you get it.
* **Be extremely careful about LLM code for novel platforms**. LLMs don't understand poorly documented software or novel hardware. Mitigate that risk with incremental roll-out of new code, and additional testing.
* **Automatically generated documentation** will be much higher quality if augmented with human insight. Be sure to review documentation, prune auto-generated fluff, and insert meaningful context. Code should document itself with intent written into variable names and methods, with purpose/indented-use annotated with comments.
* **Orchestrating Agentic LLMs** by delegating tasks in parallel can dramatically improve developer productivity. This is not safe for beginners; LLM agents doing all thinking work will deny you learning opportunities, and leave you clueless when things break. When using Agentic workflows, be ready to cannibalize Slop Code for value and start over later. If you are ready to attempt an agent workflow with these risks in mind, ask your LLM to guide you:
```
How can I delegate a software development tasks to an LLM? Be sure to explain how "agents.md" fits into the process.
```
* **Experiment to gain understanding of LLM agent's capabilities**. Start by delegating well-understood tasks that you can scrutinize yourself, so you can establish a baseline of behavior. Examples to start with:
```
Replace all debug print statements with proper logging.
```
```
Identify deprecated function calls, and research replacements. Submit a pull request for each one.
```
```
Review documentation in the code and make sure it describes code behavior accurately.
```
Find the limits of the agent's capabilities by asking for successively more difficult tasks. Take each task's success or failure as an opportunity to learn by asking questions and experimenting on new knowledge.
* **Use LLM Agents to do non-programming work on your local computer**. Examples: organize photos and videos, delete old temporarily generated files, find and delete duplicate files, summarize & analyze old logs and texts.
```
I want to use an LLM to do {task_on_my_local_computer}. Explain how I can do that.
```
You can save hours or days of personal time this way, while also practicing the technology.

## Thinking Substitution Hazards
* **Accepting sub-optimal LLM abstractions** will result is poorly written software. LLMs write class hierarchies and patterns without truly understanding why they exist. Do not assume the LLM is correct. Use your understanding to question LLM choices. Provide better choices later as context.
* **Assuming tests written by LLMs are meaningful** risks false positives from tests that don't test actual intent, and instead encode or perpetuate bugs. Audit tests personally to ensure they test intent, not syntax, not a mirror of the implementation, and not enforcement of circumstances from a prototyping environment. Infuse your tests with as much of your wisdom as possible.

## Prompting Mistakes
* **Adding more text to improve an answer** can easily distract LLMs from problem solving with noise. Context should be information relevant to your goals and the state of your problem. LLMs often respond better when prompts are concise and relevant.
* **Debugging with insufficient description** will force LLMs to spend more energy trying to generate missing context. Incorrect context may direct the LLM to solve the wrong problem. Provide technical context for technical problems: error messages, stack traces, function intent, software goals, and concrete data.
* **Iterating prompts instead of code** probably means you're avoiding understanding the system that you're building. This is the path to Slop Code.
* **Repeated micro questions**, **micro-edits to the same question**, and **asking questions without reading answers** are careless uses of your time. If you don't know what question to ask, explain your goals to the LLM and ask for help forming a question.

## Special Considerations for Industry
* **Assume Conversations are Logged**. Data from your chats can be easily recovered, and be privately sold or publicly released. Be cautious about sharing sensitive data with any service on the internet.
* **Don't Ship Unmodified LLM Output**. Intellectual Property law complexities make using exact copies risky. Create "transformative" work by making your own modifications to LLM results.

## Summary
I agree with Pablo Picasso, who said "Bad artists copy, great artists steal". I would clarify: Experiment until you own it.