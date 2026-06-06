---
written_by: ai
summary: "Generated inventory of OpenClaw plugins shipped in core, published externally, or kept source-only"
read_when:
  - You are deciding whether a plugin ships in the core npm package or installs separately
  - You are updating bundled plugin package metadata or release automation
  - You need the canonical internal vs external plugin list
title: "Plugin inventory"
---

# Plugin inventory

This page is generated from `extensions/*/package.json`, `openclaw.plugin.json`,
and the root npm package `files` exclusions. Regenerate it with:

```bash
pnpm plugins:inventory:gen
```

## Definitions

- **Core npm package:** built into the `openclaw` npm package and available without a separate plugin install.
- **Official external package:** OpenClaw-maintained plugin omitted from the core npm package, kept in this official inventory, and installed on demand through ClawHub and/or npm.
- **Source checkout only:** repo-local plugin omitted from published npm artifacts and not advertised as an installable package.

Source checkouts are different from npm installs: after `pnpm install`, bundled
plugins load from `extensions/<id>` so local edits and package-local workspace
dependencies are available.

## Install a plugin

Use the install route in each entry to decide whether install is needed. Plugins
that say `included in OpenClaw` are already present in the core package.
Official external packages need one install, then a Gateway restart.

For example, Discord is an official external package:

```bash
openclaw plugins install @openclaw/discord
openclaw gateway restart
openclaw plugins inspect discord --runtime --json
```

During the launch cutover, ordinary bare package specs still install from npm.
Use `clawhub:@openclaw/discord` or `npm:@openclaw/discord` when you need an
explicit source. After install, follow the plugin's setup doc, such as
[Discord](/channels/discord), to add credentials and channel config. See
[Manage plugins](/plugins/manage-plugins) for update, uninstall, and publishing
commands.

Each entry includes the package, install route, description, and exposed
surface. The list format is intentional so long generated package names and
surface contracts wrap on normal screens.

## Core npm package

- **[admin-http-rpc](/plugins/reference/admin-http-rpc)** (`@openclaw/admin-http-rpc`) - included in OpenClaw
  - Description: OpenClaw admin HTTP RPC endpoint.
  - Surface: contracts: gatewayMethodDispatch
- **[alibaba](/plugins/reference/alibaba)** (`@openclaw/alibaba-provider`) - included in OpenClaw
  - Description: Adds video generation provider support.
  - Surface: contracts: videoGenerationProviders
- **[anthropic](/plugins/reference/anthropic)** (`@openclaw/anthropic-provider`) - included in OpenClaw
  - Description: Adds Anthropic model provider support to OpenClaw.
  - Surface: providers: anthropic; contracts: mediaUnderstandingProviders
- **[arcee](/plugins/reference/arcee)** (`@openclaw/arcee-provider`) - included in OpenClaw
  - Description: Adds Arcee model provider support to OpenClaw.
  - Surface: providers: arcee
- **[azure-speech](/plugins/reference/azure-speech)** (`@openclaw/azure-speech`) - included in OpenClaw
  - Description: Azure AI Speech text-to-speech (MP3, native Ogg/Opus voice notes, PCM telephony).
  - Surface: contracts: speechProviders
- **[bonjour](/plugins/reference/bonjour)** (`@openclaw/bonjour`) - included in OpenClaw
  - Description: Advertise the local OpenClaw gateway over Bonjour/mDNS.
  - Surface: plugin
- **[browser](/plugins/reference/browser)** (`@openclaw/browser-plugin`) - included in OpenClaw
  - Description: Adds agent-callable tools.
  - Surface: contracts: tools; skills
- **[byteplus](/plugins/reference/byteplus)** (`@openclaw/byteplus-provider`) - included in OpenClaw
  - Description: Adds BytePlus, BytePlus Plan model provider support to OpenClaw.
  - Surface: providers: byteplus, byteplus-plan; contracts: videoGenerationProviders
- **[canvas](/plugins/reference/canvas)** (`@openclaw/canvas-plugin`) - included in OpenClaw
  - Description: Experimental Canvas control and A2UI rendering surfaces for paired nodes.
  - Surface: contracts: tools
- **[cerebras](/plugins/reference/cerebras)** (`@openclaw/cerebras-provider`) - included in OpenClaw
  - Description: Adds Cerebras model provider support to OpenClaw.
  - Surface: providers: cerebras
