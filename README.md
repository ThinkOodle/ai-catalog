# OpenCode Catalog

Curated skills and MCP servers for the agency's OpenCode users.

## Overview

This repository contains:

- **skills.json**: Index of agency-approved skills
- **mcp-servers.json**: Index of curated MCP servers
- **skills/**: Directory containing SKILL.md files

## For Oodle AI Users

This catalog is automatically fetched by Oodle AI. You don't need to manually download anything - just browse and install from within the app.

## For Catalog Maintainers

### Adding a New Skill

1. Create a new directory under `skills/`:
   ```
   skills/my-new-skill/SKILL.md
   ```

2. Write your SKILL.md with proper frontmatter:
   ```markdown
   ---
   name: my-new-skill
   description: Brief description of what this skill does
   ---
   
   ## Overview
   ...
   ```

3. Add an entry to `skills.json`:
   ```json
   {
     "id": "my-new-skill",
     "name": "My New Skill",
     "description": "Brief description of what this skill does",
     "path": "skills/my-new-skill/SKILL.md",
     ...
   }
   ```

4. Update `lastUpdated` in `skills.json`

5. Commit and push to main

### Adding a New MCP Server

1. Add an entry to `mcp-servers.json`:
   ```json
   {
     "id": "server-id",
     "name": "Server Name",
     "description": "What this server does",
     "type": "remote",
     "url": "https://...",
     ...
   }
   ```

2. Update `lastUpdated` in `mcp-servers.json`

3. Commit and push to main

### Testing Changes

Before pushing, validate the JSON files:

```bash
# Check JSON syntax
cat skills.json | jq .
cat mcp-servers.json | jq .
```

## Schema Documentation

See [CATALOG_SCHEMA.md](../docs/CATALOG_SCHEMA.md) for detailed field descriptions.

## Questions?

Contact the agency dev team.
