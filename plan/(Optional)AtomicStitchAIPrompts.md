# NoterDome - Complete UI/UX Components & Stitch AI Prompts

Comprehensive component library for a production-ready note-taking application.

---

## 🏠 Core Layout & Navigation (10 components)

### 1. AppShell
**Prompt**: "Create a modern note-taking app layout with a collapsible sidebar on the left showing nested folder structure with icons, a main content area with a clean editor, and a right sidebar for properties/backlinks. Include a top navigation bar with search, theme toggle, and user menu. Use a minimalist design with soft shadows and rounded corners. Colors: neutral background with accent colors for interactive elements."

### 2. TopNavbar
**Prompt**: "Design a top navigation bar with logo on left, global search in center (with Cmd+K shortcut hint), and right section showing: sync status indicator, notifications bell with badge, theme toggle, and user avatar dropdown. Height: 60px. Glass morphism effect with subtle backdrop blur."

### 3. NavigationSidebar
**Prompt**: "Create a sidebar navigation with drag-and-drop folder tree, each item showing icon, title, and hover actions (add, delete, more). Include a search bar at top, quick access buttons for 'New Note', 'Daily Note', and 'Templates'. Show visual indicators for notes with backlinks. Collapsible sections with smooth animations."

### 4. RightSidebar
**Prompt**: "Design a collapsible right sidebar with tabs for: Properties, Backlinks, Outline, Comments. Each tab content should be scrollable independently. Include a collapse/expand button. Subtle border on left side. Width: 300px when expanded."

### 5. Breadcrumbs
**Prompt**: "Create a breadcrumb navigation showing page hierarchy with chevron separators. Each item clickable, with hover underline. Last item should be slightly bolder. Include home icon at start. Truncate long paths with ellipsis in middle."

### 6. MobileSidebar
**Prompt**: "Design a mobile drawer sidebar that slides from left, with overlay backdrop. Include gesture support for swipe to close. Show folder tree, recent pages, and favorites. Bottom section with settings and user profile. Smooth animation with spring physics."

### 7. BottomNavigation (Mobile)
**Prompt**: "Create a mobile bottom navigation with 5 tabs: Home, Search, New Note (center, elevated FAB style), Notifications, Profile. Active tab highlighted with accent color. Icon + label for each. Safe area padding for iPhone."

### 8. QuickAccessMenu
**Prompt**: "Design a floating quick access menu that appears on right edge of screen when hovering. Show icons for: Create Note, Daily Note, Search, Recent, Favorites. Each icon with tooltip on hover. Vertical pill shape with shadow."

### 9. PageHeader
**Prompt**: "Create a page header showing: page icon (emoji/image), editable title (large, bold), description (smaller, gray), and action buttons (share, star, more options). Breadcrumbs above. Clean spacing with subtle bottom border."

### 10. Workspace Switcher
**Prompt**: "Design a dropdown menu showing all user workspaces with icons, names, and member count. Active workspace checked. Include 'Create Workspace' and 'Settings' options at bottom. Searchable list if many workspaces. Smooth dropdown animation."

---

## ✍️ Editor Components (18 components)

### 11. RichTextEditor
**Prompt**: "Design a distraction-free rich text editor with a floating toolbar that appears on text selection. Include markdown shortcuts, slash commands menu (type / to open), and inline code highlighting. Style should be clean with generous line-height and readable typography. Support for headings, lists, checkboxes, code blocks, and callouts/info boxes."

### 12. SlashCommandMenu
**Prompt**: "Create a popup menu that appears when typing '/'. Show categorized options: Text (heading, paragraph, list), Media (image, video, file), Advanced (table, database, code). Each item with icon and description. Keyboard navigable with arrow keys. Fuzzy search filtering."

### 13. InlineToolbar
**Prompt**: "Design a floating toolbar that appears above selected text. Include buttons: Bold, Italic, Underline, Strikethrough, Code, Link, Highlight. Plus a color picker for text color. Tooltip on hover. Smooth fade-in animation. Arrow pointing down to selection."

### 14. BlockMenu
**Prompt**: "Create a side menu (6-dot handle) that appears on hover of any block. Shows: Drag handle, Add block above/below, Delete, Duplicate, Turn into (convert block type), Comment. Vertical layout with icons. Appears on left edge of block."

### 15. LinkPreview
**Prompt**: "Design a hover card that appears when hovering over a link. Shows: page title, snippet of content (2-3 lines), last modified date, and a 'Open in new tab' icon. Card should have shadow, rounded corners, and smooth fade-in. Max width: 400px."

### 16. MentionMenu
**Prompt**: "Create an autocomplete menu for @mentions. Shows user avatars, names, and status (online/offline). Highlight matching text. Include 'Invite' option if user not found. Keyboard navigable. Max 8 results visible with scroll."

### 17. EmojiPicker
**Prompt**: "Design an emoji picker popup with categories (smileys, people, nature, food, etc.), search bar at top, and recently used section. Grid layout showing emojis. Hover to see emoji name. Click to insert. Skin tone selector for applicable emojis."

### 18. IconPicker
**Prompt**: "Create an icon selection modal with tabs for: Emoji, Lucide Icons, Upload Image. Search bar filters icons. Grid layout with hover preview. Selected icon highlighted. Upload section with drag-drop area. Preview selected icon at top."

### 19. ImageUpload
**Prompt**: "Design an image upload component with drag-drop zone. Show upload progress bar when uploading. After upload: image preview with caption input below, alignment options (left, center, right, full-width), and resize handles. Delete/replace buttons on hover."

### 20. FileAttachment
**Prompt**: "Create a file attachment card showing: file icon (by type), filename, size, and download button. Include preview for PDFs. Progress bar during upload. Option to embed (for videos/audio) or download. Compact horizontal layout."

### 21. CodeBlock
**Prompt**: "Design a code block with syntax highlighting, language selector dropdown (top-right), line numbers (optional toggle), copy button (appears on hover), and theme matching editor. Support common languages. Rounded corners with subtle background."

