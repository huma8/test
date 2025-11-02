# NoterDome System Patterns

## Overall Architecture
NoterDome follows a client-server architecture with the following key components:

1. **Frontend Applications** (React 18+)
   - Web application
   - Desktop application (Electron)
   - Mobile application (React Native)

2. **Backend Services** (Node.js)
   - API service for CRUD operations
   - Sync server for real-time collaboration
   - Search service for full-text search
   - AI service for intelligent features

3. **Data Storage**
   - PostgreSQL for structured data
   - IndexedDB for local client storage
   - S3-compatible storage for files

## Key Technical Patterns

### State Management
- **Frontend**: Zustand for global state, React Query for server state
- **Backend**: Express.js with middleware pattern for request processing
- **Sync**: WebSocket-based real-time updates with conflict resolution

### Component Architecture
- **UI Components**: Atomic design principles with reusable elements
- **Feature Components**: Domain-focused components that encapsulate functionality
- **Layout Components**: Structure components that define page layout

### Data Flow
1. User interacts with UI components
2. Actions are dispatched to state management system
3. State changes trigger API calls when needed
4. Server state is synced back to client
5. UI updates based on state changes

### API Design
- RESTful API for CRUD operations
- WebSocket connections for real-time updates
- GraphQL for complex data queries (future consideration)
- Consistent response format across all endpoints

## Critical Implementation Paths

### Note Creation and Storage
1. User creates new note in editor
2. Note is stored in local IndexedDB
3. Sync service queues note for server update
4. Server validates and stores note in PostgreSQL
5. Server broadcasts update to other connected clients
6. Conflict resolution occurs if needed

### Bidirectional Linking
1. User creates link using [[double brackets]]
2. Link is parsed and stored as reference
3. Backlink detection algorithm identifies reverse links
4. Backlink information is stored and updated
5. Graph visualization engine renders connections

### Search Functionality
1. Search queries are sent to search service
2. Search service queries Elasticsearch/MeiliSearch
3. Results are returned with relevance ranking
4. Results are displayed with context snippets
5. Filters are applied as needed

### Real-time Collaboration
1. WebSocket connections maintain client sessions
2. Operation transform algorithm handles concurrent edits
3. Cursor positions are shared between collaborators
4. Comment threads are synchronized in real-time
5. Permissions are enforced based on access levels

## Communication Protocols

### Client-Server Communication
- REST APIs for standard CRUD operations
- WebSocket for real-time collaboration
- Long-polling as fallback for real-time features

### Component Communication
- Prop drilling for direct parent-child communication
- Context API for shared state
- Custom events for cross-component communication
- Zustand for global state management

## Security Patterns
- JWT tokens for authentication
- Role-based access control for permissions
- Input sanitization at multiple levels
- Rate limiting for API endpoints
- End-to-end encryption for sensitive data (optional)