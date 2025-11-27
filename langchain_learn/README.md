# LangChain.js Examples - Learning Guide

This repository contains comprehensive examples from the [LangChain.js](https://github.com/langchain-ai/langchainjs) project, organized to help you learn LangChain step by step.

## 📚 What is LangChain?

LangChain is a framework for building LLM-powered applications. It helps you chain together interoperable components and third-party integrations to simplify AI application development. These examples demonstrate how to use LangChain's various features and integrations.

## 🚀 Getting Started

### Prerequisites

- **Node.js**: v24.5.0
- **pnpm**: >= 8.0 
- **API Keys**: Various examples require API keys (OpenAI, Anthropic, etc.)

### Installation

1. **Install dependencies** (from the monorepo root):
   ```bash
   pnpm install
   ```

2. **Set up environment variables**:
   Copy the example environment file and fill in your API keys:
   ```bash
   cd langchain_learn
   cp .env.example .env
   ```
   
   Then edit `.env` and add your API keys. The `.env.example` file contains a comprehensive list of all available environment variables organized by category:
   - Core LLM providers (OpenAI, Anthropic, Google, etc.)
   - Vector stores (Pinecone, Weaviate, Supabase, etc.)
   - Caching & storage (Upstash Redis, Vercel KV, etc.)
   - Search APIs (Tavily, Exa, SerpAPI, etc.)
   - Monitoring (LangSmith, Lunary)
   - And many more...
   
   **Minimum required for most examples:**
   ```bash
   OPENAI_API_KEY=your_openai_api_key_here
   ```
   
   **Recommended for full experience:**
   ```bash
   OPENAI_API_KEY=your_openai_api_key_here
   ANTHROPIC_API_KEY=your_anthropic_api_key_here
   LANGCHAIN_API_KEY=your_langsmith_api_key_here
   LANGCHAIN_TRACING_V2=true
   LANGCHAIN_PROJECT=langchain-learn
   ```

## 🎯 Running Examples

### Quick Start - Run Your First Example

From the monorepo root, run:

```bash
# Run a quickstart example
pnpm --filter langchain_learn start src/langchain-classic/get_started/quickstart.ts
```

Or from the `langchain_learn` directory:

```bash
cd langchain_learn
pnpm start src/langchain-classic/get_started/quickstart.ts
```

### Running Examples - General Syntax

```bash
# From monorepo root
pnpm --filter langchain_learn start <path-to-example>

# From langchain_learn directory
pnpm start <path-to-example>
```

The path can be specified in multiple ways:
- `src/langchain-classic/get_started/quickstart.ts`
- `./src/langchain-classic/get_started/quickstart.ts`
- `langchain-classic/get_started/quickstart.ts`

### Running Compiled Examples

If you want to run the compiled JavaScript version:

```bash
# First, build the project
pnpm --filter langchain_learn build

# Then run the compiled version
pnpm --filter langchain_learn start:dist dist/langchain-classic/get_started/quickstart.js
```

## 📖 Learning Path

### 1. **Getting Started** (Start Here!)
   - `src/langchain-classic/get_started/quickstart.ts` - Basic chat model usage
   - `src/langchain-classic/get_started/quickstart2.ts` - Prompts and chains
   - `src/langchain-classic/get_started/quickstart3.ts` - More advanced concepts

### 2. **Core Concepts**

   **Chat Models & LLMs:**
   - `src/langchain-classic/models/chat/` - Chat model examples
   - `src/langchain-classic/models/llm/` - LLM examples
   - `src/llms/` - Various LLM provider integrations

   **Prompts:**
   - `src/langchain-classic/prompts/` - Prompt templates and examples

   **Chains:**
   - `src/langchain-classic/chains/` - Various chain patterns

   **Memory:**
   - `src/langchain-classic/memory/` - Memory management examples

### 3. **Document Processing**

   **Document Loaders:**
   - `src/langchain-classic/document_loaders/` - Load documents from various sources
     - `pdf.ts` - PDF loading
     - `youtube.ts` - YouTube transcripts
     - `github.ts` - GitHub repositories
     - `web_pdf.ts` - Web pages as PDFs
     - And many more!

   **Text Splitters:**
   - `src/langchain-classic/indexes/` - Text splitting strategies

   **Document Transformers:**
   - `src/document_transformers/` - Transform documents (HTML to text, etc.)

   **Document Compressors:**
   - `src/document_compressors/` - Compress documents for retrieval

### 4. **Retrieval & Vector Stores**

   **Vector Stores:**
   - `src/langchain-classic/indexes/vector_stores/` - Various vector database integrations
     - Pinecone, Weaviate, Chroma, Qdrant, and more

   **Retrievers:**
   - `src/langchain-classic/retrievers/` - Different retrieval strategies

### 5. **Agents & Tools**

   **LangGraph (Modern Agent Framework):**
   - `src/createAgent/` - Agent creation examples
   - `src/createAgent/middleware/` - Agent middleware
   - `src/createAgent/dynamicTools/` - Dynamic tool usage

   **Classic Agents:**
   - `src/langchain-classic/chat/agent.ts` - Basic agent example
   - `src/langchain-classic/tools/` - Tool examples

### 6. **Advanced Features**

   **Callbacks & Monitoring:**
   - `src/langchain-classic/callbacks/` - Callback handlers
   - `src/langchain-classic/callbacks/lunary_quickstart.ts` - Monitoring with Lunary

   **Caching:**
   - `src/cache/` - Caching strategies
   - `src/caches/` - Cache implementations

   **Streaming:**
   - `src/createAgent/streaming.ts` - Streaming responses

   **Structured Output:**
   - `src/createAgent/structuredOutput.ts` - Structured output generation

### 7. **Use Cases**

   - `src/langchain-classic/use_cases/` - Real-world application examples

## 📁 Project Structure

```
langchain_learn/
├── src/
│   ├── langchain-classic/     # Classic LangChain examples
│   │   ├── get_started/        # Start here!
│   │   ├── models/             # Model integrations
│   │   ├── prompts/           # Prompt templates
│   │   ├── chains/             # Chain patterns
│   │   ├── memory/             # Memory management
│   │   ├── document_loaders/   # Document loading
│   │   ├── indexes/            # Text splitting & vector stores
│   │   ├── retrievers/         # Retrieval strategies
│   │   ├── tools/              # Tool examples
│   │   ├── use_cases/          # Real-world examples
│   │   └── ...
│   ├── createAgent/            # LangGraph agent examples
│   ├── cache/                  # Caching examples
│   ├── document_compressors/   # Document compression
│   ├── document_transformers/  # Document transformation
│   └── llms/                   # LLM provider examples
├── package.json
└── tsconfig.json
```

## 🔧 Common Tasks

### Build the Project

```bash
pnpm --filter langchain_learn build
```

### Lint Code

```bash
pnpm --filter langchain_learn lint
```

### Format Code

```bash
pnpm --filter langchain_learn format
```

## 💡 Tips for Learning

1. **Start Simple**: Begin with `get_started/quickstart.ts` to understand basic concepts
2. **Read the Code**: Each example is well-commented - read the code to understand what's happening
3. **Experiment**: Modify examples to see how changes affect behavior
4. **Check Documentation**: Visit [docs.langchain.com](https://docs.langchain.com) for detailed API documentation
5. **Use LangSmith**: Set up LangSmith tracing to visualize how your chains execute

## 🔗 Resources

- **Official Documentation**: [docs.langchain.com](https://docs.langchain.com/oss/javascript/langchain/)
- **GitHub Repository**: [github.com/langchain-ai/langchainjs](https://github.com/langchain-ai/langchainjs)
- **LangSmith**: [smith.langchain.com](https://smith.langchain.com) - Monitoring and debugging
- **LangGraph Documentation**: [langchain.com/docs/langgraph](https://langchain.com/docs/langgraph) - For agent examples

## 🐛 Troubleshooting

### "API key not found" errors
- Make sure your `.env` file is in the `langchain_learn` directory
- Verify your API keys are correct
- Some examples require specific API keys - check the example file for requirements

### Module not found errors
- Run `pnpm install` from the monorepo root
- Make sure you're running from the correct directory

### TypeScript errors
- Run `pnpm --filter langchain_learn build` to check for compilation errors
- Make sure your TypeScript version is compatible (5.8.3+)

## 📝 Example: Running Your First Example

```bash
# 1. Make sure dependencies are installed
pnpm install

# 2. Set up your .env file with OPENAI_API_KEY

# 3. Run a simple example
pnpm --filter langchain_learn start src/langchain-classic/get_started/quickstart.ts
```

You should see output from the chat model!

## 🤝 Contributing

This is a learning repository. Feel free to:
- Experiment with the examples
- Add your own examples
- Modify existing examples to learn
- Share what you've learned!

## 📄 License

MIT License - See LICENSE file for details

---

Happy Learning! 🦜🔗
