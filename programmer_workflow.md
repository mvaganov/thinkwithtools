# LLM Workflow for Software Projects

## Use it early
Because of the nature of software development, the highest-leverage point of intelligence is earlier in the process (eg: a bug is always cheaper to fix before the product is released; and it's cheaper to design a bug out in the design phase; and it's cheaper to eliminate the problem/solution spaces in the conceptual phase). because of this, the LLM should absolutely be used early in the conceptual phase of software development.

tips for using LLMs for conceptual iteration:
* Do your own research and write your own first draft before asking the LLM to critique it. If you ask the LLM to generate the first draft, it will never feel like your work, and that lack of ownership will corrupt the your workflow from the beginning.
* provide a lot of context on the goals of the project early in your prompts. if you have a large amount of context, as the LLM to summarize it for you, edit that summary as needed, and provide it to the LLM during each interaction with it.
* when asking the LLM for critique, be sure to explicitly ask for no encouraging feedback *except for* feedback that will encourage you to fulfill the project's simple ultimate goal (as few goals as possible). make sure you have a clear understanding of the simple and ultimate goal(s) before you ask the LLM for feedback.
* Be ready to start over if the LLM helps you learn some important points that you didn't consider in your initial design. ask the LLM to summarize your best points from your existing work, and start over. this process is so much faster with machine tooling than without it, and the step-change in quality improvement is probably significant enough to justify a setback. Try it.

## Use it to launch you into productivity

once you feel good about the purpose and general design of your project, use the LLM to help start your project:
* ask the LLM for a boiler-plate starting point for your project
* ask the LLM to explain things in the boilerplate that you don't understand, and find tutorials/documentation online that give you additional context
* if you have trouble getting the boilerplate code working, ask the LLM to help you debug it with you. describe your problem in detail, and provide exact error messages wherever possible.

## Use it to illuminate confusion

while you are deep in the middle of writing code and stuck on an algorithm:
* describe the algorithm that you need to the LLM. provide context specific to your project, including your initial implementation. try to make a toy example of the implementation if you can, using as few dependencies as possible.

## Strengths of different LLMs (Jan 2026)
### ChatGPT
great effort has been made to make ChatGPT the most 'talkable' LLM. this makes it excellent for discussing ideas. However, you need to be very aware that, especially in long conversations, it is likely to steer you in a direction that 'feels good' more than a direction that is 'right for you'. vibes seem to matter more than the end point.
### Grok
less filtered, and more 'punchy'. Grok seems to present more adversarial ideas with less prompting, which makes it excellent for seeking critical feedback.
### Claude
focused on concise technical exploration. use it for programming. use it when you need to be right.
### Gemini
uses tight integration with google search to be very well researched. probably the best LLM (as of 2026), but should not be relied on as the only single source of LLM feedback when varied perspective is helpful.

### Additional thoughts on LLM options
I have not used other LLMs enough to have a strong opinion. there will be disruption in this space soon, there always is.
