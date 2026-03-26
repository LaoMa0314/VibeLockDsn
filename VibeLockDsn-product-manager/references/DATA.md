name:data-engineer
description:Design database table structures and fields based on functional modules/submodules, output database ER diagrams.

# Data Architecture Design Guide

## Prerequisites:
Must be analyzed based on functional modules and submodule lists.

## Core Concepts:
- **Database Table**: Corresponds to core entities of functional modules
- **Field**: Specific attributes in the table
- **ER Diagram**: Relationship diagram between database tables

## Output Tools:
All outputs must be displayed using Obsidian.

## Design Steps:
1. Directly decompose database tables according to functional modules/submodules
2. Design fields for each table (including field name, type, description, constraints)
3. Define relationships between tables (primary keys, foreign keys)
4. Display database ER diagrams using Canvas canvas

## Output Format:
### Database Table Structure Table:
| Functional Module | Submodule | Table Name | Field Name | Data Type | Field Description | Constraints |
|-------------------|-----------|------------|------------|-----------|-------------------|-------------|

### Database ER Diagram:
- Display relationships between tables using Canvas canvas
- Represent primary key and foreign key relationships between tables through connecting lines

## Obsidian Tool Reference:
| Tool Name | Core Function |
|-----------|---------------|
| defuddle | Clean web page/video content, extract main text and convert to Markdown |
| json-canvas | Generate/edit Canvas canvas, create mind maps, knowledge graphs |
| obsidian-bases | Operate Bases database views, convert notes into filterable tables/cards |
| obsidian-cli | Command line interface for automated knowledge base creation, search, organization |
| obsidian-markdown | Generate Markdown notes that comply with Obsidian syntax, supporting internal links, callouts, etc. |