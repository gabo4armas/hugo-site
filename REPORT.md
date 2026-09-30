# Report

## Approach

This was my first time using Hugo, so I started with the official Quick Start and the
documentation on directory structure, content organization, menus and templates
in the link: gohugo.io/documentation. Also I used Gemini and Claude AI to understand better how to créate the page and adjust the style of it. Then, I decided to write a small custom layout instead of using a theme, to keep the project simple and to understand what each piece does. 
Steps:

1. Installed Hugo and created the site skeleton (`hugo.toml`, `content/`, `layouts/`).
2. Set a custom site title and a main menu (Home, Posts, About) in `hugo.toml`.
3. Wrote the content in Markdown: home page, About page, and two short posts.
4. Created the templates: `baseof.html` (page skeleton), `index.html` (home with
latest posts), `single.html` (pages/posts), `list.html` (posts listing), and
`header`/`footer` partials that render the navigation from the menu config.
5. Added a small CSS file (responsive, with dark mode support).

## Problems encountered and how I solved them

* **Blank Page Error:**
  - The initial build warned that no layout was found to render the home page, so I implemented `layouts/index.html` and proper `_default` fallbacks, ensuring Hugo's lookup order resolves root and section content.

* **Draft and Future Date Filtering:**
  - One of the blog posts did not render when running the local server. Using Claude AI, I identified that Hugo automatically ignores future dated content or posts with `draft: true`[cite: 1]. Corrected the front matter metadata (`draft: false` and current timestamp) to ensure standard visibility.

## How I verified it works

* Ran `hugo server` and opened http://localhost:1313/ - no errors or warnings in the terminal.
* Checked that Home, Posts and About links work from every page.
* Checked that both posts appear on the home page and in the Posts list, and open correctly.
* Confirmed the custom title appears in the header and browser tab.
* Ran `hugo` to confirm the production build succeeds and generates `public/`.
* Checked the layout on different windows sizes.

## Use of AI tools

I used Claude and Gemini to help draft the initial project structure, templates, sample content and the README/REPORT text. I then ran the project locally, reviewed each file to understand what it does, tested and adjusted it myself.

