# Open Blog

<div align="center">
    <a href="CONTRIBUTING.md#creating-a-pull-request"><img src="https://img.shields.io/badge/PRs-welcome-brightgreen.svg" alt="PRs Welcome"></a>
    <a href="https://github.com/prettier/prettier"><img alt="code style: prettier" src="https://img.shields.io/badge/code_style-prettier-ff69b4.svg"></a>
    <a href="#license"><img src="https://img.shields.io/github/license/sourcerer-io/hall-of-fame.svg?colorB=ff0000"></a>
    <a href="https://vitest.dev/"><img src="https://img.shields.io/badge/tested_with-vitest-6E511F.svg" alt="Tested with Vitest"></a>
    <a href="https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fdvbtrung2302%2Fopen-blog%2Ftree%2Fmaster"><img src="https://vercel.com/button" alt="Deploy with Vercel"/></a>
</div>

A minimal, modern blog platform built with Next.js, Tailwind CSS, and MDX. Perfect for creators, developers, and writers
who want a lightweight, customizable blogging solution.

Just write your blog in Markdown format and ship it to everyone on the internet! ✨

- **Framework**: [Next.js 15](https://nextjs.org/) with App Router
- **Deployment**: [Vercel](https://vercel.com)
- **Styling**: [Tailwind CSS](https://tailwindcss.com)
- **Content**: MDX with metadata
- **Package Manager**: [pnpm](https://pnpm.io/)

<div align="center">
    <img src="https://github.com/user-attachments/assets/82d9f7c9-17e9-4754-96e6-d88b52745818" alt="Dark Mode" width="49%">
    <img src="https://github.com/user-attachments/assets/a7a47347-54aa-4ce0-9c06-0c94b439579e" alt="Light Mode" width="49%">
</div>

## Features

- 📝 Write posts in MDX format with YAML frontmatter
- ⚡ Fast performance with Next.js - all static HTML files, **100% Core Web Vitals**
- 🖼️ Dynamic Open Graph image generation
- 📰 Auto-generated RSS and Atom feeds
- 🗺️ Automatically generated sitemap
- 🔍 SEO-friendly with structured data (JSON-LD) and semantic HTML
- ♿ WCAG 2.2 accessibility compliant with proper semantic markup
- 🎨 Customizable author branding and social links
- 📱 Responsive lightweight design with light mode and dark mode based on system preference

## Getting Started

### Prerequisites

- Node.js v18.17 or higher
- pnpm (recommended) or npm

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/open-blog.git
   cd open-blog
   ```

2. Copy the environment template and fill in your details:

   ```bash
   cp .env.example .env.local
   ```

3. Edit `.env.local` with your personal information:

   ```env
   NEXT_PUBLIC_SITE_URL=https://yourblog.com/
   NEXT_PUBLIC_SITE_NAME=Your Blog Name
   NEXT_PUBLIC_SITE_DESCRIPTION=Your blog description
   NEXT_PUBLIC_AUTHOR_NAME=Your Name
   NEXT_PUBLIC_AUTHOR_EMAIL=your.email@example.com
   NEXT_PUBLIC_AUTHOR_IMAGE_URL=https://github.com/yourusername.png
   NEXT_PUBLIC_GITHUB_URL=https://github.com/yourusername/
   NEXT_PUBLIC_LINKEDIN_URL=https://www.linkedin.com/in/yourprofile/
   NEXT_PUBLIC_TWITTER_HANDLE=@yourhandle
   NEXT_PUBLIC_COPYRIGHT_YEAR=2025
   ```

4. Install dependencies:

   ```bash
   pnpm install
   ```

5. Start the development server:

   ```bash
   pnpm dev
   ```

   Open [http://localhost:3000](http://localhost:3000) to view your blog.

## Development Commands

```bash
# Start development server
pnpm dev

# Build for production
pnpm build

# Start production server
pnpm start

# Lint code
pnpm lint

# Format code
pnpm format
pnpm format:check
```

## Creating Blog Posts

1. Create a new directory in `app/blog/`:

   ```bash
   mkdir app/blog/my-first-post
   ```

2. Add a `page.mdx` file with frontmatter:

   ```mdx
   ---
   title: "My First Post"
   description: "A brief description of the post"
   date: 2024-01-15
   ---

   Your content here...
   ```

3. The post will automatically appear on your blog at `/blog/my-first-post/`

> **📚 Check out the [example blog post](/blog/building-blog-with-open-blog/) for a complete step-by-step guide on
creating your first post!**

### Syntax Highlighting

The blog uses **Shiki** for beautiful code syntax highlighting. Here are the features you can use in your code blocks:

#### Basic Code Block

````mdx
```javascript
console.log("Hello World");
```
````

#### Highlight a Single Line

Use `// [!code highlight]` comment to highlight the line:

````mdx
```javascript
function hello() {
  console.log("This line is highlighted"); // [!code highlight]
  console.log("Normal");
}
```
````

#### Highlight Multiple Lines

Use `// [!code highlight:N]` where N is the number of lines to highlight:

````mdx
```javascript
function hello() {
  console.log("Start highlighting"); // [!code highlight:3]
  console.log("This is highlighted");
  console.log("This is also highlighted");
  console.log("Normal");
}
```
````

#### Focus on Lines

Use `// [!code focus]` for a single line or `// [!code focus:N]` for multiple lines:

````mdx
```typescript
const [count, setCount] = useState(0); // [!code focus:2]
const [step, setStep] = useState(1);

export function formatDate(date: string) {
  return new Date(date).toLocaleDateString("en-US", { // [!code focus:3]
    year: "numeric",
    month: "short",
  });
}
```
````

#### Inline Code

Use backticks for inline code: `` `const x = 10;` ``

## License

MIT License - feel free to use this project for any purpose. Attribution is appreciated!

## Support

For issues, feature requests, or questions, please open an issue on GitHub.
