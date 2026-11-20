https://claude.com/resources/articles/a-field-guide-to-claude-fable-finding-your-unknowns
## 任务开始前
### Blind Spot Pass
  In these situations, you can ask Claude to help you find your unknown unknowns and explain them to you.
  I like to use the literal words “blind spot pass” and “unknown unknowns.”
  Giving it context on who you are and what you know is usually important for Claude to understand the best way to start collaborating with you.
#### Example Prompts
- “I'm working on adding a new auth provider but I know nothing about the auth modules in this codebase. Can you do a blind spot pass to help me figure out my relevant unknown unknowns and help me prompt you better.”
- “I don’t know what color grading is but I need to grade this video. Can you teach me to understand my unknown unknowns about color grading, so that I can prompt better?”
  
### Brainstorm and Prototype
It’s extremely valuable to identify and verbalize unknown knowns early during prototyping, because finding them out during implementation can be (relatively) expensive.
This helps me start with intent to define the project’s scope. Claude often finds high-value approaches I would have missed, and sometimes misses the forest through the trees. Brainstorming prevents me from **setting too narrow or too wide a scope**.
#### Example Prompts
- "I want a dashboard for this data but I have no visual taste and don't know what's possible. Make me an HTML page with 4 wildly different design directions so I can react to them.”
- “Before wiring anything up, make a single HTML file mocking the new editor toolbar with fake data. I want to react to the layout before you touch the real app."
- "Here's my rough problem: users churn after onboarding. Search the codebase and brainstorm 10 places we could intervene, from cheapest to most ambitious. I'll tell you which ones resonate."
  
### Interviews
In this case, I ask Claude to interview me about any unknowns or ambiguities. When asking Claude to interview you, try and give it context about your problem to guide its questions.
#### Example Prompts
- "Interview me one question at a time about anything ambiguous, prioritize questions where my answer would change the architecture."

### References
Give your agent something you really like. Give it more details.
#### Example prompts
- "This Rust crate in vendor/rate-limiter implements the exact backoff behavior I want. Read it and reimplement the same semantics in our TypeScript API client."

### Implementation plans
When I think I’m ready to implement, I tend to ask Claude to put together an implementation plan for me to review. The plan focuses on the parts that might be **most likely to change** such as data models, type interfaces, or UX flows. This allows Claude to surface things I might actually need to alter.
#### Example prompt
- "Write an implementation plan in HTML, but lead with the decisions I'm most likely to tweak with: data model changes, new type interfaces, and anything user-facing. Bury the mechanical refactoring at the bottom, I trust you on that part."
---
## 任务中
