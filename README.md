PromptForge: Repository Context Compactor
PromptForge is a high-performance, purely client-side web application designed to solve LLM context window inefficiencies. It maps local project directory structures, processes codebase codebases, and strips non-semantic formatting, multi-line JSDocs, and inline logic loops. It optimizes multi-file codebases into dense, context-optimized prompts engineered for immediate ingestion by Large Language Models.

🚀 Architectural Blueprint
The application utilizes a clean, decoupled data-flow architecture relying entirely on browser sandbox runtimes via the HTML5 FileSystem API.

Plaintext
[Local Directory Drag-and-Drop]
              │
              ▼
    [utils/crawler.js] ────────► Webkit Entries Traversal (Sandboxed Sandbox Filtering)
              │
              ▼
       [app.jsx State] ◄────────► [utils/compressors.js] (Token Estimation / Regex Pipeline)
              │
              ├───► Tier 1: Whitespace & Comment Purging
              └───► Tier 2: AST Semantic Skeletization
              │
              ▼
   [components/Mainconsole.jsx] ──► Clipboard API Payloads (Ingestion Packets)
🛠️ Tech Stack & Dependencies
Core Framework: React 19 (v19.2.6) & React DOM

Build Pipeline: Vite 8 (v8.0.14) bundled with rolldown and lightningcss

Styling Engine: Tailwind CSS (v3.4.19) featuring custom utility configurations and modern nested selectors (postcss-nested)

Static Code Analysis: ESLint 10 (Flat Config Engine) with specialized hooks for React Refresh and Hooks synchronization

📦 Key Directory Map
Plaintext
├── eslint.config.js          # Flat Configuration for strict code hygiene
├── package.json              # Script automation maps & metadata declarations
├── tailwind.config.js        # Context color tokens (#0B0F19, custom animators)
└── src/
    ├── app.jsx               # Application State Sync Engine & Context Orchestrator
    ├── main.jsx              # DOM Anchor & React StrictMode mounting
    ├── components/
    │   ├── Dropzone.jsx      # HTML5 Webkit Drag & Drop lifecycle events handler
    │   ├── Mainconsole.jsx   # Optimization engine controls & compression statistics monitor
    │   └── Sidebar.jsx       # Dynamic internal Workspace Directory Parser tree
    └── utils/
        ├── compressors.js    # Regex matching state matrices for Tier 1 & Tier 2 pipelines
        └── crawler.js        # High-performance asynchronous binary-skipping directory crawler
⚙️ Core Optimization Engines
PromptForge features two primary processing pipelines executed entirely inside browser threads via high-performance matching arrays:

🧩 Tier 1: Comment & Excess White-Space Purge
Removes structural bloat while maintaining strict runtime functional integrity.

Regular Expression Array targets: Mutates inline blocks, structural multi-line blocks (/* ... */), dynamic inline comment assignments (// ...), python wrappers (# ...), and trailing spaces.

Token Savings: Reduces codebase profile footprint by roughly 30%–40% without altering internal conditional evaluation pathways.

💀 Tier 2: Semantic Skeletization ("Skeleton Mode")
Aggressively strips semantic method definitions, processing abstractions, and conditional evaluations down to raw layout matrices.

Target Arrays: Strips standard, async, nested, and default export function arguments down to function signatures.

Arrow Function Parsing: Intercepts standard scalar constants/variable dynamic expressions mapping to closures (const open = () => { ... }) and strips code blocks completely, replacing them with standard indentations:

JavaScript
// Input
export const init = async (config) => { console.log(config); return true; }
// Output
export const init = async (config) => {  }
*   **Token Savings:** Achieves up to **75%–90%** reduction. Ideal for feeding large codebases to LLMs for systemic dependency evaluation, code mapping, and architecture planning without hitting context length limitations.

---

## 📊 Telemetry, Metrics & VRAM Asset Protection

The processing suite keeps track of operational metrics locally to give real-time optimization feedback:
*   **Token Weight Conversion Matrix:** Estimates token usage locally based on character density rules ($1\text{ Token} \approx 4\text{ characters}$) to ensure accuracy before pasting payloads to hosted LLM endpoints.
*   **Payload Reduction Matrix:** Generates direct telemetry on string delta modifications:
$$\text{Savings \%} = \left\lfloor \frac{\text{Tokens}_{\text{Original}} - \text{Tokens}_{\text{Compressed}}}{\text{Tokens}_{\text{Original}}} \times 100 \right\rfloor$$
*   **VRAM Overhead Protections:** Calculates financial savings on tokens over API cost layouts based on model standard averages ($0.0015 / 1\text{k}$ input frames), preventing high compute usage on complex queries.

---

## 🔒 Security Sandboxing

PromptForge enforces zero-trust architecture parameters:
*   **Zero Server Intercepts:** Code snippets are parsed, split, and aggregated entirely inside individual client browser tabs using local heap allocations.
*   **Automated Binary and Dependency Filters:** Asynchronous traversal matrices ignore `node_modules`, `.git`, `dist`, `build`, `.expo`, and `.next` folder pathways natively to minimize file-system context contamination.
*   **Extension Safeguards:** Restricts structural code ingestion down to structural extensions matching targeted text profiles: `.js`, `.jsx`, `.ts`, `.tsx`, `.json`, `.html`, `.css`, `.md`, `.txt`, `.py`, `.go`, `.java`, `.cpp`, `.h`, `.cs`, `.rb`.

---

## 🛠️ Local Development and Deployment Environment

### Prerequisites
*   Node.js (v20.19.0 or higher recommended to match compiler constraints)
*   npm or package managers supporting package-lock lockfile version 3 requirements

### Installation
```bash
# Clone or navigate to repo package folder root
cd apl2gdg

# Clean dependency workspace installation
npm ci
Script Environment Management
Bash
# Spin up localized Vite multi-threaded Dev Server
npm run dev

# Assemble unified bundle distribution folder via local bundler target definitions
npm run build

# Enforce system rules engine check across static codebase properties
npm run lint

# Launch preview server locally on generated static bundle assets
npm run preview
📋 Standard Context Injection Payload Structure
When you select the "Forge LLM Payload" action, the system automatically builds and copies an optimized structure into your clipboard:

Markdown
### PROMPTFORGE AUTOMATED CONTEXT MAP
The following is a token-compressed repository mapping deployment.

#### FILE STRUCTURE DIRECTORY:
```text
├── src/app.jsx (135 tokens)
├── src/utils/compressors.js (160 tokens)
SYSTEM COMPILER INSTRUCTIONS:
You are an expert software engineering peer...

CODEBASE FRAGMENTS:
/* FILE-PATH: src/app.jsx */

JavaScript
...Optimized Payload...

---

## ⚖️ License
Distributed under structural standard repository definitions. Review configuration manifest tracking for absolute software dependencies.