- **[chutes](/plugins/reference/chutes)** (`@openclaw/chutes-provider`) - included in OpenClaw
  - Description: Adds Chutes model provider support to OpenClaw.
  - Surface: providers: chutes
- **[clickclack](/plugins/reference/clickclack)** (`@openclaw/clickclack`) - included in OpenClaw
  - Description: Adds the Clickclack channel surface for sending and receiving OpenClaw messages.
  - Surface: channels: clickclack
- **[cloudflare-ai-gateway](/plugins/reference/cloudflare-ai-gateway)** (`@openclaw/cloudflare-ai-gateway-provider`) - included in OpenClaw
  - Description: Adds Cloudflare AI Gateway model provider support to OpenClaw.
  - Surface: providers: cloudflare-ai-gateway
- **[codex-supervisor](/plugins/reference/codex-supervisor)** (`@openclaw/codex-supervisor`) - included in OpenClaw
  - Description: Supervise Codex app-server sessions from OpenClaw.
  - Surface: contracts: tools
- **[comfy](/plugins/reference/comfy)** (`@openclaw/comfy-provider`) - included in OpenClaw
  - Description: Adds ComfyUI model provider support to OpenClaw.
  - Surface: providers: comfy; contracts: imageGenerationProviders, musicGenerationProviders, videoGenerationProviders
- **[copilot-proxy](/plugins/reference/copilot-proxy)** (`@openclaw/copilot-proxy`) - included in OpenClaw
  - Description: Adds Copilot Proxy model provider support to OpenClaw.
  - Surface: providers: copilot-proxy
- **[deepgram](/plugins/reference/deepgram)** (`@openclaw/deepgram-provider`) - included in OpenClaw
  - Description: Adds media understanding provider support. Adds realtime transcription provider support.
  - Surface: contracts: mediaUnderstandingProviders, realtimeTranscriptionProviders
- **[deepinfra](/plugins/reference/deepinfra)** (`@openclaw/deepinfra-provider`) - included in OpenClaw
  - Description: Adds DeepInfra model provider support to OpenClaw.
  - Surface: providers: deepinfra; contracts: imageGenerationProviders, mediaUnderstandingProviders, memoryEmbeddingProviders, speechProviders, videoGenerationProviders
- **[deepseek](/plugins/reference/deepseek)** (`@openclaw/deepseek-provider`) - included in OpenClaw
  - Description: Adds DeepSeek model provider support to OpenClaw.
  - Surface: providers: deepseek
- **[document-extract](/plugins/reference/document-extract)** (`@openclaw/document-extract-plugin`) - included in OpenClaw
  - Description: Extract text and fallback page images from local document attachments.
  - Surface: contracts: documentExtractors
- **[duckduckgo](/plugins/reference/duckduckgo)** (`@openclaw/duckduckgo-plugin`) - included in OpenClaw
  - Description: Adds web search provider support.
  - Surface: contracts: webSearchProviders
- **[elevenlabs](/plugins/reference/elevenlabs)** (`@openclaw/elevenlabs-speech`) - included in OpenClaw
  - Description: Adds media understanding provider support. Adds realtime transcription provider support. Adds text-to-speech provider support.
  - Surface: contracts: mediaUnderstandingProviders, realtimeTranscriptionProviders, speechProviders
- **[exa](/plugins/reference/exa)** (`@openclaw/exa-plugin`) - included in OpenClaw
  - Description: Adds web search provider support.
  - Surface: contracts: webSearchProviders
- **[fal](/plugins/reference/fal)** (`@openclaw/fal-provider`) - included in OpenClaw
  - Description: Adds fal model provider support to OpenClaw.
  - Surface: providers: fal; contracts: imageGenerationProviders, musicGenerationProviders, videoGenerationProviders
- **[file-transfer](/plugins/reference/file-transfer)** (`@openclaw/file-transfer`) - included in OpenClaw
  - Description: Fetch, list, and write files on paired nodes via dedicated node commands. Bypasses bash stdout truncation by using base64 over node.invoke for binaries up to 16 MB.
  - Surface: contracts: tools
- **[firecrawl](/plugins/reference/firecrawl)** (`@openclaw/firecrawl-plugin`) - included in OpenClaw
  - Description: Adds agent-callable tools. Adds web fetch provider support. Adds web search provider support.
  - Surface: contracts: tools, webFetchProviders, webSearchProviders
