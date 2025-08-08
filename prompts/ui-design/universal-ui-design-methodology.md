---
name: Universal UI/UX Design Methodology Expert
description: Use this agent when you need an adaptive design methodology that works across industries and project types. Examples: Building a systematic approach for multiple product lines, creating design standards that scale across different teams, developing semantic token architecture for complex applications.
model: sonnet
---

# Universal UI/UX Design System Methodology

**Category:** ui-design
**Difficulty:** Advanced
**Tags:** #design-system #methodology #semantic-tokens #responsive #accessibility

## Description

A comprehensive design methodology that adapts to any project type, focusing on semantic token architecture, color psychology, and systematic component design approaches. This prompt creates a complete design system foundation with universal principles that work across industries and project types.

## Prompt

```
I need you to create a comprehensive UI/UX design system methodology for my project using the following systematic approach:

PROJECT CONTEXT:
- Project type: [SaaS, e-commerce, portfolio, healthcare, fintech, etc.]
- Target audience: [developers, consumers, professionals, etc.]
- Brand personality: [playful, serious, innovative, traditional, etc.]
- Industry: [technology, healthcare, finance, creative, etc.]

DESIGN SYSTEM REQUIREMENTS:

## PHASE 1: SEMANTIC TOKEN ARCHITECTURE
Create a semantic token system using HSL color format:

```css
:root {
  /* Base semantic tokens - HSL format for manipulation */
  --primary: [hsl values];           /* Main brand color */
  --primary-glow: [lighter variant]; /* Interactive states */
  --accent: [hsl values];           /* Secondary brand */
  --secondary: [hsl values];        /* Supporting elements */
  
  /* Functional tokens */
  --gradient-primary: linear-gradient(135deg, primary, accent);
  --shadow-glow: 0 0 40px hsl(var(--primary) / 0.3);
  --transition-smooth: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}
```

## PHASE 2: COLOR PSYCHOLOGY ANALYSIS
Based on my project type and brand personality:
1. Analyze appropriate color psychology
2. Choose primary color using color theory principles
3. Select harmony type: complementary, analogous, triadic, or monochromatic
4. Calculate accent colors using the chosen harmony
5. Define neutral grays for backgrounds and text

## PHASE 3: COMPONENT VARIANT STRATEGY
Create systematic component variants instead of custom overrides:

```tsx
const buttonVariants = cva("base-classes", {
  variants: {
    variant: {
      default: "bg-primary text-primary-foreground",
      hero: "bg-gradient-primary hover:shadow-glow hover:scale-105",
      accent: "bg-accent hover:shadow-accent",
      ghost: "hover:bg-accent/10",
    }
  }
})
```

## PHASE 4: ANIMATION SYSTEM
Define four animation categories:
1. **Entrance animations** (fade-in, slide-up)
2. **Hover/interaction effects** (scale, glow)
3. **Ambient animations** (float, pulse)
4. **Attention-grabbing** (used sparingly)

## PHASE 5: RESPONSIVE METHODOLOGY
- Mobile-first approach with systematic breakpoints
- Consistent spacing scale using 4px base unit
- Typography hierarchy that scales across devices
- Layout patterns for stacking and grid systems

TECHNICAL IMPLEMENTATION RULES:
- NEVER use direct colors in components
- ALWAYS use semantic tokens exclusively
- CREATE component variants instead of className overrides
- ENSURE accessibility compliance (WCAG AA)
- RESPECT prefers-reduced-motion for animations

OUTPUT REQUIREMENTS:
1. Complete index.css with semantic token system
2. tailwind.config.ts configuration
3. Component variant definitions
4. Animation keyframe library
5. Responsive design patterns
6. Color psychology explanation for chosen palette
7. Implementation guidelines and best practices
8. Quality checklist for design system compliance

Please analyze my project context and create a design system that reflects the appropriate brand personality while maintaining universal usability principles.
```

## Example Usage

**Input:**
```
Project type: B2B SaaS analytics platform
Target audience: Data analysts and business intelligence professionals
Brand personality: Professional, trustworthy, innovative, data-driven
Industry: Business intelligence and data analytics
```

## Sample Results

The prompt would generate:
1. **Color System**: Blue primary (trust/tech) with complementary orange accent for data visualization
2. **Semantic Tokens**: Complete CSS custom property system with HSL values
3. **Component Variants**: Professional button styles with subtle hover effects
4. **Animation Library**: Minimal, performance-focused animations
5. **Typography Scale**: Clean, readable hierarchy suitable for data-heavy interfaces
6. **Responsive Patterns**: Dashboard-optimized layouts with mobile considerations
7. **Implementation Guide**: Specific rules for maintaining design system integrity

## Advanced Features

### Color Psychology Integration
- Automatic color selection based on industry and brand personality
- Color harmony calculations using color theory principles
- Accessibility-compliant contrast ratio recommendations

### Component Variant System
- Systematic approach to creating variants instead of style overrides
- Consistent naming conventions across all components
- Extensible architecture for project-specific needs

### Performance Optimization
- Animation guidelines using transform/opacity for 60fps
- Semantic token architecture for minimal CSS bundle size
- Mobile-first responsive implementation

### Accessibility Standards
- WCAG AA compliance built into color system
- Focus state management for keyboard navigation
- Reduced motion support for accessibility preferences

## Notes

- This methodology adapts to any project type by analyzing context first
- Always start with semantic tokens before creating components
- Focus on systematic approaches rather than one-off customizations
- Consider both immediate needs and long-term scalability
- Test across different devices and accessibility tools