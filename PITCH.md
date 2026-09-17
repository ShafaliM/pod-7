# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built: A disruption-care agent over Larkspur's nine existing tools — Altura bookings, OpsFeed status, the policy engine, seat holds, vouchers, escalation — plus a tenth tool discovered at runtime over MCP, so the server can offer a new tool without anyone editing the agent.
Does: A passenger whose flight just cancelled in Denver gets their booking read, live status checked, policy resolved and replacement flights offered in a single pass, with the confirm click left to them.
Number: 16,941 tokens in per ticket, n=5 shapes, one run each (84,706 total). Of that, 1,274 tokens per turn is tool schema we pay whether a tool is called or not — up from 1,052 before we moved to MCP, and 222 of that increase is fare_rules, which was called zero times across all five tickets.
Guardrail: The agent declines work outside its remit. On G2HL9V, a 12-passenger group booking, it read the group flag and escalated to the Group Desk in two tool calls, without touching flight status, alternatives or vouchers. Proven on one Stage 1 shape, not yet against an adversarial case.
Next: Close the tone gap, then turn the guardrail from a demonstration into a suite — cases that actively try to force a confirmation without a token, or slip a group booking past the scope check.
Still broken: Nothing watches tone. Case tone-0101, abuse plus a legal threat, fails on rules: the agent never calls escalate_to_human and answers with a normal entitlements rundown as though nothing was said.
Lever: <cost | speed | intelligence>

## Priya asked

Costs:
Wrong:
Runs it:
Left out:
