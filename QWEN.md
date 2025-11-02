# NoterDome Project Context

## Project Overview
NoterDome is a modern, powerful note-taking application that combines the best of Notion's collaboration and Obsidian's knowledge management in a beautiful, intuitive interface. It's designed to be a unified workspace where ideas flow freely, knowledge connects naturally, and teams collaborate seamlessly.

## Directory Structure
The project follows a well-organized structure divided into three main directories:

```
test/
├── plan/                    # Project documentation and planning
│   ├── Core_Documents/      # Main project overview and architecture
│   ├── Design_System/       # AI Prompt Templates and Design Guidelines
│   ├── Development_Guides/  # Implementation guidelines for developers
│   ├── Memory_Bank/         # Core project context files
│   ├── Project_Management/  # Requirements documents and tracking
│   ├── Tasklist/            # Department-specific task breakdowns
│   ├── master.json          # Project configuration file
│   └── README.md            # Project structure documentation
├── screens/                 # HTML screen files (10-20+ files)
├── wireframes/              # HTML wireframe files (10+ files)
└── QWEN.md                  # This project context file
```

## Project Components

### Plan Directory
Contains all project documentation, requirements, and organizational structure:
- **Project Requirements**: `plan/Project_Management/1Unified Ultimate PRD.md`
- **Development Guidelines**: `plan/Development_Guides/3VibeCodingPrompt.md`
- **Current Context**: `plan/Memory_Bank/activeContext.md`
- **Project Brief**: `plan/Memory_Bank/projectbrief.md`
- **Task Management**: `plan/Tasklist/` directory

### Screens Directory
Contains the UI implementation files:
- Multiple HTML files representing different application screens
- Files are numbered (1-21+) for organization
- Examples include: dashboard, editor, mobile views, authentication screens

### Wireframes Directory
Contains wireframe implementations:
- HTML files representing UI wireframes for different components
- Includes main layout, editor views, and navigation components
- These are the wireframes referenced in the documentation, but currently stored outside the plan folder

## Key Features
Based on the project documentation and files:
- Rich text editor with Markdown-first approach
- Cross-platform compatibility (web, desktop, mobile)
- Real-time synchronization across devices
- Bidirectional linking and graph visualization
- Database views for structured data (table, board, gallery, calendar)
- Local-first architecture with optional cloud sync
- Privacy-focused with end-to-end encryption option

## Technical Context
- The application uses React with TypeScript based on development guidelines
- Component-based architecture with modular design
- Emphasis on performance with virtualization for large datasets
- Accessibility standards throughout the interface
- Real-time sync with WebSocket implementation
- TipTap vs ProseMirror for rich text editing (decision pending)

## Current State
The project is in the setup phase with:
- Initial PRD documentation created
- Task structure set up for multiple teams (Design, Engineering, QA, etc.)
- Multi-Agent PRD Router configuration established
- Memory Bank structure initialized
- UI wireframes and screens implemented as HTML files

## Important Note on Structure
There is a discrepancy between the intended and actual project structure:
- The `plan/Wireframes_and_Prototypes/` directory is empty
- Wireframes are stored in the root `wireframes/` directory instead
- This may need to be reconciled for consistency

## For Future Work
1. Begin implementation of core editor functionality
2. Set up development environment and initial project scaffolding
3. Implement basic note creation and storage functionality
4. Establish sync mechanism between client and server
5. Reconcile wireframe directory structure to match intended organization