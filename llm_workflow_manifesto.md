# Part 1: How LLMs Change What It Means to be a Developer

## LLMs Hurt Understanding by Averting Experimentation
Understanding survives tool changes, failures, and novel problems, making it the most important commodity a software developer can have. Understanding in software development comes from experimentation: start with an expectation for technology, and then test the expectation by observing actual behavior.

The experimentation process should be familiar to developers. Make a guess, introduce inputs, observe outputs, and compare the results to expectations. This cycle of testing builds the practiced judgment and intuition that distinguishes programmers. It creates reliable progress. Mastery of this skill is an implicit professional expectation. This is how understanding is earned.

**LLMs, by their nature, unintentionally deemphasize experimentation. This is a mental hazard.** Little documentation about testing makes LLMs under-represent it in practice. Consistently good code from LLMs punishes skepticism. The medium makes a choice of convenience for you. It doesn't force understanding, so you must experiment intentionally.

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

"Part 3: Programming with LLM Gotchas and Anti-patterns" is a compendium of perverse incentives and specific warnings to help recognize LLM usage habits that harm software development.

---

# Part 2: Software Development Workflow with LLMs

## Have a Note Taking Habit
Interaction with LLMs, like all software development, will push you to Cognitive Overload. You need to be practice managing cognitive load for your own mental safety. You will naturally expand cognitive limits through practicing thinking skills. If you aren't struggling, you aren't learning.

Electronic note taking takes immediate pressure off of your memory, allows you to list and prioritize ideas, supports visibility of goals over time, allows you to audit your own thinking process for improvement, and seamlessly stores information for transfer between LLMs.

When an LLM critique provides too much advice, write meaningful parts in your notes, and prioritize it. When you need to craft the perfect prompt for an LLM, write it in your notes where you won't accidentally hit submit before you're done. When you need to find context from something you were doing days ago, check your notes. When you need to refresh your LLM's context because your discussion has become to conceptually noisy, ask the LLM:
```
Please produce a concise summary suitable for pasting into a new chat as fresh context.
```
and save that result into your notes.

Use Markdown Format (*.md) text files for your notes, the simple standard already used by LLMs. Write it in any modern text editor. Other effective electronic note-takers include: private chats with yourself, emails to self, office document processors, and Personal Knowledge Management (PKM) software.

## Formalize and Focus On Your Agency
LLMs can only pursue goals that have been written down. Write down your high level goals, which you understand for yourself. Including these in prompts to help the LLM craft responses specifically motivating to you. Consider using these goals to reshape LLM compliments that would otherwise distract you and the LLM:
```
Give no encouraging feedback unless it supports {{my_goals}}.
```

If you need new writing from an LLM, write your own first draft and ask the LLM to critique it. If you ask the LLM to generate the first draft, it will never feel like your work, and that lack of ownership will corrupt the your workflow from the beginning.

When you ask questions, include relevant understanding you have as context. Include: intent, error messages, stack traces, goals, concrete data, personal theories, and expectations. This context improves answer quality, often reduces the LLMs generative compute needs, and helps you learn by keeping your mind engaged.

Articulating your thinking very clearly provides excellent context, and is also an effective debugging technique called Rubber Ducky Debugging. You can discover additional insight through personal reflection, and sometimes answer your own questions before even engaging the LLM. LLMs do this as Chain Of Thought. Humans do this as Journalism.

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
**Dramatically increase your comprehension by explaining it back** in your own words:
```
{{explanation_in_your_own_words}}
Is that correct? Prioritize corrective accuracy over conversational politeness.
```
Failure imprints learning better than success, so ask the LLM to preserve that signal.
* **Verify critical new information now**, with a web-search or another LLM. If the idea can be experimented on, prioritize testing it soon. You can also ask the LLM to help you:
```
I have just learned {{new_concept_or_idea}}. Offer a way that I can quickly verify or practice this understanding.
```
* **Describe the algorithm that you need but don't know**, including relevant context. Method signatures and initial implementation are an excellent starting point. Remember to experiment with the resulting code, to prove it is valid, and take intellectual ownership of it. You can also ask the LLM to write Unit Test code for your new algorithm.

## Automated Testing
* **LLMs can write unit tests for existing code**, which can help maintain old functionality as you refactor or develop new code. Ask the LLM to help you with generate unit tests.
* **Try Test Driven Development** if you don't have a clear path forward for writing code: writing Unit Tests before functionality. Discuss how to do this with your LLM.

## Debugging With LLMs
* **Refactor code to use as few dependencies as possible** before giving it to an LLM as example code. This is a generally helpful debugging technique called "Minimal Reproducible Example". Extra dependencies/files can distract/confuse the model.
* **Don't assume LLM generated code is production ready**, certainly not in the first pass. LLMs often prioritize functionality over security and maintainability. Review it like any other code. Take responsibility to start improving it yourself, as soon as you get it.
* **Testing code does not mean "it ran once without crashing"**. Deliberately try to falsify expectations, and the expectations of the LLM. Finding and solving a bugs as a form of experimentation is an excellent way to develop understanding.


