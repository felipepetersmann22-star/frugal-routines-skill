---
name: frugal-routines
description: Design or review scheduled jobs, reminders, monitors and digests for useful timing and efficient execution. Use when a user asks to create, consolidate or improve recurring work, including its delivery and coverage.
license: MIT
---

# Frugal routines

Match execution and delivery to the real decision, deadline and acceptable delay. Preserve the user's instructions, urgency and platform conventions. Reducing runs is useful only when the result still arrives in time and covers what matters.

## Understand the job

Identify the outcome, source, trigger, recipient and destination, time zone, active days, deadline, acceptable latency, expiry or standing nature, and notification preferences. Inspect existing related routines and the actual scheduler before proposing another one. If a decision-critical detail is missing, leave it unresolved or ask; do not invent hours, time zone or quiet periods. An urgent incident may need immediate delivery on weekends.

Separate a one-time watch through a specific event from a standing recurring alert. Use the platform's supported tools for scheduling and notification. A request to review does not itself authorize changing or disabling existing routines; apply changes when the user's request or other existing authorization covers them.

## Choose a reliable design

1. **Reuse carefully.** An existing routine is a candidate only if audience, source permissions, time zone, delivery channel, urgency and deadline fit. Keep independent failure handling where a combined failure would hide important work.
2. **Choose trigger and cadence.** Prefer a supported, reliable event trigger when it meets the deadline. Otherwise choose a polling interval that meets the acceptable delay; explain its trade-off. Confirm scheduler support rather than assuming events or flexible windows exist. Use a window only when its latest possible start still meets the deadline.
3. **Read incrementally.** Where the source supports it, persist a cursor or timestamp, deduplicate results, and define a bounded first run. On a missing or invalid cursor, use an appropriate safe lookback or request a decision; identify gaps and do not present partial coverage as complete. Advance a cursor only after the work it represents has been handled successfully.
4. **Deliver according to the request.** Honor immediate alerts, regular digests, no-change notifications and quiet hours as specified. An open-ended watch can be appropriate; set an expiry only when it serves the user's goal. Define retries or a failure signal when missed runs matter.
5. **Propose in concrete terms.** Record the current and proposed trigger, schedule with time zone, expected delay, destination, coverage, dependencies and what could be lost. Make only authorized changes. Verify the resulting configuration and report anything that could not be verified.

## Example

A user wants a weekend outage alert within five minutes. Check whether a reliable outage event can notify the chosen destination. If it cannot, propose a supported interval that meets five minutes, including an appropriate failure signal. Do not replace it with a weekday digest merely to reduce runs. A separate non-urgent summary may have a different cadence if requested.

Describe measurable changes in calls or schedules only when supported by real configuration. Do not claim token or cost savings without a suitable measurement.
