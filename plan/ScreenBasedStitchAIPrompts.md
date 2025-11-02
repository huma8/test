# NoteCraft - Stitch AI Screen/View Prompts

Production-ready screen prompts for Stitch AI. Each prompt creates a complete, functional screen.

---

## 🎯 Core Screens (Must-Have)

### 1. Main Application Shell
**Screen Name**: `MainAppLayout`

**Prompt**: 
"Create a complete note-taking application layout. Left sidebar (250px, collapsible) with nested folder tree (drag-drop enabled), search bar at top, 'New Note' button, recent pages section. Top navbar (60px) with logo, global search (Cmd+K hint), sync status, notifications bell with badge, theme toggle, user avatar menu. Main content area with clean editor (markdown + rich text). Right sidebar (300px, collapsible, tabs: Properties, Backlinks, Outline, Comments). All sidebars have collapse buttons. Dark mode compatible. Modern, minimal design with soft shadows."

**Contains**: Sidebar, TopNav, Editor Area, RightSidebar, all navigation

---

### 2. Editor View (Focus Mode)
**Screen Name**: `EditorScreen`

**Prompt**:
"Design a distraction-free editor screen. Top: breadcrumbs + page icon + editable title (large). Main area: rich text editor with floating toolbar (appears on selection: bold, italic, link, color). Slash commands menu (type / to open blocks: heading, image, table, code, callout). Inline @ mentions. Live markdown preview. Block handles (6-dot) on hover showing drag/delete/more. Bottom: word count + last saved indicator. Minimal UI, generous whitespace, focus on content."

**Contains**: Editor, InlineToolbar, SlashMenu, BlockHandles, PageHeader

---

### 3. Database Table View
**Screen Name**: `DatabaseTableView`

**Prompt**:
"Create a spreadsheet-like database view. Top toolbar: view switcher (Table, Board, Gallery, Calendar icons), filter button (shows active filters as chips), sort button, group by button, properties menu (show/hide columns), settings gear. Main area: resizable columns with headers (click to sort), inline cell editing (different input types: text, select, date, number, checkbox), row selection checkboxes, add row button at bottom, horizontal + vertical scroll. Each cell editable on click. Modern table design with hover states."

**Contains**: Table, Filters, Sorting, Grouping, PropertyEditor, ViewSwitcher

---

### 4. Database Board View (Kanban)
**Screen Name**: `DatabaseBoardView`

**Prompt**:
"Design a Kanban board view. Top: same toolbar as table view (filters, sort, etc.). Main area: horizontal columns for each status/stage (To Do, In Progress, Done), column headers with count badges + 'Add card' button. Cards show: small icon, title, properties as badges, assignee avatars. Drag-drop cards between columns. Drag-drop to reorder columns. Each column scrollable vertically. Add new column button on right. Smooth drag animations. Color-coded by status."

**Contains**: KanbanColumns, Cards, DragDrop, Filters, ViewSwitcher

---

### 5. Graph Visualization
**Screen Name**: `GraphView`

**Prompt**:
"Create an interactive knowledge graph. Full-screen canvas with nodes (circles) representing notes, sized by connection count, connected by lines. Different node colors for note types (page, database, daily note). Left panel: search filter, tag checkboxes, depth slider (1-3 levels), layout toggle (force/hierarchical). Right panel: selected node info (title, snippet, open button). Zoom controls (bottom-right): +/-, reset, minimap. Click node to navigate, drag to reposition, hover shows tooltip. Dark mode friendly with vibrant node colors."

**Contains**: GraphCanvas, FilterPanel, NodeDetails, ZoomControls, Minimap

---

### 6. Search Results
**Screen Name**: `SearchResultsScreen`

**Prompt**:
"Design search results page. Top: large search bar with filters button (date, type, author). Left sidebar: filters (Content Type, Modified Date, Created By, Tags) with checkboxes and date pickers. Main area: results list showing icon, title, matching snippet (highlighted search terms), breadcrumb path, last modified date. Click result opens page. Keyboard navigation (↑↓ to navigate, Enter to open). Count at top ('42 results for "design"'). Sort options (relevance, date). Load more at bottom."

**Contains**: SearchBar, FilterSidebar, ResultsList, Pagination

---

### 7. Canvas/Whiteboard
**Screen Name**: `CanvasWorkspace`

**Prompt**:
"Create infinite canvas workspace. Top toolbar (floating): selection tool, pen, shapes (rect, circle, arrow), text box, sticky note, connector line, undo/redo, zoom indicator. Left panel: layers list (thumbnail + name + visibility toggle). Main area: infinite pannable canvas with grid background (toggleable), objects can be placed/resized/moved anywhere. Right panel: selected object properties (color, size, opacity). Minimap in bottom-right corner. Smooth pan/zoom. Snap-to-grid option."

