# Animated GitHub Profile 🎨

A stunning, fully animated GitHub profile website with dark/light theme support, smooth animations, and modern glassmorphism design. Built with Next.js 16, React 19, Tailwind CSS, and Lucide React icons.

## Features

### ✨ Animations
- **Fade-in & Slide animations** on page load and scroll
- **Floating background blob** with particle effects
- **Rotating tech stack cards** with hover scale effects
- **Glowing text effects** on headings
- **Typewriter role cycler** with cursor blink animation
- **Pulsing badges** and animated navigation dots
- **Smooth transitions** between theme changes
- **Staggered animations** for sequential element reveals

### 🎨 Theme System
- **Dark Mode** (default): Professional dark background with cyan/purple accents
- **Light Mode**: Clean white background with vibrant colors
- **Persistent Storage**: Theme preference saved to localStorage
- **Smooth Transitions**: All colors transition smoothly when switching themes

### 📱 Responsive Design
- Mobile-first approach
- Fully responsive for all screen sizes
- Navigation dots hidden on mobile (visible on lg screens and up)
- Touch-friendly interactive elements

### 🛠 Tech Stack
Built with modern technologies:
- **Next.js 16**: React framework with App Router
- **React 19**: Latest React features and optimizations
- **Tailwind CSS v4**: Utility-first CSS framework
- **Lucide React**: Beautiful icon library
- **TypeScript**: Type-safe component development

## Project Structure

```
.
├── app/
│   ├── layout.tsx          # Root layout with theme meta tags
│   ├── page.tsx            # Main page component
│   └── globals.css         # Global styles and animations
├── components/
│   ├── ThemeToggle.tsx      # Dark/light theme switcher button
│   ├── AnimatedBackground.tsx # Floating blob background
│   ├── HeroSection.tsx      # Main hero with intro and CTA
│   ├── AboutSection.tsx     # About me section with feature cards
│   ├── TechStack.tsx        # Technology cards grid
│   ├── Projects.tsx         # Featured projects showcase
│   └── Contact.tsx          # Contact section with social links
├── lib/
│   └── utils.ts            # Utility functions (cn helper)
├── public/                 # Static assets
└── package.json            # Dependencies
```

## Components Overview

### **ThemeToggle.tsx**
Renders a sun/moon icon button in the top-right corner to switch between dark and light themes. Saves preference to localStorage and updates the `data-theme` attribute on the HTML element.

**Props:**
- `theme`: Current theme ('dark' or 'light')
- `toggleTheme`: Callback function to change theme

### **AnimatedBackground.tsx**
Creates an animated gradient background with floating blob elements. Uses CSS animations for continuous motion and positioning utilities for responsive layout.

**Features:**
- Floating animated blobs
- Gradient background
- Responsive sizing
- Fixed positioning for parallax effect

### **HeroSection.tsx**
Main landing section featuring:
- Animated greeting message
- Typewriter-effect role display (cycles through developer roles)
- Professional introduction text
- Call-to-action buttons (View Work, Get in Touch)
- Animated scroll indicator

**Animation Details:**
- Text animates in on page load
- Role rotates every 3 seconds
- Buttons have hover scale effects
- Scroll arrow bounces continuously

### **AboutSection.tsx**
"About Me" section with:
- Animated section title
- Feature cards (Clean Code, Performance, User-Focused)
- Description text
- Staggered card animations on scroll

**Animation Details:**
- Cards fade in from left/right
- Hover effects scale and glow
- Smooth color transitions
- Glass-morphism design

### **TechStack.tsx**
Grid of technology cards featuring:
- 12+ tech stack items (Python, JavaScript, React, etc.)
- Tech icons (emoji or Lucide icons)
- Rotating animation on hover
- Color-coded categories

**Tech Categories:**
- Languages
- Frontend
- Backend
- Tools & Deployment

### **Projects.tsx**
Featured projects showcase with:
- Project cards with gradient borders
- Project descriptions and tech tags
- Live demo and GitHub code buttons
- Hover animations and scale effects

**Default Projects:**
- E-commerce Platform
- Task Management App
- Analytics Dashboard
- Social Media Platform

### **Contact.tsx**
Contact section featuring:
- Email contact box
- Social media links (LinkedIn, GitHub, Email)
- Contact form with validation
- Animated social icons with hover effects

