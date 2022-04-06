<h1 align="center">
  Gatsby Starter MiniBlog
</h1>

Typography driven, feature-rich blogging theme with minimal aesthetics. Includes tags/categories support and extensive features for code blocks such as live preview, line numbers, and line highlighting. Using the Gatsby Theme [`@lekoarts/gatsby-theme-minimal-blog`](https://github.com/LekoArts/gatsby-themes/tree/main/themes/gatsby-theme-minimal-blog).

## ✨ Features

- MDX
- Fully customizable through the usage of Gatsby Themes (and Theme UI)
- Light Mode / Dark Mode
- Typography driven, minimal style
- Tags/Categories support
- Code highlighting with [prism-react-renderer](https://github.com/FormidableLabs/prism-react-renderer) and [react-live](https://github.com/FormidableLabs/react-live) support. Also allows adding line numbers, line highlighting, language tabs, and file titles.
- RSS Feed for blog posts
- SEO (Sitemap, OpenGraph tags, Twitter tags)
- WebApp Manifest

## 🚀 Installation

```sh
npm install --legacy-peer-deps
npm run develop
```

The site is now running at `http://localhost:8000`!

## 📝 Using and modifying this starter

### Adding content

#### Adding a new blog post

New blog posts will be shown on the index page (the three most recent ones) of this theme and on the blog overview page. They can be added by creating MDX files inside `content/posts`. General setup:

1. Create a new folder inside `content/posts`
1. Create a new `index.mdx` file, and add the frontmatter
1. Add images to the created folder (from step 1) you want to reference in your blog post
1. Reference an image as your `banner` in the frontmatter
1. Write your content below the frontmatter
1. Add a `slug` to the frontmatter to use a custom slug, e.g. `slug: "/my-slug"` (Optional)
1. Use `defer` to opt-in into Deferred Static Generation (DSG) (optional)

**Frontmatter reference:**

```md
---
title: Introduction to "Defence against the Dark Arts"
date: 2019-11-07
description: Defence Against the Dark Arts (abbreviated as DADA) is a subject taught at Hogwarts School of Witchcraft and Wizardry and Ilvermorny School of Witchcraft and Wizardry.
defer: false
tags:
  - Tutorial
  - Dark Arts
banner: ./defence-against-the-dark-arts.jpg
canonicalUrl: https://random-blog-about-curses.com/curses-counter-curses-and-more
---
```

**The fields `description`, `banner`, `defer` and `canonicalUrl` are optional!** If no description is provided, an excerpt of the blog post will be used. If no banner is provided, the default `siteImage` (from `siteMetadata`) is used. If no `canonicalUrl` is provided, it will not be included in the header.

The `date` field has to be written in the format `YYYY-MM-DD`!

#### Adding a new page

Additional pages can be created by placing MDX files inside `contents/pages`, e.g. an "About" or "Contact" page. You'll manually need to link to those pages, for example by adding them to the navigation (in `siteMetadata`). General instructions:

1. Create a new folder inside `content/pages`
1. Create a new `index.mdx` file, and add the frontmatter
1. Write your content below the frontmatter
1. Optionally add files/images to the folder you want to reference from the page
1. Use `defer` to opt-in into Deferred Static Generation (DSG) (optional)

**Frontmatter reference:**

```md
---
title: About
slug: "/about"
defer: false
---
```

### Changing the "Hero" text

To edit the hero text ("Hi, I'm Lupin...), create a file at `src/@lekoarts/gatsby-theme-minimal-blog/texts/hero.mdx` to edit the text.

### Changing the "Projects" part

To edit the projects part below "Latest posts", create a file at `src/@lekoarts/gatsby-theme-minimal-blog/texts/bottom.mdx` to edit the contents.

### Extending the footer of the post

Inside the [`<Post />` component](https://github.com/LekoArts/gatsby-themes/blob/main/themes/gatsby-theme-minimal-blog/src/components/post.tsx) there's also a `<PostFooter />` component that you can shadow to display elements between the end of the post and the global footer. By default it returns `null`. Create a file at `src/@lekoarts/gatsby-theme-minimal-blog/components/post-footer.jsx` to edit this section. The `<PostFooter />` component receives the complete `post` prop that `<Post />` also receives.

## License

Licensed under the [CC0-1.0](LICENSE) license.
