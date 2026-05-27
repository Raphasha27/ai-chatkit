<div align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=0:0d1117,100:B39DDB&height=200&section=header&text=AI%20Chatkit&fontSize=50&fontColor=ffffff&fontAlignY=40&desc=Extensible%20AI%20Chat%20Toolkit%20for%20Enterprise&descAlignY=65" width="100%"/>

  [![Status](https://img.shields.io/badge/Status-Active-00ffcc?style=for-the-badge)](#)
  [![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](#)
</div>

## 🤖 Overview
**ai-chatkit** is an extensible AI chat toolkit designed for the rapid integration of advanced LLMs (like Gemini, Claude, and OpenAI) into enterprise applications. It bridges the gap between raw LLM APIs and production-ready chat interfaces.

---

## 📐 System Architecture Demo

The toolkit provides a standardized interface for message history, streaming, and tool execution across different AI providers.

```mermaid
graph LR
    %% Styling
    classDef client fill:#050d12,stroke:#00ffcc,stroke-width:2px,color:#fff
    classDef core fill:#B39DDB,stroke:#fff,stroke-width:2px,color:#111
    classDef provider fill:#0a0a0a,stroke:#3b82f6,stroke-width:1px,color:#fff

    %% Nodes
    App[Client App<br>React / Vue]:::client
    
    SDK[AI Chatkit Core<br>Unified Interface]:::core
    
    P1[Google Gemini]:::provider
    P2[OpenAI GPT-4]:::provider
    P3[Anthropic Claude]:::provider

    %% Relationships
    App -->|Stream Request| SDK
    SDK -->|Adapter| P1
    SDK -->|Adapter| P2
    SDK -->|Adapter| P3
```

### ⚡ Core Capabilities
1. **Unified Streaming:** Handle Server-Sent Events (SSE) from any provider with a single API.
2. **Tool Orchestration:** Easily map local functions to LLM tool calls.
3. **Memory Management:** Built-in adapters for vector stores and conversational history.

---

## 🛠️ Usage Example

```javascript
import { ChatClient } from 'ai-chatkit';

const chat = new ChatClient({ provider: 'gemini' });

await chat.sendMessage("Analyze the system architecture", {
  onStream: (chunk) => console.log(chunk),
  tools: [searchDocs]
});
```

## 🗺️ Roadmap
- [x] Standardize Provider Adapters.
- [x] Add Architectural Diagrams.
- [ ] Add built-in RAG (Retrieval-Augmented Generation) helpers.

---
**Innovative. Performant. Sovereign.**
*Built by Koketso Raphasha (Raphasha27)*
