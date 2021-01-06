# A statically generated blog example using Plasmic, Next.js and Markdown

This example showcases Next.js's [Static Generation](https://nextjs.org/docs/basic-features/pages) feature using Markdown files as the data source.

The blog posts are stored in `/_posts` as Markdown files with front matter support. Adding a new Markdown file in there will create a new blog post.

To create the blog posts we use [`remark`](https://github.com/remarkjs/remark) and [`remark-html`](https://github.com/remarkjs/remark-html) to convert the Markdown files into an HTML string, and then send it down as a prop to the page. The metadata of every post is handled by [`gray-matter`](https://github.com/jonschlinkert/gray-matter) and also sent in props to the page.

## Demo

[https://next-blog-starter.vercel.app/](https://next-blog-starter.vercel.app/)

## Deploy your own

Deploy the example using [Vercel](https://vercel.com?utm_source=github&utm_medium=readme&utm_campaign=next-example):

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/import/git?c=1&s=https://github.com/vercel/next.js/tree/canary/examples/blog-starter)

### Related examples

- [WordPress](/examples/cms-wordpress)
- [DatoCMS](/examples/cms-datocms)
- [Sanity](/examples/cms-sanity)
- [TakeShape](/examples/cms-takeshape)
- [Prismic](/examples/cms-prismic)
- [Contentful](/examples/cms-contentful)
- [Strapi](/examples/cms-strapi)
- [Agility CMS](/examples/cms-agilitycms)
- [Cosmic](/examples/cms-cosmic)
- [ButterCMS](/examples/cms-buttercms)
- [Storyblok](/examples/cms-storyblok)
- [GraphCMS](/examples/cms-graphcms)
- [Kontent](/examples/cms-kontent)

## 🚀 Quick start

1.  **Create a Next.js site.**

    Execute [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app) with [npm](https://docs.npmjs.com/cli/init) or [Yarn](https://yarnpkg.com/lang/en/docs/cli/create/) to bootstrap the example:

    ```bash
    yarn create next-app --example https://github.com/plasmicapp/nextjs-starter-blog blog-starter-app
    # or
    npx create-next-app --example https://github.com/plasmicapp/nextjs-starter-blog blog-starter-app

    cd blog-starter-app/
    ```

1. **Clone the Starter Blog Plasmic project**

    Log into [Plasmic](https://studio.plasmic.app/?starters=site-builder)
    and clone the "Starter blog" project into your own workspace.
    When you do, note the `PROJECT_ID` in the URL (e.g. `https://studio.plasmic.app/projects/PROJECT_ID`).
    Please check that you have write-access to the project,
    otherwise you may be referencing read-only components.

1. **Configure PlasmicLoader.**

    Open `next.config.js` and update the plugin configuration for `@plasmicapp/loader`
    with the project ID of your copy of Starter Blog.

    ```json
    const plasmic = require("@plasmicapp/loader/next");
    const withPlasmic = plasmic({
      dir: __dirname, // The root directory of your project.
      projectIds: ["some-project-id"], // An array of project ids.
    });

    module.exports = withPlasmic({
      // Your NextJS config.
    });
    ```

## How to use

Your blog should be up and running on [http://localhost:3000](http://localhost:3000)! If it doesn't work, post on [GitHub discussions](https://github.com/vercel/next.js/discussions).

Deploy it to the cloud with [Vercel](https://vercel.com/import?filter=next.js&utm_source=github&utm_medium=readme&utm_campaign=next-example) ([Documentation](https://nextjs.org/docs/deployment)).

# Notes

This blog-starter uses [Tailwind CSS](https://tailwindcss.com). To control the generated stylesheet's filesize, this example uses Tailwind CSS' v2.0 [`purge` option](https://tailwindcss.com/docs/controlling-file-size/#removing-unused-css) to remove unused CSS.
