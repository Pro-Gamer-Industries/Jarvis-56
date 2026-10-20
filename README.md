# JARVIS — Your Assistant. Your Models. Your Rules.

This is the Mark 56 version of our Project called Jarvis
**Mark LV gave the assistant a screen. Mark LVI gives you control over what powers it.**

JARVIS is evolving beyond a single AI provider. With Mark LVI, you can choose how your assistant listens, thinks, and speaks — whether through Gemini Live, locally hosted AI models, or third-party APIs. Configure everything through **⚙ → ENGINE & PROVIDERS**, without editing configuration files.

Previously, the assistant depended entirely on Gemini. Quota limits, network outages, and privacy requirements could leave you without an assistant. Mark LVI introduces a flexible, modular engine system that gives you more control over your AI experience.

Run models locally using **Ollama, LM Studio, llama.cpp, or vLLM**, or connect to providers such as **OpenAI, Groq, DeepSeek, Mistral, xAI, OpenRouter, and Together**. Choose your speech recognition, language model, and voice independently. You can even route background requests through a different model without changing your live voice conversation.

### Lightweight by Design

Optional providers remain unloaded when unused. On the default installation, the `providers/` package is not imported during startup, tool execution, or settings access. The measured provider-selection overhead is just **0.16 ms**, with no provider modules loaded. The provider folder can also be removed without affecting the default engine.

### Everything You Already Love, Still Intact

Your selected engine integrates with JARVIS's existing capabilities, including its animated avatar, lip-sync, self-echo protection, push-to-talk, wake word, persistent memory, undo system, confirmation gates, actions, and plugins.

### Actions You Can Trust

JARVIS doesn't confuse attempting an action with completing it. Tools now distinguish between `done`, `unverified`, and `failed`. Applications are checked against running processes, and closing an application involves requesting a graceful shutdown before verifying its state.

**JARVIS doesn't simply tell you what it tried to do. It tells you what it could verify.**

This isn't just another AI assistant. It's an extensible, customizable extension of your digital life — built by **Pro Gamer Industries**.

---

## 🚀 Capabilities

### 🧠 AI Engines & Intelligence

| Feature | Description |
|---|---|
| 🔌 Choose Your Engine | Switch between Gemini Live and a configurable STT + LLM + TTS pipeline directly from the UI. |
| 🏠 Local & Third-Party Models | Connect Ollama, LM Studio, llama.cpp, vLLM, OpenAI, Groq, DeepSeek, Mistral, xAI, OpenRouter, and Together. |
| 🚀 Faster Live Engine | Uses Gemini 3.1 Flash Live, with approximately 2× faster time-to-first-word than the previous model. |
| 🪜 Model Ladder | Automatically falls back through nine Gemini models when quota limits, timeouts, or outages occur. |
| 🧮 Smart Tool Budget | Gives smaller models only the most relevant tools, prioritizing core functionality and reducing prompt overhead. |
| 🧩 Self-Describing Skills | Automatically discovers bundled skills through their declared `TOOL` dictionaries and handlers. |
| 🧩 Plugin System | Add a single `.py` file to `plugins/` to introduce a new skill on the next launch. |
| 🛡️ Untrusted Content Protection | Treats content from webpages and documents as data rather than trusted instructions. |
| 🪪 Runtime Self-Awareness | Dynamically determines its name, operating system, capabilities, and limitations each session. |
| 🤝 Verified Action Reporting | Reports `done`, `unverified`, or `failed` according to the result of an action. |

### 🎙️ Voice & Conversation

| Feature | Description |
|---|---|
| 🎙️ Real-Time Voice | Supports low-latency, multilingual conversations through the Gemini Live API. |
| 🗣️ Local Speech Processing | Uses Whisper for speech recognition and Piper for speech synthesis, enabling offline voice interaction. |
| 🌍 Multilingual Conversations | Recognizes your spoken language and responds in the corresponding language and voice where supported. |
| 🎙️ ElevenLabs Integration | Streams natural-sounding speech using an ElevenLabs voice across supported languages. |
| 🎚️ Voice Selection | Choose from five native Gemini voices and switch between them without restarting. |
| 🎤 Push-to-Talk | Hold **Ctrl + Space** to activate the microphone. Global hotkey support is available on Windows; other platforms may be window-scoped. |
| 🎙️ Wake Word | Detects the local wake phrase **"Hey Jarvis"**, sleeps after two minutes of silence, and avoids streaming audio while asleep. |
| 🔇 Self-Echo Protection | Recognizes and filters the assistant's own spoken output to prevent self-triggering. |
| ⚡ Instant Acknowledgment | Provides a brief, context-aware spoken response in your language when a longer task begins. |
| 🧑‍💻 Language Adaptation | Detects your spoken language and adapts subsequent sessions automatically. |
| 🤫 Private Reasoning Output | Prevents supported `<think>` blocks from models such as Qwen3 and DeepSeek-R1 from being spoken aloud. |
| 🔗 Session Continuity | Preserves conversation continuity across connection drops and voice or audio-device changes. |
| ♾️ Extended Sessions | Uses sliding-window context compression to support long conversations. |
| ⌨️ Hybrid Input | Switch seamlessly between typed messages and voice commands. |
| 🎧 Audio Device Selection | Select supported microphones and speakers by name, with device checks to help identify usable options. |