**Contains**: Toolbar, Canvas, LayersPanel, PropertiesPanel, Minimap

---

### 8. Settings Screen
**Screen Name**: `SettingsScreen`

**Prompt**:
"Design comprehensive settings. Left sidebar: navigation tabs (General, Appearance, Shortcuts, Account, Workspace, Billing, Integrations) with icons. Main area: form layouts with sections and dividers. Appearance section: theme picker (light/dark/auto with previews), accent color swatches, font family dropdown, size slider, live preview pane. Account section: profile picture upload circle, name/email inputs, password change, 2FA toggle. Save changes button (sticky bottom-right). Clean, organized layout."

**Contains**: SettingsNav, Forms, ThemePicker, ProfileUpload, PreviewPane

---

### 9. Login/Signup Screen
**Screen Name**: `AuthScreen`

**Prompt**:
"Create split-screen auth page. Left side (60%): hero image or gradient background, app logo, tagline ('Your second brain'), feature highlights with icons. Right side (40%): centered form card with shadow. Tabs at top (Login / Sign Up). Login form: email input, password input (show/hide eye icon), remember me checkbox, forgot password link, login button (full width, accent color), divider with 'OR', social login buttons (Google, Apple, GitHub with logos). Signup form similar with name field added and password strength meter. Mobile: stacked layout."

**Contains**: LoginForm, SignupForm, SocialAuth, HeroSection

---

### 10. Onboarding Wizard
**Screen Name**: `OnboardingFlow`

**Prompt**:
"Design multi-step onboarding. Top: progress bar (4 steps indicator: 1●●○○). Step 1: Welcome (hero image, 'Welcome to NoteCraft', personalized greeting, continue button). Step 2: Workspace setup (name input, icon picker, description). Step 3: Invite team (email inputs, role dropdowns, skip option). Step 4: Choose template or start blank (template cards in grid: Meeting Notes, Project Tracker, Personal Journal, each with preview image and description). Bottom: Previous/Next buttons, Skip link. Smooth slide transitions between steps."

**Contains**: ProgressIndicator, WizardSteps, TemplateGallery, Navigation

---

## 🎨 Secondary Screens (Important)

### 11. User Profile Screen
**Screen Name**: `UserProfileScreen`

**Prompt**:
"Create user profile page. Top banner: cover image (editable), profile picture (large, overlapping banner), name (editable inline), role badge, edit profile button. Below: tabs (About, Activity, Settings). About tab: bio, joined date, pages created count, location, social links. Activity tab: timeline of recent actions (created X, edited Y, commented on Z) with timestamps. Clean card-based layout. Sidebar showing user's favorite pages and recent workspaces."

---

### 12. Workspace Dashboard
**Screen Name**: `WorkspaceDashboard`

**Prompt**:
"Design workspace overview. Top: workspace name + icon, member avatars (show 5, +N more), invite button, settings gear. Grid of cards: Quick Stats (total pages, active members, storage used - each as card with icon + number + sparkline), Recent Activity (list of latest edits), Frequently Visited (page thumbnails in grid), Shortcuts (create note, daily note, templates). Sidebar: workspace switcher, folder tree. Modern dashboard layout with spacing."

---

### 13. Page History/Versions
**Screen Name**: `VersionHistoryScreen`

**Prompt**:
"Create version history interface. Left sidebar: timeline of versions (newest first) showing date, time, author avatar, change summary. Click version to preview. Main area: split view showing selected version on left, current version on right, with diff highlighting (additions in green, deletions in red strikethrough). Top: restore this version button, close history button. Scrub through versions with slider at bottom."

---

### 14. Share & Collaborate Screen
**Screen Name**: `ShareScreen`

**Prompt**:
"Design sharing modal (centered overlay). Top: 'Share [Page Name]' title. Section 1: Link sharing toggle (on/off), generated link input (copy button), permission dropdown (view/comment/edit), expiry date picker, password protection toggle. Section 2: Invite by email (email input + role dropdown + send button). Section 3: Current access list (table: user avatar, name, email, role dropdown, remove button). Bottom: Done button. Modern modal with blur backdrop."

---

### 15. Template Gallery
**Screen Name**: `TemplateGalleryScreen`

