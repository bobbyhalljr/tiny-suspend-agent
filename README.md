# tiny-suspend-agent

A tiny TypeScript agent that is pure data between turns.

- Every tool call is a suspension point. The slice persists history and ends.
- The agent lives in a store as one JSON string.
- A tool result resumes it. Later events arrive as synthetic `receive_event__injected` tool calls.
- Events with a bad signature or an unknown call id are dropped.

Small model of the idea in AWS's [Infinity](https://aws.amazon.com/blogs/opensource/introducing-infinity-a-runtime-for-extreme-agent-concurrency/) runtime, not its implementation. Fake model. No API key. No network.

```bash
npm install
npx tsx suspend.ts
```

MIT, by Bobby Hall Jr.

Read the write-up on Dev.to: https://dev.to/bobbyhalljr/aws-open-sourced-infinity-lets-build-a-tiny-agent-that-sleeps-between-tool-calls-in-typescript-3mja
