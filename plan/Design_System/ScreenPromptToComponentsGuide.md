# Stitch HTML → Modüler Component Dönüşümü

## 🎯 Strateji: Hybrid Approach

**İdeal Yöntem:** Stitch AI ile ekran oluştur → Modüler componentlere böl → Yeniden kullan

---

## 📦 Adım 1: Stitch AI Çıktısını Analiz Et

Verdiğin HTML'deki yapı:
```
<body>
  <div> <!-- Root -->
    <div> <!-- Layout Container -->
      <header> <!-- Top Navbar -->
      <div> <!-- Main Content Area -->
        <div> <!-- Left Sidebar -->
        <div> <!-- Center Content -->
        <div> <!-- Right Sidebar -->
```

---

## 🔨 Adım 2: Component Ağacını Belirle

```
EditorScreen (main screen)
├── TopNavbar
│   ├── Logo
│   ├── SearchBar
│   └── UserMenu
├── Sidebar (left)
│   ├── NavigationItem
│   ├── FolderTree
│   └── NewNoteButton
├── EditorArea (center)
│   ├── SearchInput
│   ├── TitleInput
│   └── ContentTextarea
└── PropertiesPanel (right)
    ├── PropertySelect
    └── BacklinksSection
```

---

## ⚙️ Adım 3: Componentleri Çıkar ve Modülerleştir

### **3.1. TopNavbar Component**

**Stitch HTML'den:**
```html
<header class="flex items-center justify-between whitespace-nowrap border-b border-solid border-b-[#282e39] px-10 py-3">
  <div class="flex items-center gap-4 text-white">
    <!-- Logo ve başlık -->
  </div>
  <div class="flex flex-1 justify-end gap-8">
    <!-- Search, buttons, avatar -->
  </div>
</header>
```

**React Component'e Dönüştür:**
```typescript
// components/TopNavbar.tsx
interface TopNavbarProps {
  logo?: React.ReactNode;
  title: string;
  onSearch?: (query: string) => void;
  user?: {
    name: string;
    avatar: string;
  };
}

export function TopNavbar({ logo, title, onSearch, user }: TopNavbarProps) {
  return (
    <header className="flex items-center justify-between whitespace-nowrap border-b border-solid border-b-[#282e39] px-10 py-3">
      <div className="flex items-center gap-4 text-white">
        {logo && <div className="size-4">{logo}</div>}
        <h2 className="text-white text-lg font-bold leading-tight tracking-[-0.015em]">
          {title}
        </h2>
      </div>
      
      <div className="flex flex-1 justify-end gap-8">
        <SearchBar onSearch={onSearch} />
        <ListButton />
        <UserAvatar user={user} />
      </div>
    </header>
  );
}
```

---

### **3.2. Sidebar Component**

**Stitch HTML'den:**
```html
<div class="layout-content-container flex flex-col w-80">
  <div class="flex h-full min-h-[700px] flex-col justify-between bg-[#111318] p-4">
    <div class="flex flex-col gap-4">
      <!-- Navigation items -->
    </div>
    <div class="flex flex-col gap-4">
      <!-- New Note button, Trash -->
    </div>
  </div>
</div>
```

**React Component'e Dönüştür:**
```typescript
// components/Sidebar.tsx
interface SidebarProps {
  items: Array<{
    icon: React.ReactNode;
    label: string;
    active?: boolean;
    onClick?: () => void;
  }>;
  onNewNote?: () => void;
}

export function Sidebar({ items, onNewNote }: SidebarProps) {
  return (
    <div className="layout-content-container flex flex-col w-80">
      <div className="flex h-full min-h-[700px] flex-col justify-between bg-[#111318] p-4">
        {/* Navigation Items */}
        <div className="flex flex-col gap-4">
          {items.map((item, idx) => (
            <NavigationItem key={idx} {...item} />
          ))}
        </div>
        
        {/* Actions */}
        <div className="flex flex-col gap-4">
          <button
            onClick={onNewNote}
            className="flex min-w-[84px] cursor-pointer items-center justify-center overflow-hidden rounded-lg h-10 px-4 bg-[#135bec] text-white text-sm font-bold"
          >
            New Note
          </button>
          <TrashItem />
        </div>
      </div>
    </div>
  );
}
```

