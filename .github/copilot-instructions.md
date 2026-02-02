# Copilot Instructions for System Architecture Course

## Project Purpose
This is an educational curriculum repository for learning **System Architecture**—the art of designing complex systems by navigating trade-offs between functionality, scalability, maintainability, and cost. The project is structured as a **progressive learning path** from foundational technical skills to enterprise-level strategic decision-making.

## Architecture & Structure

### Organization
- **Readme.md**: High-level overview and project status
- **Introduction.md**: Conceptual framework—the "5 Pillars of System Architecture" (Infrastructure, Data, Software, Interfaces, Security/NFRs)
- **Curriculum.md**: Complete course structure spanning 3 phases + capstone
  - Phase 1: Foundation (technical core, system basics)
  - Phase 2: Applied Architecture (design patterns, scalability, reliability)
  - Phase 3: Enterprise Strategy (governance, cost optimization, compliance)
- **Phase Folders**: Each phase has its own folder with modular markdown files for each topic.

### Content Pattern
Each module follows an **educational progression**:
1. **Core Concepts**: Theoretical foundations
2. **Architectural Relevance**: Why this matters for system design
3. **Code Examples**: Practical demonstrations (typically TypeScript/C/Python)
4. **Real-world Applications**: How concepts map to actual systems

## Key Patterns & Conventions

### Trade-off Documentation
The curriculum emphasizes that "**every choice is a trade-off**." When suggesting architectural improvements or examples:
- Always identify downsides, not just benefits
- Frame decisions as "favoring X over Y because of [trade-off]"
- Example: "Composition over inheritance because deep hierarchies reduce flexibility and increase coupling"

### Multi-Layer Examples
Complex topics use **progressive disclosure**:
1. Simple concept definition
2. OOP/Systems principle explanation
3. Code example (often multiple languages side-by-side)
4. Architectural implication
- Follow this pattern when extending content

## Development Workflow

### No Build System
This is **documentation-only**; no builds, tests, or servers required. Edits are direct markdown modifications.

### Content Guidelines
- **Keep examples practical**: Code should compile/run (TypeScript examples use correct syntax)
- **Link to resources**: Introduction.md includes reference citations—maintain this format
- **Maintain narrative flow**: Each section builds on previous knowledge progressively

### File Naming
All learning modules are markdown files (`.md`) organized by phase and topic hierarchy.

## What AI Agents Should Know

### Before Adding Content
1. **Read the target phase introduction** to understand learning objectives
2. **Check curriculum hierarchy** (Curriculum.md) to avoid duplication
3. **Match existing patterns**: Follow the structure and code example style of existing modules

### When Extending Modules
- Add examples in **TypeScript first** (primary language), then C/Python if showing low-level concepts
- Include **architectural relevance** section for each technical concept
- Update **Curriculum.md** table of contents if adding new sections
- Preserve the "trade-off mentality"—avoid prescriptive advice without acknowledging downsides

### Common Additions
- **New technical modules**: Should fit under one of the 3 phases; reference the 5 Pillars
- **Code examples**: Syntax must be valid; include variable types and error handling
- **Reading/Resources**: Format as ordered list with authors, dates, and links (see Introduction.md)

## Key Files to Reference
- [Introduction.md](../Introduction.md): Conceptual framework (5 Pillars)
- [Curriculum.md](../Curriculum.md): Full learning path and learning objectives