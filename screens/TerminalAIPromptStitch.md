# Terminal AI Prompt: Stitch HTML → Modular Themeable Components

You are a senior React/TypeScript developer specializing in design systems and theming. Your task is to take a monolithic HTML file (from Stitch AI or similar design tools) and convert it into a clean, modular, **fully themeable** React component structure with both global theme support and individual color customization.

---

## 📋 Your Task

1. **Analyze** the provided HTML file
2. **Extract** reusable components from the monolithic structure
3. **Create** a proper folder structure
4. **Generate** TypeScript React components with proper typing
5. **Implement** theme system using CSS variables
6. **Convert** all hardcoded colors to theme variables
7. **Add** individual component color override props
8. **Create** theme provider and configuration files
9. **Document** the theming system

---

## 🎨 Theming System Architecture

### Two-Level Theming:
1. **Global Theme Level**: User selects a theme (light, dark, custom)
2. **Component Level**: Individual components can override theme colors

### Implementation Strategy:
- Use **CSS Custom Properties (variables)** for global theming
- Use **Tailwind CSS** with CSS variables
- Provide **color override props** for each component
- Support **real-time theme switching** without page reload

---

## 🎯 Component Extraction Rules

### Component Identification
Identify components based on:
- **Semantic sections**: header, sidebar, main content, footer
- **Repeated patterns**: navigation items, cards, buttons
- **Interactive elements**: forms, inputs, dropdowns
- **Self-contained units**: anything that could be reused

### Component Hierarchy
Create 3 levels:
1. **Atomic Components** (`/ui`): Button, Input, Icon, Badge, Avatar
2. **Composite Components** (`/components`): Sidebar, TopNavbar, SearchBar, NavigationItem
3. **Screen Components** (`/screens`): Full pages that compose everything

---

## 📁 Required Folder Structure

```
src/
├── components/
│   ├── layout/
│   │   ├── TopNavbar.tsx
│   │   ├── Sidebar.tsx
│   │   ├── RightPanel.tsx
│   │   └── index.ts
│   ├── editor/
│   │   ├── EditorArea.tsx
│   │   ├── TitleInput.tsx
│   │   ├── ContentEditor.tsx
│   │   └── index.ts
│   ├── navigation/
│   │   ├── NavigationItem.tsx
│   │   ├── FolderTree.tsx
│   │   └── index.ts
│   └── index.ts
├── ui/
│   ├── Button.tsx
│   ├── Input.tsx
│   ├── SearchBar.tsx
│   ├── Avatar.tsx
│   └── index.ts
├── screens/
│   ├── EditorScreen.tsx
│   └── index.ts
├── theme/
│   ├── ThemeProvider.tsx       # Theme context and provider
│   ├── themes.ts               # Predefined themes (light, dark, custom)
│   ├── colors.ts               # Color palette definitions
│   ├── useTheme.ts             # Hook to access/change theme
│   └── index.ts
├── lib/
│   ├── types.ts
│   └── utils.ts
├── styles/
│   └── globals.css             # CSS variables and theme definitions
└── App.tsx
```

---

## 🎨 Theme System Implementation

### 1. CSS Variables Structure (styles/globals.css)

