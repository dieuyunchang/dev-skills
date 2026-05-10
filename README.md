# 🛠️ dev-skills

A curated collection of specialized skills designed for AI coding agents. These skills enhance the capabilities of agents like Antigravity, Claude Code, and Windsurf, enabling them to handle complex tasks with expert-level precision.

---

## 🚀 Installation & Usage

To use these skills, you need to copy the desired skill folder from this repository into the configuration directory of your AI agent.

### 📂 Target Directories (macOS)

| Agent | Target Path |
| :--- | :--- |
| **Antigravity** | `~/.gemini/antigravity/skills/` |
| **Claude Code** | `~/.claude/skills/` |
| **Windsurf** | `~/.windsurf/skills/` or Project Root |
| **Codex** | `~/.codex/skills/` |

### 💻 Quick Install Command

Run the following command in your terminal to copy a specific skill (replace `<skill-name>` with the folder name):

```bash
cp -r skills/<skill-name> ~/.gemini/antigravity/skills/
```

To install **all** available skills to Antigravity:

```bash
cp -r skills/* ~/.gemini/antigravity/skills/
```

---

## 🤖 Supported Agents

- **Antigravity**: Google DeepMind's advanced agentic coding assistant.
- **Claude Code**: Anthropic's powerful CLI-based coding agent.
- **Windsurf**: The first agentic IDE by Codeium.
- **Codex**: Various specialized AI agent implementations.

---

## 🧠 Available Skills

### 📊 Visualization & Architecture
#### [ascii-architecture-diagram](file:///Users/yunchang/Workspace/dev-skills/skills/ascii-architecture-diagram)
- **Focus**: System architecture design using text/ASCII.
- **Capabilities**: Generating diagrams, writing technical docs, and building Git-friendly knowledge bases.

### 🔍 Code Quality & Review
(Add more skills here as they are added to the repo)

---

> [!TIP]
> After copying a skill, you may need to restart your AI agent session for the new capabilities to be recognized.
