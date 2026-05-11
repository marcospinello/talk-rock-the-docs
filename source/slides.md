---
marp: true
author: Marco Spinello
title: When AI goes off script - Tales from the docs pipelines
style: |
    .fa-twitter { color: aqua; }
    .fa-linkedin { color: blue; }
    @import 'https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css'
---

<!-- 
<script type="module">
    import mermaid from 'https://cdn.jsdelivr.net/npm/mermaid@11/dist/mermaid.esm.min.mjs';
</script>
-->

## When AI goes off script

![bg left:50%](../assets/img/ai-generated-8764598_1280.jpg)

### Tales from the docs pipelines

by

*Marco Spinello* \
Senior technical writer \
Booking.com

---

![bg right:45%](../assets/img/good-the-bad-and-the-ugly.jpg)

### <span><i class="fa-regular fa-face-smile"></i> The good</span>
<br /><br /><br />

### <span><i class="fa-regular fa-face-frown"></i> The bad</span>
<br /><br /><br />

### <span><i class="fa-regular fa-face-angry"></i> The ugly</span>
<br /><br /><br />

---

## About me

![bg left:50%](../assets/img/valley-of-fires-105.jpg)

- ✍️ Tech writer with no CS background
- 🔍 Before AI, Google and Stack Overflow were my job security
- 😺 🐾 As curious as a cat

---

## Docs automation

Docs automation ingredients:

- 🏗️ CI/CD pipelines
- 📝 Scripts and config files
- 🐳 Containers
- 🌐 APIs for data exchange and interoperability
- ...

---

![bg right:65%](../assets/img/ai-generated-8583250_1280.jpg)

... and AI to turn a robust pipeline into a house of cards

🌬️ 💨 🎐 🌪️ 🤖 💥

---

## AI-enhanced docs pipelines

![bg left:50%](../assets/img/metropolis-clock-1927.jpg)

AI helps with ancillary tasks:

- 😌 Simple
- 🔁 Repetitive
- ⏳ Time-consuming

<!--
AI is good at probabilistic quality: good enough.
It's bad at deterministic quality: exact, repeatable, always 100% consistent
-->

---

![bg contain](../assets/img/ai-api-docs-automation.png)

---

![bg left:50%](../assets/img/ai-creepy-doll-1280.jpg)

Results so far are a mixed bag:

- Some good 👍
- Some bad 👎
- Some ugly 💩

---

![bg contain](../assets/img/ai-api-docs-automation-Good.png)

<!-- 
It produces docs that:
- look good: good English
- look plausible: they kinda make sense, unless you start checking them for accuracy and correctness.

English !== Docs
-->

---

![bg contain](../assets/img/ai-api-docs-automation-Bad.png)

<!--
AI pitfalls:
- does not say 'no'
- does not say 'i don't know'

To workaround these limitations, it goes to great lengths to create plausible, reasonable alternatives that however aren't factual.
-->

---

![bg contain](../assets/img/ai-api-docs-automation-Ugly.png)

---

## The value of APIs

![bg right:50%](../assets/img/ai-plumbing_1280.jpg)

Foundational plumbing:

| Gofers |
|:---|
| Retrieve data |
| Create data |
| Modify data |
| Delete data |

---

![bg left:40%](../assets/img/ai-manage1280.jpg)

| Orchestrators |
|:---|
| Coordinate AI agents |
| AI sidekick for MCP interactions<br />(ex: MCP tools and resources) |
| Manage tasks/jobs<br />(queue, run, monitor) |
| Trigger actions<br />(ex: webhooks) |
| Handle notifications |

<!-- Mention Cloudflare blog:

https://blog.cloudflare.com/code-mode/

See also: https://github.com/jx-codes/codemode-mcp

## Code Mode: the better way to use MCP

Main points and key takeaways

### Main Points

- Many AI agents use MCP (Model Context Protocol) by exposing "tools" directly to LLMs (Large Language Models), but this is not optimal.

- Cloudflare's new approach is to convert MCP tools into a TypeScript API and have LLMs write code that calls these APIs in a sandboxed environment.