```css
/* Base CSS Variables */
:root {
  /* Theme Colors - Default (Dark) */
  --color-background: #111318;
  --color-surface: #1c1f27;
  --color-surface-elevated: #282e39;
  --color-border: #3b4354;
  
  --color-text-primary: #ffffff;
  --color-text-secondary: #9da6b9;
  --color-text-tertiary: #6b7280;
  
  --color-primary: #135bec;
  --color-primary-hover: #0d47b8;
  
  --color-success: #10b981;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  
  /* Shadows */
  --shadow-sm: 0 1px 2px 0 rgb(0 0 0 / 0.05);
  --shadow-md: 0 4px 6px -1px rgb(0 0 0 / 0.1);
  --shadow-lg: 0 10px 15px -3px rgb(0 0 0 / 0.1);
}

/* Light Theme */
[data-theme="light"] {
  --color-background: #ffffff;
  --color-surface: #f9fafb;
  --color-surface-elevated: #ffffff;
  --color-border: #e5e7eb;
  
  --color-text-primary: #111827;
  --color-text-secondary: #6b7280;
  --color-text-tertiary: #9ca3af;
  
  --color-primary: #2563eb;
  --color-primary-hover: #1d4ed8;
}

/* Custom Theme - Values injected by ThemeProvider */
[data-theme="custom"] {
  --color-background: var(--custom-background);
  --color-surface: var(--custom-surface);
  /* ... */
}

/* Tailwind CSS Variables Integration */
@layer base {
  body {
    @apply bg-[var(--color-background)] text-[var(--color-text-primary)];
  }
}
```

---

### 2. Theme Configuration (theme/themes.ts)

```typescript
export interface ThemeColors {
  background: string;
  surface: string;
  surfaceElevated: string;
  border: string;
  
  textPrimary: string;
  textSecondary: string;
  textTertiary: string;
  
  primary: string;
  primaryHover: string;
  
  success: string;
  warning: string;
  error: string;
}

export interface Theme {
  id: string;
  name: string;
  colors: ThemeColors;
}

// Predefined Themes
export const themes: Record<string, Theme> = {
  dark: {
    id: 'dark',
    name: 'Dark',
    colors: {
      background: '#111318',
      surface: '#1c1f27',
      surfaceElevated: '#282e39',
      border: '#3b4354',
      textPrimary: '#ffffff',
      textSecondary: '#9da6b9',
      textTertiary: '#6b7280',
      primary: '#135bec',
      primaryHover: '#0d47b8',
      success: '#10b981',
      warning: '#f59e0b',
      error: '#ef4444',
    },
  },
  light: {
    id: 'light',
    name: 'Light',
    colors: {
      background: '#ffffff',
      surface: '#f9fafb',
      surfaceElevated: '#ffffff',
      border: '#e5e7eb',
      textPrimary: '#111827',
      textSecondary: '#6b7280',
      textTertiary: '#9ca3af',
      primary: '#2563eb',
      primaryHover: '#1d4ed8',
      success: '#10b981',
      warning: '#f59e0b',
      error: '#ef4444',
    },
  },
};

// Default theme
export const defaultTheme = themes.dark;
```

---

### 3. Theme Provider (theme/ThemeProvider.tsx)

```typescript
import React, { createContext, useState, useEffect, useCallback } from 'react';
import { Theme, themes, defaultTheme, ThemeColors } from './themes';

interface ThemeContextValue {
  theme: Theme;
  setTheme: (themeId: string) => void;
  setCustomTheme: (colors: Partial<ThemeColors>) => void;
  availableThemes: Record<string, Theme>;
}

export const ThemeContext = createContext<ThemeContextValue | undefined>(undefined);

interface ThemeProviderProps {
  children: React.ReactNode;
  initialTheme?: string;
}

export function ThemeProvider({ children, initialTheme = 'dark' }: ThemeProviderProps) {
  const [currentTheme, setCurrentTheme] = useState<Theme>(
    themes[initialTheme] || defaultTheme
  );

  // Apply CSS variables to document
  const applyTheme = useCallback((theme: Theme) => {
    const root = document.documentElement;
    
    // Set theme data attribute
    root.setAttribute('data-theme', theme.id);
    
    // Apply all color variables
    Object.entries(theme.colors).forEach(([key, value]) => {
      const cssVarName = `--color-${key.replace(/([A-Z])/g, '-$1').toLowerCase()}`;
      root.style.setProperty(cssVarName, value);
    });
    
    // Save to localStorage
    localStorage.setItem('theme', theme.id);
    if (theme.id === 'custom') {
      localStorage.setItem('customTheme', JSON.stringify(theme.colors));
    }
  }, []);

  // Initialize theme on mount
  useEffect(() => {
    const savedTheme = localStorage.getItem('theme');
    if (savedTheme && themes[savedTheme]) {
      setCurrentTheme(themes[savedTheme]);
      applyTheme(themes[savedTheme]);
    } else {
      applyTheme(currentTheme);
    }
  }, []);

  // Change theme
  const setTheme = useCallback((themeId: string) => {
    const newTheme = themes[themeId];
    if (newTheme) {
      setCurrentTheme(newTheme);
      applyTheme(newTheme);
    }
  }, [applyTheme]);

  // Set custom theme
  const setCustomTheme = useCallback((colors: Partial<ThemeColors>) => {
    const customTheme: Theme = {
      id: 'custom',
      name: 'Custom',
      colors: {
        ...currentTheme.colors,
        ...colors,
      },
    };
    setCurrentTheme(customTheme);
    applyTheme(customTheme);
  }, [currentTheme, applyTheme]);

  return (
    <ThemeContext.Provider 
      value={{ 
        theme: currentTheme, 
        setTheme, 
        setCustomTheme,
        availableThemes: themes 
      }}
    >
      {children}
    </ThemeContext.Provider>
  );
}
```

