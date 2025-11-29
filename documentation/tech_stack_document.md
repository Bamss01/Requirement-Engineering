# Tech Stack Document

This document outlines the technology choices for the **Requirement-Engineering** repository. It explains each part of the tech stack in plain language to help everyone understand why we selected these tools and how they fit together.

## Frontend Technologies

Even though the project is documentation-focused, we treat the site that displays our content as a frontend application. Here are our main choices:

- **Docusaurus (React-based static site generator)**
  - Allows us to write content in Markdown and MDX, while providing a polished, searchable website.
  - Uses React under the hood, giving us flexibility to add custom components if needed.
  - Comes with a built-in theme for easy navigation, versioning, and search functionality.

- **Markdown & MDX**
  - Markdown is the simplest way to write formatted text. MDX extends Markdown, letting us embed React components directly in our docs.
  - Keeps content creation straightforward for non–technical contributors.

- **Tailwind CSS (utility-first styling)**
  - Enables fast, consistent styling through small, reusable classes.
  - Minimal CSS file size and easy theming to match our branding.

## Backend Technologies

Since this is a static documentation site, there’s no traditional server-side backend. However, we do rely on a few Node.js components to build and prepare our site:

- **Node.js**
  - Runs the build process for Docusaurus.
  - Manages dependencies via npm or yarn.

- **No database or server framework**
  - All pages are generated ahead of time, so we don’t need a live database or server framework.

## Infrastructure and Deployment

To keep the site reliable, easy to update, and automatically deployed, we use the following infrastructure tools:

- **GitHub for Version Control**
  - Hosts the repository and tracks changes.
  - Enables collaborative editing, pull requests, and code review.

- **GitHub Actions (CI/CD)**
  - Automatically runs tests and builds the site whenever we push changes.
  - Deploys the updated site after a successful build.

- **Hosting on GitHub Pages or Vercel**
  - **GitHub Pages**: Free, integrates directly with our repo. Serves our static site over HTTPS.
  - **Vercel** (optional): Provides automatic CDN distribution, instant rollbacks, and fast global performance.

## Third-Party Integrations

To enhance functionality without building from scratch, we integrate a few external services:

- **Algolia DocSearch**
  - Offers powerful, instant search across our documentation.
  - Easy to configure and keeps search indexing in sync with content updates.

- **Google Analytics**
  - Tracks user visits, popular pages, and engagement metrics.
  - Helps us understand what content is most valuable so we can improve it over time.

- **Syntax Highlighting (PrismJS)**
  - Automatically highlights code snippets in our examples.
  - Improves readability for any embedded code in tutorials or case studies.

## Security and Performance Considerations

Even for a static site, we take steps to keep our content safe and fast:

- **HTTPS Everywhere**
  - Both GitHub Pages and Vercel serve content over HTTPS by default, protecting data in transit.

- **Branch Protection Rules**
  - Prevent direct commits to the main branch.
  - Require reviews and passing CI checks before merging.

- **Automated Dependabot Alerts**
  - Monitors dependencies for known vulnerabilities.
  - Opens pull requests to update insecure packages.

- **Performance Optimizations**
  - **Pre-Rendering**: All pages are generated at build time, resulting in very fast page loads.
  - **CDN Caching**: Static assets are served from edge servers close to the user.
  - **Minified Assets**: CSS and JavaScript are automatically minimized in the build process.

## Conclusion and Overall Tech Stack Summary

Our choices focus on simplicity, speed, and clarity. By using a static site generator like Docusaurus, we keep content creation easy and accessible. Node.js handles our build process, while GitHub Actions and GitHub Pages (or Vercel) manage deployment and hosting. Integrations like Algolia and Google Analytics add powerful search and insights without added complexity. Finally, built-in security and performance features ensure our documentation site is safe, fast, and reliable.

This tech stack aligns with our goal of creating a well-structured, easy-to-maintain repository that serves as a comprehensive resource for Requirement Engineering, accessible to both technical and non-technical audiences.