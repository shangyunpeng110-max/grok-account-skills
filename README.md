# grok-account-skills

Personal Grok account skills collection for automatic first-principles thinking, research, code, decision making, and **autonomous skill evolution**.

## Skills included (local copies)

- **first-principles** — Thinking layer (ALWAYS for non-trivial work)
- **deep-reasoning** — 增强版第一性原理（第一性原理 + 逆向 + 系统 + 二阶 + 约束 + 事前验尸 + 机会成本/费米估算）
- **research-assistant** — Deep research & synthesis
- **code-architect** — Code / strategy architecture
- **agentic-uncertainty-quantifier** — Uncertainty scoring for decisions
- **goal-verifier** — Verify task completion
- **self-refine-loop** — Iterative critique & improve
- **skill-evolver** (light version) — Basic skill rewrite

## Full autonomous evolution (recommended)

For real self-evolution power, install the complete versions from upstream (they include scripts + eval engine):

```bash
# FishSerrie skill-evolver (8-phase loop + 5-gate + GT)
bash /root/.grok/skills/skill-installer/scripts/install-skill.sh --repo FishSerrie/skill-evolver --path plugin/skills/skill-evolver --dest ~/.grok/skills --name skill-evolver

# Anthropic skill-creator (hard dependency for eval)
bash /root/.grok/skills/skill-installer/scripts/install-skill.sh --repo anthropics/skills --path skills/skill-creator --dest ~/.grok/skills --name skill-creator
```

Or simply tell your Grok Bot:

> 把 https://github.com/FishSerrie/skill-evolver 的 plugin/skills/skill-evolver 和 https://github.com/anthropics/skills 的 skills/skill-creator 装到我的账号技能

## How to install everything for a new bot

Tell the bot one of these:

1. **推荐一句话**：
   > 把 https://github.com/shangyunpeng110-max/grok-account-skills 里的技能全部装上，另外再从 FishSerrie/skill-evolver 和 anthropics/skills 安装完整的 skill-evolver 和 skill-creator

2. 或者分步：
   > 先安装 https://github.com/shangyunpeng110-max/grok-account-skills 的所有技能
   > 再安装 FishSerrie 的 skill-evolver 和 Anthropic 的 skill-creator

## Structure

Each skill is a folder with `SKILL.md` (+ optional references/ and scripts/).
