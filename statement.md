# Why I Built Moltis

I built Moltis because I wanted an AI assistant stack I could trust, run myself, and fully understand.

I love what [OpenClaw](https://openclaw.ai) is doing. That gateway-first direction is exactly the future I believe in. I also believe AI should feel simple: agents should work for you quietly in the background and help with day-to-day tasks instead of adding more complexity. Moltis is my Rust-native take on that idea: local-first, secure by design, practical in daily use, and focused on useful automation over hype.

## What Moltis Is

Moltis is a personal AI gateway written in Rust.

In practice, it is one binary that runs your assistant runtime: web UI, provider routing, tools, sessions, memory, hooks, and integrations - without a Node runtime or dependency sprawl.

At a high level, Moltis is designed to:

- Connect multiple LLM providers behind one consistent gateway
- Keep you in control with full support for local LLMs, so private workflows can stay on your own machine
- Stream responses in real time
- Support agent workflows with tools, MCP, and long-term memory
- Run across channels (web, API, Telegram) while keeping context coherent
- Execute actions safely with sandboxing and approval controls

So instead of chatting with one model in one tab, you run an assistant system you own.

## Why Rust

Moltis sits on a sensitive boundary: model traffic, tool execution, credentials, and automation. That boundary must be boringly reliable.

Rust gives me that foundation:

- Memory safety by default
- Strong compile-time guarantees
- High performance without garbage-collector pauses
- Predictable behavior under streaming and concurrency load

For AI systems, these are not abstract advantages. They directly impact safety, latency, and uptime.

Moltis also leans into Rust's security strengths in concrete ways: no unsafe code by default, strict secret handling, and explicit execution/network boundaries.

## Security and Control

AI assistants are useful when they can act - and risky when they act without boundaries.

Moltis is built with defense in depth:

- Sandboxed execution (Docker or Apple Container backends)
- Human-in-the-loop approval for sensitive actions
- SSRF protections and origin validation
- Passkeys support (WebAuthn), plus scoped authentication and API key controls
- Safer secret lifecycle handling

The goal is simple: useful automation without blind trust.

## Open Source

Moltis is MIT licensed and built in the open.

That matters because infrastructure you depend on should be inspectable, auditable, and forkable. Open source keeps the architecture honest and gives users a real exit path. If project direction changes, your stack is still yours.

I want Moltis to be shaped by real operators and builders - people running assistants in production, at home, and everywhere in between.

## What This Project Is About

Moltis is about owning your AI runtime.

Not outsourcing core control.
Not treating safety as an afterthought.
Not locking the future behind a hosted box.

Just a fast, secure, extensible gateway you can run yourself.

[Fabien Penso](https://pen.so)
