---
title: 'First post'
description: 'Getting started with Astro and Cloudflare'
pubDate: 'September 23 2026'
heroImage: '../../assets/blog-placeholder-3.jpg'
---

Steps in setting up this blog:

1. Install npm

Check version

node -v
(v24.18.0)

npm -v
(11.16.0)

2. Install npx

Create ./jottings folder with Cloudflare and Astro framework

Directory: ./jottings
Start with: Framework Starter
Development Framework: Astro
Deployment Platform: Pages

npx create-astro@5.2.4 jotttings --no-install --no-git

Package installed: create-astro@5.2.4

Use blog template

npm create cloudflare@latest -- jottings --framework=astro --platform=pages

├ Copying template files
│ files copied to project directory
│
├ Installing dependencies
│ installed via `npm install`
│
╰ Application created

╭ Configuring your application for Cloudflare Step 2 of 3
│
├ Installing wrangler A command line tool for building Cloudflare Workers
│ installed via `npm install wrangler --save-dev`
│
├ Selecting workerd compatibility date
│ compatibility date 2026-09-21
│
├ Installing adapter
│ installed via `npx astro add cloudflare`
│
├ Updating configuration in astro.config.mjs
│
├ Adding Wrangler files to the .gitignore file
│ updated .gitignore file
│
├ Updating `package.json` scripts
│ updated `package.json`
│
├ Generating types for your application
│ generated to `./worker-configuration.d.ts` via `npm run cf-typegen`
│
├ Installing @types/node
│ installed via npm
│
├ Do you want to use git for version control?
│ yes git
│
├ Initializing git repo
│ initialized git


├ git commit
│
╰ Application configured

╭ Deploy with Cloudflare Step 3 of 3
│
├ Do you want to deploy your application?
│ yes deploy via `npm run deploy`
│
├ Logging into Cloudflare checking authentication status
│ not logged in
│
├ Logging into Cloudflare This will open a browser window
│ allowed via `wrangler login`
│
├ Selecting Cloudflare account retrieving accounts
│ account Simon.fermor@gmail.com's Account
│
├ Creating Pages project
│ created via `npx wrangler pages project create jottings --production-branch main`
│
├ Verifying Pages project
│ verified project is ready for deployment
│

astro build && wrangler pages deploy

npm i -D wrangler@latest

npm install scripts present

To run Wrangler:

npx wrangler

To check Wrangler version

npx wrangler --version

To run Wrangler

npx wrangler

To login to wrangler

wrangler login

To set up Wrangler

wrangler setup


3. To make sure the local installation of Wrangler is the latest:

npm update @astrojs/cloudflare wrangler

3. To run the dev site locally

    npm run dev

4. To build the public site (updates files in /dist/client/)

(npm run build?)
    npx astro build

To upload to Cloudflare:

    npx wrangler deploy

5. Upload site to Cloudflare

    npx

Links:

<https://developers.cloudflare.com/workers/static-assets/migration-guides/migrate-from-pages/>

<https://www.codewithkarani.com/blog/vite-504-outdated-optimize-dep-explained>

<https://docs.astro.build/en/guides/deploy/cloudflare/>