**Prompt**:
"Create template marketplace. Top: search bar, filter dropdown (category, popularity, recent). Left sidebar: categories (Personal, Work, Education, Creative) with icons and counts. Main grid: template cards (3 per row) showing preview thumbnail, title, description, author, use count, 'Use Template' button. Hover shows larger preview. Click card opens full preview modal (full template structure, use button, details). Featured section at top. Load more at bottom."

---

### 16. Notifications Center
**Screen Name**: `NotificationsScreen`

**Prompt**:
"Design notifications page. Top tabs: All, Unread, Mentions, Comments, Activity. Each notification card: icon (type indicator), avatar (who), message ('John mentioned you in Meeting Notes'), timestamp (2 hours ago), mark as read button, click to navigate. Group by date (Today, Yesterday, This Week). Bulk actions: mark all as read, clear read notifications. Empty state with illustration. Filter by workspace dropdown."

---

### 17. Admin Dashboard
**Screen Name**: `AdminDashboardScreen`

**Prompt**:
"Create admin control panel. Top nav: tabs (Overview, Members, Audit Log, Settings, Billing). Overview: stats cards (total members, storage, active users today, AI usage), usage charts (storage over time, daily active users graph), system health indicators (API status, sync status, search status - green/red). Quick actions: invite members, view audit log, manage billing. Recent activity feed in sidebar. Professional, data-heavy design."

---

### 18. Mobile Note Editor
**Screen Name**: `MobileEditorScreen`

**Prompt**:
"Design mobile-optimized editor (360px width). Top: back button, page title (editable, large), more menu (3 dots). Main: editor with large tap targets, simplified toolbar (sticky at bottom above keyboard): bold, italic, heading, list, link, image, more. Slash commands menu (takes 70% screen height, dismissable). Swipe actions: swipe block left for delete, swipe right for more options. Bottom toolbar: undo, redo, formatting, done. Safe area padding."

---

### 19. Mobile Navigation
**Screen Name**: `MobileNavScreen`

**Prompt**:
"Create mobile sidebar (drawer from left). Top: user profile section (avatar, name, workspace). Quick actions: New Note (prominent), Daily Note, Search. Folder tree (collapsible sections). Recent pages list. Bottom: Settings, Help, Sign Out. Swipe from left edge to open, tap outside or back to close. Overlay backdrop. Smooth slide animation."

---

### 20. Command Palette
**Screen Name**: `CommandPaletteModal`

**Prompt**:
"Design command palette (Cmd+K). Centered modal (600px width): large search input at top, live-filtered results below categorized (Recent, Pages, Actions, Templates, People). Each result: icon, title, category badge, keyboard shortcut (if any). Keyboard navigation (↑↓ to move, Enter to select, Esc to close). Fuzzy search. Show recent searches when empty. Blur backdrop. Fast, responsive filtering."

---

## 📱 Mobile-Only Screens

### 21. Mobile Home
**Screen Name**: `MobileHomeScreen`

**Prompt**:
"Design mobile home screen. Top: search bar (tap to open search), create FAB (bottom-right, + icon). Main: sections (Recent, Favorites, Workspaces) each with horizontal scrollable cards. Pull-to-refresh gesture. Bottom nav: Home, Search, Create (center, elevated), Notifications, Profile. Card-based layout optimized for touch."

---

### 22. Mobile Search
**Screen Name**: `MobileSearchScreen`

**Prompt**:
"Create mobile search. Top: back button, search input (auto-focused), voice search icon, filter button. Recent searches below (swipe left to delete). Results as list cards: icon, title, snippet, swipe actions (open, star). Empty state with suggestions. Keyboard has search button. Filter sheet slides from bottom."

---

## 🎯 Summary

### **Total: 22 Complete Screens** (not 200 components)

**Why This Works for Stitch AI:**
1. ✅ Each prompt creates **ONE complete, functional screen**
2. ✅ Components are **naturally included** within screens
3. ✅ **Less redundancy** - no duplicate work
4. ✅ **Faster iteration** - change whole screen at once
5. ✅ **More cohesive** - designs match better

**Implementation Order:**
1. **Week 1-2**: Screens 1, 2, 9 (Shell, Editor, Auth) → MVP
2. **Week 3-4**: Screens 3, 4, 6 (Database views, Search)
3. **Week 5-6**: Screens 5, 7, 10 (Graph, Canvas, Onboarding)
4. **Week 7-8**: Screens 8, 11-20 (Settings, secondary screens)
5. **Week 9-10**: Screens 21-22 + Polish

**For Each Screen:**
- Generate in Stitch AI
- Export as React component
- Integrate into your app
- Customize as needed

This is **the right approach for Stitch AI** - think in screens, not atoms! 🎯
