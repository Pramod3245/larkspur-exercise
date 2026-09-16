# PITCH.md

Six lines and a lever. Your words. The last two are scored.

Built: A custom tool that translates internal disruption cause codes (WX, ATC, MX, CREW, SEC) into plain-English explanations customers can understand. Integrated MCP-served tools into the tool list so Claude can reach them alongside our own.
Does:When a customer asks why their flight was disrupted, Claude now calls cause_in_plain_words to explain the reason in words the customer recognizes instead of jargon. The agent went from 9 tools to 12.
Number:Schema tokens: 822 with 10 tools (Build 2.1) → 1,261 with 12 tools (Build 2.2). Each new tool adds cost on every turn, whether Claude uses it or not.
Guardrail: Tool descriptions drive routing. Our first probe ("When can I fly?") didn't trigger the tool because it didn't ask for explanation. Changing it to "Why was my flight cancelled?" made Claude pick the right tool—same agent, same tools, just better question.
Next:Build 3. Create eval cases that grade the ager it completes. The gate checks correctness
Still broken:The abusive ticket still gets a calm, normal resolution. No gate catches tone violations yet. That's Build 4's job.
Lever: intelligence

## Priya asked

Costs:
Wrong:
Runs it:
Left out:
