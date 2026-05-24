# Security Policy

## Reporting

If you discover an error:

DO NOT open a public issue.

Email directly to:
contact@aikungfu.dev

## Scope

This repository contains prompt templates only — no executable code, no API keys, no credentials.

Prompts that work with mpesa-mcp or wapimaji-mcp are subject to those packages' security policies:
- [mpesa-mcp/SECURITY.md](https://github.com/gabrielmahia/mpesa-mcp/blob/main/SECURITY.md) — NSA CSI U/OO/6030316-26 compliant
- [wapimaji-mcp/SECURITY.md](https://github.com/gabrielmahia/wapimaji-mcp/blob/main/SECURITY.md)

## Prompt Injection Awareness

When using these prompts in production systems:
- Validate all [placeholder] values before injection
- Do not allow end users to inject arbitrary text into formula fields
- Log all prompt invocations (see mpesa-mcp audit logging for reference implementation)