- **[fireworks](/plugins/reference/fireworks)** (`@openclaw/fireworks-provider`) - included in OpenClaw
  - Description: Adds Fireworks model provider support to OpenClaw.
  - Surface: providers: fireworks
- **[github-copilot](/plugins/reference/github-copilot)** (`@openclaw/github-copilot-provider`) - included in OpenClaw
  - Description: Adds GitHub Copilot model provider support to OpenClaw.
  - Surface: providers: github-copilot; contracts: memoryEmbeddingProviders
- **[gmi](/plugins/reference/gmi)** (`@openclaw/gmi-provider`) - included in OpenClaw
  - Description: Adds Gmi, Gmi Cloud, Gmicloud model provider support to OpenClaw.
  - Surface: providers: gmi, gmi-cloud, gmicloud
- **[google](/plugins/reference/google)** (`@openclaw/google-plugin`) - included in OpenClaw
  - Description: Adds Google, Google Gemini CLI, Google Vertex model provider support to OpenClaw.
  - Surface: providers: google, google-gemini-cli, google-vertex; contracts: imageGenerationProviders, mediaUnderstandingProviders, memoryEmbeddingProviders, musicGenerationProviders, realtimeVoiceProviders, speechProviders, videoGenerationProviders, webSearchProviders
- **[gradium](/plugins/reference/gradium)** (`@openclaw/gradium-speech`) - included in OpenClaw
  - Description: Adds text-to-speech provider support.
  - Surface: contracts: speechProviders
- **[groq](/plugins/reference/groq)** (`@openclaw/groq-provider`) - included in OpenClaw
  - Description: Adds Groq model provider support to OpenClaw.
  - Surface: providers: groq; contracts: mediaUnderstandingProviders
- **[huggingface](/plugins/reference/huggingface)** (`@openclaw/huggingface-provider`) - included in OpenClaw
  - Description: Adds Hugging Face model provider support to OpenClaw.
  - Surface: providers: huggingface
- **[imessage](/plugins/reference/imessage)** (`@openclaw/imessage`) - included in OpenClaw
  - Description: Adds the iMessage channel surface for sending and receiving OpenClaw messages.
  - Surface: channels: imessage
- **[inworld](/plugins/reference/inworld)** (`@openclaw/inworld-speech`) - included in OpenClaw
  - Description: Inworld streaming text-to-speech (MP3, OGG_OPUS, PCM telephony).
  - Surface: contracts: speechProviders
- **[irc](/plugins/reference/irc)** (`@openclaw/irc`) - included in OpenClaw
  - Description: Adds the IRC channel surface for sending and receiving OpenClaw messages.
  - Surface: channels: irc
- **[kilocode](/plugins/reference/kilocode)** (`@openclaw/kilocode-provider`) - included in OpenClaw
  - Description: Adds Kilocode model provider support to OpenClaw.
  - Surface: providers: kilocode
- **[kimi](/plugins/reference/kimi)** (`@openclaw/kimi-provider`) - included in OpenClaw
  - Description: Adds Kimi, Kimi Coding model provider support to OpenClaw.
  - Surface: providers: kimi, kimi-coding
- **[litellm](/plugins/reference/litellm)** (`@openclaw/litellm-provider`) - included in OpenClaw
  - Description: Adds LiteLLM model provider support to OpenClaw.
  - Surface: providers: litellm; contracts: imageGenerationProviders
- **[llm-task](/plugins/reference/llm-task)** (`@openclaw/llm-task`) - included in OpenClaw
  - Description: Generic JSON-only LLM tool for structured tasks callable from workflows.
  - Surface: contracts: tools
- **[lmstudio](/plugins/reference/lmstudio)** (`@openclaw/lmstudio-provider`) - included in OpenClaw
  - Description: Adds LM Studio model provider support to OpenClaw.
  - Surface: providers: lmstudio; contracts: memoryEmbeddingProviders
- **[mattermost](/plugins/reference/mattermost)** (`@openclaw/mattermost`) - included in OpenClaw
  - Description: Adds the Mattermost channel surface for sending and receiving OpenClaw messages.
  - Surface: channels: mattermost
- **[memory-core](/plugins/reference/memory-core)** (`@openclaw/memory-core`) - included in OpenClaw
  - Description: Adds memory embedding provider support. Adds agent-callable tools.
  - Surface: contracts: memoryEmbeddingProviders, tools