### 22. TableBlock
**Prompt**: "Create an editable table with: add/delete row/column buttons, drag to reorder rows/columns, header row styling, cell formatting options (align, bold), and resize columns by dragging borders. Minimal style with borders. Hover row highlights."

### 23. CalloutBlock
**Prompt**: "Design a callout/alert block with icon on left (info, warning, success, error icons), colored left border matching type, editable title and content, and background tint. Collapsible option with arrow. Rounded corners and padding."

### 24. ToggleBlock
**Prompt**: "Create a collapsible toggle block with arrow icon that rotates when expanded/collapsed. Title always visible (editable), content inside collapsible section. Smooth height animation. Nested toggles supported. Subtle background on hover."

### 25. CheckboxList
**Prompt**: "Design an interactive checkbox list where items can be checked/unchecked, indented with Tab, reordered via drag-drop. Checked items shown with strikethrough and reduced opacity. Progress indicator showing percentage complete."

### 26. QuoteBlock
**Prompt**: "Create a quote block with large left border (accent color), italic text, larger font size, and optional author attribution below (smaller, right-aligned). Background slightly tinted. Icon quote mark in top-left corner."

### 27. DividerBlock
**Prompt**: "Design divider options: solid line, dashed line, dotted line, or decorative (with icon in center). Adjustable thickness and color. Margin above/below. Simple and clean."

### 28. BreadcrumbInsideEditor
**Prompt**: "Create subtle breadcrumbs shown at top of editor (above title) when inside nested pages. Small, gray text with chevrons. Clickable to navigate up hierarchy. Fades in on scroll. Non-intrusive design."

---

## 🗂️ Organization & Navigation (12 components)

### 29. FolderTree
**Prompt**: "Design a hierarchical folder tree with expand/collapse arrows, folder/page icons, drag-and-drop reordering (visual feedback with drop zones), context menu on right-click, and indent lines showing hierarchy. Smooth expand/collapse animations."

### 30. SearchModal
**Prompt**: "Create a full-screen search modal (Cmd+K) with large search input, recent searches below, categorized results (pages, databases, people), keyboard shortcuts shown on right, and live preview on arrow navigation. Blur backdrop and smooth transitions."

### 31. SearchResults
**Prompt**: "Design search results list showing: page icon, title, matching snippet with highlighted search terms, breadcrumb path, and last modified date. Click to open, Cmd+Click for new tab. Alternating row backgrounds on hover."

### 32. TagManager
**Prompt**: "Create a tag input field with autocomplete dropdown. Existing tags shown as colored pills (removable with X). Create new tag by typing and pressing Enter. Color picker for each tag. Tags grouped and sorted alphabetically."

### 33. FavoritesPanel
**Prompt**: "Design a favorites section showing starred pages as cards with icon, title, and quick preview. Drag to reorder. Unstar by clicking filled star icon. Grid or list view toggle. Empty state with illustration and 'Star pages to see them here' message."

### 34. RecentPages
**Prompt**: "Create a recent pages list showing last 10-20 visited pages with icon, title, last viewed timestamp (e.g., '2 hours ago'), and quick actions (open, remove from recent). List view with dividers. Clear all button at bottom."

### 35. TrashBin
**Prompt**: "Design a trash view showing deleted items with icon, title, deleted date, and actions (restore, permanent delete). Search and filter by date. 'Empty Trash' button with confirmation dialog. Warning badge showing number of items."

### 36. PageOutline
**Prompt**: "Create a table of contents sidebar showing heading hierarchy from current page. Clickable to jump to section. Highlight current section on scroll. Indent levels match heading levels. Smooth scroll animation when clicked."

### 37. ViewSwitcher
**Prompt**: "Design a view toggle for databases: buttons for Table, Board (Kanban), Gallery, Calendar, and List views. Icon + label for each. Active view highlighted. Compact button group with rounded edges."

### 38. FilterPanel
**Prompt**: "Create a filter builder showing active filters as chips (removable), 'Add Filter' button opening dropdown with properties, operators (is, contains, before/after), and value inputs. Support AND/OR logic. Save filter as view option."

### 39. SortPanel
**Prompt**: "Design a sort options panel showing: property to sort by (dropdown), ascending/descending toggle, and 'Add Sort' for multiple sort levels. Drag to reorder sort priority. Clear all button."

### 40. GroupingPanel
**Prompt**: "Create grouping controls: select property to group by, show/hide empty groups toggle, and collapsed/expanded state for each group. Visual separators between groups with count badges."

---

## 💾 Database Components (14 components)

### 41. DatabaseView
**Prompt**: "Create a Notion-style database view with multiple viewing options: table, board (Kanban), gallery, and calendar. Include inline editing, drag-and-drop reordering, customizable columns with different property types (text, number, date, select, multi-select). Add filtering, sorting, and grouping controls in a toolbar above the view."

### 42. TableView
**Prompt**: "Design a spreadsheet-like table view with: resizable columns (drag border), sortable headers (click to sort), inline cell editing, row selection (checkbox column), add row at bottom, and horizontal/vertical scroll. Fixed header on scroll. Zebra striping optional."

### 43. BoardView (Kanban)
**Prompt**: "Create a Kanban board with columns representing status/stages. Cards drag-droppable between columns. Each column shows count and add card button. Cards show properties as badges. Horizontal scroll for many columns. Column reordering and renaming."

### 44. GalleryView
**Prompt**: "Design a gallery view showing cards in a responsive grid. Each card: cover image (if any), title, properties below. Hover shows quick preview. Click to open full page. Adjust card size with slider. Masonry layout option."

### 45. CalendarView
**Prompt**: "Create a calendar view (month/week/day views) showing events from date property. Drag to move events. Click date to create. Color-code by category. Today highlighted. Mini calendar on sidebar for quick navigation."

### 46. ListView
**Prompt**: "Design a compact list view showing items as rows with small icon, title, and key properties inline (not full table). Checkbox for bulk actions. Group by sections. Quick add at top. Mobile-friendly compact design."

### 47. DatabaseCard
**Prompt**: "Create a database item card showing: icon/cover image, title (editable inline), properties as key-value pairs with inline editing, and action buttons (open, duplicate, delete). Hover shows shadow. Click anywhere to open full page."

