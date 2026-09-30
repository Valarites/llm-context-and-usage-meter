# LLM Context & Usage Meter

LLM Context & Usage Meter helps you see how much of an LLM conversation's
context window is being used before response quality starts to decline.

It runs locally in the browser, estimates token usage from the visible chat,
and displays warnings as a conversation approaches its estimated context
limit. It is designed for long-running conversations with ChatGPT, Claude,
Gemini, DeepSeek, and other supported web LLMs.

## Highlights

- Live in-page context meter and browser popup.
- Local token estimation based on message text and model profiles.
- Warning states for degradation and critical context usage.
- Configurable warning thresholds for Pro users.
- Model selection and manual model overrides.
- “Summarize & Continue” for transferring a conversation into a fresh thread.
- Full-history loading for supported virtualized conversations.
- Local conversation usage history and peak-token analytics.
- ExtensionPay checkout and subscription management for Pro.
- No raw conversation text uploaded to the publisher.

## Supported platforms

The extension currently supports:

- ChatGPT — `chatgpt.com`
- Claude — `claude.ai`
- Gemini — `gemini.google.com`
- DeepSeek — supported DeepSeek domains
- Microsoft Copilot — `copilot.microsoft.com`
- Grok — `grok.com` and the Grok experience on `x.com`
- Perplexity — `perplexity.ai`
- Meta AI — `meta.ai`
- Poe — `poe.com`
- Mistral Le Chat — `chat.mistral.ai`
- Qwen Chat — `chat.qwen.ai`
- Kimi — `kimi.com` and supported Moonshot domains

Provider interfaces change frequently. Some providers and models may be
marked experimental or may require a manual model selection when the web
interface does not expose a stable model name.

## Free and Pro

The Free plan provides core local tracking on one selected platform and the
standard meter. Pro adds multi-platform tracking, custom warning thresholds,
additional appearance palette, and the complete Summarize & Continue workflow.

Pro checkout and subscription management are handled through ExtensionPay.
The extension uses ExtensionPay's paid-status response to enable Pro features;
payment-card details are not stored by the extension.

## Privacy

Conversation text is read from supported chat pages and processed locally to
estimate tokens, identify message roles, display the meter, and perform
requested summary transfers. Raw conversation text is not sent to the
publisher, stored as conversation history, or included in telemetry.

The extension stores settings, model selections, consent state, context
snapshots, and aggregate usage history in browser extension storage.
“Summarize & Continue” can send the user-approved prompt and summary to the
selected LLM provider, as requested by the user.

The extension does not load executable JavaScript or WebAssembly from remote
URLs. All extension code, including the bundled ExtensionPay client, is
included in the published package.

## Installation

Install the published extension from the Chrome Web Store. On first use,
review the local-processing disclosure and grant consent before the meter
reads supported chat content.


## Estimates and limitations

Token counts are local estimates, not provider-authoritative measurements.
Actual usage can differ because providers may add hidden instructions,
metadata, tool calls, attachments, or system content that is not visible in
the page.

Context-window limits and web interfaces can change without notice. The
extension reports confidence levels and allows manual model selection where
automatic detection is uncertain. Do not use the meter as a guarantee that a
provider will accept a prompt or preserve response quality.


## License and support

See the repository's published license, privacy policy, terms, refund policy,
support information, and third-party notices for the applicable conditions
on https://valarites.github.io/llm-context-and-usage-meter.
