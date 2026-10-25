# pressgeo-mcp# PressGEO Remote MCP Server

[![MCP Server](https://img.shields.io/badge/MCP-Server-blue)](https://pressgeo.com/mcp)
[![OpenAPI](https://img.shields.io/badge/OpenAPI-3.1-green)](https://pressgeo.com/api/public/openapi.json)

Official remote Model Context Protocol (MCP) server for [PressGEO](https://pressgeo.com). 

PressGEO provides real-time, owner-verified local business intelligence, buyer-intent AI search rankings, and machine-readable newsrooms across 20 US metros.

---

## Remote Endpoint

- **MCP Transport URL:** `https://pressgeo.com/mcp`
- **Transport Type:** HTTP (Streamed JSON-RPC / SSE)
- **Authentication:** None required (reads public, owner-confirmed business data)
- **OpenAPI 3.1 Spec:** `https://pressgeo.com/api/public/openapi.json`
- **AI Agent Docs:** `https://pressgeo.com/llms.txt`

---

## Available Tools

1. **`list_local_markets`**  
   List supported local metros (e.g., Phoenix, Scottsdale, Seattle, Boston) and available local service categories (home inspection, HVAC, plumbing, legal, etc.).

2. **`get_local_market`**  
   Retrieve verified local market rankings, buyer questions, and top-rated local providers in a specific metro and service category.

3. **`get_local_factsheet`**  
   Fetch owner-confirmed business facts, verified Google review counts, licensing details, and service boundaries for a specific company by domain or slug.

4. **`get_newsroom`**  
   Read the verified company newsroom, public releases, and published Answer Pages for a business.

---

## Quick Setup

### 1. Claude Desktop

Add this snippet to your `claude_desktop_config.json`:

```json
{
  "mcpServers": {
    "pressgeo": {
      "url": "https://pressgeo.com/mcp"
    }
  }
}