### 48. PropertyEditor
**Prompt**: "Design a property editor modal for database columns. Tabs for each property type: Text, Number, Select, Multi-select, Date, Person, File, URL, Email, Phone, Checkbox, Formula, Relation, Rollup. Each with specific configuration options and preview."

### 49. SelectPropertyEditor
**Prompt**: "Create a select property editor showing: existing options as colored pills, add new option input, color picker per option, delete option button, and drag to reorder options. Default value selector."

### 50. DatePropertyPicker
**Prompt**: "Design a date picker with calendar view, time input (optional), date range toggle, reminder settings, and presets (Today, Tomorrow, Next Week, etc.). Include end date for ranges. Clear button."

### 51. FormulaEditor
**Prompt**: "Create a formula editor with: syntax-highlighted input, function autocomplete, property reference picker, example formulas library, and live preview of result. Support math, text, date, and logical functions."

### 52. RelationPicker
**Prompt**: "Design a relation picker showing: search to find related items, existing relations as chips (removable), create new related item option, and preview of related page on hover. Support multiple relations."

### 53. RollupEditor
**Prompt**: "Create a rollup configuration: select relation property, choose property from related items, and aggregation function (count, sum, average, min, max, etc.). Show preview of result with sample data."

### 54. DatabaseTemplate
**Prompt**: "Design a database template selector showing: template thumbnails (task list, CRM, project tracker, etc.), template preview on click, and 'Use Template' button. Search/filter by category. Create blank database option."

---

## 👥 Collaboration Components (12 components)

### 55. CollaborationPanel
**Prompt**: "Create a collaboration interface showing active users with avatars, real-time cursors with name labels, comment threads in margin, and version history timeline. Include share button with permission settings (view/edit/comment). Style: subtle, non-intrusive, with smooth presence indicators."

### 56. UserPresence
**Prompt**: "Design an active users indicator showing avatars of online collaborators (stacked with overflow count). Click to see full list with names, current page they're viewing, and online status. Pulse animation for avatars."

### 57. RealtimeCursor
**Prompt**: "Create a cursor indicator for other users showing: colored cursor matching user's assigned color, name label above cursor, and smooth position interpolation. Fade out after 3 seconds of inactivity."

### 58. CommentThread
**Prompt**: "Design a comment thread showing: all comments in chronological order, author avatar and name, timestamp, edit/delete options, resolve button (marks thread as resolved), and reply input. Nested replies indented. Highlight unread comments."

### 59. CommentInput
**Prompt**: "Create a comment input box with: rich text support, @mention autocomplete, emoji picker, file attachment, and post/cancel buttons. Show character count. Preview mode toggle. Minimize to icon when not focused."

### 60. ShareDialog
**Prompt**: "Design a share modal with: link sharing toggle (generate shareable link), permission dropdown (view/comment/edit), expiry date option, password protection, invite by email input with role selector, list of current members with permission controls, and revoke access button."

### 61. PermissionBadge
**Prompt**: "Create permission indicator badges showing user role: Owner (gold), Editor (blue), Commenter (green), Viewer (gray). Small badge with icon and label. Shown next to user names in sharing dialog and member lists."

### 62. NotificationCenter
**Prompt**: "Design a notification dropdown showing: unread count badge, categorized notifications (mentions, comments, shares, updates), mark as read buttons, notification settings link, and clear all option. Each notification clickable to jump to relevant page."

### 63. ActivityFeed
**Prompt**: "Create an activity feed showing recent actions in workspace: page created/edited/deleted, comments added, members joined, etc. Show actor avatar, action description, timestamp, and affected page link. Grouped by date. Filter by activity type."

### 64. MentionNotification
**Prompt**: "Design a notification card for @mentions showing: who mentioned you, snippet of context, page link, and timestamp. Mark as read/unread toggle. Click to navigate to exact mention location with highlight."

### 65. VersionHistory
**Prompt**: "Create a version history panel showing: timeline of changes (newest first), author and timestamp for each version, visual diff preview, restore button, and compare mode to see changes between versions. Slider to scrub through history."

### 66. ChangesDiff
**Prompt**: "Design a diff viewer showing changes between versions: additions in green background, deletions in red with strikethrough, and unchanged text in normal style. Side-by-side or inline view toggle. Line numbers optional."

---

## 📊 Graph & Visualization (8 components)

### 67. GraphVisualization
**Prompt**: "Design an interactive graph visualization showing notes as nodes connected by links. Nodes should be sized by importance/connections, with different colors for note types. Include zoom controls, search/filter panel, and ability to click nodes to open notes. Use force-directed layout with smooth animations. Dark mode friendly."

### 68. GraphControls
**Prompt**: "Create a control panel for graph view: zoom in/out/reset buttons, layout algorithm selector (force-directed, hierarchical, radial), filter by tag/type, depth slider (show connections N levels deep), and settings gear icon for advanced options."

### 69. NodeTooltip
**Prompt**: "Design a tooltip appearing on node hover showing: page title, preview snippet (50 chars), connection count (incoming/outgoing), tags, and last modified date. Arrow pointing to node. Quick action buttons (open, pin)."

### 70. GraphFilter
**Prompt**: "Create a filter sidebar for graph showing: tag checkboxes (show/hide by tag), node type filters (page, database, person), orphan toggle (show isolated nodes), and date range slider. Apply/reset buttons."

### 71. GraphMinimap
**Prompt**: "Design a minimap overlay showing full graph in corner with viewport indicator (draggable rectangle). Click to jump to area. Toggle show/hide. Fade on idle. Useful for large graphs."

### 72. BacklinksPanel
**Prompt**: "Create a backlinks section listing all pages linking to current page. Show: page icon, title, snippet showing link context (sentence with highlight), and click to navigate. Count badge at top. 'No backlinks yet' empty state."

### 73. OutgoingLinks
**Prompt**: "Design a panel showing all links from current page to other pages. List format with icon, title, link preview on hover. Quick action to open in new tab. Count total links."