## Animation Classes

All custom animations are defined in `globals.css` and available as Tailwind utilities:

| Animation | Class | Description |
|-----------|-------|-------------|
| Fade In Up | `animate-fade-in-up` | Element fades in and slides up |
| Slide Left | `animate-slide-in-left` | Element slides in from left with fade |
| Slide Right | `animate-slide-in-right` | Element slides in from right with fade |
| Glow | `animate-glow` | Box shadow glows in and out |
| Float | `animate-float` | Element floats up and down continuously |
| Pulse Glow | `animate-pulse-glow` | Opacity pulses smoothly |
| Rotate 360 | `animate-rotate-360` | Element rotates continuously |
| Shimmer | `animate-shimmer` | Shimmer effect across element |
| Gradient Shift | `animate-gradient-shift` | Background gradient shifts continuously |
| Typewriter | `animate-typewriter` | Text types out character by character |
| Blink | `animate-blink` | Cursor blinks on and off |

## Theme System

### CSS Variables (globals.css)

**Dark Theme (default):**
```css
--background: #0f0f0f
--foreground: #fafafa
--primary: #36bcf7 (Sky Blue)
--primary-dark: #0ea5e9
--accent: #9d4edd (Purple)
--accent-light: #c77dff
--surface: #1a1a1a
--surface-hover: #2a2a2a
--border: #333333
--muted: #666666
```

**Light Theme:**
```css
--background: #ffffff
--foreground: #0f0f0f
--primary: #0ea5e9
--primary-dark: #0284c7
--accent: #7c3aed
--accent-light: #a78bfa
--surface: #f5f5f5
--surface-hover: #e8e8e8
--border: #e0e0e0
--muted: #999999
```

### How Theme System Works

1. **Initial Load**: App checks localStorage for saved theme preference
2. **Toggle**: User clicks theme button
3. **Update**: HTML element's `data-theme` attribute changes
4. **CSS Application**: CSS selectors `[data-theme='dark']` and `[data-theme='light']` apply correct colors
5. **Persistence**: New theme preference saved to localStorage

## Customization Guide

### Change Personal Information

**Update HeroSection.tsx:**
```tsx
// Line 15: Change greeting
const greeting = "Hi, I'm [Your Name]";

// Line 17: Update roles
const roles = ["Full Stack Developer", "Your Role", "Another Role"];

// Line 19: Update description
const description = "Your professional description here";
```

**Update AboutSection.tsx:**
```tsx
// Line 15-20: Customize feature cards
const features = [
  { icon: '✨', title: 'Your Feature', description: 'Your description' },
  // ...
];
```

### Customize Tech Stack

**Edit TechStack.tsx (lines 8-40):**
```tsx
const technologies = [
  { name: 'Python', emoji: '🐍', category: 'Languages' },
  { name: 'Your Tech', emoji: '⚡', category: 'Your Category' },
  // Add or remove technologies
];
```

### Add or Modify Projects

**Edit Projects.tsx (lines 8-50):**
```tsx
const projects = [
  {
    title: 'Your Project',
    description: 'Project description',
    tags: ['React', 'Node.js', 'MongoDB'],
    image: '/project-image.png',
    link: 'https://project-link.com',
    github: 'https://github.com/your-repo'
  },
  // Add more projects
];
```

### Update Social Links

**Edit Contact.tsx (lines 18-21):**
```tsx
const socialLinks = [
  { icon: Briefcase, href: 'YOUR_LINKEDIN_URL', label: 'LinkedIn', color: 'hover:text-blue-400' },
  { icon: Code, href: 'YOUR_GITHUB_URL', label: 'GitHub', color: 'hover:text-gray-300' },
  { icon: Mail, href: 'mailto:YOUR_EMAIL@example.com', label: 'Email', color: 'hover:text-purple-400' },
];
```

### Change Colors

**Edit globals.css (lines 4-20):**

Update CSS variables in the `:root` selector for dark theme and `[data-theme='light']` selector for light theme:

```css
:root {
  --primary: #36bcf7;        /* Main accent color */
  --accent: #9d4edd;         /* Secondary accent */
  --surface: #1a1a1a;        /* Card background */
}
```

### Modify Animations