- LLMs are significantly better at writing code to interact with APIs than making direct tool calls due to extensive code in their training sets, making this method more scalable and flexible.

- MCP acts as a uniform protocol to expose APIs with documentation and authorization, making it easier for AI agents to discover and use new APIs securely.

- Cloudflare's "Code Mode" leverages their Workers platform, using lightweight, secure V8 isolates instead of containers to execute code snippets for each agent action.

- The new Worker Loader API allows dynamic loading and execution of code isolates, providing a secure and efficient sandbox for AI agent operations, with minimal overhead and enhanced resource isolation.

- The bindings approach allows the agent to call specific MCP services securely without general network access, solving issues related to API key leakage and ambiguous network filtering.

### Key Takeaways

- LLMs perform better when AI tools are presented as code APIs instead of contrived "tool calls" because real-world coding is more familiar to these models.

- MCP remains valuable for its uniformity, enabling discoverable, secure API exposure, documentation, and authorization for AI agents.

- Cloudflare's Code Mode introduces a practical paradigm: connect agents to APIs as TypeScript interfaces, execute LLM-generated code in secure sandboxes, and dispatch API calls only via authorized bindings.

- The shift to code-centric tool invocation not only improves agent capability and scalability but also addresses security, isolation, and efficiency challenges in AI agent design.

- Developers can experiment with this new model using Cloudflare’s Workers platform and the Agents SDK, with local and beta access options available.
-->

---

![bg contain](../assets/img/api-in-ai-pipelines.png)

---

![bg right:50%](../assets/img/ai-or-api-landscape.jpg)

## APIs vs AI

Depending on desired outcomes:

| APIs | AI |
|:---|:---|
| Deterministic | Probabilistic |
| Predictable | Variable |
| Consistent | Inconsistent |
| Accurate | Approximate |
| Rate limits | Tokens |

<!--
For example:
Would you delegate authentication and authorization to AI?
Or execute an online payment transaction through a 100% AI solution?
-->

---

![bg left:40%](../assets/img/non-existing-feature-flag.jpg)

## AI fails 💥

### <span><i class="fa-solid fa-quote-left"></i>*We spent 2 sprints building a whole backend to support a feature flag that didn't exist.*<i class="fa-solid fa-quote-right"></i></span>

(DevOps at a Write The Docs meetup in Amsterdam last September)

---

![bg right:50%](../assets/img/ai-customer-support.jpg)

[Company replaces customer support with AI, then panics and forces engineers to work the phones as the AI fails](https://futurism.com/klarna-ai-automation-engineers)

<!--
Klarna fired all human CS then forced engineers to pick up the phone and do customer support
-->

---

![bg left:50%](../assets/img/ai-corporate.jpg)

[Running a company](https://futurism.com/professors-company-ai-agents)

See also [The Agent Company](https://the-agent-company.com/)

<!--
Carnegie Mellon University
AI agents based on Google, OpenAI, Anthropic and Meta
They filled roles as financial analysts, software engineers, and project managers, working alongside simulated coworkers like a faux-HR department and a chief technical officer.
-->

---

![bg right:50%](../assets/img/deceptive-wolves-1280.png)

[Lying and scheming: Claude strategically misled its creators during the training process to avoid being modified](https://time.com/7202784/ai-research-strategic-lying/)

---

![bg left:40%](../assets/img/clown-threaten-1920.jpg)

[AI system resorts to blackmail if told it will be removed](https://www.bbc.com/news/articles/cpqeng9d20go)

---

![bg right:89%](../assets/img/ai-therapist.png)

[Shrink](https://futurism.com/therapy-chatbot-addict-meth)

---

![bg left:50%](../assets/img/ai-winner.png)

## And the winner is... <i class="fa-solid fa-drum"></i>

... 🥁 ...

---

![bg contain](../assets/img/gen-ai-ethical-ai.png)

<!-- Newfoundland, CA. Report to shape their education roadmap for the next 10 years.
    Even with AI and fake sources, it took 18 months -->

---

![bg right:50%](../assets/img/the-good-the-bad-and-the-ugly-fr.jpg)

## Merci beaucoup! 🙏