### 🧑‍🎤 Avatar & Interface

| Feature | Description |
|---|---|
| 🧑‍🎤 Holographic Avatar | Displays an animated human head with software-rendered facial geometry and lighting, without requiring a dedicated GPU. |
| 👄 Real-Time Lip-Sync | Generates approximately 50 mouth-shape updates per second using audio formants and transcript information. |
| 🌍 Script-Aware Articulation | Uses Unicode-based text processing for Latin, Cyrillic, and Greek scripts, with fallbacks for scripts that require different pronunciation handling. |
| 🙂 Facial Expressions | Animates eyebrows, gaze, blinking, and subtle head movements to make conversations feel more natural. |
| 😐 Expressive Status Indicators | Changes gaze and eyelid behavior to reflect listening, thinking, sleeping, and incoming content. |
| 🎨 Live Theming | Customize the HUD using a hue wheel or hexadecimal color value, including the avatar's tint. |
| 〰️ Reactive Waveform | Visualizes real microphone audio while listening and assistant audio while speaking. |
| 📺 Video on the HUD | Plays YouTube videos, local video files, and supported video URLs in the HUD, starting muted until audio is requested. |
| 🗺️ Dynamic Content Panel | Displays scrollable web results, news, and search information beneath the HUD. |
| 🪪 Assistant Customization | Change the assistant's name, your name, voice, and theme color directly in the UI, with immediate effect. |
| 📱 Remote Dashboard | Access and control the assistant from your phone through QR-code pairing. |

### 🖥️ System & Desktop Control

| Feature | Description |
|---|---|
| 🖥️ System Control | Launch applications, adjust volume and brightness, manage Wi-Fi, trigger shortcuts, and perform supported power operations using voice commands. |
| 🖱️ Desktop Control | Manage windows, interact with the taskbar, and perform supported desktop-level operations. |
| 🚪 Smart Application Closing | Identifies running applications, requests graceful closure, and checks whether the application has exited. |
| 🪟 Focus Existing Applications | Brings an already-running application to the foreground instead of unnecessarily launching another instance. |
| 🎚️ Per-Device Volume | Adjusts the selected audio output device rather than blindly targeting the system default. |
| 🎤 Microphone Testing | Includes a live microphone test meter to verify that audio is actually being received. |
| 🐧 Platform-Aware Control | Reports limitations caused by Wayland, macOS permissions, or other platform restrictions instead of pretending an action succeeded. |
| ⚠️ Explicit Confirmation | Requires your confirmation for sensitive operations such as shutdown, restart, and Wi-Fi changes. |
| ↩️ Undo Support | Reverses supported file operations and settings changes, including files moved, renamed, created, or written. |
| ⚡ Startup Integration | Supports automatic startup through platform-specific mechanisms on Windows, macOS, and Linux. |

### 🧠 Memory & Proactive Assistance

| Feature | Description |
|---|---|
| 🧠 Persistent Memory | Retains useful information about your projects, preferences, and context across sessions. |
| 🔍 Recallable Memory | Searches locally stored memories on demand instead of relying exclusively on the information that fits into the current prompt. |
| 👁️ Memory Management Panel | Lets you inspect stored information, see when it was learned, and delete individual entries. |
| 🌅 Morning Briefing | Greets you on first boot, announces the time, summarizes the previous day, and retrieves current news when available. |
| 🔔 Proactive Assistance | Provides context-aware check-ins based on the time, your projects, and recent conversations. |
| 🗓️ Session Memory | Summarizes conversations for later reference and uses that context naturally in a subsequent morning briefing. |
| 👁️ Background Monitoring | Monitors user-configured topics and checks for new headlines daily, with relevant notifications. |
| 📊 Hardware Monitoring | Tracks CPU, RAM, GPU, and temperature telemetry, with localized voice alerts. |
| 🌤️ Weather Reports | Retrieves current weather information for your city and personalizes reports using available context. |
| ⏰ Smart Reminders | Uses native scheduling mechanisms such as Windows Task Scheduler, macOS LaunchAgents, and Linux systemd. |

### 🌐 Web, Files & Integrations

| Feature | Description |
|---|---|
| 👁️ Visual Awareness | Captures screen and webcam information for processing through the main Gemini session, identifying each source. |
| 🔍 Multi-Mode Web Search | Supports `news`, `research`, `price`, `compare`, and `search`, using Gemini Grounding first and DuckDuckGo as a fallback. |
| 🌐 Browser Control | Opens URLs, navigates browser tabs, and performs supported browser interactions through voice commands. |
| 📂 File Processing | Reads local files, summarizes their contents, and answers questions about them. |
| 📨 Messaging Integration | Composes and sends messages through supported integrations, including WhatsApp and Telegram. |
| 📋 Clipboard Intelligence | Opens a floating action panel when you copy text, offering Translate, Summarize, Explain, and Fix operations. |

---

## 🏢 About Pro Gamer Industries

JARVIS is part of our commitment to developing innovative software and hardware projects. We aim to build useful tools, explore new technologies, and make our work accessible to the community.

Follow our work and explore our other projects:

- **Instagram:** https://www.instagram.com/pro_gamer_industries/
- **GitHub:** https://github.com/Pro-Gamer-Industries

**Built with innovation by Pro Gamer Industries.**