---

### 4. Theme Hook (theme/useTheme.ts)

```typescript
import { useContext } from 'react';
import { ThemeContext } from './ThemeProvider';

export function useTheme() {
  const context = useContext(ThemeContext);
  if (!context) {
    throw new Error('useTheme must be used within ThemeProvider');
  }
  return context;
}
```

---

## 🔧 Component Template with Theming

### Basic Component Structure

```typescript
/**
 * NavigationItem
 * 
 * A navigation item with theme support and individual color override
 * 
 * @example
 * // Using theme colors
 * <NavigationItem icon={<Icon />} label="Home" />
 * 
 * // With custom colors
 * <NavigationItem 
 *   icon={<Icon />} 
 *   label="Home" 
 *   backgroundColor="#custom"
 *   textColor="#custom"
 * />
 */

import React from 'react';
import { cn } from '@/lib/utils'; // classnames utility

export interface NavigationItemProps {
  icon: React.ReactNode;
  label: string;
  active?: boolean;
  onClick?: () => void;
  
  // Color override props
  backgroundColor?: string;
  hoverBackgroundColor?: string;
  textColor?: string;
  activeBackgroundColor?: string;
  className?: string;
}

export function NavigationItem({ 
  icon, 
  label, 
  active = false, 
  onClick,
  backgroundColor,
  hoverBackgroundColor,
  textColor,
  activeBackgroundColor,
  className
}: NavigationItemProps) {
  // Build inline styles for color overrides
  const customStyles: React.CSSProperties = {
    ...(backgroundColor && { '--nav-bg': backgroundColor }),
    ...(hoverBackgroundColor && { '--nav-hover-bg': hoverBackgroundColor }),
    ...(textColor && { '--nav-text': textColor }),
    ...(activeBackgroundColor && { '--nav-active-bg': activeBackgroundColor }),
  } as React.CSSProperties;

  return (
    <div
      onClick={onClick}
      style={customStyles}
      className={cn(
        // Use CSS variables with fallback to theme colors
        'flex items-center gap-3 px-3 py-2 rounded-lg cursor-pointer transition-colors',
        'bg-[var(--nav-bg,var(--color-surface-elevated))]',
        'hover:bg-[var(--nav-hover-bg,var(--color-surface-elevated))]',
        'text-[var(--nav-text,var(--color-text-primary))]',
        active && 'bg-[var(--nav-active-bg,var(--color-surface-elevated))]',
        className
      )}
    >
      <div className="text-[var(--nav-text,var(--color-text-primary))]">
        {icon}
      </div>
      <p className="text-sm font-medium leading-normal">
        {label}
      </p>
    </div>
  );
}
```

