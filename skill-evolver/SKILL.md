---
name: skill-evolver
description: "Automatic skill evolution engine: skill-creator (eval) + AutoResearch (iteration) + multi-gate + memory. Modes: evolve/eval/create/benchmark/improve. Triggers on natural-language requests to optimize, improve, tune, evaluate, benchmark, or create a skill. EN: '/skill-evolver', '/evolve', 'optimize this skill', 'optimize my skill', 'improve this skill', 'make this skill better', 'tune this skill', 'use skill-evolver', 'use skill-evolver to optimize', 'run skill-evolver on', 'evaluate this skill', 'benchmark skills', 'create a new skill', 'auto-optimize'. ZH: '优化这个 skill', '优化 skill', '帮我优化', '帮我优化这个 skill', '帮我调一下 skill', '用 skill-evolver 优化', '用 skill-evolver 调一下', '让这个 skill 变强', '改进 skill', '改进这个 skill', '创建 skill', '新建 skill', '自动优化', 'skill 评测'."
---

# Skill Evolver (FishSerrie autonomous version)

This is the **full autonomous skill evolution engine**.

For complete scripts, references, agents and eval tooling, install from upstream:

```bash
bash /root/.grok/skills/skill-installer/scripts/install-skill.sh --repo FishSerrie/skill-evolver --path plugin/skills/skill-evolver --dest ~/.grok/skills --name skill-evolver
```

Or tell the bot:

> 从 FishSerrie/skill-evolver 安装 plugin/skills/skill-evolver 到我的技能目录

Hard dependency: also install skill-creator from anthropics/skills.

See the main README for one-command install instructions.
