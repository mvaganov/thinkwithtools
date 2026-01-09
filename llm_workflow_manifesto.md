# Part 1: How LLMs Change What It Means to be a Developer

## LLMs Hurt Understanding by Averting Testing
Understanding survives tool changes, failures, and novel problems, making it the most important commodity a software developer can have. Understanding in software development comes from testing: start with an expectation for technology, and then test the expectation by observing actual behavior.

The experimentation process should be familiar to developers. Make a guess, introduce inputs, observe outputs, and compare the results to expectations. This cycle of testing builds the practiced judgment and intuition that distinguishes programmers. It creates reliable progress. Mastery of this skill is an implicit professional expectation. This is how understanding is earned.

**LLMs, by their nature, unintentionally deemphasize testing. This is a mental hazard.** Little documentation about testing makes LLMs under-represent it in practice. Consistently good code from LLMs punishes skepticism. The medium makes a choice of convenience for you. It doesn't force understanding, so you must experiment intentionally.

## Use LLMs Early, Before You Code
LLMs are not just vending machines for code. The LLM should be used early, while scope is being defined. The tool can help you discover what you don't know. Confusion is a "Technical Debt" which compounds over time with repeated sub-optimal decisions.

Explain what you are trying to solve to the LLM, and ask it to help discover blind spots, weakness in expertise, or poor workflow. This could increase your abilities and improve your scope before you consider a line of code.

## Critique as Intelligence Augmentation
LLMs can help you test and experiment on your own thoughts, with critiques. A code review prompt could at the very least point out easy to miss mistakes in your writing. And in the best case, you could get actionable advice, sourced and adapted from intelligent training data you never would have discovered otherwise.

Remember that you can read and apply critical feedback at your own pace. You are free to disagree with any LLM suggestions. You can ignore or reframe any implied goals. You can choose how to use this tool as an engine for growth.

## Ownership
You must be aware that LLMs can unintentionally and confidently mislead users with bad knowledge. They optimize for plausible sounding output, not correctness in the real world. Premier LLMs can explain how their own technology *necessarily* causes this behavior.

As an LLM user, you need to be skeptical of LLM output. Bad advice is possible. Turn a new idea into a hypothesis, and test it early. How you respond to the new knowledge is your complete responsibility. Experiment on the new knowledge to understand it.

Once you understand, it becomes knowledge that you own. This is the basis of the Ownership that senior software developers encourage in their teams. Ownership means you can explain, modify, and debug code without the LLM. Hit "Commit", and you are known to own the code. If it breaks in production, "AI wrote it" is not an excuse. You are expected to want to fix it. If you can't explain it, don't commit it. Experiment until you own it.

## Summary
LLMs can produce code without understanding; growth belongs to developers who choose to earn it.

## Next Steps
"Part 2: Software Development Workflow with LLMs" is a list of tactics to get value out of LLMs in your programming workflow, while augmenting your intelligence as a developer, without needing a compute token budget afforded to software professionals.

"Part 3: Programming with LLM Gotchas and Anti-patterns" is a compendium of perverse incentives and specific warnings to help recognize LLM usage habits that harm software development.

---

# Part 2: Software Development Workflow with LLMs

## Have a Note Taking Strategy
* Interaction with LLMs will likely to flood you with information. Use electronic writing tools to help you remember thoughts, prioritize work, keep you safe from cognitive overload, and offer security by equipping you for self-audits of your own thinking and decision making.
* Text files using markdown (*.md) format are common for notes, and natively understood by LLMs. Other effective related tools/workflows for reducing cognitive overload include: TODO list apps, notes in an electronic calendar, emails to self, private chat with yourself, office document processors.
* Having written notes will help you gather context, and manage the context window of LLMs with Context Reset. This technique focuses LLM attention, and makes your project more portable across different LLMs.
```
Please produce a concise summary suitable for pasting into a new chat as fresh context.
```

## Formalize Your Agency
* Write down high level goals you understand for yourself. Including these in prompts will help the LLM craft responses specifically motivating to you. Without this personal intellectual grounding, you will be more susceptible to having your agency distracted or even hijacked by stray ideas you encounter. For example, when asking the LLM for critique, explicitly include:
```
Give no encouraging feedback unless it encourages {{my_goals}}
```
* In general, when you ask questions, include as much relevant context as you can. Include: intent, error messages, stack traces, software goals, concrete data, personal theories, and expectations. This context improves answer quality, often reduces the LLMs compute needs, and helps you learn by keeping your mind engaged.
* Before asking for a plan, write your own first draft and ask the LLM to critique it. If you ask the LLM to generate the first draft, it will never feel like your work, and that lack of ownership will corrupt the your workflow from the beginning. 
* Articulating your problems very clearly is an effective debugging technique called "Rubber Ducky Debugging". It can lead to additional insights, and sometimes help you answer your own questions, before even engaging the LLM.

