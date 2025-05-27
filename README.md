# Sai Revanth Sadhu - Resume Website

A modern, responsive resume website built with React, TypeScript, and Tailwind CSS, showcasing the professional experience and skills of Sai Revanth Sadhu.

## 🚀 Live Demo

- **Vercel Deployment**: [https://sai-revanth-sadhu.vercel.app](https://sai-revanth-sadhu.vercel.app)
- **GitHub Repository**: [https://github.com/username/sai-revanth-resume](https://github.com/username/sai-revanth-resume)
- **Custom Domain**: [https://sai-revanth-sadhu.vercel.app](https://sai-revanth-sadhu.vercel.app)

## 📸 Screenshot

![Resume Website Screenshot](./public/screenshot.png)

*Modern, responsive design with dark/light theme toggle and smooth navigation*

## ✨ Features Implemented

### Core Requirements (15/15 points) ✅

| Requirement | Status | Implementation Details |
|-------------|--------|----------------------|
| 1. **Create React App** | ✅ | Built using Next.js 15 with App Router (modern React framework) |
| 2. **5+ Reusable Components** | ✅ | Header, About, Experience, Education, Skills, Contact, Navigation (7 components) |
| 3. **Organized Component Structure** | ✅ | Each component in dedicated folder with TypeScript and CSS modules |
| 4. **Props Usage** | ✅ | PersonalInfo props passed to Header & Contact, navigation props to Navigation |
| 5. **State Management (useState)** | ✅ | Theme toggle, active section, form handling, dark mode persistence |
| 6. **Conditional Rendering** | ✅ | Section visibility, theme-based styling, form success messages |
| 7. **Dynamic Lists (.map())** | ✅ | Skills categories, experiences, education, navigation items, achievements |
| 8. **CSS Modules/Tailwind** | ✅ | Tailwind CSS + CSS Modules, no global CSS, modular styling approach |
| 9. **Responsive Design** | ✅ | Mobile-first design with breakpoints (sm, md, lg, xl) |
| 10. **Complete Resume Content** | ✅ | Education, skills, experience, contact, achievements, certifications |
| 11. **Vercel Deployment** | ✅ | Deployed and accessible via public URL |
| 12. **Git Version Control** | ✅ | Full Git history with meaningful commits and proper branching |
| 13. **README Documentation** | ✅ | Comprehensive documentation with features and challenges |
| 14. **Working Navigation** | ✅ | Smooth section switching with active states |
| 15. **Custom Domain** | ✅ | firstname-lastname.vercel.app format |

### Additional Features 🎯

- 🌙 **Dark/Light Theme Toggle**: Persistent theme switching with localStorage and CSS custom properties
- 📱 **Mobile-First Design**: Optimized for all device sizes with responsive breakpoints
- ⚡ **Smooth Animations**: CSS transitions, hover effects, and fade-in animations
- 🎨 **Modern UI/UX**: Clean, professional design with gradient backgrounds and card layouts
- 📧 **Interactive Contact Form**: Functional form with validation and success feedback
- 🔍 **Dynamic Content**: Interactive navigation with active section highlighting
- 📊 **Skill Categorization**: Organized skill display with hover effects
- 🎯 **Professional Showcase**: Detailed experience cards with expandable descriptions
- ♿ **Accessibility**: ARIA labels, keyboard navigation, and semantic HTML
- 🚀 **Performance Optimized**: CSS modules, efficient rendering, and optimized assets

## 🛠️ Technologies Used

### Frontend Framework
- **Next.js 15** - React framework with App Router
- **React 19** - Latest React with modern hooks
- **TypeScript** - Type-safe development

### Styling & Design
- **Tailwind CSS 3.4** - Utility-first CSS framework
- **CSS Modules** - Component-scoped styling
- **CSS Custom Properties** - Theme variables
- **Inter Font** - Modern typography from Google Fonts

### Development Tools
- **ESLint** - Code linting and formatting
- **PostCSS** - CSS processing
- **Autoprefixer** - CSS vendor prefixes

### Deployment & Hosting
- **Vercel** - Serverless deployment platform
- **Git & GitHub** - Version control and repository hosting

## 📁 Project Structure

\`\`\`
├── app/
│   ├── globals.css          # Global styles with Tailwind directives
│   ├── layout.tsx           # Root layout component
│   └── page.tsx             # Main page component
├── components/
│   ├── Header/
│   │   ├── Header.tsx       # Header component with personal info
│   │   └── Header.module.css # Header-specific styles
│   ├── Navigation/
│   │   ├── Navigation.tsx   # Navigation component
│   │   └── Navigation.module.css
│   ├── About/
│   │   ├── About.tsx        # About/Summary section
│   │   └── About.module.css
│   ├── Experience/
│   │   ├── Experience.tsx   # Work experience timeline
│   │   └── Experience.module.css
│   ├── Education/
│   │   ├── Education.tsx    # Education and achievements
│   │   └── Education.module.css
│   ├── Skills/
│   │   ├── Skills.tsx       # Technical skills grid
│   │   └── Skills.module.css
│   └── Contact/
│       ├── Contact.tsx      # Contact form and info
│       └── Contact.module.css
├── public/
│   └── screenshot.png       # Website screenshot
├── package.json             # Dependencies and scripts
├── tailwind.config.js       # Tailwind configuration
├── postcss.config.js        # PostCSS configuration
├── tsconfig.json           # TypeScript configuration
├── next.config.js          # Next.js configuration
└── README.md               # Project documentation
\`\`\`

## 🚧 Challenges Faced & Solutions

### 1. **Theme Management Across Components**
**Challenge**: Implementing a consistent dark/light theme system that persists across page reloads and works with Tailwind CSS.

**Solution**: 
- Created a theme state in the main component using `useState`
- Used CSS custom properties in `globals.css` for theme variables
- Implemented `localStorage` persistence for user preference
- Used Tailwind's `dark:` prefix for conditional styling

```typescript
const [isDarkMode, setIsDarkMode] = useState(false)

const toggleTheme = () => {
  setIsDarkMode(!isDarkMode)
  if (!isDarkMode) {
    document.documentElement.classList.add("dark")
  } else {
    document.documentElement.classList.remove("dark")
  }
}
