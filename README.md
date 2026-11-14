# Frugal Routines

Design scheduled checks, alerts and digests around the decision they support. Frugal Routines helps an agent reduce unnecessary runs while preserving deadlines, coverage and the owner's notification preferences.

## Try it

```sh
npx skills add felipepetersmann22-star/frugal-routines-skill
```

Or copy this repository into your agent's skills directory, keeping its files together. Restart or refresh skill discovery if your agent requires it. Review the instructions before installing any third-party skill.

Ask your agent: “Review my existing routine for duplicate checks. Keep my weekend outage alerts immediate and show me the timing trade-offs before changing anything.”

The review should identify the real schedule, time zone, source and delivery requirements, then propose compatible changes. An urgent weekend alert must remain timely; the skill does not silently replace it with a weekday digest. It uses available platform tools and cannot establish schedules, delivery guarantees or savings without checking them.

## Source and license

Derived from the [original public skill](https://github.com/felipepetersmann22-star/agent-skills/tree/1b7a3d8867363c0ff0dda0f9a117aacb7a16a347/skills/frugal-routines). See [credits](CREDITS.md) and the [MIT license](LICENSE).
