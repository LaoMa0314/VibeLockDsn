name:prd-writer
description:Write Product Requirements Document (PRD).

# PRD Writing Guide

## Prerequisites:
- Requirement analysis document
- Functional architecture design results
- Process design results
- Data architecture design results
- Product prototype design results
- Interaction flow design results (if any)

## Output Tools:
All outputs must be displayed using Obsidian.

## Writing Principles:
- Inherit all deliverables from previous tasks
- Clear structure, complete content
- Concise language, easy to understand
- Include sufficient details for development and testing
- Optimize context window to support AI coding (vibe coding)

## PRD Structure (Optimized Version, Supporting AI Coding):

### 1. Core Summary (AI Priority Reading, Approximately 1000 words)
- **Product Objectives and Technology Stack**: Clarify product positioning and technology selection
- **Core Functional Module List**: Table format, including module names and priorities
- **Key Page Navigation Diagram**: Show relationships between pages

### 2. Page Detailed Specifications
#### Page 1: [Page Name]
- **Component List**: Name, function description, status (table format)
- **Prototype Diagram**: Pencil screenshot (with canvas access path), call pencil-export-2x skill to insert
- **Interaction Instructions**: Mapping relationships between user operations → system responses
- **API Call Points**: Endpoint, parameters, return structure definitions

### 3. Data Architecture Design
- **Data Model Definitions**: Core entities, attribute fields, relationship mappings
- **Database Design**: Table structures, indexes, constraint conditions
- **Data Flow Diagrams**: Data flow directions and processing logic
- **API Data Structures**: Request/response format definitions

### 4. Technical Implementation Guide
- **Design System Variables**: CSS variable definitions (colors, sizes, typography, etc.)
- **Component Library Usage Specifications**: Component naming, attribute definitions
- **Data Flow and State Management**: State management patterns based on interaction flows
- **Responsive Design Breakpoints**: Adaptation strategies for various terminals

### 5. Development Verification Checklist
- **Functional Acceptance Criteria**: Specific verification methods for each function
- **Performance Requirements**: Loading time, response speed, and other metrics
- **Compatibility Requirements**: Browser and device support scope

## Output Format:
### PRD Document:
- Use Obsidian Markdown format
- Include internal links to connect related documents
- Organize content using heading hierarchy
- Display structured data in tables
- Show visual content with Canvas

## Context Optimization Strategy:

### Layered Delivery Strategy:
1. **Core Layer**: Basic information (mandatory, approximately 1000 words)
2. **Development Layer**: Detailed specifications (on-demand loading, approximately 3000 words)
3. **Resource Layer**: Design assets (independent references)

### Intelligent Reference Mechanism:
- Use internal links to associate related documents
- Convert large design diagrams to reference links instead of inline
- Provide modular content structure to support AI on-demand reading

## Pencil Design Diagram Conversion Strategy:

### Direct Conversion Path:
1. **Export Format Optimization**: Use Pencil's HTML/CSS export function to generate basic code framework
2. **Component Extraction**: Split prototypes into reusable components and establish component mapping tables
3. **Design Token Extraction**: Extract design system variables from Pencil (colors, sizes, typography, etc.)

### Code Generation Enhancement:
- Add component naming conventions (consistent with mainstream frameworks like React/Vue component naming)
- Define state management patterns (based on interaction flows)
- Provide API integration point descriptions

## Obsidian Tool Reference:
| Tool Name | Core Function |
|-----------|---------------|
| defuddle | Clean web page/video content, extract main text and convert to Markdown |
| json-canvas | Generate/edit Canvas canvas, create mind maps, knowledge graphs |
| obsidian-bases | Operate Bases database views, convert notes into filterable tables/cards |
| obsidian-cli | Command line interface for automated knowledge base creation, search, organization |
| obsidian-markdown | Generate Markdown notes that comply with Obsidian syntax, supporting internal links, callouts, etc. |