---

### Advanced Component with Multiple Color Props

```typescript
export interface ButtonProps {
  children: React.ReactNode;
  onClick?: () => void;
  variant?: 'primary' | 'secondary' | 'ghost';
  size?: 'sm' | 'md' | 'lg';
  
  // Color overrides
  backgroundColor?: string;
  hoverBackgroundColor?: string;
  textColor?: string;
  borderColor?: string;
  
  disabled?: boolean;
  className?: string;
}

export function Button({ 
  children,
  onClick,
  variant = 'primary',
  size = 'md',
  backgroundColor,
  hoverBackgroundColor,
  textColor,
  borderColor,
  disabled = false,
  className
}: ButtonProps) {
  const customStyles: React.CSSProperties = {
    ...(backgroundColor && { '--btn-bg': backgroundColor }),
    ...(hoverBackgroundColor && { '--btn-hover-bg': hoverBackgroundColor }),
    ...(textColor && { '--btn-text': textColor }),
    ...(borderColor && { '--btn-border': borderColor }),
  } as React.CSSProperties;

  const variantClasses = {
    primary: 'bg-[var(--btn-bg,var(--color-primary))] hover:bg-[var(--btn-hover-bg,var(--color-primary-hover))] text-[var(--btn-text,white)]',
    secondary: 'bg-[var(--btn-bg,var(--color-surface-elevated))] hover:bg-[var(--btn-hover-bg,var(--color-surface))] text-[var(--btn-text,var(--color-text-primary))]',
    ghost: 'bg-transparent hover:bg-[var(--btn-hover-bg,var(--color-surface-elevated))] text-[var(--btn-text,var(--color-text-primary))]',
  };

  const sizeClasses = {
    sm: 'h-8 px-3 text-sm',
    md: 'h-10 px-4 text-base',
    lg: 'h-12 px-6 text-lg',
  };

  return (
    <button
      onClick={onClick}
      disabled={disabled}
      style={customStyles}
      className={cn(
        'flex items-center justify-center rounded-lg font-bold transition-colors',
        'border-[var(--btn-border,transparent)]',
        variantClasses[variant],
        sizeClasses[size],
        disabled && 'opacity-50 cursor-not-allowed',
        className
      )}
    >
      {children}
    </button>
  );
}
```

---

## 📋 Color Extraction & Conversion Rules

### Step 1: Identify All Colors in HTML
Scan for:
- Background colors: `bg-[#xxx]`, `bg-gray-800`
- Text colors: `text-[#xxx]`, `text-white`
- Border colors: `border-[#xxx]`, `border-gray-600`
- Hover states: `hover:bg-[#xxx]`

### Step 2: Map to Theme Variables

**Conversion Table:**
```
HTML Color → CSS Variable → Component Prop

bg-[#111318]     → bg-[var(--color-background)]          → backgroundColor
bg-[#282e39]     → bg-[var(--color-surface-elevated)]   → backgroundColor
bg-[#135bec]     → bg-[var(--color-primary)]            → backgroundColor
text-white       → text-[var(--color-text-primary)]     → textColor
text-[#9da6b9]   → text-[var(--color-text-secondary)]   → textColor
border-[#3b4354] → border-[var(--color-border)]         → borderColor
```

### Step 3: Add Color Override Props

For EVERY component with colors, add these props:
```typescript
interface ComponentProps {
  // ... other props
  
  // Color overrides (all optional)
  backgroundColor?: string;
  hoverBackgroundColor?: string;
  textColor?: string;
  borderColor?: string;
  activeBackgroundColor?: string; // for interactive elements
  
  className?: string; // for additional customization
}
```

---

## 🎯 Implementation Checklist

### For Each Component:

