# Multi-Video Hero 🎬✨

An interactive, scroll-driven hero media expansion component built with **Next.js 14**, **React**, **TypeScript**, **Framer Motion**, and **Tailwind CSS**. 

Transform your landing pages with an immersive experience where videos and images smoothly scale from a framed showcase card to a full-screen canvas as users scroll or swipe.

---

## 🌟 Features

- **Interactive Scroll & Gesture Expansion**
  - Buttery-smooth expansion from a compact framed card to a full-screen immersive media canvas based on user scroll progress.
  - Seamless touch gesture controls for mobile devices (`touchstart`, `touchmove`, `touchend`).
  - Native wheel listener integration with smart edge-locking and smooth delta scaling.

- **Dual Media Mode (Video & Image)**
  - **Video Hero**: Supports self-hosted MP4/WebM videos, CDN-streamed videos, and YouTube embeds with automatic autoplay, loop, mute, and UI cleanups.
  - **Image Hero**: Optimized static and dynamic images using Next.js `<Image />` with custom aspect ratio preservation and blur/poster transitions.

- **Kinetic Typography & Dynamic Text Blending**
  - Animated split-title headers that fluidly translate across the screen in sync with the user's scroll.
  - Optional `textBlend` mode creating stunning layered contrast between foreground typography and background media.
  - Customizable metadata badges (e.g. date, category tag, "Scroll to Expand" prompt).

- **Rich Content Reveal**
  - Smoothly reveals children content and narrative sections once the media has expanded, creating natural visual storytelling.

- **Responsive & Mobile-Optimized**
  - Dynamic scaling curves that automatically adapt between mobile (`< 768px`) and desktop viewports.

---

## 🛠️ Tech Stack

- **Framework**: [Next.js 14 (App Router)](https://nextjs.org/)
- **UI Library**: [React 18](https://react.dev/)
- **Language**: [TypeScript](https://www.typescriptlang.org/)
- **Animations**: [Framer Motion](https://www.framer.com/motion/)
- **Styling**: [Tailwind CSS](https://tailwindcss.com/)
- **Utility**: `clsx`, `tailwind-merge`

---

## 📁 Project Structure

```text
multi-video-hero/
├── public/                     # Static media and hero image assets
│   └── assets/                 # Demo hero backgrounds and posters
├── src/
│   ├── app/
│   │   ├── favicon.ico
│   │   ├── globals.css         # Tailwind base and global style rules
│   │   ├── layout.tsx          # Root HTML layout & font definitions
│   │   └── page.tsx            # Main showcase entry point
│   ├── components/
│   │   └── ui/
│   │       ├── demo.tsx        # Interactive demo controller with toggle controls
│   │       └── scroll-expansion-hero.tsx  # Core ScrollExpandMedia component
│   └── lib/
│       └── utils.ts            # Class merge helper utilities
├── .gitignore
├── next.config.js
├── package.json
├── tailwind.config.js
└── tsconfig.json
```

---

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed:
- **Node.js**: `v18.17.0` or higher
- **npm**, **yarn**, **pnpm**, or **bun**

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/girishlade111/multi-video-hero.git
   cd multi-video-hero
   ```

2. Install dependencies:
   ```bash
   npm install
   # or
   yarn install
   # or
   pnpm install
   # or
   bun install
   ```

3. Start the development server:
   ```bash
   npm run dev
   ```

4. Open your browser and navigate to:
   ```text
   http://localhost:3000
   ```

---

## 💻 Usage & Examples

### Basic Component Usage

Import and use `ScrollExpandMedia` in any React component or Next.js page:

```tsx
import ScrollExpandMedia from "@/components/ui/scroll-expansion-hero";

export default function HeroSection() {
  return (
    <ScrollExpandMedia
      mediaType="video"
      mediaSrc="https://assets.example.com/hero-video.mp4"
      posterSrc="https://assets.example.com/poster.jpg"
      bgImageSrc="/assets/hero-bg.png"
      title="Cosmic Exploration"
      date="Featured Project"
      scrollToExpand="Scroll to Expand"
      textBlend={true}
    >
      <div className="max-w-4xl mx-auto py-12 px-6">
        <h2 className="text-3xl font-bold mb-4">About the Experience</h2>
        <p className="text-lg text-gray-700 dark:text-gray-300">
          Content placed here will gracefully fade in once the user completes the expansion scroll.
        </p>
      </div>
    </ScrollExpandMedia>
  );
}
```

### Component Props Reference (`ScrollExpandMediaProps`)

| Prop | Type | Default | Description |
| :--- | :--- | :--- | :--- |
| `mediaType` | `'video' \| 'image'` | `'video'` | Determines whether to render a video player or an image. |
| `mediaSrc` | `string` | *(Required)* | URL or local path to video (MP4/WebM/YouTube) or image. |
| `posterSrc` | `string` | `undefined` | Thumbnail/poster image displayed while the video loads. |
| `bgImageSrc` | `string` | *(Required)* | Background image that fades out smoothly as media expands. |
| `title` | `string` | `undefined` | Hero title text with dynamic split-word kinetic translation. |
| `date` | `string` | `undefined` | Small header tag/badge above the main title. |
| `scrollToExpand` | `string` | `undefined` | Bottom prompt indicating scroll action to the visitor. |
| `textBlend` | `boolean` | `false` | Enables mix-blend typography styling for high-contrast effects. |
| `children` | `ReactNode` | `undefined` | Content revealed beneath the media once fully expanded. |

---

## 🎨 Presets & Variants

The demo includes ready-to-use variants exported from `@/components/ui/demo`:

- **`VideoExpansionTextBlend`**: Video hero with kinetic text blending.
- **`ImageExpansionTextBlend`**: High-resolution image showcase with text blending.
- **`VideoExpansion`**: Clean video expansion without text blending overlays.
- **`ImageExpansion`**: Clean image expansion ideal for photography portfolios.

---

## 📜 Scripts

| Script | Command | Description |
| :--- | :--- | :--- |
| `dev` | `npm run dev` | Runs the Next.js development server on `http://localhost:3000` |
| `build` | `npm run build` | Compiles and optimizes the app for production |
| `start` | `npm run start` | Runs the compiled production build |
| `lint` | `npm run lint` | Runs ESLint to check for code quality and syntax issues |

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the [issues page](https://github.com/girishlade111/multi-video-hero/issues).

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'feat: add some amazing feature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License.

---

## 👤 Author

**Built by Girish Lade** — [ladestack.in](https://ladestack.in)
