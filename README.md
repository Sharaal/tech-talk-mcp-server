# Tech Talk MCP Server

MCP = Model Context Protocol

Created by Anthropic (Claude), supported by OpenAI (ChatGPT).

## Without MCP

![Without MCP](1-without-mcp.png)

Tools like Cursor, VSCode implement features like web requests to provide context to the AI models.

Two large issues:
* Different tools have different features
* Tool maintainer needs to support features

## With MCP

Tools = MCP Client
Features = MCP Server

![With MCP](2-with-mcp.png)

The tools only know how to use MCP Servers. The MCP Servers provide functionalities.

Advantages:
* A lot of functionalities can be used with every tool
* The maintainer of functionalities can provide MCP server, indepent of the tool 

Functionality = context & actions.

# Examples

## Example MCP Server: Postgres

```
Look at the posgres database via mcp server postgres and create a `database.md` file with the relational database model using mermaid.

Also make a markdown table with the first row of each table.
```

## (Maybe) useful MCP Servers

* [crawl4ai](https://github.com/unclecode/crawl4ai) - Crawl documentation for local knowledge base
* [Brave](https://github.com/modelcontextprotocol/servers/tree/main/src/brave-search) - Request URLs
* [File system](https://github.com/modelcontextprotocol/servers/tree/main/src/filesystem) - Access to file system (outside of project workspace)
* [Git](https://github.com/modelcontextprotocol/servers/tree/main/src/git) - Commit, branch in the AI chat
* [Taskmaster AI](https://www.taskmaster.one/) - Task management inside AI chat

Some other maintained by MCP themself: 
https://github.com/modelcontextprotocol/servers/tree/main/src

## Example usage: n8n Workflow

https://n8n.io/

# Build own MCP Server

https://modelcontextprotocol.io/quickstart/server#node

# Future

* Currently only dev tools supporting it