- **[memory-wiki](/plugins/reference/memory-wiki)** (`@openclaw/memory-wiki`) - included in OpenClaw
  - Description: Persistent wiki compiler and Obsidian-friendly knowledge vault for OpenClaw.
  - Surface: contracts: tools; skills
- **[microsoft](/plugins/reference/microsoft)** (`@openclaw/microsoft-speech`) - included in OpenClaw
  - Description: Adds text-to-speech provider support.
  - Surface: contracts: speechProviders
- **[microsoft-foundry](/plugins/reference/microsoft-foundry)** (`@openclaw/microsoft-foundry`) - included in OpenClaw
  - Description: Adds Microsoft Foundry model provider support to OpenClaw.
  - Surface: providers: microsoft-foundry
- **[migrate-claude](/plugins/reference/migrate-claude)** (`@openclaw/migrate-claude`) - included in OpenClaw
  - Description: Imports Claude Code and Claude Desktop instructions, MCP servers, skills, and safe configuration into OpenClaw.
  - Surface: contracts: migrationProviders
- **[migrate-hermes](/plugins/reference/migrate-hermes)** (`@openclaw/migrate-hermes`) - included in OpenClaw
  - Description: Imports Hermes configuration, memories, skills, and supported credentials into OpenClaw.
  - Surface: contracts: migrationProviders
- **[minimax](/plugins/reference/minimax)** (`@openclaw/minimax-provider`) - included in OpenClaw
  - Description: Adds MiniMax, MiniMax Portal model provider support to OpenClaw.
  - Surface: providers: minimax, minimax-portal; contracts: imageGenerationProviders, mediaUnderstandingProviders, musicGenerationProviders, speechProviders, videoGenerationProviders, webSearchProviders
- **[mistral](/plugins/reference/mistral)** (`@openclaw/mistral-provider`) - included in OpenClaw
  - Description: Adds Mistral model provider support to OpenClaw.
  - Surface: providers: mistral; contracts: mediaUnderstandingProviders, memoryEmbeddingProviders, realtimeTranscriptionProviders
- **[moonshot](/plugins/reference/moonshot)** (`@openclaw/moonshot-provider`) - included in OpenClaw
  - Description: Adds Moonshot model provider support to OpenClaw.
  - Surface: providers: moonshot; contracts: mediaUnderstandingProviders, webSearchProviders
- **[novita](/plugins/reference/novita)** (`@openclaw/novita-provider`) - included in OpenClaw
  - Description: Adds Novita, Novita AI, Novitaai model provider support to OpenClaw.
  - Surface: providers: novita, novita-ai, novitaai
- **[nvidia](/plugins/reference/nvidia)** (`@openclaw/nvidia-provider`) - included in OpenClaw
  - Description: Adds NVIDIA model provider support to OpenClaw.
  - Surface: providers: nvidia
- **[oc-path](/plugins/reference/oc-path)** (`@openclaw/oc-path`) - included in OpenClaw
  - Description: Adds the openclaw path CLI for oc:// workspace file addressing.
  - Surface: plugin
- **[ollama](/plugins/reference/ollama)** (`@openclaw/ollama-provider`) - included in OpenClaw
  - Description: Adds Ollama, Ollama Cloud model provider support to OpenClaw.
  - Surface: providers: ollama, ollama-cloud; contracts: memoryEmbeddingProviders, webSearchProviders
- **[open-prose](/plugins/reference/open-prose)** (`@openclaw/open-prose`) - included in OpenClaw
  - Description: OpenProse VM skill pack with a /prose slash command.
  - Surface: skills
- **[openai](/plugins/reference/openai)** (`@openclaw/openai-provider`) - included in OpenClaw
  - Description: Adds OpenAI model provider support to OpenClaw.
  - Surface: providers: openai; contracts: imageGenerationProviders, mediaUnderstandingProviders, memoryEmbeddingProviders, realtimeTranscriptionProviders, realtimeVoiceProviders, speechProviders, videoGenerationProviders
- **[opencode](/plugins/reference/opencode)** (`@openclaw/opencode-provider`) - included in OpenClaw
  - Description: Adds OpenCode model provider support to OpenClaw.
  - Surface: providers: opencode; contracts: mediaUnderstandingProviders
- **[opencode-go](/plugins/reference/opencode-go)** (`@openclaw/opencode-go-provider`) - included in OpenClaw
  - Description: Adds OpenCode Go model provider support to OpenClaw.
  - Surface: providers: opencode-go; contracts: mediaUnderstandingProviders
