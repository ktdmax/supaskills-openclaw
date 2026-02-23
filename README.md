# supaskills-openclaw

> 1,000+ skills | 6D scored | min 80 to publish

[SupaSkills](https://www.supaskills.ai) is a library of quality-scored expert AI skills. Each skill is a research-backed system prompt scored across 6 dimensions (Research Quality, Prompt Engineering, Practical Utility, Completeness, User Satisfaction, Decision Usefulness). This repo packages SupaSkills as an OpenClaw skill for one-click installation.

## Install

```bash
clawhub install supaskills
```

## Requirements

You need a SupaSkills API key (free signup):

1. Sign up at [supaskills.ai/signup](https://www.supaskills.ai/signup)
2. Go to Dashboard > API Keys
3. Create a key (starts with `sk_supa_`)
4. Set as environment variable: `export SUPASKILLS_API_KEY=sk_supa_...`

**Never commit your API key to git.** Use `.env` files or your system's secret manager.

## Usage Examples

### Find a legal expert
```
you: I need help reviewing an NDA

agent: [searches SupaSkills] Found 3 matching skills:
  1. contract-review-analyst (Score: 87, Platinum)
  2. nda-compliance-checker (Score: 85, Platinum)
  3. commercial-contract-drafter (Score: 84, Gold)

Which one should I load?
```

### Get finance expertise
```
you: Build me a DCF model for a SaaS company

agent: [loads financial-model-builder, Score: 86, Platinum]
       Using the 7-phase financial modeling methodology...
```

### Security audit guidance
```
you: Audit our Kubernetes cluster security

agent: [loads cloud-security-posture-manager, Score: 85, Platinum]
       Starting with the CIS Kubernetes Benchmark framework...
```

## What's inside

```
skills/
  supaskills/
    SKILL.md    # OpenClaw skill definition (ClawHub format)
```

The skill teaches your agent to search, load, and apply expert skills from the SupaSkills API. It handles the full flow: search > pick > load > apply > report.

## Links

- [SupaSkills](https://www.supaskills.ai) — Platform
- [Browse Skills](https://www.supaskills.ai/skills) — Full catalog
- [Benchmark Results](https://www.supaskills.ai/benchmark) — Quality proof
- [API Docs](https://www.supaskills.ai/docs) — Developer reference
- [Pricing](https://www.supaskills.ai/pricing) — Free: 3 slots, Pro: 15, Max: 100

## License

MIT