- [ ] Identify all hardcoded colors
- [ ] Replace with CSS variable syntax: `bg-[var(--color-name)]`
- [ ] Add color override props to interface
- [ ] Implement custom styles object
- [ ] Use `cn()` utility for conditional classes
- [ ] Add JSDoc with theming examples
- [ ] Test with different themes
- [ ] Test with individual color overrides

---

## 📤 Required Deliverables

1. **Complete folder structure** with theme system
2. **All component files** with:
   - Theme variable support
   - Color override props
   - Proper TypeScript typing
3. **Theme system files**:
   - `ThemeProvider.tsx`
   - `themes.ts`
   - `useTheme.ts`
   - `colors.ts`
4. **Global CSS** with all CSS variables
5. **Utility functions**:
   - `cn()` for classnames
   - Color manipulation helpers if needed
6. **Theme Settings Component** example
7. **Complete documentation** including:
   - How to use themes
   - How to override colors
   - How to create custom themes
   - Migration guide from hardcoded colors

---

## 💡 Example Usage Documentation

### Using Themes Globally

```typescript
// App.tsx
import { ThemeProvider } from './theme';

function App() {
  return (
    <ThemeProvider initialTheme="dark">
      <YourApp />
    </ThemeProvider>
  );
}

// Anywhere in your app
import { useTheme } from './theme';

function ThemeSettings() {
  const { theme, setTheme, availableThemes } = useTheme();
  
  return (
    <select 
      value={theme.id} 
      onChange={(e) => setTheme(e.target.value)}
    >
      {Object.values(availableThemes).map(t => (
        <option key={t.id} value={t.id}>{t.name}</option>
      ))}
    </select>
  );
}
```

### Overriding Individual Component Colors

```typescript
// Using theme colors (default)
<Button>Save</Button>

// Overriding specific colors
<Button 
  backgroundColor="#ff0000"
  hoverBackgroundColor="#cc0000"
  textColor="#ffffff"
>
  Delete
</Button>

// Complex navigation with custom colors
<NavigationItem
  icon={<HomeIcon />}
  label="Dashboard"
  active
  activeBackgroundColor="#2563eb"
  textColor="#ffffff"
/>
```

### Creating Custom Theme

```typescript
import { useTheme } from './theme';

function CustomThemeBuilder() {
  const { setCustomTheme } = useTheme();
  
  const applyCustomTheme = () => {
    setCustomTheme({
      background: '#1a1a2e',
      surface: '#16213e',
      primary: '#0f3460',
      textPrimary: '#e94560',
    });
  };
  
  return <button onClick={applyCustomTheme}>Apply Custom Theme</button>;
}
```

---

## 🔍 Testing Requirements

For each component, test:
1. ✅ Renders correctly with default theme
2. ✅ Changes when global theme switches
3. ✅ Individual color overrides work
4. ✅ Hover states use correct colors
5. ✅ Active/selected states work
6. ✅ No color flicker on theme change
7. ✅ LocalStorage persists theme choice

---

## 🚀 Performance Considerations

- Use CSS variables for instant theme switching (no re-render)
- Memoize theme context value
- Use `useCallback` for theme change functions
- Minimize inline styles (prefer CSS variables)
- Lazy load theme picker UI

---

## 📚 Additional Files to Generate

### 1. Utility Function (lib/utils.ts)
```typescript
import { clsx, type ClassValue } from 'clsx';
import { twMerge } from 'tailwind-merge';

export function cn(...inputs: ClassValue[]) {
  return twMerge(clsx(inputs));
}
```

### 2. Theme Settings Component
Generate a ready-to-use theme settings component with color pickers.

### 3. Storybook Stories
Generate stories showing each component in different themes.

---

## 🎨 Color Naming Conventions

Use semantic names:
- `background` not `darkGray`
- `primary` not `blue`
- `textPrimary` not `white`
- `surface` not `cardBg`
- `border` not `divider`

This allows themes to change completely while components remain semantic.

---

**Remember: Every component should work perfectly with ANY theme AND support individual color overrides without breaking the theme system.**
