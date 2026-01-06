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
* Ask the LLM for a boiler-plate starting point for your project. Get that boiler-plate compiling and running ASAP.
* Ask the LLM to explain things in the boilerplate that you don't understand, and find tutorials/documentation online that give you additional context
* If you have trouble getting the boilerplate code working, ask the LLM to help you debug it with you. Describe your problem in detail, and provide exact error messages wherever possible.

## Use it to illuminate confusion
While you are deep in the middle of writing code and stuck on an algorithm:
* Describe the algorithm that you need to the LLM. Provide context specific to your project, including your initial implementation (code).
* Always try to give a simpler example of the code you have a question about, using as few dependencies as possible. Extra dependencies use up context window size, and that reduces the amount of intelligence the AI can apply to problem solving.

## Strengths of different LLMs (Jan 2026)
### ChatGPT
Great effort has been made to make ChatGPT the best LLM for chatting. This makes it excellent for discussing ideas. However, you need to be very aware that, especially in long conversations, it is likely to steer you in directions that 'feel good' rather than 'are correct'. Vibes seem to matter more than the end point, which can certainly be useful.
### Grok
Less filtered, and more 'punchy' than others. Grok seems to present more adversarial ideas with less prompting, which makes it excellent for seeking critical feedback.
### Claude
Focused on concise technical exploration. Use for code, and when you need to be correct.
### Gemini
Uses tight integration with Google search to be very well researched. Probably the best LLM (as of 2026), but should not be relied on as the only source of LLM feedback when varied perspective is helpful.

### Additional thoughts on LLM options
I have not used other LLMs enough to have a strong opinion. There will be disruption in this space soon, there always is.

## General tips for prompting
* Give a lot of context.
* If you don't know what you want, give the LLM your goals and ask the LLM to interview you to discover what you want.
* LLMs are not real intelligence. You don't need to feel justified to answer its questions or defend yourself against it's incorrect assertions.
* If you keep your mind engaged, your mind will grow stronger and you will be smarter.
* If you don't keep your mind engaged, your mind will atrophy, and you will be easier to replace with an LLM.