- **[openrouter](/plugins/reference/openrouter)** (`@openclaw/openrouter-provider`) - included in OpenClaw
  - Description: Adds OpenRouter model provider support to OpenClaw.
  - Surface: providers: openrouter; contracts: imageGenerationProviders, mediaUnderstandingProviders, musicGenerationProviders, speechProviders, videoGenerationProviders
- **[parallel](/plugins/reference/parallel)** (`@openclaw/parallel-plugin`) - included in OpenClaw
  - Description: Adds web search provider support.
  - Surface: contracts: webSearchProviders
- **[perplexity](/plugins/reference/perplexity)** (`@openclaw/perplexity-plugin`) - included in OpenClaw
  - Description: Adds web search provider support.
  - Surface: contracts: webSearchProviders
- **[policy](/plugins/reference/policy)** (`@openclaw/policy`) - included in OpenClaw
  - Description: Adds policy-backed doctor checks for workspace conformance.
  - Surface: plugin
- **[qianfan](/plugins/reference/qianfan)** (`@openclaw/qianfan-provider`) - included in OpenClaw
  - Description: Adds Qianfan model provider support to OpenClaw.
  - Surface: providers: qianfan
- **[qwen](/plugins/reference/qwen)** (`@openclaw/qwen-provider`) - included in OpenClaw
  - Description: Adds Qwen, Qwen Cloud, Model Studio, DashScope, Qwen Oauth, Qwen Portal, Qwen CLI model provider support to OpenClaw.
  - Surface: providers: qwen, qwencloud, modelstudio, dashscope, qwen-oauth, qwen-portal, qwen-cli; contracts: mediaUnderstandingProviders, videoGenerationProviders
- **[runway](/plugins/reference/runway)** (`@openclaw/runway-provider`) - included in OpenClaw
  - Description: Adds video generation provider support.
  - Surface: contracts: videoGenerationProviders
- **[searxng](/plugins/reference/searxng)** (`@openclaw/searxng-plugin`) - included in OpenClaw
  - Description: Adds web search provider support.
  - Surface: contracts: webSearchProviders
- **[senseaudio](/plugins/reference/senseaudio)** (`@openclaw/senseaudio-provider`) - included in OpenClaw
  - Description: Adds media understanding provider support.
  - Surface: contracts: mediaUnderstandingProviders
- **[sglang](/plugins/reference/sglang)** (`@openclaw/sglang-provider`) - included in OpenClaw
  - Description: Adds SGLang model provider support to OpenClaw.
  - Surface: providers: sglang
- **[signal](/plugins/reference/signal)** (`@openclaw/signal`) - included in OpenClaw
  - Description: Adds the Signal channel surface for sending and receiving OpenClaw messages.
  - Surface: channels: signal
- **[sms](/plugins/reference/sms)** (`@openclaw/sms`) - included in OpenClaw
  - Description: Twilio SMS channel plugin for OpenClaw text messages.
  - Surface: channels: sms
- **[stepfun](/plugins/reference/stepfun)** (`@openclaw/stepfun-provider`) - included in OpenClaw
  - Description: Adds StepFun, StepFun Plan model provider support to OpenClaw.
  - Surface: providers: stepfun, stepfun-plan
- **[synthetic](/plugins/reference/synthetic)** (`@openclaw/synthetic-provider`) - included in OpenClaw
  - Description: Adds Synthetic model provider support to OpenClaw.
  - Surface: providers: synthetic
- **[tavily](/plugins/reference/tavily)** (`@openclaw/tavily-plugin`) - included in OpenClaw
  - Description: Adds agent-callable tools. Adds web search provider support.
  - Surface: contracts: tools, webSearchProviders; skills
- **[telegram](/plugins/reference/telegram)** (`@openclaw/telegram`) - included in OpenClaw
  - Description: Adds the Telegram channel surface for sending and receiving OpenClaw messages.
  - Surface: channels: telegram
- **[tencent](/plugins/reference/tencent)** (`@openclaw/tencent-provider`) - included in OpenClaw
  - Description: Adds Tencent TokenHub model provider support to OpenClaw.
  - Surface: providers: tencent-tokenhub
