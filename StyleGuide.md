# Lawyers-Hub Style Guide

## Core Principles
1. **Trust & Authority**: Professional color palette and clear typography.
2. **Efficiency**: High information density without sacrificing clarity.
3. **Accessibility**: Standard WCAG 2.1 compliant contrast and navigation.
4. **Agentic Interaction**: Smooth transitions and clear feedback for AI-driven features.

## Design Tokens

### Colors
- **Primary**: `#1f278c` (Indigo 900) - Main brand color, authority.
- **Secondary**: `#f1f5f9` (Slate 100) - Backgrounds, subtle UI elements.
- **Accent**: `#f59e0b` (Amber 500) - Call to actions, AI highlights.
- **Destructive**: `#e11d48` (Rose 600) - Errors, deletions.
- **Background**: `#ffffff` - Pure white for clean interface.
- **Foreground**: `#0f172a` (Slate 900) - High readability text.

### Typography
- **Headings**: Sans-serif (Inter/Geist), Bold, tight tracking.
- **Body**: Sans-serif (Inter/Geist), Regular, normal tracking.
- **Mono**: For document metadata and hashes.

### Border Radius
- **Base**: `0.75rem` (xl)
- **Large**: `1rem` (2xl)
- **Card/Container**: `1.5rem` (3xl) - Mobile
- **Card/Container (MD+)**: `2.5rem` ([2.5rem]) - Desktop
- **Modal**: Standardized to match Card/Container rounding.

## Atomic Components

### Atoms
- **LegalButton**: Interactive triggers with motion feedback.
- **LegalBadge**: Status indicators.
- **LegalInput**: Form fields with focus states.
- **LegalTypography**: Standardized text components.

### Molecules
- **LegalCard**: Content containers with soft shadows.
- **LegalSectionHeader**: Consistent headers for sections.
- **LegalModal**: Overlay containers for focused tasks.

### Organisms
- **DocumentIntelligenceCard**: AI-enhanced document analysis display.
- **NavigationSidebar**: Primary app navigation.

## Animations (Framer Motion)
- **Page Transitions**: Slide up + Fade in.
- **Hover States**: Subtle lift (y: -4px) and shadow enhancement.
- **Loading**: Pulse and spin for async operations.