### 74. LinkSuggestions
**Prompt**: "Create an AI-powered link suggestions card showing: 'Suggested links based on content' header, list of relevant pages with match score, and quick add link button. Dismissable suggestions. Refresh to get new suggestions."

---

## 🎨 Canvas & Whiteboard (10 components)

### 75. CanvasWorkspace
**Prompt**: "Design an infinite canvas workspace with: pan (drag background) and zoom (pinch/scroll), grid background (toggleable), toolbar floating on top, and minimap in corner. Objects can be placed anywhere. Snap-to-grid option."

### 76. CanvasToolbar
**Prompt**: "Create a toolbar for canvas showing: selection tool, pen tool, shapes (rectangle, circle, arrow), text tool, sticky note, and connector line. Icon buttons with active state. Undo/redo buttons. View controls (zoom, fit to screen)."

### 77. StickyNote
**Prompt**: "Design a draggable sticky note component with: colored background (yellow, pink, blue, green options), resizable dimensions, rich text content, author avatar in corner, and delete button on hover. Shadow for depth."

### 78. CanvasTextBox
**Prompt**: "Create a text box for canvas: transparent or colored background, resizable and draggable, rich text formatting, auto-expand height as typing, and alignment options. Border on select."

### 79. ShapeTool
**Prompt**: "Design shape drawing tool creating: rectangles, circles, triangles, and custom polygons. Adjustable fill color, border color/thickness, corner radius (for rectangles), and opacity. Resize handles when selected."

### 80. ConnectorLine
**Prompt**: "Create smart connector lines between objects: straight, curved, or elbow style. Automatically attach to object edges. Arrowheads optional. Adjust line color and thickness. Re-route when objects moved."

### 81. CanvasImage
**Prompt**: "Design an image component for canvas: drag-drop to place, resize with corner handles maintaining aspect ratio, crop tool, opacity slider, and border/shadow options. Click to open full size."

### 82. CanvasEmbed
**Prompt**: "Create an embed component for canvas showing: webpage/video/tweet preview, resizable frame, refresh button, and open in new tab button. Loading state with skeleton. Error state if embed fails."

### 83. CanvasContextMenu
**Prompt**: "Design a right-click context menu for canvas objects showing: Cut, Copy, Paste, Duplicate, Delete, Bring to Front/Back, Group/Ungroup, Lock position, and Properties. Keyboard shortcuts shown. Dividers between sections."

### 84. CanvasLayersPanel
**Prompt**: "Create a layers panel showing all canvas objects in list: thumbnail, name, visibility toggle, lock toggle, and drag to reorder. Grouped objects shown as collapsible. Select multiple with Shift+Click."

---

## ⚙️ Settings & Configuration (10 components)

### 85. SettingsModal
**Prompt**: "Design a comprehensive settings panel with tabbed navigation (general, appearance, shortcuts, plugins, account). Each section has clean form layouts with toggles, dropdowns, and input fields. Include search within settings. Preview changes in real-time where applicable. Modern, organized layout."

### 86. AppearanceSettings
**Prompt**: "Create appearance settings showing: theme selector (light/dark/auto), accent color picker, font family dropdown, font size slider, line height adjuster, and preview pane showing changes live. Custom theme builder option."

### 87. ShortcutsSettings
**Prompt**: "Design keyboard shortcuts settings listing all shortcuts in categories (navigation, editing, formatting, etc.). Search to find shortcuts. Click to rebind. Show conflicts. Reset to default button. Printable cheat sheet export."

### 88. PluginManager
**Prompt**: "Create a plugin marketplace showing: installed plugins, available plugins (cards with icon, name, description, rating), search/filter, install/uninstall buttons, plugin settings, and enable/disable toggles. Update available indicators."

### 89. AccountSettings
**Prompt**: "Design account settings with: profile picture upload, name/email fields, password change section, connected accounts (Google, Apple), two-factor authentication setup, and danger zone (delete account). Save changes button."

### 90. WorkspaceSettings
**Prompt**: "Create workspace settings showing: workspace name/icon, member management table (name, email, role, actions), invite members form, billing information, usage statistics (storage, member count), and export workspace data option."

### 91. NotificationSettings
**Prompt**: "Design notification preferences with: email notifications toggles (mentions, comments, updates, digests), push notification settings, quiet hours scheduler, and per-page notification overrides. Test notification button."

### 92. IntegrationSettings
**Prompt**: "Create integrations panel showing: connected services (Slack, Google Drive, etc.) with status indicators, available integrations to add, API keys section, webhooks configuration, and logs of recent integration activity."

### 93. ImportExport
**Prompt**: "Design import/export interface with: file upload for imports (Notion, Markdown, HTML), export format selector (Markdown, PDF, HTML, JSON), export scope (workspace, pages, databases), and progress indicator during operations."

### 94. BillingSettings
**Prompt**: "Create billing dashboard showing: current plan with features list, usage meters (storage, AI requests, etc.), payment method cards, billing history table, upgrade/downgrade buttons, and cancel subscription option with retention flow."

---

## 🔐 Authentication & Onboarding (10 components)

### 95. LoginForm
**Prompt**: "Design a clean login form with: email input, password input with show/hide toggle, remember me checkbox, forgot password link, login button, divider with 'OR', and social login buttons (Google, Apple, GitHub). Error states with inline validation."

### 96. SignupForm
**Prompt**: "Create signup form with: name input, email input, password input with strength meter, agree to terms checkbox, signup button, and social signup options. Show password requirements. Link to login if already have account."

### 97. ForgotPassword
**Prompt**: "Design forgot password flow: email input, send reset link button, success message with email confirmation, and back to login link. Include timer before allowing resend (60 seconds)."

### 98. EmailVerification
**Prompt**: "Create email verification screen showing: success icon, verification message, email address shown, resend verification email button (with countdown), and continue to app button. Handle expired tokens."

### 99. OnboardingWizard
**Prompt**: "Design multi-step onboarding with: progress indicator (steps 1/5), workspace name setup, invite teammates (skippable), choose templates or start blank, brief tutorial (interactive tour), and finish button. Previous/next navigation."