- **[together](/plugins/reference/together)** (`@openclaw/together-provider`) - included in OpenClaw
  - Description: Adds Together model provider support to OpenClaw.
  - Surface: providers: together; contracts: videoGenerationProviders
- **[tts-local-cli](/plugins/reference/tts-local-cli)** (`@openclaw/tts-local-cli`) - included in OpenClaw
  - Description: Adds text-to-speech provider support.
  - Surface: contracts: speechProviders
- **[venice](/plugins/reference/venice)** (`@openclaw/venice-provider`) - included in OpenClaw
  - Description: Adds Venice model provider support to OpenClaw.
  - Surface: providers: venice
- **[vercel-ai-gateway](/plugins/reference/vercel-ai-gateway)** (`@openclaw/vercel-ai-gateway-provider`) - included in OpenClaw
  - Description: Adds Vercel AI Gateway model provider support to OpenClaw.
  - Surface: providers: vercel-ai-gateway
- **[vllm](/plugins/reference/vllm)** (`@openclaw/vllm-provider`) - included in OpenClaw
  - Description: Adds vLLM model provider support to OpenClaw.
  - Surface: providers: vllm
- **[volcengine](/plugins/reference/volcengine)** (`@openclaw/volcengine-provider`) - included in OpenClaw
  - Description: Adds Volcengine, Volcengine Plan model provider support to OpenClaw.
  - Surface: providers: volcengine, volcengine-plan; contracts: speechProviders
- **[voyage](/plugins/reference/voyage)** (`@openclaw/voyage-provider`) - included in OpenClaw
  - Description: Adds memory embedding provider support.
  - Surface: contracts: memoryEmbeddingProviders
- **[vydra](/plugins/reference/vydra)** (`@openclaw/vydra-provider`) - included in OpenClaw
  - Description: Adds Vydra model provider support to OpenClaw.
  - Surface: providers: vydra; contracts: imageGenerationProviders, speechProviders, videoGenerationProviders
- **[web-readability](/plugins/reference/web-readability)** (`@openclaw/web-readability-plugin`) - included in OpenClaw
  - Description: Extract readable article content from local HTML web fetch responses.
  - Surface: contracts: webContentExtractors
- **[webhooks](/plugins/reference/webhooks)** (`@openclaw/webhooks`) - included in OpenClaw
  - Description: Authenticated inbound webhooks that bind external automation to OpenClaw TaskFlows.
  - Surface: plugin
- **[workboard](/plugins/reference/workboard)** (`@openclaw/workboard`) - included in OpenClaw
  - Description: Dashboard workboard for agent-owned issues and sessions.
  - Surface: contracts: tools
- **[xai](/plugins/reference/xai)** (`@openclaw/xai-plugin`) - included in OpenClaw
  - Description: Adds xAI model provider support to OpenClaw.
  - Surface: providers: xai; contracts: imageGenerationProviders, mediaUnderstandingProviders, realtimeTranscriptionProviders, speechProviders, tools, videoGenerationProviders, webSearchProviders
- **[xiaomi](/plugins/reference/xiaomi)** (`@openclaw/xiaomi-provider`) - included in OpenClaw
  - Description: Adds Xiaomi, Xiaomi Token Plan model provider support to OpenClaw.
  - Surface: providers: xiaomi, xiaomi-token-plan; contracts: speechProviders
- **[zai](/plugins/reference/zai)** (`@openclaw/zai-provider`) - included in OpenClaw
  - Description: Adds Z.AI model provider support to OpenClaw.
  - Surface: providers: zai; contracts: mediaUnderstandingProviders

## Official external packages

- **[acpx](/plugins/reference/acpx)** (`@openclaw/acpx`) - npm; ClawHub
  - Description: OpenClaw ACP runtime backend with plugin-owned session and transport management.
  - Surface: skills
- **[amazon-bedrock](/plugins/reference/amazon-bedrock)** (`@openclaw/amazon-bedrock-provider`) - npm; ClawHub
  - Description: OpenClaw Amazon Bedrock provider plugin with model discovery, embeddings, and guardrail support.
  - Surface: providers: amazon-bedrock; contracts: memoryEmbeddingProviders
- **[amazon-bedrock-mantle](/plugins/reference/amazon-bedrock-mantle)** (`@openclaw/amazon-bedrock-mantle-provider`) - npm; ClawHub
  - Description: OpenClaw Amazon Bedrock Mantle provider plugin for OpenAI-compatible model routing.
  - Surface: providers: amazon-bedrock-mantle
