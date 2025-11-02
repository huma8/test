# NoterDome

> A modern, powerful note-taking application that combines the best of Notion's collaboration and Obsidian's knowledge management in a beautiful, intuitive interface.

## 🎯 Vision

NoterDome is designed to be your **second brain** - a unified workspace where ideas flow freely, knowledge connects naturally, and teams collaborate seamlessly. Whether you're a student organizing research, a developer documenting projects, or a team managing workflows, NoterDome adapts to your needs.

## ✨ Key Features

### 🔴 Core Features (Tier 1)
- **Rich Text Editor**: Markdown-first editing with WYSIWYG preview, supporting headings, lists, code blocks, callouts, and more
- **Smart Organization**: Flexible folder structure with tags, favorites, and powerful full-text search
- **Cross-Platform**: Native apps for Windows, macOS, Linux, iOS, Android + Progressive Web App
- **Real-Time Sync**: Instant synchronization across all your devices with conflict resolution
- **Markdown Support**: First-class markdown editing and viewing with syntax highlighting
- **Media Embedding**: Images, videos, PDFs, audio files, and web embeds with drag-and-drop
- **Theme System**: Beautiful dark and light themes with customizable accent colors

### 🟡 Power Features (Tier 2)
- **Bidirectional Linking**: Create wiki-style connections between notes with automatic backlink detection
- **Database Views**: Organize data with tables, Kanban boards, galleries, and calendar views
- **Template System**: Quick-start templates for meetings, projects, journals, and custom workflows
- **Collaboration**: Real-time co-editing, comments, mentions, and granular permissions
- **Web Clipper**: Browser extension to save articles, tweets, and web content directly to NoterDome
- **Offline Mode**: Full functionality without internet - sync when reconnected
- **Export Flexibility**: Export to Markdown, PDF, HTML, or backup entire workspace
- **Advanced Search**: Filter by date, tags, content, and custom properties with boolean operators

### 🟢 Advanced Features (Tier 3)
- **Graph View**: Interactive visualization of note connections with zoom, filter, and navigation
- **AI Assistant**: Intelligent writing helper for summarization, expansion, translation, and more
- **Plugin Ecosystem**: Extend functionality with community plugins or build your own
- **Canvas Mode**: Infinite whiteboard for visual thinking, mind mapping, and brainstorming
- **Relational Databases**: Link databases together with many-to-many relationships
- **Version History**: Complete revision history with diff viewer and one-click restore
- **End-to-End Encryption**: Optional E2EE for maximum privacy and security
- **Custom Domains**: Publish notes as a website with your own domain and SEO optimization

### 🔵 Unique Differentiators
- **Hybrid Architecture**: Best of both worlds - collaborative like Notion, powerful like Obsidian
- **Object-Based System**: Intelligent note types (person, project, meeting) with automatic properties
- **Daily Notes Automation**: Automatic daily note creation with templates and calendar integration
- **Query Language**: Dynamic content blocks that auto-update based on filters (e.g., "all tasks due this week")
- **Nested Databases**: Embed databases within notes for context-rich data management
- **Spaced Repetition**: Built-in flashcard system for learning and memorization
- **Publish & Share**: One-click publishing to web with customizable themes and analytics
- **Smart Linking**: AI-powered suggestion of related notes and automatic link creation
- **Focus Mode**: Distraction-free writing with typewriter mode and customizable UI
- **API-First Design**: Comprehensive REST API for integrations and automation

## 🏗️ Architecture

### Tech Stack
- **Frontend**: React 18+ with TypeScript
- **State Management**: Zustand for global state, React Query for server state
- **Editor**: ProseMirror or TipTap for rich text editing with custom extensions
- **Storage**: Local-first with IndexedDB, sync via WebSocket + REST API
- **Backend**: Node.js with Express or Fastify
- **Database**: PostgreSQL for structured data, S3-compatible storage for files
- **Real-Time**: WebSocket (Socket.io) for collaboration and live sync
- **Search**: Elasticsearch or MeiliSearch for full-text search
- **Desktop**: Electron for native apps with deep OS integration
- **Mobile**: React Native for iOS and Android

### Data Model
```
Workspace
├── Pages (recursive hierarchy)
│   ├── Content (rich text blocks)
│   ├── Properties (custom fields)
│   ├── Links (bidirectional)
│   └── Comments & Mentions
├── Databases
│   ├── Views (table, board, gallery, calendar)
│   ├── Filters, Sorts, Groups
│   └── Relations to other databases
├── Templates
├── Settings & Permissions
└── Plugins & Integrations
```

## 🎨 Design Philosophy

1. **Clarity Over Complexity**: Every feature should be intuitive and discoverable
2. **Performance First**: Fast page loads, instant search, smooth animations
3. **Local-First**: Data lives on your device; sync is an enhancement, not a requirement
4. **Keyboard-Driven**: Power users should be able to navigate entirely via keyboard
5. **Beautiful by Default**: No configuration needed to look great
6. **Extensible**: Plugin system allows customization without bloating core

## 📱 User Experience

### Core Workflows

#### Quick Capture
1. Press `Cmd/Ctrl + Shift + N` anywhere in the OS to create a new note
2. Type naturally - markdown formats automatically
3. Use `/` to insert blocks (headings, images, code, etc.)
4. `Cmd/Ctrl + K` for command palette to search, navigate, or execute actions