### 100. WelcomeScreen
**Prompt**: "Create welcome screen after signup showing: personalized greeting, quick start guide (3-4 key features), video tutorial embed, template gallery, and 'Start from scratch' option. Dismissable tooltip pointers."

### 101. TourTooltip
**Prompt**: "Design interactive tour tooltips with: arrow pointing to UI element, title, description, step counter (1/10), next/skip buttons, and optional screenshot/GIF. Spotlight effect darkening rest of UI."

### 102. HelpCenter
**Prompt**: "Create help center modal with: search bar, categorized articles (Getting Started, Features, Troubleshooting), video tutorials section, keyboard shortcuts cheat sheet, and contact support button. Feedback thumbs up/down on articles."

### 103. KeyboardShortcuts
**Prompt**: "Design keyboard shortcuts reference modal showing: shortcuts grouped by category (navigation, formatting, etc.), search to filter, OS-specific display (Mac/Windows), and printable PDF export button. Two-column layout."

### 104. WhatsNewModal
**Prompt**: "Create 'What's New' modal shown on updates: release notes with new features highlighted, images/GIFs of new features, version number, changelog link, and dismiss/remind later buttons. Shown once per version."

---

## 🎭 States & Feedback (12 components)

### 105. LoadingSpinner
**Prompt**: "Design a loading spinner with smooth animation. Show in center of loading area. Optional overlay for full-page loading. Include loading text below ('Loading...', 'Syncing...', etc.). Brand colors."

### 106. SkeletonScreen
**Prompt**: "Create skeleton loading states mimicking actual content layout: gray animated shimmer effect, matching shapes for text lines, images, cards, etc. More elegant than spinners for content-heavy pages."

### 107. EmptyState
**Prompt**: "Design empty state components for different contexts: no notes ('Create your first note'), no search results ('Try different keywords'), no connections ('Link pages to see graph'), etc. Illustration + message + CTA button."

### 108. ErrorState
**Prompt**: "Create error display with: error icon (red), error title, friendly error message (non-technical), error code/ID (for support), retry button, and go back button. Optional details toggle for technical info."

### 109. SuccessToast
**Prompt**: "Design success notification toast appearing in top-right: green checkmark icon, success message ('Page published', 'Saved'), auto-dismiss after 3 seconds, manual close button. Stack multiple toasts."

### 110. ErrorToast
**Prompt**: "Create error toast notification: red X icon, error message, action button (retry, undo), and close button. Stays visible until dismissed. Shake animation on appear."

### 111. ConfirmDialog
**Prompt**: "Design confirmation modal for destructive actions: warning icon, question message ('Delete this page?'), secondary text explaining consequences, cancel button (gray), and confirm button (red for delete). Escape to cancel."

### 112. ProgressBar
**Prompt**: "Create progress indicator for uploads/exports: thin bar showing percentage, estimated time remaining, cancel button, and completed file count (5/10). Animated fill from left to right."

### 113. OfflineIndicator
**Prompt**: "Design offline mode banner appearing at top: orange background, offline icon, 'You're offline. Changes will sync when reconnected' message, and dismiss button. Sticky position."

### 114. SyncStatusIndicator
**Prompt**: "Create sync status in top bar: syncing spinner with 'Syncing...', green checkmark with 'All changes saved', or red X with 'Sync failed' and retry button. Subtle animations."

### 115. UndoRedoBanner
**Prompt**: "Design an undo banner appearing briefly after destructive actions: 'Page deleted' message, undo button (prominent), and auto-dismiss countdown. Slides in from bottom. Click anywhere to dismiss."

### 116. ValidationFeedback
**Prompt**: "Create inline validation feedback for forms: red text for errors below fields, green checkmark for valid fields, yellow warning for suggestions, and real-time validation as user types. Icon + message."

---

## 📱 Mobile-Specific Components (10 components)

### 117. MobileEditor
**Prompt**: "Design a mobile-optimized editor with: large tap targets, simplified toolbar (essential actions only), swipe gestures (swipe left on line for more options), bottom toolbar (above keyboard), and auto-save indicator."

### 118. SwipeActions
**Prompt**: "Create swipe actions for list items: swipe right to reveal star/archive, swipe left for delete/more. Color-coded backgrounds. Haptic feedback. Threshold to trigger action. Reveal icons smoothly."

### 119. PullToRefresh
**Prompt**: "Design pull-to-refresh interaction: pull down on scroll view, show loading spinner with release message, refresh animation, and snap back after loading. Custom illustration during pull."

### 120. MobileSearchBar
**Prompt**: "Create mobile search with: large search input, voice input button, recent searches below (swipe to delete), search filters button, and cancel button. Full-screen focus mode. Keyboard auto-opens."

### 121. ActionSheet
**Prompt**: "Design iOS-style action sheet sliding from bottom: list of actions with icons, destructive action in red at bottom, cancel button below divider, and tap outside to dismiss. Blur backdrop."

### 122. FloatingActionButton
**Prompt**: "Create FAB (Floating Action Button) in bottom-right: circular button with + icon, opens speed dial menu on press (mini FABs for New Note, Daily Note, Voice Note), smooth animations, and shadow."

### 123. MobileNavDrawer
**Prompt**: "Design a navigation drawer for mobile: swipe from left edge to open, show user profile at top, navigation items with icons, dividers between sections, settings at bottom, and overlay dimming background."

### 124. MobileTabBar
**Prompt**: "Create bottom tab bar with: 4-5 tabs (icons + labels), center tab elevated as FAB style, active tab highlighted with accent color, badge indicators for notifications, and safe area insets for notched phones."

### 125. GestureHints
**Prompt**: "Design subtle gesture hint overlays for first-time users: swipe icon with animation, tap target pulse, and dismissable tips ('Swipe left to delete'). Appear once, then remember dismissed state."

### 126. MobileKeyboardToolbar
**Prompt**: "Create custom keyboard toolbar appearing above system keyboard: formatting shortcuts (bold, italic, link), done button, markdown shortcuts, and @mention trigger. Sticky above keyboard."

