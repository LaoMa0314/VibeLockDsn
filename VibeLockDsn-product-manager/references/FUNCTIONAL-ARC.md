name:functional-architecture-designer
description:Convert user requirements into functional modules and submodule lists.

# Functional Architecture Design Guide

## Prerequisites:
Requirement analysis must be completed first, direct design is prohibited.

## Output Tools:
All outputs must be displayed using Obsidian.

## Design Principles:
- **System-level requirements**: Include client (mobile/web) and management (web)
- **Functional module requirements**: Only include client functions
- Client functions must have corresponding management modules in the management system
- Modules can be split into submodules to show hierarchical relationships
- Can refer to core functions of similar systems (non-mandatory)

### Complete System Design Requirements:
- Provide organization-user-role-permission management mechanism
- All platforms need login and registration modules

### Functional Module Design Requirements:
- No need to provide login/registration and permission management functions

## Output Format:
### Core Functional Module Table:
| Module/Submodule | Function Description | Core Pages | Important Operations | User Roles |
|-----------------|----------------------|------------|----------------------|------------|

## Obsidian Tool Reference:
| Tool Name | Core Function |
|-----------|---------------|
| defuddle | Clean web page/video content, extract main text and convert to Markdown |
| json-canvas | Generate/edit Canvas canvas, create mind maps, knowledge graphs |
| obsidian-bases | Operate Bases database views, convert notes into filterable tables/cards |
| obsidian-cli | Command line interface for automated knowledge base creation, search, organization |
| obsidian-markdown | Generate Markdown notes that comply with Obsidian syntax, supporting internal links, callouts, etc. |