## Specific Workflow Advice
* Start a new software project with a prompt like:
```
I'm starting a new project.
{{goals_for_project}}
{{relevant_personal_goals}}
{{relevant_context}}
{{first_draft_high_level_project_plan}}
Help me discover blind spots, weakness in expertise, or poor workflow that I can correct. My short term goal is to understand how to define a project scope that sets me up for success.
```
* Take notes on what the LLM discusses with you. Prioritize ideas that you want to follow up on later.
* Many software developers are (or feel) self-taught, and LLMs can provide great comfort by giving technical and academic explanations:
```
explain {{this_code_or_concept}} like I'm a junior developer
```
* Brainstorm how you can test new knowledge. If you can verify information quickly, like with a web-search, do it now. If you think of a more time consuming experiment to verify a new idea, write it in your notes so you can prioritize it. If you are unsure how to prove a new idea to yourself, ask the LLM:
```
I have just learned {{new_concept_or_idea}} and want to understand it more clearly. Please explain it more clearly. Offer ways that I can quickly verify or practice this understanding.
```
* If you decide to use a technology stack you are not fast or familiar with, ask the LLM for a minimal boiler-plate starting point for your project. Your power as a developer is expressed in the implementation/testing iterative loop, and LLM automation can help you get into that loop sooner.
* LLMs are excellent at debugging and explaining boiler-plate code examples because of abundant and high-quality tutorial documentation on the web. Ask questions about this kind of code, you will get great answers.
* If you don't have a clear path forward for writing code, consider Test Driven Development: writing Unit Tests before functionality. Ask an LLM to explain Test Driven Development if you need. LLMs are able to write Unit Tests quickly, which make project coding tasks very visible and more motivating. Example prompt:
```
Act as a Senior Software Architect and TDD Practitioner. Your goal is to write a suite of unit tests for a feature that has NOT been implemented yet. These tests will serve as the technical specification for the upcoming development.
### 1. Technical Environment
- **Language/Framework:** {{language_and_framework}}
- **Test Runner:** {{test_library}}
- **Mocking Strategy:** {{mocking_library_and_approach}}
### 2. Feature Specification (The "What")
- **Component Name:** {{component_name}}
- **Input Parameters:** {{input_definitions}}
- **Expected Return/Side Effects:** {{output_definitions}}
- **Business Logic Rules:** {{business_requirements_list}}
### 3. Interface Definition (The "How")
Use the following interface/signature as the foundation for the tests:
{{interface_or_stub_code}}
### 4. TDD Test Cases
Generate tests that cover:
- **Success Criteria:** Verify that the component fulfills the core business logic.
- **Input Validation:** Tests that ensure {{component_name}} handles invalid data according to specs.
- **External Dependencies:** Mock {{external_services}} and verify they are called with the correct parameters.
### 5. Output Requirement
Provide the complete test file code. Ensure the code compiles but expect all tests to fail (Red phase) until the implementation is written.
```
* LLMs can write unit tests for existing code, which can help maintain old functionality as you refactor or develop new code. You can ask the LLM generate a prompt that will generate unit tests for you:
```
Write a prompt that an LLM will use to generate automated unit tests for my code. Include variables I need to supply in {{Double Mustache}} format.
```
* If you need an algorithm that you don't know, describe what you need to the LLM, including programming language target, and any additional relevant context. Include an initial implementation if you can. Remember to experiment with the code, to prove it is valid, and take intellectual ownership of it.
* Before giving an LLM example code you have a question about, refactor it to use as few dependencies as possible. This is a general debugging technique called "Minimal Reproducible Example". Extra dependencies/files can distract/confuse the model.
* Don't assume LLM generated code is production ready, certainly not in the first pass. LLMs often prioritize functionality over security and maintainability. Review it like any other code.
* Testing code does not mean "it ran once without crashing", It means deliberately trying to falsify expectations, and the expectations of the LLM. If you can solve a bug yourself that you find while testing, you should do so.
* As of January 2026, most LLMs do not learn from mistakes after training. You should not feel obligated to explain a mistake to the LLM. Do explain that you solved the bug if you think the LLM can teach you something about your solution, or the bugfix might help the context of your current discussion.
* Ask the LLM for a code reviews; this is an extremely high leverage use of artificial intelligence:
```
Review this code as if you were a Senior Developer looking for style inconsistencies, potential bugs and edge cases, readability improvements, and performance bottlenecks.
```
* After a long session, especially one involving iteration over drafts, it's a good idea to start a new chat session. Software development discussions often involve superseded versions of text, resolved problems, and meta-reasoning about tangential scope, all of which does hurt the signal-to-noise ratio of discussions.
* Senior developers use LLMs differently because speed of typing and testing becomes the limiting factor instead of understanding and compute tokens. A junior developer should not assume responsibility for code-reviewing LLM agents if they don't understand the code being written or the full scope of the project.
* Judgement (using understanding to make a decision) remains a bottleneck for all developers, even when using LLMs. Focus on making judgement more efficient to dispense. Senior devs should use LLMs to automate testing and aggregate results. Junior devs should use LLMs to improve build time, runtime, and UX performance, so fast compile-test loops can quickly debug individual issues.
* Different models have different strengths and weaknesses, and are worth trying for different purposes. Ask your LLM to tell you about the current models of the day:
```
Act as an objective AI analyst. Compare the current leading LLM vendors, highlighting their distinct strengths, known weaknesses, and best-fit use cases.
```
* If one model gets stuck on your project, it's likely another model will not get stuck in the same way, because of differences in Model Weights.