#### Knowledge Building
1. Write notes with `[[double brackets]]` to create links
2. Hover over links to preview content without navigating
3. View graph to discover unexpected connections
4. Use backlinks panel to see what references current note

#### Team Collaboration
1. Share workspace or individual pages with teammates
2. Set permissions: view, comment, or edit
3. See real-time cursors and edits as they happen
4. Leave inline comments and @mention team members
5. Track changes with version history

#### Project Management
1. Create a database for tasks/projects
2. Switch between table, board, and calendar views
3. Add custom properties (status, priority, assignee, dates)
4. Use filters to create saved views (e.g., "My Tasks This Week")
5. Embed database views in project pages for context

## 🔐 Privacy & Security

- **Data Ownership**: Your data is yours. Export anytime in open formats.
- **Privacy Options**: 
  - Local-only mode (no cloud sync)
  - Self-hosted option for complete control
  - End-to-end encryption for sensitive data
- **Transparency**: Open-source core with regular security audits
- **GDPR Compliant**: Full data portability and right to deletion

## 🚀 Getting Started

### Installation
```bash
# Desktop (Electron)
Download from: https://NoterDome.app/download

# Web App
Visit: https://app.NoterDome.app

# Self-Hosted
docker pull NoterDome/server:latest
docker run -d -p 3000:3000 NoterDome/server
```

### First Steps
1. Create your first workspace
2. Start with a blank page or choose a template
3. Try typing `/` to see available blocks
4. Create links with `[[page name]]`
5. Invite team members from settings

## 📦 Project Structure

```
NoterDome/
├── apps/
│   ├── web/                 # Web application (React)
│   ├── desktop/             # Electron wrapper
│   ├── mobile/              # React Native app
│   └── web-clipper/         # Browser extension
├── packages/
│   ├── editor/              # Core editor (ProseMirror/TipTap)
│   ├── ui/                  # Shared UI components
│   ├── database/            # Database views & logic
│   ├── sync/                # Sync engine
│   ├── plugins/             # Plugin system
│   └── api-client/          # API client library
├── services/
│   ├── api/                 # Backend API (Node.js)
│   ├── sync-server/         # WebSocket sync server
│   ├── search/              # Search service
│   └── ai/                  # AI assistant service
└── docs/                    # Documentation
```

## 🎯 Development Roadmap

### Phase 1: Foundation (Months 1-3)
- [ ] Core editor with markdown support
- [ ] Folder structure and basic organization
- [ ] Local storage with IndexedDB
- [ ] Dark/light themes
- [ ] Cross-platform apps (web, desktop)

### Phase 2: Knowledge Graph (Months 4-6)
- [ ] Bidirectional linking
- [ ] Backlinks panel
- [ ] Graph visualization
- [ ] Search and filtering
- [ ] Templates system

### Phase 3: Collaboration (Months 7-9)
- [ ] Cloud sync infrastructure
- [ ] Real-time collaboration
- [ ] Comments and mentions
- [ ] Sharing and permissions
- [ ] Version history

### Phase 4: Power Features (Months 10-12)
- [ ] Database views (table, board, gallery, calendar)
- [ ] Canvas/whiteboard mode
- [ ] Web clipper extension
- [ ] API and webhooks
- [ ] Plugin marketplace

### Phase 5: AI & Advanced (Months 13-18)
- [ ] AI writing assistant
- [ ] Smart linking suggestions
- [ ] Auto-categorization
- [ ] Publish to web
- [ ] Mobile apps (iOS, Android)

### Phase 6: Enterprise (Months 19-24)
- [ ] Self-hosted option
- [ ] End-to-end encryption
- [ ] Advanced analytics
- [ ] SSO and SAML
- [ ] Admin controls and audit logs

## 🤝 Contributing

We welcome contributions! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Areas for Contribution
- **Core Features**: Editor enhancements, database views, sync engine
- **Plugins**: Build extensions for community needs
- **Themes**: Design beautiful color schemes
- **Translations**: Help make NoterDome multilingual
- **Documentation**: Improve guides and tutorials
- **Bug Fixes**: Review issues and submit PRs

## 📄 License

NoterDome Core is licensed under AGPL-3.0 (open source).
NoterDome Cloud is a proprietary service built on top of the open-source core.

## 🔗 Links

- **Website**: https://NoterDome.app
- **Documentation**: https://docs.NoterDome.app
- **Blog**: https://blog.NoterDome.app
- **Community Forum**: https://community.NoterDome.app
- **GitHub**: https://github.com/NoterDome/NoterDome
- **Discord**: https://discord.gg/NoterDome

## 💬 Community & Support

- **Discord**: Join our Discord for real-time chat and support
- **Forum**: Ask questions and share ideas
- **Twitter**: Follow [@NoterDome](https://twitter.com/NoterDome) for updates
- **Email**: support@NoterDome.app

## 🙏 Acknowledgments

Inspired by the best aspects of:
- **Notion**: Collaboration and database views
- **Obsidian**: Graph view and local-first architecture
- **Roam Research**: Bidirectional linking
- **Coda**: Dynamic content and formulas
- **OneNote**: Freeform canvas
- **Evernote**: Web clipper and organization

Built with ❤️ by a community of developers, designers, and note-taking enthusiasts who believe knowledge should be free, interconnected, and beautiful.

---

**Ready to build your second brain?** [Download NoterDome](https://NoterDome.app/download) or [Try it online](https://app.NoterDome.app)
