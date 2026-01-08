1. Create a directory for your build to work out of:

    ```
    mkdir mcp_demo
    ```

2. Change into the directory:

    ```
    cd mcp_demo
    ```

3. Create your `Claude.md` file.  This file will act as a jumping off point contextually for your application.  Copy the following contents:

    ```
    # CLAUDE.md

    This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

    ## Overview

    This demo is supposed to be showing how we utilize MCPs within the wider development process utilizing Claude Code itself.

    The application is utilizing the React and Tailwind frameworks to help generate a simple application that does the following:

    * Watch Claude Code use MCP servers to build a Pokémon fan site
    * Claude Code generates a polished React UI with Tailwind
    * Context7 provides current React/Tailwind documentation
    * Interactive Pokémon cards with stats and ratings

    ## Configuration

    The entire application will just be encapsulated in a single web page. There will be no stateful information saved as this is just a demo 
    ```

5. Start up Claude Code, famililarize yourself with the slash (/) commands of Claude, execute the following:

    ```
    /model - lists out models available to you.  Choose Sonnet or Opus.
    /stats - show your CC usage statistics.
    ```

6. Review your current context usage:

    ```
    /context
    ```

7. With no MCP servers loaded, your context available should be near the following:

    ![alt text](image-3.png)

4. Lets get some initial MCP servers configured for your application. Create a new `.mcp.json` and copy the following in.  This file is locally scoped to your project:

    ```
    {
        "mcpServers": {
            "context7": {
                "command": "npx",
                "args": ["-y", "@upstash/context7-mcp"]
            }
        }
    }
    ```

6. validate that your MCP server is up and running using the `/mcp` command.

    ![Validate MCP Servers](image.png)


7. Note your context consumed has now increased:
    ![alt text](image-4.png)








Notes:
The working build is located here for reference -> https://github.com/toddward/claude-code-mcp-demo