* Ask the LLM for a code reviews; this is an extremely high leverage use of artificial intelligence:
```
Review the attached code as if you were a Senior Developer looking for style inconsistencies, potential bugs and edge cases, readability improvements, and performance bottlenecks.
```

### Use Different LLMs
* **Different models have different strengths and weaknesses**, and are worth trying for different purposes. Ask your LLM to tell you about contemporary models:
```
Act as an objective AI analyst. Compare the current leading LLM vendors, highlighting their distinct strengths, known weaknesses, and best-fit use cases.
```
* **Another model may not get stuck in the same way** because of differences in Model Weights.

---

# Part 3: Programming with LLM Gotchas and Anti-patterns


* Senior developers use LLMs differently than junior developers. For seniors, speed of typing and testing is the limiting factor instead of understanding and compute token use. A junior developer should not assume responsibility for code-reviewing LLM agents if they don't understand the code being written or the full scope of the project.
* Making Decisions remains a bottleneck for all developers, at all times, even when using LLMs. Focus on making decisions more efficient to make. Senior devs should use LLMs to automate testing and aggregate results, so decisions can be made in batches, with lots of data. Junior devs should use LLMs to improve build time, runtime, and UX performance, so fast compile-test loops can quickly expose individual issues, and help iterate on understanding at the same time.

## LLM Usage Anti-patterns

### Thinking Substitution
* *Prompting for full solutions before understanding the problem*. This outsources your intelligence, preventing you from forming transferable abstractions. Instead, keep your mind engaged by decomposing problems, and ask the LLM to consider specifics with you before generating code.
* *Using LLMs to avoid documentation entirely*. Poorly considered logic and poor naming is a distraction from problem solving, which will harm the LLMs understanding as well as yours. Rewrite LLM generated syntax to document itself with intent written into variable names and methods, and annotate code with comments describing purpose and indented use.
* *Accepting explanations without verifying behavior*. LLMs can and do hallucinate, seeming very confident as they do it. Build a habit of skepticism because it helps you learn. Replace "that sounds right" with "I observed it".
* *Accepting LLM abstractions*. LLMs write class hierarchies and patterns without understanding why they exist. Use your human experience to question LLM choices, and discuss those choices with the LLM to change abstractions.
* *Using LLMs to avoid reading primary sources*. LLMs are not perfect, are not always fully aligned with your goals, and can be distracted or confused. If you have access to primary source material, read it; it could be written by humans for humans, and might teach you better/faster/more-cheaply than an LLM.

### False Confidence
* *Assuming tests written by LLMs are meaningful.* Automatically written tests do not always test actual intent, some tests can encode & perpetuate bugs. Audit tests to ensure they test intent, not syntax, not a mirror of the implementation, and not enforcement of circumstances from a prototyping environment.
* *Trusting green tests without reading code*. Computer software, even LLMs, won't always do what you want. Infuse your tests with as much of your wisdom as possible if they become a potential source of false-positives.
* *Assuming code will work without testing on the target hardware*. LLMs don't understand poorly documented hardware. Mitigate that risk with incremental roll-out of new code, and additional testing.

### Poor Prompting
* *More text improves an answer*. You can easily distract LLMs from problem solving with noise. Context should improve signal, as information relevant to your goals and the state of your problem.
* *Debugging with insufficient description*. LLMs will spend lots of energy trying to generate missing context, and may solve the wrong problem, or hallucinate a solution to a problem that never existed. Provide as much context for technical problems as possible: error messages, stack traces, function intent, software goals, and concrete data.
* *Iterating prompts instead of code*. You're avoiding understanding the system that you're building. Develop better understanding so you can correctly diagnose problems.

### Wasteful Interaction
* *Repeated micro questions*. Careless use of compute tokens has a negative impact on the LLM system. Wasteful LLM effort has real economic and environmental costs, build a habit of developing questions that are worth asking.
* *Syntax trivia*. LLMs are not as good (fast/efficient) at verifying code as a compiler running on your own computer. Use your own computer to answer syntax questions wherever you can.
* *Asking the same question with micro-edits*. You don't know what exact question you want to ask is. Explain your goal to the LLM, and ask it to help you write the correct prompt.
* *Asking questions without reading the answer*. You are too distracted to engage your mind with the LLM. Take a step back and address what is really distracting you, the LLM will still be here when you are done.

## Three Hard Rules for LLM Use
* **Assume Conversations are Logged**. Data from your chats can be easily recovered. It could be be sold, or given to third party governments or law enforcement. What you write into another company's LLM can possibly become public. Don't write things you can't justify.
* **Don't Paste Secrets**. Putting API keys, database credentials, or proprietary PII (Personally Identifiable Information) into an LLM can lead to termination at many companies. Sanitize your context.
* **Don't Ship Unmodified LLM Output**. Intellectual Property law complexities make using exact copies risky. Create "transformative" work by making your own modifications to LLM results.