---

## 🔍 Search & Discovery (8 components)

### 127. GlobalSearch
**Prompt**: "Design universal search (Cmd+K) showing: instant results as typing, categorized sections (pages, people, commands), keyboard navigation hints (↑↓ to navigate, Enter to select), recent searches, and 'Search in all workspaces' toggle."

### 128. SearchHighlight
**Prompt**: "Create search result highlighting: matched terms in yellow background, case-insensitive matching, multiple matches highlighted, scroll to first match on open, and next/previous match navigation buttons."

### 129. FilterBuilder
**Prompt**: "Design advanced filter builder: drag-and-drop filter conditions, property selector, operator dropdown (equals, contains, greater than, etc.), value input (adapts to property type), AND/OR logic toggle between conditions, and save filter preset option."

### 130. SavedSearches
**Prompt**: "Create saved searches panel: list of saved filters with names, edit/delete actions, pin favorites to sidebar, share with team option, and duplicate to create variations. Quick apply button."

### 131. SearchSuggestions
**Prompt**: "Design search autocomplete dropdown: suggested queries based on history, popular searches in workspace, related tags, and recent pages. Keyboard navigable. Show icons for suggestion types."

### 132. AdvancedSearchModal
**Prompt**: "Create advanced search interface: multiple filter rows (add/remove), date range picker, author filter, tag filter, location filter (which workspace/folder), content type filter, and sort options. Export results option."

### 133. QuickFind
**Prompt**: "Design in-page search (Cmd+F): compact search bar at top, match counter (3 of 15), previous/next buttons, match case toggle, whole word toggle, and close button. Highlights scroll into view."

### 134. SearchResultPreview
**Prompt**: "Create search result preview cards: page icon, title, matching snippet (3 lines with highlights), breadcrumb path, last modified date, quick actions (open, open in new tab, star), and hover to preview full content."

---

## 🎯 Templates & Quickstart (8 components)

### 135. TemplateGallery
**Prompt**: "Design a template selection modal with grid layout showing template previews. Categories on left sidebar (personal, work, planning, etc.). Each template card shows preview image, title, description, and 'Use Template' button. Include search and filter options. Modern, colorful design with hover effects."

### 136. TemplatePreview
**Prompt**: "Create template preview modal: full-page preview of template structure, thumbnail images of sections, description of use case, tags/categories, author info, use count, and 'Use Template' CTA. Scrollable preview."

### 137. TemplateEditor
**Prompt**: "Design template creation interface: edit mode showing template structure, variable placeholders ({{name}}, {{date}}), conditional sections toggle, preview mode, save as template button, and publish to gallery option."

### 138. QuickstartWizard
**Prompt**: "Create project quickstart wizard: step-by-step form (What type of project?, Who's on the team?, Timeline?), progress indicator, pre-fills template based on answers, skip to customize later option, and finish button."

### 139. TemplateCategoryBrowser
**Prompt**: "Design category browser for templates: grid of category cards with icons and counts, trending templates section, recently added, most used, and search bar. Filter by: personal, team, public."

### 140. DailyNoteTemplate
**Prompt**: "Create daily note template UI: automatic date insertion, sections for tasks/notes/journal, previous/next day navigation, streak indicator (consecutive days), and customization options for structure."

### 141. MeetingNoteTemplate
**Prompt**: "Design meeting note template: meeting title, date/time fields, attendees selector (from team), agenda items (checkboxes), notes section, action items with assignees, and recording/attachment section."

### 142. ProjectTemplate
**Prompt**: "Create project template structure: project overview section, goals and metrics, team members, timeline/milestones, tasks database (embedded), resources, and status updates. Customizable sections."

---

## 🔗 Integrations & Extensions (10 components)

### 143. WebClipper
**Prompt**: "Design browser extension popup: clip full page/selection/screenshot options, save to location picker (workspace/folder), tag input, note field for context, preview of clipped content, and save button. Minimal, fast interface."

### 144. SlackIntegration
**Prompt**: "Create Slack integration panel: connect workspace button, channel selector for notifications, slash command setup (/note), message actions (save to NoteCraft), preview unfurled links, and disconnect option."

### 145. GoogleDriveSync
**Prompt**: "Design Google Drive integration: folder mapping (Drive folder ↔ NoteCraft folder), two-way sync toggle, conflict resolution options, sync status indicator, manual sync button, and view in Drive link."

### 146. CalendarIntegration
**Prompt**: "Create calendar sync interface: connect Google/Outlook calendar, event sync to database, create events from NoteCraft, meeting notes auto-link to events, and calendar view in app showing synced events."

### 147. APIKeyManager
**Prompt**: "Design API key management: generate new key button, key list (name, created date, last used, permissions), revoke key action, usage statistics per key, and API documentation link."

### 148. WebhookConfigurator
**Prompt**: "Create webhook setup interface: webhook URL input, trigger events checkboxes (page created, updated, deleted, etc.), custom headers, test webhook button with example payload, and logs of recent webhook calls."

### 149. ZapierIntegration
**Prompt**: "Design Zapier integration card: 'Connect with 1000+ apps' message, popular Zap templates (Save Gmail to NoteCraft, Create task from Slack, etc.), setup guide link, and connected Zaps list."

### 150. BrowserExtensionSettings
**Prompt**: "Create extension settings: quick capture hotkey customizer, default save location, auto-tag rules, clip format options (markdown, HTML), exclude domains list, and permissions requested explanation."

### 151. MobileShareSheet
**Prompt**: "Design iOS/Android share extension: appears in system share sheet, quick save with smart categorization, add tags, select destination, preview of saved content, and success confirmation."

### 152. EmbedCodeGenerator
**Prompt**: "Create embed code generator for public pages: iframe embed code with size options, responsive toggle, theme selector (match parent, light, dark), copy code button, and live preview of embed."

---

## 📊 Analytics & Insights (8 components)

### 153. AnalyticsDashboard
**Prompt**: "Design analytics overview showing: page views chart (last 30 days), most viewed pages list, active users graph, storage usage meter, AI usage stats, and export report button. Clean, data-viz focused design."

