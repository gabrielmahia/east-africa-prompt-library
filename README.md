# East Africa Prompt Library

> Curated AI prompt library for East African civic tech, fintech, and social infrastructure — tested prompts for Swahili contexts, Kenya institutional APIs, and community coordination.

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![NSA MCP Compliant](https://img.shields.io/badge/NSA%20CSI%20U%2FOO%2F6030316--26-MCP%20Security%20Compliant-blue)](https://www.nsa.gov/Portals/75/documents/Cybersecurity/CSI_MCP_SECURITY.pdf)
[![Part of East African Decision Infrastructure](https://img.shields.io/badge/Portfolio-East%20African%20Decision%20Infrastructure-orange)](https://gabrielmahia.github.io)

A structured prompt library adapted for East African contexts — Kenya, East Africa, and underrepresented communities — organized by domain and following the **General → Formula → Specific** pattern.

Prompts are designed to work with:
- [mpesa-mcp](https://github.com/gabrielmahia/mpesa-mcp) — M-Pesa financial API
- [wapimaji-mcp](https://github.com/gabrielmahia/wapimaji-mcp) — Kenya drought intelligence
- [civic-agent-kit](https://github.com/gabrielmahia/civic-agent-kit) — civic AI SDK
- [kenya-3d](https://github.com/gabrielmahia/kenya-3d) — 3D civic data visualization
- [taarifa-ai](https://github.com/gabrielmahia/taarifa-ai) — East African journalism AI
- All Streamlit apps at [gabrielmahia.github.io](https://gabrielmahia.github.io)

---

## Structure

```
prompts/
├── fintech/          M-Pesa, chamas, mobile money
├── civic/            Government, policy, accountability
├── environment/      Drought, water, flood risk
├── education/        ShuleAI prompts for Kenya curriculum
├── health/           AfyaAI prompts for Kenya health system
├── journalism/       TaarifaAI — East African investigative journalism
├── career/           KaziAI — Kenya job market
├── diaspora/         RemitAI — diaspora services
└── social/           Community organizing, human rights
```

---

## Prompt Format

Every prompt in this library follows the **General → Formula → Specific** pattern:

```
## [Use Case Name]

**General prompt:**
"[Example prompt in plain language]"

**Formula:**
"[Template with [placeholders] for context injection]"

**East Africa examples:**
- "[Kenyan/East African specific example]"
- "[Swahili/multilingual variant]"
- "[Rural/low-bandwidth context variant]"
```

---

## Quick Start

### With mpesa-mcp

```python
from mpesa_mcp import MpesaMCP

mcp = MpesaMCP()
# Use prompts from prompts/fintech/mpesa_transactions.md
result = mcp.stk_push(
    phone_number="254712345678",
    amount=500,
    account_reference="SCHOOL_FEES_TERM2"
)
```

### With Claude directly

```python
import anthropic

client = anthropic.Anthropic()
# Load a prompt template
prompt = open("prompts/civic/public_policy.md").read()
response = client.messages.create(
    model="claude-sonnet-4-20250514",
    max_tokens=1024,
    messages=[{"role": "user", "content": prompt}]
)
```

---

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). East Africa-specific additions welcome.  
Issues only — no unsolicited PRs.

## License

MIT © Gabriel Mahia | [contact@aikungfu.dev](mailto:contact@aikungfu.dev)
