# NoterDome Active Context

## Current Work Focus
Currently setting up the project structure and initial documentation for NoterDome. Establishing the core architecture pattern based on the PRD requirements and preparing for initial development phases. Additionally, reconciling the project structure to address a discrepancy where wireframes are stored in the root wireframes/ directory rather than in the plan/Wireframes_and_Prototypes/ directory as indicated in the documentation.

## Recent Changes
- Created initial PRD documentation (1Unified Ultimate PRD.md)
- Set up task structure for multiple teams (Design, Engineering, QA, etc.)
- Created Multi-Agent PRD Router configuration
- Established Vibe Coding Agent Prompt for NoterDome
- Initialized Memory Bank structure
- Discovered structural discrepancy with wireframe storage location
- Created comprehensive QWEN.md file documenting project structure and context

## Next Steps
1. Begin implementation of core editor functionality
2. Set up development environment and initial project scaffolding
3. Implement basic note creation and storage functionality
4. Establish sync mechanism between client and server
5. Reconcile wireframe directory structure to match intended organization (decide whether to move wireframes to plan/Wireframes_and_Prototypes/ or update documentation to reflect current structure)

## Active Decisions and Considerations
- Editor choice: TipTap vs ProseMirror for rich text editing
- Real-time sync approach: WebSocket implementation details
- Database schema for notes, links, and metadata
- Frontend architecture: Component structure and state management
- Directory structure: Whether to move wireframes to plan/Wireframes_and_Prototypes/ or update documentation to match current structure

## Important Patterns and Preferences
- Follow React best practices with TypeScript
- Use modular, component-based architecture
- Prioritize performance with virtualization for large datasets
- Implement comprehensive error handling and offline support
- Maintain accessibility standards throughout
- Ensure project documentation accurately reflects actual file structure

## Learnings and Project Insights
- The multi-agent approach allows for parallel development of different components
- Memory Bank documentation is critical for maintaining context across sessions
- The PRD structure provides clear direction for development phases
- Task breakdown by department ensures accountability and progress tracking
- Consistency between project documentation and actual file structure is important for maintainability