**Edit globals.css (lines 25-120):**

Example - Change fade-in-up animation duration:
```css
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade-in-up {
  @apply animate-[fadeInUp_0.8s_ease-out]; /* Change 0.6s to 0.8s */
}
```

## Installation & Setup

### Prerequisites
- Node.js 18+ 
- npm, yarn, pnpm, or bun

### Local Development

1. **Clone or download the project**

2. **Install dependencies:**
```bash
pnpm install
# or
npm install
# or
yarn install
```

3. **Run development server:**
```bash
pnpm dev
# or
npm run dev
```

4. **Open in browser:**
Navigate to [http://localhost:3000](http://localhost:3000)

5. **Make changes:**
- Edit component files and see changes in real-time
- Update content in individual component files
- Modify animations in `globals.css`

### Build for Production

```bash
pnpm build
pnpm start
```

## Deployment

### Deploy to Vercel (Recommended)

1. **Push to GitHub**
2. **Connect to Vercel:**
   - Visit [vercel.com](https://vercel.com)
   - Click "Add New" → "Project"
   - Select your GitHub repository
   - Click "Deploy"

3. **Add custom domain** (optional)
   - Go to project settings
   - Add your custom domain

### Deploy to Other Platforms

**Netlify:**
```bash
pnpm build
# Upload the `.next` folder
```

**AWS Amplify, GitHub Pages, etc.:** Follow their Next.js deployment guides

## Performance Optimization

- **CSS animations**: GPU-accelerated with `transform` and `opacity`
- **Code splitting**: Automatic with Next.js 16
- **Image optimization**: Use Next.js Image component
- **Font loading**: Web fonts are optimized
- **Lazy loading**: Components load on demand

## Browser Support

- Chrome/Edge 90+
- Firefox 88+
- Safari 14+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Accessibility

- Semantic HTML elements (`<main>`, `<section>`, `<header>`)
- Screen reader text with `.sr-only` class
- Keyboard navigation support
- Color contrast meets WCAG AA standards
- Alt text for images

## Troubleshooting

### Theme not persisting
- Clear browser localStorage and cache
- Check that `data-theme` attribute is on `<html>` element

### Animations not playing
- Verify `globals.css` is properly imported
- Check that Tailwind CSS is configured correctly
- Ensure GPU acceleration is enabled in browser

### Icons not showing
- Verify `lucide-react` is installed: `npm list lucide-react`
- Check icon names are correct (case-sensitive)

## File Size & Performance

- **Build size**: ~150-200KB (optimized)
- **Animations**: GPU-accelerated, 60 FPS on modern devices
- **Core Web Vitals**: Optimized for LCP, CLS, and INP

## Technologies Used

| Technology | Purpose |
|-----------|---------|
| Next.js 16 | React framework with routing |
| React 19 | UI components and state |
| TypeScript | Type-safe development |
| Tailwind CSS v4 | Styling and animations |
| Lucide React | Icons |
| CSS Animations | Smooth effects |

## Future Enhancements

- Add animation preferences (reduce-motion)
- Blog section with animated posts
- Downloadable resume PDF
- Real-time visitor counter
- Analytics integration
- Email notification system

## License

MIT License - Feel free to use this project for personal or commercial purposes.

## Support

For issues or questions:
1. Check the Troubleshooting section
2. Review component comments for implementation details
3. Visit [Next.js Documentation](https://nextjs.org/docs)
4. Check [Tailwind CSS Docs](https://tailwindcss.com/docs)

## Credits

- Built with **Next.js** and **React**
- Styled with **Tailwind CSS**
- Icons from **Lucide React**
- Animations with **CSS**

---

**Made with ❤️ for beautiful web experiences**

## Quick Reference

### Add new animation
1. Define keyframes in `globals.css`
2. Create utility class in `@layer utilities`
3. Use `animate-[name]` on elements

### Add new component
1. Create `.tsx` file in `components/`
2. Use client/server component directives
3. Import in `app/page.tsx`
4. Add animations and styling

### Change theme colors
1. Edit CSS variables in `globals.css`
2. Update both `:root` (dark) and `[data-theme='light']` selectors
3. Colors automatically update across all components

### Deploy changes
1. Commit and push to GitHub
2. Vercel auto-deploys on push
3. View live changes immediately