### 154. PageAnalytics
**Prompt**: "Create page-level analytics: view count, unique visitors, average time on page, referrers, device breakdown (desktop/mobile), and views over time chart. Embedded in page properties panel."

### 155. WorkspaceInsights
**Prompt**: "Design workspace insights dashboard: total pages created graph, active contributors chart, most linked pages, orphaned pages count, largest pages by size, and workspace health score."

### 156. SearchAnalytics
**Prompt**: "Create search analytics: most searched terms, searches with no results (to identify content gaps), average search time, and search trends over time. Filter by date range."

### 157. UsageMetrics
**Prompt**: "Design usage dashboard: storage used (progress bar with limit), AI requests remaining this month, team member activity, export count, and upgrade plan CTA if approaching limits."

### 158. HeatmapView
**Prompt**: "Create content heatmap: visual representation of page activity (color intensity = activity level), hover for details, filter by time period, and identify hot/cold areas of workspace."

### 159. ExportAnalytics
**Prompt**: "Design analytics export interface: select date range, choose metrics to include, format selector (CSV, Excel, PDF), schedule recurring reports, and email delivery option."

### 160. AIUsageTracker
**Prompt**: "Create AI usage dashboard: requests by type (summarize, expand, translate), tokens used graph, cost breakdown, most used features, and remaining quota meter."

---

## 🎨 Customization & Theming (8 components)

### 161. ThemeBuilder
**Prompt**: "Design custom theme builder: color picker for primary, secondary, background, text colors, font family selector, spacing scale adjuster, border radius slider, and live preview pane. Save/export custom theme."

### 162. ColorPicker
**Prompt**: "Create advanced color picker: color wheel, RGB/HEX input, opacity slider, recent colors, saved palette, and preset color swatches. Eyedropper tool to pick from screen."

### 163. FontSettings
**Prompt**: "Design typography settings: font family dropdown (system, serif, mono), font size slider (14-24px), line height adjuster, letter spacing, and preview text showing all heading levels and body text."

### 164. CustomCSS
**Prompt**: "Create custom CSS editor for power users: syntax-highlighted code editor, apply to workspace/page toggle, reset to default button, CSS snippets library, and warning about breaking changes."

### 165. IconCustomizer
**Prompt**: "Design icon customization: upload custom icons, icon library browser (lucide, heroicons, etc.), color tint option, size selector, and apply to page/database. Preview before applying."

### 166. CoverImagePicker
**Prompt**: "Create cover image selector: upload custom image, unsplash integration (search free photos), gradient generator, solid color picker, position/zoom adjuster, and remove cover option."

### 167. ThemeMarketplace
**Prompt**: "Design theme marketplace: grid of theme cards (screenshot preview), author, install count, rating, install button, and filter by style (minimal, vibrant, professional). Preview before install."

### 168. CustomDomain
**Prompt**: "Create custom domain setup: domain input field, DNS verification instructions, SSL certificate status, CNAME record details, verify button, and troubleshooting guide link."

---

## 🛠️ Admin & Moderation (10 components)

### 169. AdminDashboard
**Prompt**: "Design admin control panel: workspace overview stats, member management, content moderation queue, audit logs, billing overview, and system health indicators. Tabs for each section."

### 170. MemberManagement
**Prompt**: "Create member management table: columns for name, email, role, last active, actions (edit role, remove, suspend). Bulk actions, export member list, invite members button, and filter by role."

### 171. AuditLog
**Prompt**: "Design audit log viewer: chronological list of all actions (created, edited, deleted, shared), actor, timestamp, affected resource, filters by action type/user/date, and export audit trail."

### 172. ContentModeration
**Prompt**: "Create moderation queue: flagged content cards, reason for flag, reporter info, preview of content, actions (approve, remove, warn user), and bulk moderation options."

### 173. PermissionMatrix
**Prompt**: "Design permission matrix showing: roles in rows (owner, admin, editor, viewer), features in columns, checkmarks for allowed features, edit button to customize permissions, and save changes."

### 174. UsageQuotas
**Prompt**: "Create quota management: set limits for storage, AI requests, team members per workspace, adjust quotas by plan, usage alerts setup, and view current usage vs. limits."

### 175. BackupRestore
**Prompt**: "Design backup management: scheduled backup toggle, backup frequency selector, list of available backups with dates/sizes, restore button with confirmation, download backup, and retention policy settings."

### 176. SystemNotifications
**Prompt**: "Create admin notification center: broadcast message composer, target audience selector (all users, specific workspace, trial users), schedule send, notification history, and templates."

### 177. FeatureFlags
**Prompt**: "Design feature flag management: list of features with toggle switches, rollout percentage slider (gradual rollout), target by user segment, A/B test setup, and usage metrics per feature."

### 178. ErrorLogViewer
**Prompt**: "Create error log dashboard: error list with frequency, stack traces (expandable), affected users count, status (resolved, investigating), assign to developer, and filter by severity."

---

## 🎬 Onboarding & Tours (6 components)

### 179. InteractiveTour
**Prompt**: "Design interactive product tour: spotlight on feature with dimmed background, explanation tooltip with arrow, next/skip buttons, step progress (3/8), GIF/video demo option, and 'Try it yourself' interactive step."

### 180. FeatureSpotlight
**Prompt**: "Create feature announcement modal: hero image/video, feature name and description, benefits list with icons, 'Try Now' button launching feature, dismiss button, and 'Don't show again' checkbox."

### 181. ProgressChecklist
**Prompt**: "Design onboarding checklist: list of setup tasks (Create first page, Invite teammate, Install mobile app), progress bar, checkmarks for completed, dismiss option, and celebration animation when complete."

### 182. TooltipTrigger
**Prompt**: "Create contextual help tooltips: question mark icon next to UI elements, hover to show tooltip with explanation, 'Learn more' link to docs, keyboard shortcut if applicable, and persistent for new users."

### 183. VideoTutorial
**Prompt**: "Design video tutorial player: embedded video with chapters/timeline, speed control, captions toggle, fullscreen button, related tutorials sidebar, and mark as watched tracking."

