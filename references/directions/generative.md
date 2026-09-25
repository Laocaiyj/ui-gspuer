# Generative UI: compose controlled components from intent

Last reviewed: 2026-09-23. Vercel documentation and example source were read; no real model or business service was invoked.

## Research basis

- [Generative UI source documentation](https://github.com/vercel/ai/blob/main/content/docs/04-ai-sdk-ui/04-generative-user-interfaces.mdx): tool results map to authored components; the Weather example returns simulated data.
- [Tool usage](https://github.com/vercel/ai/blob/main/content/docs/04-ai-sdk-ui/03-chatbot-tool-usage.mdx) and [message persistence](https://github.com/vercel/ai/blob/main/content/docs/04-ai-sdk-ui/03-chatbot-message-persistence.mdx): dispatch by message part/type/state and validate message data and stable IDs.
- [Stopping streams](https://github.com/vercel/ai/blob/main/content/docs/06-advanced/02-stopping-streams.mdx): client stopping and server generation cancellation are separate paths. Server cancellation also depends on runtime propagation and abortSignal; check the current version for interactions with stream resumption.
- [RSC overview](https://ai-sdk.dev/docs/ai-sdk-rsc/overview): at review time, AI SDK RSC was experimental and AI SDK UI was recommended for production. This does not mean React Server Components in general are deprecated.

## Implementation recipe

1. Select controlled tools and local components from user goals/data. Validate schemas and business permissions on the backend and type/state before frontend rendering. Do not execute generated code or inject arbitrary HTML.
2. Distinguish streaming input, complete arguments, successful output, errors, and stopped states. Partial arguments may support tolerant previews but must not be passed to result components requiring complete props. Unknown types receive a safe, readable fallback.
3. Give messages, tool calls, component instances, and edits stable IDs and clear ownership. New results preserve pending inputs and selection; late old requests must not overwrite newer ones. Generation must not remove navigation or return paths.
4. Stopping preserves completed results and user input. Incomplete parts show accurate status and retry options. Verify frontend stopping separately from whether the backend continues working.
5. Read the project lockfile and use documentation/types for the installed version. Default-branch examples and cached documentation may describe different API versions. Keep helpers version-compatible and preserve the project's dependency versions unless an upgrade is within scope.
6. Connect model services only within user scope. Label local fixtures accurately: they validate frontend state, not generation capability.

## Acceptance

Using the agreed generation mechanism, compare at least two intents or data sets for component selection and state changes. Check streaming input, success, no result, schema/tool errors, stop, retry, late responses, and state after reload. Keep evidence for normal UI, simulation, and real services separate. One final screenshot cannot establish the full chain.
