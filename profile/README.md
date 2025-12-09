# Character Foundry

**Character Foundry** is an open-source ecosystem of tools for the creation, management, preservation, and federation of AI character cards. Our mission is to provide robust, standard-compliant, and interoperable primitives for the AI roleplay community.

## The Ecosystem

### 🏗️ [Card Architect](https://github.com/character-foundry/character-architect)
> *The Editor & IDE*

A modern, self-hostable character card editor and format converter.
- **Visual Editing:** Rich UI for CCv2 and CCv3 formats.
- **Format Conversion:** Lossless conversion between formats (where possible).
- **Validation:** Real-time schema validation against community standards.
- **Monorepo:** Built with React (Vite) and Fastify.


### 🌐 [Character Federation](https://github.com/character-foundry/character-federation)
> *The Hub (CardsHub)*

A federated community platform for sharing and discovery.
- **ActivityPub:** Built on W3C standards for decentralized social networking.
- **Universal Loader:** Wraps the Foundry primitives for a seamless reading experience.
- **Community:** Follow creators, star cards, and syndicate content across hubs.

### 🛠️ [Character Foundry (SDK)](https://github.com/character-foundry/character-foundry)
> *The Shared Brain*

The core TypeScript libraries that power the entire ecosystem. Available as npm packages.
- **`@character-foundry/core`**: Binary, ZIP, and URI primitives.
- **`@character-foundry/loader`**: Universal `parseCard()` for PNG, CharX, Voxta, and JSON.
- **`@character-foundry/exporter`**: Format conversion with strict loss reporting.
- **`@character-foundry/schemas`**: Zod schemas for CCv2, CCv3, and Voxta.
- **`@character-foundry/voxta`**: specialized handling for multi-character packages.

---

## Supported Formats

We strive for maximum interoperability while respecting the unique constraints of each format.

| Format | Extension | Read | Write | Notes |
|:---|:---:|:---:|:---:|:---|
| **TavernCard v2** | `.png`, `.json` | ✅ | ✅ | The classic standard. |
| **TavernCard v3** | `.png`, `.json` | ✅ | ✅ | Rich metadata, embedded assets. |
| **CharX** | `.charx` | ✅ | ✅ | ZIP-based container for CCv3 + Assets. |
| **Voxta** | `.voxpkg` | ✅ | ✅ | Multi-character packages for Voxta AI. |
| **RisuAI** | `.png` | ✅ | ⚠️ | Read-only script support; opaque preservation. |

---

## Architecture Philosophy

> **"Centralize the brain, distribute the body."**

1.  **Permissive Read:** We accept "messy" data from the wild. If it looks like a card, we load it.
2.  **Strict Write:** We only export valid, spec-compliant files. Normalization happens at export time.
3.  **Data Integrity:** We never mutate the source file upon import. Transformations are explicit user actions.
4.  **No Lock-in:** All tools are self-hostable and use open standard formats.

## Getting Started

This is a **monorepo** ecosystem. Most individual tools can be run via Docker or Node.js.

### Prerequisites
- Node.js 20+
- pnpm 9+
- Docker (optional, recommended for Archive/Federation)

### Installation (SDK)

```bash
npm install @character-foundry/loader @character-foundry/exporter
```

## Contributing

We welcome contributions! Please see the `CONTRIBUTING.md` in each repository for specific guidelines.

- **Standards:** We adhere to the [Character Card V3 Spec](https://github.com/malfoys-code/chara-card-v3-spec).

---

*Est. 2025. Maintained by the Character Foundry Team.*