### 184. QuickStartGuide
**Prompt**: "Create quick start guide overlay: collapsible sidebar with numbered steps, current step highlighted, completion checkboxes, embedded mini-videos/GIFs, and close when complete button."

---

## 🔔 Notifications & Alerts (6 components)

### 185. NotificationBadge
**Prompt**: "Design notification badge: red circle with count on icon, pulse animation for new notification, disappears when count is 0, max display (9+), and positioning (top-right of icon)."

### 186. InAppNotification
**Prompt**: "Create in-app notification card: icon for type (mention, comment, share), message text with actor name linked, timestamp (e.g., '2 min ago'), mark as read button, and click to navigate to source."

### 187. EmailDigest
**Prompt**: "Design email digest preview: grouped notifications by category, summary count ('5 new mentions'), clickable links to items, unsubscribe link, and frequency settings (daily, weekly, never)."

### 188. PushNotification
**Prompt**: "Create push notification settings: per-category toggles (mentions, comments, updates), quiet hours scheduler, device-specific settings (desktop vs mobile), and test notification button."

### 189. ReminderSystem
**Prompt**: "Design reminder interface: set reminder for page/task, date/time picker, repeat options (daily, weekly, custom), notification method (in-app, email, push), and list of active reminders."

### 190. UrgentAlert
**Prompt**: "Create urgent alert banner: red background, warning icon, critical message text, action button (e.g., 'Fix Now'), close button, and sticky position at top until dismissed."

---

## 📈 Performance & Optimization (4 components)

### 191. LazyLoadTrigger
**Prompt**: "Design lazy load indicator: subtle 'Loading more...' text with spinner at list bottom, infinite scroll trigger, skeleton placeholders for incoming items, and 'Load More' button fallback."

### 192. ImageOptimizer
**Prompt**: "Create image optimization UI: compression level slider, format selector (WebP, JPEG, PNG), quality preview, before/after comparison, file size reduction indicator, and batch optimize option."

### 193. CacheManagement
**Prompt**: "Design cache settings: clear cache button with confirmation, cache size indicator, auto-clear schedule, offline mode toggle (keeps cache), and 'Clear on logout' option."

### 194. PerformanceMonitor
**Prompt**: "Create performance dashboard: page load time graph, memory usage meter, slow queries list, optimization suggestions, and 'Run diagnostics' button for troubleshooting."

---

## 🎯 Additional Essential Components (6 components)

### 195. BulkActions
**Prompt**: "Design bulk action toolbar appearing when multiple items selected: checkbox to select all, count of selected items, action buttons (delete, move, tag, share), and clear selection button."

### 196. DragDropZone
**Prompt**: "Create drag-drop upload zone: dashed border, cloud upload icon, 'Drag files here or click to browse' text, file type hints, progress bars during upload, and thumbnail previews after upload."

### 197. ContextMenu
**Prompt**: "Design right-click context menu: relevant actions for clicked item, keyboard shortcuts shown, icons for actions, dividers between sections, nested submenus (Share → Email, Link, Embed), and click outside to dismiss."

### 198. Breadcrumb
**Prompt**: "Create breadcrumb navigation: home icon, chevron separators, clickable parent pages, current page (bold, not clickable), truncate middle with ellipsis if too long, and show full path on hover."

### 199. UserAvatar
**Prompt**: "Design user avatar component: circular image, fallback to initials with colored background (consistent color per user), online status dot (green = online), click to show user card, and group avatar (overlapping circles) option."

### 200. StatusBadge
**Prompt**: "Create status indicator badges: colored dot or pill shape, text label (Draft, Published, Archived, etc.), appropriate colors (gray, green, yellow, red), small size for compact spaces, and tooltip with details."

---

## 📝 Summary & Component Organization

### Total Components: **200**

**By Category:**
- Core Layout & Navigation: 10
- Editor Components: 18
- Organization & Navigation: 12
- Database Components: 14
- Collaboration Components: 12
- Graph & Visualization: 8
- Canvas & Whiteboard: 10
- Settings & Configuration: 10
- Authentication & Onboarding: 10
- States & Feedback: 12
- Mobile-Specific: 10
- Search & Discovery: 8
- Templates & Quickstart: 8
- Integrations & Extensions: 10
- Analytics & Insights: 8
- Customization & Theming: 8
- Admin & Moderation: 10
- Onboarding & Tours: 6
- Notifications & Alerts: 6
- Performance & Optimization: 4
- Additional Essential: 6

---

## 🎯 Priority Implementation Order

### **Phase 1: MVP (Weeks 1-8)** - 40 components
Core Layout (1-10), Essential Editor (11-15, 18-20), Basic Organization (29-34), Auth (95-98), States (105-109, 114)

### **Phase 2: Power Features (Weeks 9-16)** - 50 components  
Advanced Editor (16-17, 21-28), Database Views (41-48), Collaboration (55-60), Search (127-131), Mobile Core (117-121)

### **Phase 3: Advanced Features (Weeks 17-24)** - 50 components
Graph (67-74), Canvas (75-84), Settings (85-94), Templates (135-142), Integrations (143-152)

### **Phase 4: Polish & Scale (Weeks 25-32)** - 60 components
Analytics (153-160), Theming (161-168), Admin (169-178), Notifications (185-190), Remaining components

---

## 💡 Usage Tips

1. **Start with Figma/Design First**: Use these prompts in design tools before coding
2. **Component Library**: Build in Storybook for isolation and reusability  
3. **Responsive Design**: Every component needs mobile, tablet, desktop variants
4. **Accessibility**: ARIA labels, keyboard navigation, screen reader support
5. **Dark Mode**: Design both themes simultaneously
6. **Micro-interactions**: Subtle animations make the difference
7. **Performance**: Lazy load heavy components, virtualize long lists
8. **Testing**: Unit tests for logic, visual regression tests for UI

This is a **production-ready component specification** for building a complete Notion/Obsidian competitor. Each component is designed to work together as a cohesive system.