---

# Part 3: Programming with LLM Gotchas and Anti-patterns

## Thinking Substitution
* Prompting for full solutions before understanding the problem --> outsources your intelligence, prevents you from forming transferable abstractions. Instead, keep your mind engaged by decomposing problems and asking the LLM to consider specifics with you.
* Using LLMs to avoid documentation entirely --> poorly considered logic and poor naming is technical debt, which will probably harm the project later. Write syntax to document itself, annotate with comments describing purpose and indented use.
* Accepting explanations without verifying behavior --> LLMs can and do hallucinate, seeming very confident as they do it. Be skeptical, and test the output, especially for something you didn't know before the LLM taught you. Replace "that sounds right" with "I observed it". Also, documentation could be incorrect, and an LLM could have no way of knowing.
* Accepting LLM abstractions --> LLMs write class hierarchies and patterns without understanding why they exist. Use your human experience to question LLM choices, and discuss those choices.
* Using LLMs to avoid reading primary sources --> LLMs are not perfect, are not always fully aligned with your goals, and can be confused. If you have access to primary source material, read it. It could be written by humans for humans, and might teach you better/faster/more-cheaply than an LLM.

## False Confidence
* Trusting green tests without reading code --> computer software, even LLMs, won't always do what you want. Assume ownership of code you commit, make sure it is what you want; let your wisdom be the final test.
* Assuming tests written by LLMs are meaningful --> automatically written tests do not always test actual intent, some tests can encode & perpetuate bugs. Audit tests to make ensure they test intent, not syntax, not a mirror of the implementation, and not enforcement of circumstances from a prototyping environment.
* Assuming code will work without testing on the target hardware --> LLMs are risky to use for writing software on poorly documented hardware. Mitigate that risk with additional testing.

## Poor Prompting
* More text improves an answer --> you can easily distracting LLMs from problem solving with noise. Context should improve signal, not noise.
* Debugging with insufficient description --> LLMs will spend lots of energy trying to generate missing context, and may solve the wrong problem, or hallucinate a solution to a problem that never existed to begin with. Provide as much context for technical problems as possible: error messages, stack traces, function intent, software goals, and concrete data.
* Iterating prompts instead of code --> it probably means you're avoiding uncertainty in the system. If you don't develop necessary understanding, you may never be able to correctly diagnose problems.

## Wasteful Interaction
* Repeated micro questions --> careless use of compute tokens has a negative impact on the LLM system. An LLM query on a premier LLM has real economic and environmental costs. Build a habit of developing questions that are worth asking.
* Syntax trivia --> LLMs are not as good (fast/efficient) at verifying code as a compiler running on your own computer. Use your own computer to answer questions wherever you can.
* Asking the same question with micro-edits --> like micro questions point, this squanders LLM resources. Be thoughtful about your question before you ask it. If you don't know what exact question you want to ask, explain your goal to the LLM and ask it to help you write the prompt.
* Asking questions without reading answers --> if you have a habit of avoiding reading, you should change that habit before you start interacting with LLMs. The most wasteful thing you can do with an LLM is ask it complex questions and do nothing with the answer.

## Three Hard Rules for LLM Use
* **Assume Conversations are Logged**. Data from your chats can conceivably be sold, or given to third party law enforcement. What you write into another company's LLM can possibly become public. Sanitize your context.
* **Don't Paste Secrets**. Putting API keys, database credentials, or proprietary PII (Personally Identifiable Information) into an LLM can lead to termination at many companies. Sanitize your context.
* **Don't Ship Unmodified LLM Output**. Intellectual Property law complexities make using exact copies risky. Create "transformative" work by making your own modifications.
