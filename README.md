# 🚀 React Frontend Template

Modern, production-ready React template with Firebase integration, advanced theming, and comprehensive user management. Built with TypeScript, Material-UI, and modern web development best practices.

[![React](https://img.shields.io/badge/React-18.3-61DAFB?style=flat&logo=react&logoColor=white)](https://reactjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5.8-3178C6?style=flat&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![MUI](https://img.shields.io/badge/MUI-7.3-007FFF?style=flat&logo=mui&logoColor=white)](https://mui.com/)
[![Firebase](https://img.shields.io/badge/Firebase-11.0-FFCA28?style=flat&logo=firebase&logoColor=black)](https://firebase.google.com/)
[![Vite](https://img.shields.io/badge/Vite-7.0-646CFF?style=flat&logo=vite&logoColor=white)](https://vitejs.dev/)

> **⚠️ Status**: This project is currently in active development. Features are being continuously refined and expanded.

## 📖 Overview

A comprehensive React frontend template designed to accelerate web application development. Features complete authentication flow, customizable theming system, internationalization support, and a flexible dashboard with draggable/resizable widgets.

**Key Differentiators:**

- **Complete Firebase Integration**: Authentication, Firestore, Storage, and Cloud Functions
- **Advanced Theming System**: Dynamic light/dark mode with custom primary color selection (including color picker)
- **Smart State Management**: Theme and settings persistence - localStorage for guests, Firebase for authenticated users
- **Interactive Dashboard**: Drag-and-drop, resizable widgets with responsive layouts powered by React Grid Layout
- **Fully Internationalized**: Multi-language support (English, Latvian) with easy extensibility
- **Type-Safe Development**: Comprehensive TypeScript coverage with strict mode enabled

## ✨ Features

### 🔐 Authentication & User Management

- **Firebase Authentication Integration**:
  - Email/password registration with display name validation
  - Secure login flow with form validation (React Hook Form + Zod)
  - Animated sliding panel design for login/signup forms
  - Persistent session management
  - Protected routes and navigation guards
- **Profile Management**:
  - Public and private profile information storage (Firestore)
  - Avatar upload with Firebase Storage
  - Image cropping functionality (react-easy-crop)
  - Image compression before upload
  - Profile photo display across application
- **Account Settings**:
  - Tabbed interface (Profile, Security, Account Actions)
  - Edit public info (username, name, surname, email)
  - Edit private info (address, city, state, zip, phone)
  - Password change with reauthentication
  - Account deletion with confirmation
  - Profile ID display

### 🎨 Theming & Customization

- **Dynamic Theme System**:
  - Light and dark mode toggle with smooth transitions
  - Real-time theme switching without page reload
  - MUI theme integration with custom palette extensions
  - Neon glow effects on buttons and dialogs
  - Responsive font sizing and spacing
- **Primary Color Customization**:
  - Predefined color palette (Orange, Blue, Green, Purple)
  - Custom color picker with eyedropper tool
  - Automatic contrast adjustment for accessibility
  - Color brightness validation for readability
  - Persistent color preferences
- **Customizer Sidebar**:
  - Right sidebar with theme controls
  - Visual theme toggle switch
  - Color swatch grid with preview
  - Settings button with animated toggle
  - Collapsible design (desktop/mobile)

### 🌍 Internationalization (i18n)

- **Multi-Language Support**:
  - i18next integration with React
  - Language switcher in navbar
  - Supported languages: English (EN), Latvian (LV)
  - Easy to extend with additional languages
- **Smart Language Persistence**:
  - Logged-in users: Saved to Firebase Firestore
  - Guest users: Saved to browser localStorage
  - Automatic language detection and loading
  - Real-time language switching without reload

### 📊 Interactive Dashboard

- **React Grid Layout Implementation**:
  - Drag-and-drop widget repositioning
  - Resize widgets with southeast handle
  - Collision prevention between widgets
  - Visual placeholder during drag operations
- **Responsive Breakpoints**:
  - 5 breakpoints: lg (1200px), md (996px), sm (768px), xs (480px), xxs (0px)
  - Adaptive layouts per breakpoint
  - Automatic reorganization on screen resize
  - Mobile-optimized single-column layout
- **Persistent State**:
  - Layout saved to localStorage
  - Per-breakpoint configuration storage
  - Widget state management
  - Reset to default layout option
- **Widget System**:
  - Modular widget architecture
  - Configurable minimum heights (enforced minH: 2)
  - Maximum rows constraint
  - Extensible widget descriptor interface

### 🧭 Navigation System

- **Multi-Level Navigation**:
  - Top navbar with brand logo and main links
  - Left sidebar with collapsible navigation groups
  - Right sidebar for customization settings
  - Responsive hamburger menus for mobile
- **Navbar Features**:
  - Active link highlighting with React Router
  - Profile button (context-aware: login vs account settings)
  - Theme toggle button with icons (sun/moon)
  - Language selector dropdown
  - Logout button (visible when authenticated)
- **Left Sidebar**:
  - Collapsible navigation groups (Main Pages, Additional Pages, More)
  - Icon-based navigation items
  - Active section highlighting
  - Persistent open/collapsed state (localStorage)
  - Slide-in animation on mobile
  - Hamburger toggle button
- **Right Sidebar**:
  - App customizer panel
  - Theme controls
  - Primary color picker
  - Logout button (when authenticated)
  - Slide-in animation

### 📄 Pages & Routes

1. **Home (Dashboard Page)**
   - Interactive widget dashboard
   - Drag-and-resize functionality
   - Responsive container with dynamic max rows
   - Section wrapper with title

2. **Login Page**
   - Sliding panel animation between login/signup
   - Sign In form with email/password
   - Sign Up form with email/password/display name
   - Form validation with helpful error messages
   - Gradient background with primary color
   - Already logged-in notification

3. **Account Settings Page**
   - Nested routing (profile, security, actions)
   - Vertical tabs on desktop, horizontal on mobile
   - Profile Tab:
     - Avatar display and upload
     - Public info viewer (username, email, name)
     - Private info viewer (address, city, state, zip, phone)
     - Edit dialogs with forms
     - Profile ID display
   - Security Tab:
     - Change password modal
     - Current password reauthentication
   - Account Actions Tab:
     - Delete account with password confirmation

4. **About Page**
   - Project overview and description
   - Technology stack information
   - Feature highlights
   - Responsive content layout

5. **404 Not Found Page**
   - Custom styling
   - Navigation back to home

### 🔔 Dialog & Modal System

- **Dialog Provider Context**:
  - Global dialog state management
  - Centralized dialog rendering
  - Promise-based API for user responses
- **Modal Types**:
  - **Confirm Dialog**:
    - Customizable title, message, buttons
    - Optional password input for sensitive actions
    - Promise returns user choice or password
  - **Error Dialog**:
    - Error message display
    - Standardized error handling
    - Auto-focus on close button
  - **Status Dialog**:
    - Success/failure notifications
    - Timeout-based auto-close
    - Customizable icons and colors
  - **Login Modal** (component-based):
    - Embedded in dedicated login page
    - Can be reused as modal in other contexts

### 📷 Image Management

- **Avatar Upload System**:
  - Click-to-upload interaction
  - File input with image type restriction
  - Image compression before upload (browser-image-compression)
  - Cropping dialog with:
    - Pan and zoom controls
    - 1:1 aspect ratio enforcement
    - Slider for zoom adjustment
    - Save/cancel actions
  - Upload to Firebase Storage
  - Update user profile with photo URL
  - Loading states during upload

## 🛠 Tech Stack

### Core Technologies

| Technology            | Version | Purpose                 |
| --------------------- | ------- | ----------------------- |
| **React**             | 18.3.1  | UI framework            |
| **TypeScript**        | 5.8.3   | Type safety             |
| **Vite**              | 7.0.5   | Build tool & dev server |
| **Material-UI (MUI)** | 7.3.2   | Component library       |
| **Emotion**           | 11.14.0 | CSS-in-JS styling       |

### Backend & Infrastructure

| Technology           | Version | Purpose                      |
| -------------------- | ------- | ---------------------------- |
| **Firebase**         | 11.0.1  | Backend as a Service         |
| **Firebase Auth**    | -       | User authentication          |
| **Firestore**        | -       | NoSQL database               |
| **Firebase Storage** | -       | File storage                 |
| **Cloud Functions**  | -       | Serverless backend functions |

### State & Forms

- **React Hook Form** (7.62.0) - Form state management & validation
- **Zod** (4.1.5) - Schema validation
- **@hookform/resolvers** (5.2.1) - Form validation integration
- **Context API** - Global state (User, Dialog, UI, Style)

### Routing & Navigation

- **React Router DOM** (6.27.1) - Client-side routing with nested routes

### Internationalization

- **i18next** (25.3.2) - Internationalization framework
- **react-i18next** (15.6.1) - React bindings for i18next

### UI Components & Interactions

- **React Grid Layout** (1.5.2) - Drag-and-drop grid system
- **React Resizable** (3.0.5) - Resizable components
- **React Easy Crop** (5.5.0) - Image cropping interface
- **@mui/icons-material** (7.1.0) - Material Design icons

### Utilities

- **browser-image-compression** (2.0.2) - Client-side image compression
- **Sass** (1.80.4) - CSS preprocessor

### Development Tools

- **@vitejs/plugin-react** (4.7.0) - Vite React plugin
- **firebase-tools** (13.24.1) - Firebase CLI
- **ESLint** - Code linting (via Vite)
- **TypeScript** - Type checking

## 📸 Screenshots

### Desktop Experience

1. **Login Page with Sign In Tab**
   - Animated sliding panel design with gradient background
   - Sign in form with email/password validation
   - Navbar showcasing: logo, navigation links, profile button, theme toggle (sun/moon icon), language selector, logout button
   - Left sidebar visible with collapsible navigation groups and icons
   - Right sidebar (customizer) showing theme toggle switch and primary color picker with predefined swatches and color picker tool
   - Clean, modern interface with neon glow effects

2. **Login Page with Sign Up Tab**
   - Sliding panel animation revealing sign-up form
   - Registration fields including email, password, and display name
   - Form validation messages for duplicate usernames
   - Smooth transition between login/signup views
   - Same navbar and sidebar structure visible

3. **Account Settings - Profile Tab**
   - Tabbed interface with vertical tabs (profile, security, account actions)
   - Profile header with avatar display
   - Public info section: username, email, name, surname with edit button
   - Private info section: address details with edit button
   - Profile ID display
   - Logout button in top-right
   - Responsive layout with clean spacing

4. **Account Settings - Edit Private Info Modal**
   - Dialog with primary color border and glow effect
   - Form fields: address, apartment/floor, city, state, zip, phone number
   - Save and Cancel buttons with hover effects
   - Validation feedback
   - Dark mode styling with proper contrast

5. **Light Mode with Latvian Language**
   - Complete UI in Latvian language (LV)
   - Light theme with adjusted colors
   - Proper contrast and readability
   - All navigation, buttons, and labels translated
   - Demonstrates full i18n capability

6. **Interactive Dashboard**
   - Drag-and-drop widget grid
   - Resizable widgets with southeast handles
   - Visual placeholder during drag operations
   - Responsive grid adapting to container size
   - Multiple widgets with different sizes and positions
   - Smooth animations during interactions

7. **About Page**
   - Project description and overview
   - Technology stack details
   - Feature highlights
   - Responsive content sections
   - Clean typography and spacing

### Mobile Experience

_Responsive design adapts seamlessly to mobile devices with optimized layouts and touch interactions._

8. **Mobile - Account Settings**
   - Horizontal scrolling tabs for mobile
   - Touch-optimized form inputs
   - Responsive spacing and font sizes
   - Full-screen layout utilization
   - Avatar display with upload option

9. **Mobile - Left Sidebar**
   - Hamburger menu activation
   - Slide-in animation from left
   - Full-screen overlay
   - Collapsible navigation groups
   - Touch-friendly icon sizes
   - Close button or backdrop tap to dismiss

10. **Mobile - Right Sidebar (Customizer)**
    - Settings button opens right sidebar
    - Slide-in animation from right
    - Theme toggle switch
    - Primary color picker
    - Touch-optimized controls
    - Responsive color swatch grid

## 📁 Project Structure

```
src/
├── components/
│   ├── buttons/                    # Reusable button components
│   │   └── logout-button/          # Logout button with confirmation
│   │
│   ├── global-modals/              # Global modal renderer
│   │   └── global-modals.tsx       # Dialog provider consumers
│   │
│   ├── layout/                     # Layout components
│   │   ├── info-section/           # Info display sections
│   │   └── section-wrapper/        # Page section container
│   │
│   ├── modals/                     # Modal components
│   │   ├── confirm/                # Confirmation dialog
│   │   ├── error/                  # Error display dialog
│   │   ├── login/                  # Login/signup forms
│   │   └── status/                 # Status notification dialog
│   │
│   ├── parts/                      # Small reusable parts
│   │   ├── chevron-icon/           # Expandable section icons
│   │   ├── data-display/           # Data display components
│   │   ├── icon/                   # Icon wrapper component
│   │   ├── spinner/                # Loading spinner
│   │   └── status-chip/            # Status badge component
│   │
│   └── widgets/                    # Dashboard widgets
│       ├── currency-list-widget/   # Currency display widget
│       └── map-widget/             # Map widget placeholder
│
├── features/                       # Feature modules
│   ├── account-settings/           # Account settings feature
│   │   ├── account-settings.tsx    # Main settings component
│   │   ├── tabs/                   # Settings tabs
│   │   │   ├── profile-tab/        # Profile management
│   │   │   │   ├── profile-tab.tsx
│   │   │   │   ├── parts/          # Profile sub-components
│   │   │   │   └── forms/          # Public/private info forms
│   │   │   ├── security-tab/       # Password management
│   │   │   └── actions-tab/        # Account deletion
│   │   └── parts/                  # Shared settings components
│   │
│   ├── cropper-dialog/             # Image cropping feature
│   │   ├── cropper-dialog.tsx      # Crop dialog component
│   │   └── crop-image.ts           # Cropping logic
│   │
│   ├── dashboard/                  # Dashboard feature
│   │   ├── components/
│   │   │   ├── dashboard-grid/     # Grid layout component
│   │   │   └── dashboard-widget/   # Widget wrapper
│   │   ├── hooks/                  # Dashboard hooks
│   │   │   └── use-dashboard-layout.ts  # Layout state management
│   │   └── types/                  # Dashboard type definitions
│   │
│   ├── navbar/                     # Top navigation bar
│   │   ├── navbar.tsx              # Main navbar component
│   │   └── parts/                  # Navbar sub-components
│   │       ├── hamburger/          # Mobile menu toggle
│   │       ├── language-select/    # Language dropdown
│   │       ├── our-button/         # Custom navbar button
│   │       └── nav-constants.ts    # Navigation configuration
│   │
│   └── sidebars/                   # Sidebar features
│       ├── left-bar/               # Navigation sidebar
│       │   ├── left-bar.tsx
│       │   └── parts/
│       │       ├── nav/            # Navigation groups
│       │       └── left-bar-hamburger/  # Toggle button
│       │
│       └── right-bar/              # Customizer sidebar
│           ├── right-bar.tsx
│           └── parts/
│               ├── theme-toggle/   # Theme switch component
│               └── color-pickers/  # Color picker components
│
├── firebase/                       # Firebase integration
│   ├── firebaseConfig.ts           # Firebase initialization
│   ├── functionsClient.ts          # Cloud Functions client
│   ├── storage.ts                  # Storage utilities
│   └── services/
│       ├── auth.ts                 # Authentication services
│       └── userSettings.ts         # User settings CRUD
│
├── hooks/                          # Custom React hooks
│   ├── auth/
│   │   ├── use-login-handlers.ts   # Login/signup logic
│   │   └── useFirebaseAuth.ts      # Auth state hook
│   ├── firestore/
│   │   └── useFirestore.ts         # Firestore utilities
│   └── user/
│       └── use-account-settings.ts # Account settings logic
│
├── layouts/
│   └── app-layout.tsx              # Main application layout
│
├── pages/                          # Page components
│   ├── about-page/                 # About page
│   ├── account-page/               # Account settings page
│   ├── home-page/                  # Dashboard page
│   ├── login-page/                 # Login/signup page
│   └── not-found-page/             # 404 page
│
├── providers/                      # Context providers
│   ├── dialog-provider.tsx         # Dialog state management
│   ├── style-provider.tsx          # Theme state management
│   ├── ui-provider.tsx             # UI state (sidebars, etc.)
│   ├── user-provider.tsx           # User and settings state
│   └── main/
│       └── provider.tsx            # Combined provider wrapper
│
├── styles/                         # Global styles
│   ├── index.scss                  # Global SCSS
│   ├── theme-mixins.ts             # Theme utility mixins
│   └── theme.ts                    # MUI theme configuration
│
├── translate/                      # Internationalization
│   ├── i18n.ts                     # i18next configuration
│   └── locales/
│       ├── en.json                 # English translations
│       └── lv.json                 # Latvian translations
│
├── types/                          # TypeScript type definitions
│   ├── dialog-types.ts             # Dialog-related types
│   ├── react-grid-layout.d.ts      # Grid layout type augmentation
│   ├── sidebar-types.ts            # Sidebar configuration types
│   └── style-types.ts              # Style-related types
│
├── utils/                          # Utility functions
│   └── common/
│       └── style-utils/            # Style utility functions
│           ├── style-utils.ts      # Color manipulation, etc.
│           └── ui-state-cache.ts   # UI state persistence
│
├── App.tsx                         # Root application component
├── index.tsx                       # Application entry point
└── vite-env.d.ts                   # Vite type definitions

functions/                          # Firebase Cloud Functions
├── src/
│   ├── index.ts                    # Functions entry point
│   ├── config/
│   │   └── region.ts               # Firebase region configuration
│   └── services/
│       ├── auth/
│       │   └── registerUserWithDisplayName.js  # User registration
│       └── profile/
│           ├── updatePublicProfile.js          # Public info update
│           ├── updatePrivateProfile.js         # Private info update
│           └── updateLanguage.js               # Language preference
│
├── lib/                            # Compiled JavaScript output
└── package.json                    # Functions dependencies
```

## 🎯 Performance Optimizations

- **Code Splitting**:
  - Route-based splitting via React Router
  - Lazy loading for modals and heavy components
  - Dynamic imports reduce initial bundle size

- **Memoization**:
  - `useMemo` for expensive calculations (theme creation)
  - `useCallback` for event handlers in child components
  - Context value stabilization

- **Image Optimization**:
  - Client-side compression before upload
  - Proper image sizing (cropping to 1:1)
  - Firebase Storage CDN delivery

- **State Persistence**:
  - Debounced localStorage writes (300ms for dashboard)
  - Batched Firestore updates
  - Optimistic UI updates

- **Bundle Optimization**:
  - Vite's automatic code splitting
  - Tree-shaking for unused code
  - Production build minification

## 📄 License

© 2024-2026. All Rights Reserved.

This project is a development template for internal use. The code is proprietary and not licensed for public reuse, modification, or distribution without explicit permission.

## 📬 Contact

**Alex Anackis**

- 🌐 Portfolio: [alexanackis.com](https://www.alexanackis.com/)
- 💼 LinkedIn: [linkedin.com/in/alex-anackis](https://www.linkedin.com/in/aleksandrs-anackis-9831371a8)
- 🐙 GitHub: [@anackis](https://github.com/anackis)

---

**Built with ❤️ using React, TypeScript, Firebase, and Material-UI**
