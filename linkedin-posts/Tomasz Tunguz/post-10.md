I've been using state-of-the-art models to teach small models running on my computer how I work.

My personal agent, based on Pi, runs my inbox, my deal pipeline, my blog publishing, my calendar, & my research. It looks less like a chatbot & more like a small operating system.

Three layers do almost all of the work.

The first is QMD, a local markdown knowledge base of about eighty workflow files. Before answering any procedural question, the agent searches QMD for the right playbook.

The second is Skills — atomic SKILL.md files that describe one job each. The skills are written by a frontier model. So are the evaluations that grade them. The same system writes, tests, & rewrites each skill until accuracy converges.

The third is the Agent Loop, a model running Plan → Tool Call → Observe → Refine, calling out to seventeen Rust APIs.

The technique I've started to use is skill distillation. A frontier model — Opus 4.7, GPT-5.1, Gemini 3 Pro — authors the skill files. A smaller model — Qwen 35B or Gemma 26B running locally — executes them. The teacher transfers procedural knowledge to the student through markdown.

This is fundamentally different from classical knowledge distillation, instruction tuning, or RAG.

Skill distillation retrieves procedures. The smaller model doesn't have to know how to evaluate a company. It just has to know how to follow the steps.

The frontier model becomes a teacher. The library becomes the company's institutional knowledge. The student becomes whichever model happens to be cheapest this quarter.

Full post : https://lnkd.in/gefHkbtz
