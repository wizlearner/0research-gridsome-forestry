<p align="center">
  <a style="padding-right: 16px;" href="https://forestry.io">
    <img src="https://app.forestry.io/assets/forestry-logotype-pos-c71a6bd237d9199d0457ba2811553997ff5bab0d2cd0e740686ab26c00d9c240.svg" width="112" height="28">
  </a>
  <a href="https://gridsome.org/">
    <img src="/static/gridsome-logo.svg" width="112" height="28">
  </a>
</p>
<h1 align="center">
  Brevifolia
</h1>

## About

[![Netlify Status](https://api.netlify.com/api/v1/badges/314f6fb1-b4a6-484a-ad3d-c26663a63bca/deploy-status)](https://app.netlify.com/sites/brevifolia-gridsome-forestry/deploys)

Brevifolia is minimalist blog starter to get you going using [Forestry](https://forestry.io/) with [Gridsome](https://gridsome.org). Check out the demo [here](https://brevifolia-gridsome-forestry.netlify.com/)

This blog is statically generated by Gridsome, a rendered combination of Vue components and markdown files. It is preconfigured to work with Forestry as a way to manage your content. Forestry makes changes by editing markdown or data files, uploading media to the correct directory and committing these updates to your repo directly.

The styles were coded & designed by yours truly, using [scss](https://sass-lang.com/) with the [Gridsome style](https://gridsome.org/docs/assets-css) structure. The font used is [Work Sans](https://fonts.google.com/specimen/Work+Sans). 

##  Quick Setup

#### *Import Directly to Forestry*

<a href="https://app.forestry.io/quick-start?repo=kendallstrautman/brevifolia-gridsome-forestry&engine=other">
    <img alt="Import this project into Forestry" src="https://assets.forestry.io/import-to-forestryK.svg" />
</a>

#### *Using the Gridsome CLI*
TBD...
#### *Set-up Locally*
In your terminal, navigate to where you would like this blog to live, then run 
```bash
#clone the repo
git clone git@github.com:kendallstrautman/brevifolia-gridsome-forestry.git

#navigate to the directory
cd brevifolia-gridsome-forestry

#install dependencies & run dev server with yarn 
yarn install
yarn dev

#or with npm 
npm install
npm run dev
```
A new browser window should open with the dev server running or you can navigate to localhost:8080 

### Plugins

With Gridsome offering a plugin-rich ecosystem, there are a few key plugins that make this project possible. 

- [Gridsome Source Filesystem](https://gridsome.org/plugins/@gridsome/source-filesystem) transforms local project files into content that can be fetched with GraphQL in the components.
- [Grisome Transformer Remark](https://gridsome.org/plugins/@gridsome/transformer-remark) transforms markdown files.

## Project Structure 

- Site-level configuration is stored in `src/assets/config.json`. This file is loaded in the `gridsome.config.js` to configure Gridsome and all it to be accessible via metaData in your graphql queries.
- Add and access plugin options or metaData via `gridsome.config.js`.
- Access Gridsome's [server api](https://gridsome.org/docs/server-api) via `gridsome.server.js`. Currently this is just boilerplate. 
- Edit global & reset styles via `src/assets/styles/...`. Edit styles specific to a page or component within the `.vue` file between the `<style>` tags
- `src/assets/content/`contains all your markdown blog posts, images & data files (e.g. authors list, info page data). These are all editable by Forestry. 
- `src/pages` is a very important and required directory for Gridsome. This is where all your pages for the site live. 
- Blog posts are built from a template that can be accessed at `src/templates`. The routing and config for this template lives in `gridsome.config.js` within the `@gridsome/source-filesystem` plugin object.
- The pages & template are comprised of components from `src/components`.

## Using Forestry as your CMS

The `.forestry` directory contains all the settings information and frontmatter configuration to allow Forestry to setup the sidebar structure and editing capacity for this blog. After importing this blog into forestry, you can [access and edit](https://forestry.io/docs/editing/) all of the content via the sidebar. 

You can add new blog posts, [data files](https://forestry.io/docs/editing/data-files/), or entire pages and sections to fit your needs. You can also [customize how media](https://forestry.io/docs/media/) is handled, by configurating gitLFS, Cloudinary, S3, or Netlify Large Media.

You can set up a [remote admin](https://forestry.io/docs/editing/remote-admin/) for content editors to log in directly to yoururl.com/admin to make content updates.

### Instant Previews

The [instant preview](https://forestry.io/docs/previews/instant-previews/) method spins up the Gatsby development server for a long-lived preview that can quickly respond to content updates. When using instant previews, your preview command should be the develop command. The development server spawned by this command should be available over port 8080, and bind to 0.0.0.0. The forestry:preview command in this project's package.json will spin up a Gatsby dev server compatible with Forestry's instant previews.

## Deploy Options

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/kendallstrautman/brevifolia-gridsome-forestry)

[Netlify](https://www.netlify.com/blog/2016/09/29/a-step-by-step-guide-deploying-on-netlify/) is a great way to easily deploy sites. There's no special setup you need to do with Forestry to deploy with Netlify. When Forestry makes commits to your repo, Netlify will auto-trigger a rebuild / deploy when new commits are made.
