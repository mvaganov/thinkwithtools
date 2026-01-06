# LLM Workflow for Software Projects

## Use it early
Because of the nature of software development, the highest-leverage point of intelligence is earlier in the process (eg: a bug is always cheaper to fix before the product is released; and it's cheaper to design a bug out in the design phase; and it's cheaper to eliminate the problem/solution spaces in the conceptual phase). because of this, the LLM should absolutely be used early in the conceptual phase of software development.

tips for using LLMs for conceptual iteration:
* Do your own research and write your own first draft before asking the LLM to critique it. If you ask the LLM to generate the first draft, it will never feel like your work, and that lack of ownership will corrupt the your workflow from the beginning.
* Provide a lot of context on the goals of the project early in your prompts. if you have a large amount of context, ask the LLM to summarize it for you, edit that summary as needed, and provide those concise goals to the LLM during each new interaction.
* When asking the LLM for critique, be sure to explicitly ask "give no encouraging feedback *except for* feedback that will encourage [the project's simple ultimate goal]". make sure you have a clear understanding of the project's simple and ultimate goal(s) before you ask the LLM for feedback.
* Be ready to start over if the LLM helps you learn some important points that you didn't consider in your initial design. Before you start over, ask the LLM to summarize your best points from your existing work, and then start over. This process is so much faster with machine tooling than without it, and the step-change in quality improvement is probably significant enough to justify a setback. Try it.

## Use it to launch you into productivity
Once you feel good about the purpose and general design of your project, use the LLM to help start your project:
* Ask the LLM for a boiler-plate starting point for your project. Get that boiler-plate compiling and running ASAP, and then read through it, line by line. Your power as a developer is expressed in the implementation/testing iterative loop, and LLMs can help you get into that loop sooner.
* Ask the LLM to explain things in the boilerplate that you don't understand, and find tutorials/documentation online that give you additional context. There are many good reasons that experts stress "fundamentals", so don't be afraid to use LLMs to polish these skills. "explain [this_code_or_concept] like I'm a junior developer"
* If you have trouble getting the boilerplate code working, ask the LLM to help you debug it with you. Describe your problem in detail, and provide exact error messages wherever possible.
* If you don't have a clear path forward, Test Driven Development is a solid approach (write tests before you write the functionality, ask an LLM to explain the term if you need). LLMs are often good at writing tests, which make project tasks very visible and even motivating. Give the LLM your context, and ask it to write tests in a Test Driven Development style.

## Build your own mental muscle
* Over-reliance on LLMs will reduce the strength of your own mind. Try to do the mental "lift" on your own first. When you feel stuck because you have tried your own solutions and there seems to be a magical piece of missing knowledge, that is a great time to prompt an LLM for help.
* If you are a hobbyist, you will use up your LLM compute tokens very quickly asking lots of small questions. You will get the more bang-for-your-buck by asking high-leverage questions with lots of context. Discard this bullet-point if you are being paid as a software developer, since the cost of an LLM query is trivial compared to even a junior developer's salary.
* If you don't want the LLM to use compute tokens answering a specific question for you, answer it first as part of the context for your prompt. This exercise of articulating your situation very clearly is an effective debugging technique called "Rubber Ducky Debugging", and can help you answer your own questions without the aid of the LLM.
* As you become a more skilled developer, understanding becomes less of a bottleneck. Senior developers will use LLMs differently (more often) because typing and testing speed becomes the bottleneck.

## NEVER use LLMs for certain things
* Pasting API keys, database credentials, or proprietary PII (Personally Identifiable Information) into a public LLM can lead to termination at many companies. Be responsible, sanitize your context.
* Your chats with LLMs are searchable by the companies providing the LLM service. Those companies can theoretically read and sell your data. Those companies can also be compelled by law enforcement or state and local governments to give up your de-anonymized data. It's best to keep that in mind. Don't share secrets with the LLM, or create the illusion of unethical behavior.

## Use it to illuminate confusion
While you are deep in the middle of writing code and stuck on an algorithm:
* Describe the algorithm that you need to the LLM. Provide context specific to your project, including your initial implementation (code).
* Always try to refactor example code you have a question about to use as few dependencies as possible. This is also a debugging technique called "Minimal Reproducible Example". Extra dependencies will distract the model, essentially hurting the signal-to-noise ratio of your prompt. More noise reduces the amount of intelligence the LLM can apply to actual problem solving.
* LLMs are can help you write test code, or at the very least, help you brainstorm what kind of tests you need to write. Writing Unit Tests in particular is a high-leverage use of LLMs.
* Ask the LLM for a code review: "Review this code as if you were a Senior Developer looking for style inconsistencies, potential bugs and edge cases, readability improvements, and performance bottlenecks." This can help you catch embarrassing mistakes, and offer insight into how your programming can improve.

## Strengths of different LLMs (Jan 2026)
These oversimplified descriptions will quickly become obsolete. You should try different models yourself, whatever the most popular models of the day are, to develop your own understanding. Also, if one model gets stuck on your project, it's likely another model will not get stuck in the same way, because of differences in model weights. Assume all models have been trained on computer programming, since it's known that training a model on programming improves their reasoning abilities.
### ChatGPT (OpenAI)
*The Generalist*, excellent at conversational reasoning and broad knowledge. It is capable at "logic puzzles" and breaking down abstract concepts. Best for brainstorming architecture, explaining difficult concepts ("Explain this like I'm 5"), and general debugging. If you need to have a back-and-forth conversation to understand why something works, start here.
### Grok
*The Skeptic*, has a less filtered personality. Best for adversarial testing. If you want a "second opinion" that might not align with the standard corporate-safe consensus, or you want to test how robust your logic is against a someone more critical.
### Claude (Anthropic)
*The Coder*, favored by developers for strict adherence to instructions and high-quality code generation. Best for complex refactoring, writing unit tests, and following very specific formatting rules. It tends to be less "chatty" and more precise with syntax than others. Also offers more Agentic features for programming (as of Jan 2026).
### Gemini (Google)
*The Researcher*, distinguishes itself with a massive context window and live internet integration. Best for "Read the Manual" tasks. Paste entire documentation libraries, massive files, or complete projects, and ask questions. Also excellent for checking if code uses up-to-date libraries versus deprecated ones.

### Additional thoughts on LLM options
I have not used other LLMs enough to have a strong opinion. There will be disruption in this space soon, there always is.

## General tips for prompting
* Give a lot of context.
* If you don't know what you want, give the LLM your goals and ask the LLM to interview you to discover what you want.
* LLMs can sometimes be very wrong. For example, LLM Hallucination can cause it to believe in API calls that don't exist. LLMs only understand APIs that were included in their training data set, and can suggest using deprecated API calls. LLMs don't have a context for the real world, and how software can have real negative impacts on physical reality (like robotics, or hardware prototyping). Verify that the code works before accepting it. Implement and test complex code incrementally when physical assets could be harmed by malfunction.
* LLMs are not real intelligence. You don't need to feel justified to answer its questions or defend yourself against it's incorrect assertions.
* If you keep your mind engaged, your mind will grow stronger and you will be smarter.
* If you don't keep your mind engaged, your mind will atrophy, and you will be easier to replace with an LLM.
* Spend real time with a problem (30 minutes is a good amount) before asking an LLM for an answer. If you build your own mental scaffolding, you will be more ready to *understand* the solution that the LLM gives you. And *understanding* is the price that must be paid.
* Senior devs care most about "ownership". Once you hit 'Commit', you are the owner of that code. If it breaks in production, 'the AI wrote it' is not an acceptable excuse.
