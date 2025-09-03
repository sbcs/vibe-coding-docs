# Windows Setup Instructions

## 1. Download Claude Desktop
[Download Claude Desktop](https://claude.ai/download)

## 2. Login on Claude Desktop
Open Claude Desktop and log in with your account.

## 3. Node.js Dependency
1. Visit https://nodejs.org/en/download
2. Download the MSI installer for Windows
3. Run the installer after it downloads

## 4. Configure Claude Desktop
1. In Claude Desktop, go to the hamburger menu → File → Settings → Developer → Edit Config
2. Open `claude_desktop_config.json` with Notepad
3. Replace the contents with:
```json
{
  "mcpServers": {
    "filesystem": {
      "command": "npx",
      "args": [
        "-y",
        "@modelcontextprotocol/server-filesystem",
        "C:\\Users\\NAME\\Desktop",
        "C:\\Users\\NAME\\Downloads"
      ]
    }
  }
}
```
4. Replace `NAME` with your actual Windows username
5. Save and close the file

## 5. Install MCP Server
Run the following command in Command Prompt or PowerShell:
```bash
npm install -g @modelcontextprotocol/server-filesystem
```

## 6. Restart Claude Desktop
1. Exit Claude Desktop completely (quit from the bottom)
2. Open Claude Desktop again

The filesystem MCP server should now be active and allow Claude to access your Desktop and Downloads folders.