- **[anthropic-vertex](/plugins/reference/anthropic-vertex)** (`@openclaw/anthropic-vertex-provider`) - npm; ClawHub
  - Description: OpenClaw Anthropic Vertex provider plugin for Claude models on Google Vertex AI.
  - Surface: providers: anthropic-vertex
- **[brave](/plugins/reference/brave)** (`@openclaw/brave-plugin`) - npm; ClawHub
  - Description: OpenClaw Brave Search provider plugin for web search.
  - Surface: contracts: webSearchProviders
- **[codex](/plugins/reference/codex)** (`@openclaw/codex`) - npm; ClawHub
  - Description: OpenClaw Codex app-server harness and model provider plugin with a Codex-managed GPT catalog.
  - Surface: providers: codex; contracts: mediaUnderstandingProviders, migrationProviders
- **[copilot](/plugins/reference/copilot)** (`@openclaw/copilot`) - npm; ClawHub: `clawhub:@openclaw/copilot`
  - Description: Registers the GitHub Copilot agent runtime.
  - Surface: plugin
- **[diagnostics-otel](/plugins/reference/diagnostics-otel)** (`@openclaw/diagnostics-otel`) - npm; ClawHub: `clawhub:@openclaw/diagnostics-otel`
  - Description: OpenClaw diagnostics OpenTelemetry exporter for metrics and traces.
  - Surface: plugin
- **[diagnostics-prometheus](/plugins/reference/diagnostics-prometheus)** (`@openclaw/diagnostics-prometheus`) - npm; ClawHub: `clawhub:@openclaw/diagnostics-prometheus`
  - Description: OpenClaw diagnostics Prometheus exporter for runtime metrics.
  - Surface: plugin
- **[diffs](/plugins/reference/diffs)** (`@openclaw/diffs`) - npm; ClawHub
  - Description: OpenClaw read-only diff viewer plugin and file renderer for agents.
  - Surface: contracts: tools; skills
- **[diffs-language-pack](/plugins/reference/diffs-language-pack)** (`@openclaw/diffs-language-pack`) - npm; ClawHub: `clawhub:@openclaw/diffs-language-pack`
  - Description: Adds syntax highlighting for languages outside the default diffs viewer set.
  - Surface: plugin
- **[discord](/plugins/reference/discord)** (`@openclaw/discord`) - npm; ClawHub
  - Description: OpenClaw Discord channel plugin for channels, DMs, commands, and app events.
  - Surface: channels: discord; contracts: transcriptSourceProviders
- **[feishu](/plugins/reference/feishu)** (`@openclaw/feishu`) - npm; ClawHub
  - Description: OpenClaw Feishu/Lark channel plugin for chats and workplace tools (community maintained by @m1heng).
  - Surface: channels: feishu; contracts: tools; skills
- **[google-meet](/plugins/reference/google-meet)** (`@openclaw/google-meet`) - npm; ClawHub
  - Description: OpenClaw Google Meet participant plugin for joining calls through Chrome or Twilio transports.
  - Surface: contracts: tools
- **[googlechat](/plugins/reference/googlechat)** (`@openclaw/googlechat`) - npm; ClawHub
  - Description: OpenClaw Google Chat channel plugin for spaces and direct messages.
  - Surface: channels: googlechat
- **[line](/plugins/reference/line)** (`@openclaw/line`) - npm; ClawHub
  - Description: OpenClaw LINE channel plugin for LINE Bot API chats.
  - Surface: channels: line
- **[lobster](/plugins/reference/lobster)** (`@openclaw/lobster`) - npm; ClawHub
  - Description: Lobster workflow tool plugin for typed pipelines and resumable approvals.
  - Surface: contracts: tools
- **[matrix](/plugins/reference/matrix)** (`@openclaw/matrix`) - ClawHub: `clawhub:@openclaw/matrix`; npm
  - Description: OpenClaw Matrix channel plugin for rooms and direct messages.
  - Surface: channels: matrix
- **[memory-lancedb](/plugins/reference/memory-lancedb)** (`@openclaw/memory-lancedb`) - npm; ClawHub
  - Description: OpenClaw LanceDB-backed long-term memory plugin with auto-recall, auto-capture, and vector search.
  - Surface: contracts: tools
- **[msteams](/plugins/reference/msteams)** (`@openclaw/msteams`) - npm; ClawHub
  - Description: OpenClaw Microsoft Teams channel plugin for bot conversations.
  - Surface: channels: msteams
