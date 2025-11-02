# NoterDome Tech Context

## Technologies Used

### Frontend Stack
- **Framework**: React 18+ with TypeScript
- **State Management**: Zustand for global state, React Query for server state
- **Styling**: Tailwind CSS with custom theme system
- **Editor**: TipTap or ProseMirror for rich text editing
- **Build Tool**: Vite for development and build processes
- **Testing**: Jest, React Testing Library, Cypress

### Backend Stack
- **Runtime**: Node.js
- **Framework**: Express.js or Fastify
- **Database**: PostgreSQL for structured data
- **Search**: Elasticsearch or MeiliSearch
- **File Storage**: S3-compatible object storage
- **Real-time**: WebSocket with Socket.io
- **Testing**: Jest, Supertest

### Infrastructure
- **Containerization**: Docker for consistent environments
- **Orchestration**: Docker Compose for local development
- **CI/CD**: GitHub Actions
- **Monitoring**: Application performance monitoring tools
- **Logging**: Structured logging system

## Development Setup

### Required Dependencies
- Node.js v18+ (LTS recommended)
- PostgreSQL 13+
- Docker and Docker Compose
- Git
- Package manager (npm, yarn, or pnpm)

### Development Workflow
1. Clone the repository
2. Run `docker-compose up` to start services
3. Install dependencies with your chosen package manager
4. Configure environment variables
5. Start development servers

### Environment Configuration
Environment variables are managed through:
- `.env` files for local development
- Environment variables in deployment
- Configuration validation at startup

### Project Structure and Documentation
- Organized in directories: plan/, screens/, wireframes/, QWEN.md
- Planning and documentation in the plan/ directory
- HTML prototypes in screens/ and wireframes/ directories
- Comprehensive project context in QWEN.md for AI collaboration
- Memory Bank system in plan/Memory_Bank/ for maintaining project continuity

### API Documentation
- OpenAPI/Swagger for API endpoint documentation
- Postman collections for testing
- Inline code documentation with JSDoc

## Technical Constraints

### Performance Requirements
- Application should load in under 2 seconds
- Editor should respond to input in under 16ms
- Search should return results in under 500ms
- Sync operations should complete in under 1 second

### Scalability Targets
- Support 10,000+ concurrent users
- Handle 1M+ notes per workspace
- Support 1000+ connections per sync server
- Store unlimited attachments (within user quota)

### Security Requirements
- All data in transit encrypted with TLS
- Optional end-to-end encryption for sensitive data
- Passwords hashed with bcrypt
- Rate limiting on all public endpoints
- Input sanitization to prevent XSS

### Compatibility Requirements
- Modern browsers (Chrome, Firefox, Safari, Edge)
- Windows 10+, macOS 10.15+, Linux
- iOS 13+, Android 8+
- Screen readers and accessibility tools

## Tool Usage Patterns

### Git Workflow
- Feature branches for development
- Pull requests with code review
- Conventional commits for semantic versioning
- Automated testing on all changes

### Code Quality
- TypeScript for type safety
- ESLint for code style consistency
- Prettier for code formatting
- Automated testing with minimum 80% coverage
- Pre-commit hooks for code quality checks

### Package Management
- npm for dependency management
- Semantic versioning for releases
- Lock files for reproducible builds
- Vulnerability scanning for dependencies

### Documentation and Knowledge Management
- Memory Bank system for maintaining project context
- QWEN.md for comprehensive project documentation
- Regular updates to project structure documentation
- Resolution of structural discrepancies between docs and implementation

### Monitoring and Observability
- Structured logging with severity levels
- Performance monitoring and alerting
- Error tracking and reporting
- Usage analytics (privacy-compliant)
- Health checks for services