# NexaCode Coding Agent

NexaCode Coding Agent is a Visual Studio Code extension that brings AI-powered coding assistance directly into your editor. It leverages OpenAI models and custom agents to help you debug, explain, and improve your code with conversational and context-aware interactions.

---

## Features

- **AI Chat Panel**: Interact with an AI assistant in a dedicated sidebar panel, styled for clarity and focus.
- **Code Debugging**: Select a file and ask the agent to debug or review your code.
- **Code Explanation**: Hover over code to get instant explanations powered by AI.
- **Diff & Replace**: Choose to view AI-suggested changes as a diff or apply them directly to your file.
- **Customizable Models**: Configure which OpenAI model to use for your tasks.
- **Secure API Key Handling**: Your OpenAI API key is securely stored in VS Code settings.

---

## Getting Started

### Prerequisites

- [Visual Studio Code](https://code.visualstudio.com/) (latest recommended)
- An [OpenAI API key](https://platform.openai.com/account/api-keys)

### Installation

1. **Clone the Repository**
   ```sh
   git clone https://github.com/yourusername/andromeda-coding-agent.git
   cd andromeda-coding-agent
   ```

2. **Install Dependencies**
   ```sh
   npm install
   ```

3. **Open in VS Code**
   ```sh
   code .
   ```

4. **Run the Extension**
   - Press `F5` to launch a new Extension Development Host window.

---

## Usage

### Setting Your OpenAI API Key

- On first use, you will be prompted to enter your OpenAI API key.
- You can update or clear your key in VS Code settings:  
  `File > Preferences > Settings` → search for `openaiAgent.openaiKey`.

### Chat Panel

- Open the **Andromeda Agent Chat** from the sidebar.
- Type your question or request (e.g., "How do I refactor this function?").
- The agent will respond in the chat, with code blocks styled for readability.

### Debugging & Code Actions

- Open any code file.
- Run the command palette (`Ctrl+Shift+P`) and select `Andromeda: Run Agent`.
- Describe your debugging or code improvement request.
- Choose to view the AI's suggestion as a diff or replace your file content.

### Code Explanation

- Hover over any symbol or code in the editor.
- The agent will provide an explanation in a hover popup.

---

## Configuration

You can customize the extension via `.vscode/mcp.json` and VS Code settings:

- **OpenAI Model**:  
  Set your preferred model in settings:  
  `openaiAgent.openaiModel` (default: `gpt-4.1`)

- **API Key**:  
  `openaiAgent.openaiKey` (stored securely)

- **Server Integrations**:  
  See `.vscode/mcp.json` for server and tool configuration.

---

## Security

- Your API key is stored using VS Code's secure settings storage.
- No data is sent to third parties except OpenAI (or configured providers).

---

## Development

- Main extension code: [`src/extension.ts`](src/extension.ts)
- Chat panel UI: [`src/chatPanel.ts`](src/chatPanel.ts)
- Configuration: [`.vscode/mcp.json`](.vscode/mcp.json)

### Scripts

- `npm run compile` — Compile TypeScript
- `npm run watch` — Watch and compile on changes

---

## Troubleshooting

- **No active editor found**: Open a file before running the agent.
- **API key not set**: Set your OpenAI API key in settings.
- **No output from agent**: Try rephrasing your request or check your API key.

---

## License

MIT License

---

## Credits

- Built with [OpenAI Agents SDK](https://github.com/openai/agents)
- Inspired by modern AI coding assistants

---

## Screenshots

![Chat Panel Example](./docs/screenshot-chat.png)

---

## Contributing

Pull requests and issues are welcome! Please open an issue for bugs or