---

### **3.3. NavigationItem Component (Atomic)**

```typescript
// components/NavigationItem.tsx
interface NavigationItemProps {
  icon: React.ReactNode;
  label: string;
  active?: boolean;
  onClick?: () => void;
}

export function NavigationItem({ 
  icon, 
  label, 
  active = false, 
  onClick 
}: NavigationItemProps) {
  return (
    <div
      onClick={onClick}
      className={`flex items-center gap-3 px-3 py-2 rounded-lg cursor-pointer ${
        active ? 'bg-[#282e39]' : 'hover:bg-[#282e39]/50'
      }`}
    >
      <div className="text-white">{icon}</div>
      <p className="text-white text-sm font-medium leading-normal">
        {label}
      </p>
    </div>
  );
}
```

---

### **3.4. EditorArea Component**

**Stitch HTML'den:**
```html
<div class="layout-content-container flex flex-col max-w-[960px] flex-1">
  <div class="px-4 py-3">
    <!-- Search input -->
  </div>
  <div class="flex max-w-[480px] flex-wrap items-end gap-4 px-4 py-3">
    <!-- Title input -->
  </div>
  <div class="flex max-w-[480px] flex-wrap items-end gap-4 px-4 py-3">
    <!-- Content textarea -->
  </div>
</div>
```

**React Component'e Dönüştür:**
```typescript
// components/EditorArea.tsx
interface EditorAreaProps {
  title: string;
  content: string;
  onTitleChange: (title: string) => void;
  onContentChange: (content: string) => void;
  onSearch?: (query: string) => void;
}

export function EditorArea({
  title,
  content,
  onTitleChange,
  onContentChange,
  onSearch
}: EditorAreaProps) {
  return (
    <div className="layout-content-container flex flex-col max-w-[960px] flex-1">
      {/* Search */}
      <SearchInput onSearch={onSearch} />
      
      {/* Title */}
      <TitleInput 
        value={title} 
        onChange={onTitleChange}
        placeholder="Untitled" 
      />
      
      {/* Content */}
      <ContentEditor 
        value={content} 
        onChange={onContentChange}
      />
    </div>
  );
}
```

---

### **3.5. PropertiesPanel Component**

```typescript
// components/PropertiesPanel.tsx
interface PropertiesPanelProps {
  properties: Array<{
    label: string;
    type: 'select' | 'text' | 'date';
    options?: string[];
    value?: string;
  }>;
  backlinks: Array<{
    title: string;
    url: string;
  }>;
}

export function PropertiesPanel({ properties, backlinks }: PropertiesPanelProps) {
  return (
    <div className="layout-content-container flex flex-col">
      <h3 className="text-white text-lg font-bold px-4 pb-2 pt-4">
        Properties
      </h3>
      
      {properties.map((prop, idx) => (
        <PropertyField key={idx} {...prop} />
      ))}
      
      <h3 className="text-white text-lg font-bold px-4 pb-2 pt-4">
        Backlinks
      </h3>
      
      {backlinks.length === 0 ? (
        <EmptyBacklinks />
      ) : (
        <BacklinksList links={backlinks} />
      )}
    </div>
  );
}
```

---

## 🏗️ Adım 4: Ana Ekranı Compose Et

```typescript
// screens/EditorScreen.tsx
import { TopNavbar } from '@/components/TopNavbar';
import { Sidebar } from '@/components/Sidebar';
import { EditorArea } from '@/components/EditorArea';
import { PropertiesPanel } from '@/components/PropertiesPanel';

export function EditorScreen() {
  const [title, setTitle] = useState('');
  const [content, setContent] = useState('');
  
  const sidebarItems = [
    { icon: <NoteIcon />, label: 'All Notes', active: true },
    { icon: <NotebookIcon />, label: 'Notebooks' },
    { icon: <HashIcon />, label: 'Tags' },
    { icon: <UsersIcon />, label: 'Shared' },
  ];
  
  return (
    <div className="relative flex h-auto min-h-screen w-full flex-col bg-[#111318]">
      <div className="layout-container flex h-full grow flex-col">
        <TopNavbar 
          title="NoteApp" 
          user={{ name: 'John', avatar: 'url' }}
        />
        
        <div className="gap-1 px-6 flex flex-1 justify-center py-5">
          <Sidebar 
            items={sidebarItems}
            onNewNote={() => console.log('New note')}
          />
          
          <EditorArea
            title={title}
            content={content}
            onTitleChange={setTitle}
            onContentChange={setContent}
          />
          
          <PropertiesPanel
            properties={[]}
            backlinks={[]}
          />
        </div>
      </div>
    </div>
  );
}
```

