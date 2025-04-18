# MCPchat
MCPchat is terminal-based LLM chat client supporting multiple Model Context Protocol (MCP) servers with real-time server management and dynamic model switching.

# MCPChat

A powerful terminal-based chat application that connects to multiple Model Context Protocol (MCP) servers, enabling seamless interaction with various LLM providers through a unified interface.

![Node.js Version](https://img.shields.io/badge/node-%3E%3D18.0.0-brightgreen)
![TypeScript](https://img.shields.io/badge/TypeScript-5.3.2-blue)


## Features

- 🌐 **Multi-Server Support**: Connect to multiple MCP servers simultaneously
- 🔄 **Dynamic Model Switching**: Switch between different models and servers on the fly
- 🔍 **Real-time Health Monitoring**: Automatic server health checks and status updates
- 💾 **Session Management**: Maintain chat history and context across conversations
- 🎨 **Interactive CLI**: User-friendly terminal interface with color-coded messages
- 🛡️ **Type Safety**: Full TypeScript support with Zod schema validation
- 📝 **Comprehensive Logging**: Detailed logging system for debugging and monitoring

## Prerequisites

- Node.js >= 18.0.0
- npm or yarn
- Access to one or more MCP servers

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/mcpchat.git
cd mcpchat

# Install dependencies
npm install

# Copy environment file and configure
cp .env.example .env

# Build the project
npm run build
```
## Configuration

Edit the `.env` file with your MCP server details and API keys:

```env
# MCP Server Configurations
MCP_SERVER_1_URL=http://localhost:8080
MCP_SERVER_1_NAME=local-ollama
MCP_SERVER_1_API_KEY=optional_key_1

MCP_SERVER_2_URL=http://remote-server:8080
MCP_SERVER_2_NAME=remote-mcp
MCP_SERVER_2_API_KEY=optional_key_2

# Logging
LOG_LEVEL=info
```

## Usage

Start the application:

```bash
npm start
```

### Available Commands

- `/switch` - Switch to a different server or model
- `/clear` - Clear chat history
- `/status` - Show current connection status
- `/help` - Display available commands
- `/exit` - Exit the application

## Development

```bash
# Run in development mode
npm run dev

# Run linting
npm run lint

# Run tests
npm run test
```
# Project Structure
```
mcpchat/
├── src/
│ ├── config/ # Configuration management
│ ├── mcp/ # MCP server handling
│ ├── chat/ # Chat session management
│ ├── utils/ # Utilities and helpers
│ └── index.ts # Application entry point
├── tests/ # Test files
├── .env.example # Example environment variables
├── .gitignore # Git ignore rules
├── package.json # Project dependencies
└── tsconfig.json # TypeScript configuration
```

## Architecture

MCPChat is built with a modular architecture focusing on:

- **Server Management**: Handles connections to multiple MCP servers with real-time health monitoring
- **Chat Sessions**: Manages conversation context and history
- **CLI Interface**: Provides an intuitive terminal-based user interface
- **Configuration**: Handles environment-based configuration with validation
- **Logging**: Comprehensive logging system for debugging and monitoring

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## Error Handling

The application includes comprehensive error handling:

- Server connection failures
- API response errors
- Configuration validation
- Runtime errors

All errors are logged and displayed appropriately in the CLI.

## Logging

Logs are stored in:
- `error.log` - Error-level messages
- `combined.log` - All log messages

Log levels can be configured in the `.env` file.

## Security

- API keys are stored in environment variables
- Server connections use secure protocols
- No sensitive data is logged

## License

This project is licensed under the BSD-3 License 

 ## Acknowledgments

- [Model Context Protocol](https://github.com/model-context-protocol) for the MCP specification
- [LangChain.js](https://js.langchain.com/) for inspiration
- All contributors and maintainers

## Support

For support, please open an issue in the GitHub repository or contact the maintainers.

---
