## **HR-ASSIST Agentic AI System**
---
HR ASSIST is an Agentic AI system designed to help HR teams automate routine workflows. This example demonstrates automation of the employee onboarding process, streamlining tasks that typically require manual intervention.

In terms of technical architecture, for MCP client we use Claude Desktop and the code base here represents the MCP server with necessary tools that will be used by MCP client 

🛠️ Setup Instructions

To set up and run HR ASSIST, follow these steps:

- Configure claude_desktop_config.json
Add the following configuration to your claude_desktop_config.json file:

    ```json
    {
    "mcpServers": {
        "hr-assist": {
        "command": "C:\\Users\\sibas\\.local\\bin\\uv",
        "args": [
            "--directory",
            "C::\\code\\hr-assist",
            "run",
            "server.py"
        ],
        "env": {
            "EMAIL": "YOUR_EMAIL",
            "EMAIL_PWD": "YOUR_APP_PASSWORD"
        }
        }
    }
    }
    ```

- Replace "command" with the actual path to your uv.exe file
- Replace EMAIL with your actual email.
- Replace APP_PASSWORD with your email provider’s app-specific password (e.g., for Gmail).
- Run `uv init` and `uv add mcp[cli]`.
- Finally, run `uv run mcp install server.py` to build the server in the claude desktop app.  

**Usage**
- Click on the `+` icon and select the `Add from hr-assist` option, and send the request.
- Fill the details for the new employee:

<img src="resources\image.jpg" alt="Claude desktop prompt with fields" style="width:auto;height:300px;padding-left:30px">

Alternatively, you can draft a custom prompt and let the agent take over.