---

## 📁 Adım 5: Proje Yapısı

```
src/
├── screens/
│   ├── EditorScreen.tsx          (Stitch'ten gelen komple ekran)
│   ├── DashboardScreen.tsx
│   └── SearchScreen.tsx
│
├── components/
│   ├── layout/
│   │   ├── TopNavbar.tsx         (Çıkarılan modüler component)
│   │   ├── Sidebar.tsx
│   │   └── PropertiesPanel.tsx
│   │
│   ├── editor/
│   │   ├── EditorArea.tsx
│   │   ├── TitleInput.tsx
│   │   └── ContentEditor.tsx
│   │
│   ├── ui/                       (Atomic components)
│   │   ├── NavigationItem.tsx
│   │   ├── SearchBar.tsx
│   │   ├── Button.tsx
│   │   └── Input.tsx
│   │
│   └── icons/
│       └── index.tsx
│
└── lib/
    └── utils.ts
```

---

## 🔄 Adım 6: Yeniden Kullanım

Artık componentler modüler olduğu için:

```typescript
// Farklı ekranlarda aynı componentleri kullan

// DashboardScreen.tsx
<TopNavbar title="Dashboard" user={user} />
<Sidebar items={dashboardItems} />

// SearchScreen.tsx  
<TopNavbar title="Search" user={user} />
<SearchResults results={results} />

// SettingsScreen.tsx
<TopNavbar title="Settings" user={user} />
<SettingsForm />
```

---

## ⚡ Adım 7: Component Library Oluştur (Storybook)

```typescript
// NavigationItem.stories.tsx
export default {
  title: 'Components/NavigationItem',
  component: NavigationItem,
};

export const Default = () => (
  <NavigationItem 
    icon={<NoteIcon />} 
    label="All Notes" 
  />
);

export const Active = () => (
  <NavigationItem 
    icon={<NoteIcon />} 
    label="All Notes" 
    active={true}
  />
);
```

---

## 🎯 Özet: Senin İçin En İyi Yaklaşım

### **✅ HYBRID Yöntem (Tavsiye Edilen):**

1. **Stitch AI** → 22 komple ekran tasarla
2. **İlk ekran hazır olunca** → Modüler componentlere böl
3. **Component library oluştur** → Atomic + Composite
4. **Sonraki ekranlar** → Mevcut componentlerle hızlı compose et
5. **Eksik component** → Stitch'te yeni ekran yap, component çıkar

### **Avantajları:**
- ✅ Stitch AI'ın hızından faydalanırsın
- ✅ Modüler, yeniden kullanılabilir kod
- ✅ Sürdürülebilir ve test edilebilir
- ✅ Hem tasarım hem kod hızı
- ✅ Component library oluşur (design system)

### **İş Akışı:**
```
Hafta 1-2: Stitch'te 5 ana ekran → Componentlere böl
Hafta 3-4: Component library oturdu → Compose ile hızlan
Hafta 5+:   Yeni ekranlar artık çok hızlı (mevcut componentlerle)
```

---

## 💡 Pratik Örnek: Sonraki Ekran

Artık **DashboardScreen** yapacaksan:

```typescript
// Stitch'e sadece eksik componentler için prompt at
// Geri kalanını mevcut componentlerle yap:

function DashboardScreen() {
  return (
    <>
      <TopNavbar {...} />      // ✅ Mevcut
      <Sidebar {...} />         // ✅ Mevcut
      <StatsCards {...} />      // ❌ YENİ → Stitch'te yap, çıkar
      <ActivityFeed {...} />    // ❌ YENİ → Stitch'te yap, çıkar
    </>
  );
}
```

Bu **en verimli ve sürdürülebilir** yaklaşım! 🚀
