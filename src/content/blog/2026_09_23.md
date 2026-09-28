---
title: 'Cloudflare with Astro: Getting Started'
description: 'Getting started with Astro and Cloudflare'
pubDate: 'September 23 2026'
tags: ["astro", "node", "npm", "nvm"]
---

This post describes the initial steps in setting up this blog site.

Requirements
-----------

The following applications need to be installed before creating websites with Astro on Cloudflare:

1. [Node.js](https://nodejs.org/en/download)

    Check version: node -v

    Astro supports even version numbers of Node

2. [npm](https://www.npmjs.com/) (Node Package Manager)

    Check version: npm -v

3. [nvm](https://www.nvmnode.com/) (Node Version Manager)

This website was created using Node.js version v24.18.0 and npm version 11.16.0

1 Initialize An Astro Project
-----------------

Creating the ./jottings folder and get started with the Astro framework:

> npx create-astro@5.2.4 jotttings --no-install --no-git

(tutorial suggestion: npm create astro@latest)

Settings:

    Directory: ./jottings
    Start with: Framework Starter
    Development Framework: Astro
    Deployment Platform: Pages

Package installed: create-astro@5.2.4

Use blog template

2 Scaffold the site on Cloudflare
----------------------------

Create a Cloudflare pages site:

> npm create cloudflare@latest -- jottings --framework=astro --platform=pages

Output:

    Copying template files - files copied to project directory

    Installing dependencies
        installed via `npm install`

    Application created

    Configuring your application for Cloudflare Step 2 of 3

    Installing wrangler A command line tool for building Cloudflare Workers

        installed via `npm install wrangler --save-dev`

    Selecting workerd compatibility date, compatibility date 2026-09-23

    Installing adapter
        installed via `npx astro add cloudflare`

    Updating configuration in astro.config.mjs

    Adding Wrangler files to the .gitignore file
        updated .gitignore file

    Updating `package.json` scripts
        updated `package.json`

    Generating types for your application
    generated to `./worker-configuration.d.ts` via `npm run cf-typegen`

    Installing @types/node
        installed via npm

    Do you want to use git for version control?
        yes git

    Initializing git repo
        initialized git

    Deploy with Cloudflare Step 3 of 3

    Do you want to deploy your application?
        yes deploy via `npm run deploy`

    Logging into Cloudflare checking authentication status
        not logged in

    Logging into Cloudflare This will open a browser window
    allowed via `wrangler login`

    Selecting Cloudflare account retrieving accounts
        account Simon.fermor@gmail.com's Account

    Creating Pages project
        created via `npx wrangler pages project create jottings --production-branch main`

    Verifying Pages project
        verified project is ready for deployment

3 Add Cloudflare to the packages
-------------

    npm run astro add cloudflare

See astro.config.mjs

4 Build and Deploy
---------------

> astro build && wrangler pages deploy

<!-- -->
> npm i -D wrangler@latest

<!-- -->
> npm install scripts present

5 Running Wrangler
-------------

Check the version of Wrangler:

> npx wrangler --version

To run Wrangler:

> npx wrangler

To login to Wrangler:

> wrangler login

To set up Wrangler

> wrangler setup

To make sure the local installation of Wrangler is the latest:

> npm update @astrojs/cloudflare wrangler

6 To run the dev site locally
------------

> npm run dev

7 To build the public site (updates files in /dist/client/)
-------------

> npx astro build

8 To upload to Cloudflare
-------------

The site on Cloudflare is a Pages project, good for static sites.

> npx wrangler deploy

9 DNS
------

For DNS I did the following:

- add a sub-domain for fermor.org on the domain provider
- create a CNAME target on the domain registration site to point to jottings-woh.pages.dev (the Cloudflare site url)
- update Cloudflare to set the custom domain (blog.fermor.org) to point to the Cloudflare site

More details
-------

[Cloudflare Astro Deployment Guide](https://developers.cloudflare.com/pages/framework-guides/deploy-an-astro-site/)

[Migrating from Cloudflare Pages to Workers](https://developers.cloudflare.com/workers/static-assets/migration-guides/migrate-from-pages/)

[Resolving Dependancy Version Errors](https://www.codewithkarani.com/blog/vite-504-outdated-optimize-dep-explained)

[Cloudflare Deployment Guide](https://docs.astro.build/en/guides/deploy/cloudflare/)

[YouTube Cloudflare Astro guide](https://youtu.be/c_IBs1crl4k)

[Astro Guide to Cloudflare Deployment](https://docs.astro.build/en/guides/deploy/cloudflare/)

[Astro Guide to Using Endpoints](https://docs.astro.build/en/guides/endpoints/)

[Favicon Generator](https://redketchup.io/favicon-generator)

[PNG to ICO conversion](https://www.freeconvert.com/png-to-ico/download)

[Noun Project Bike Icon](https://thenounproject.com/icon/bike-6651907/)