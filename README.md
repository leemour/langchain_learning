# Monochain - LangChain/LangGraph Learning Monorepo

A pnpm monorepo containing LangChain.js examples and learning materials.

## 📦 Workspace Packages

- **`langchain_learn`** - Comprehensive LangChain.js examples from the official repository

## 🚀 Quick Start

### Installation

```bash
# Install all dependencies
pnpm install
```

### Running Examples

```bash
# Run an example from langchain_learn
pnpm --filter langchain_learn start src/langchain-classic/get_started/quickstart.ts
```

For detailed instructions, see the [langchain_learn README](./langchain_learn/README.md).

## 📁 Project Structure

```
monochain/
├── langchain_learn/     # LangChain.js examples and learning materials
├── package.json         # Root package.json (monorepo configuration)
├── pnpm-workspace.yaml  # pnpm workspace configuration
└── README.md           # This file
```

## 🛠️ Available Scripts

From the root directory, you can run:

```bash
# Build all packages
pnpm build

# Lint all packages
pnpm lint

# Format all packages
pnpm format

# Run scripts in a specific package
pnpm --filter langchain_learn <script>
```

## 📚 Learn More

- [LangChain.js Documentation](https://docs.langchain.com/oss/javascript/langchain/)
- [LangChain.js GitHub](https://github.com/langchain-ai/langchainjs)
- [LangGraph Documentation](https://langchain.com/docs/langgraph)

---

Happy Learning! 🦜🔗
