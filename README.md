# GH Tools

A collection of browser-based tools for everyday tasks. No installation required — runs entirely in your browser.

## 🛠️ Available Tools

| Tool | Description |
|------|-------------|
| [PDF Month Highlighter](tools/pdf-month-highlighter-bonus-nido.html) | Merges multiple PDFs and highlights dates/month names |
| [LLM Cost Calculator](tools/llm-cost-calc.html) | Compare costs across LLM providers (OpenAI, Anthropic, Mistral, etc.) |
| [Agent Cost Monte Carlo](tools/agent-cost-monte-carlo.html) | Monte Carlo simulation for AI agent costs |

## 🚀 Running Locally

Simply open `index.html` in your browser. No build step or server required.

## ➕ Adding a New Tool

### 1. Create your tool

Add your HTML file to the `tools/` folder:

```
tools/your-new-tool.html
```

### 2. Register it on the homepage

Open `index.html` and find the `TOOLS` array in the `<script>` section (around line 474). Add a new entry:

```javascript
const TOOLS = [
    // ... existing tools ...
    {
        id: 'your-tool-id',           // Unique identifier (kebab-case)
        title: 'Your Tool Name',       // Display name
        category: 'Category Name',     // e.g., 'PDF Tools', 'AI Tools', 'Utilities'
        description: 'Brief description of what your tool does.',
        icon: '🔧',                    // Emoji icon for the card
        url: 'tools/your-new-tool.html',  // Relative path to your tool
        tags: ['Tag1', 'Tag2'],        // Short tags shown on the card
        keywords: ['search', 'terms']  // Additional terms for search functionality
    }
];
```

### Tool Entry Fields

| Field | Required | Description |
|-------|----------|-------------|
| `id` | ✅ | Unique identifier in kebab-case |
| `title` | ✅ | Human-readable name |
| `category` | ✅ | Tool category for grouping |
| `description` | ✅ | Brief explanation (1-2 sentences) |
| `icon` | ✅ | Single emoji for visual identification |
| `url` | ✅ | Relative path to the tool HTML file |
| `tags` | ✅ | Array of short tags (3-5 recommended) |
| `keywords` | ✅ | Array of search terms (include variations) |

### Tips

- **Keywords**: Include common misspellings, abbreviations, and related terms
- **Icons**: Use descriptive emojis (📄 for documents, 💰 for money/costs, 🔧 for utilities)
- **Tags**: Keep them short (1-2 words max)

## 📁 Project Structure

```
ghtools/
├── index.html          # Homepage with search and tools grid
├── README.md           # This file
└── tools/              # Individual tool pages
    ├── agent-cost-monte-carlo.html
    ├── pdf-month-highlighter-bonus-nido.html
    └── llm-cost-calc.html
```

## 📝 License

MIT