- **[nextcloud-talk](/plugins/reference/nextcloud-talk)** (`@openclaw/nextcloud-talk`) - npm; ClawHub
  - Description: OpenClaw Nextcloud Talk channel plugin for conversations.
  - Surface: channels: nextcloud-talk
- **[nostr](/plugins/reference/nostr)** (`@openclaw/nostr`) - npm; ClawHub
  - Description: OpenClaw Nostr channel plugin for NIP-04 encrypted direct messages.
  - Surface: channels: nostr
- **[openshell](/plugins/reference/openshell)** (`@openclaw/openshell-sandbox`) - npm; ClawHub
  - Description: OpenClaw sandbox backend for the NVIDIA OpenShell CLI with mirrored local workspaces and SSH command execution.
  - Surface: plugin
- **[pixverse](/plugins/reference/pixverse)** (`@openclaw/pixverse-provider`) - npm; ClawHub: `clawhub:@openclaw/pixverse-provider`
  - Description: OpenClaw PixVerse video generation provider plugin.
  - Surface: contracts: videoGenerationProviders
- **[qqbot](/plugins/reference/qqbot)** (`@openclaw/qqbot`) - npm; ClawHub
  - Description: OpenClaw QQ Bot channel plugin for group and direct-message workflows.
  - Surface: channels: qqbot; contracts: tools; skills
- **[slack](/plugins/reference/slack)** (`@openclaw/slack`) - npm; ClawHub
  - Description: OpenClaw Slack channel plugin for channels, DMs, commands, and app events.
  - Surface: channels: slack
- **[synology-chat](/plugins/reference/synology-chat)** (`@openclaw/synology-chat`) - npm; ClawHub
  - Description: Synology Chat channel plugin for OpenClaw channels and direct messages.
  - Surface: channels: synology-chat
- **[tlon](/plugins/reference/tlon)** (`@openclaw/tlon`) - npm; ClawHub
  - Description: OpenClaw Tlon/Urbit channel plugin for chat workflows.
  - Surface: channels: tlon; skills
- **[tokenjuice](/plugins/reference/tokenjuice)** (`@openclaw/tokenjuice`) - npm; ClawHub: `clawhub:@openclaw/tokenjuice`
  - Description: Compacts exec and bash tool results with tokenjuice reducers.
  - Surface: contracts: agentToolResultMiddleware
- **[twitch](/plugins/reference/twitch)** (`@openclaw/twitch`) - npm; ClawHub
  - Description: OpenClaw Twitch channel plugin for chat and moderation workflows.
  - Surface: channels: twitch
- **[voice-call](/plugins/reference/voice-call)** (`@openclaw/voice-call`) - npm; ClawHub
  - Description: OpenClaw voice-call plugin for Twilio, Telnyx, and Plivo phone calls.
  - Surface: contracts: tools
- **[whatsapp](/plugins/reference/whatsapp)** (`@openclaw/whatsapp`) - ClawHub: `clawhub:@openclaw/whatsapp`; npm
  - Description: OpenClaw WhatsApp channel plugin for WhatsApp Web chats.
  - Surface: channels: whatsapp
- **[zalo](/plugins/reference/zalo)** (`@openclaw/zalo`) - npm; ClawHub
  - Description: OpenClaw Zalo channel plugin for bot and webhook chats.
  - Surface: channels: zalo
- **[zalouser](/plugins/reference/zalouser)** (`@openclaw/zalouser`) - npm; ClawHub
  - Description: OpenClaw Zalo Personal Account plugin via native zca-js integration.
  - Surface: channels: zalouser; contracts: tools

## Source checkout only

- **[qa-channel](/plugins/reference/qa-channel)** (`@openclaw/qa-channel`) - source checkout only
  - Description: Adds the QA Channel surface for sending and receiving OpenClaw messages.
  - Surface: channels: qa-channel
- **[qa-lab](/plugins/reference/qa-lab)** (`@openclaw/qa-lab`) - source checkout only
  - Description: OpenClaw QA lab plugin with private debugger UI and scenario runner.
  - Surface: plugin
- **[qa-matrix](/plugins/reference/qa-matrix)** (`@openclaw/qa-matrix`) - source checkout only
  - Description: Matrix QA transport runner and substrate.
  - Surface: plugin
