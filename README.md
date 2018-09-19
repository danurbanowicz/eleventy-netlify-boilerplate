# Eleventy Netlify Boilerplate

## What is it?

An extremely simple and lightweight template for building a website with blog and CMS using the [Eleventy](https://www.11ty.io/) static site generator, with deployment to [Netlify](https://www.netlify.com).

Use it as a basis for your own projects or as an easy way to get started building static sites with Eleventy.

Based on the [Eleventy Base Blog](https://github.com/11ty/eleventy-base-blog) repo (see there for additional info on Eleventy usage).

## [Demo Site](https://eleventy-netlify-boilerplate.netlify.com//)

## Features

* Sample pages and blog with tag support
* Pre-builds and minifies your HTML
* CSS 2kb minified, inline for fastest page render
* Responsive CSS Grid layout, with fallbacks (see [Browser Support](#browser-support))
* Uses Markdown files for content (works with Netlify CMS)
* Uses Liquid and/or Nunjucks templates for layout
* Contains no boilerplate JS or other bloat (100% framework free)
* Optional Javascipt pipeline for minified inline scripts
* Continuous Integration (CI) workflow

## Want to try it out now?

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/danurbanowicz/eleventy-netlify-boilerplate&stack=cms)

Clicking the button above will deploy a copy the demo website to your Netlify
account (you can create an account during this process if you don't have one)
and everything needed for running the CMS:

* A new repository in your GitHub account with the code
* Full Continuous Deployment to Netlify's global CDN network
* Control users and access with Netlify Identity
* Manage content with Netlify CMS
* Process form data with Netlify Forms

### Setup authentication

After deploying this project, you will need to add yourself as a Netlify CMS
user if you wish to access the CMS. It is recommended to use the
[OAuth](https://www.netlify.com/docs/identity/#external-provider-login) method of logging into the CMS with your Github account (or other OAuth
provider). Using OAuth removes the need for an email & password to log in
to the CMS and is generally more secure. You can enable this in your Netlify
app settings under "Identity" > "External providers".

Next, navigate to `/admin` on your site, choose your OAuth provider from the
login box and you should then be logged into your CMS. Cool huh?

Now you're all set, and you can start editing content!

## Gotchas

If you change the repo that was created at deploy time from public to private, you'll need to regenerate your token,
as the token generated using the deploy to Netlify button can only access public repositories. To
regenerate your token, head to "Settings" in your Netlify site dashboard, go to the "Identity"
section, then scroll to "Services" where you'll see an "Edit settings" button. Click that and you'll
see a text link to "Generate access token in GitHub".

If you need any help with setting up Netlify CMS, you can reach out to the Netlify team in the [Netlify CMS Gitter](https://gitter.im/netlify/netlifycms).

## Local development

### 1. Clone this repository:

```
git clone https://github.com/danurbanowicz/eleventy-netlify-boilerplate.git my-blog-name
```


### 2. Navigate to the directory

```
cd my-blog-name
```

Specifically have a look at `.eleventy.js` to see if you want to configure any Eleventy options differently.

### 3. Install dependencies

```
npm install
```

### 4. Edit _data/metadata.json

This file contains your site title and author details.

### 5. Run Eleventy (builds the site)

```
npx eleventy
```

Or build automatically when a template changes:
```
npx eleventy --watch
```

Or in debug mode:
```
DEBUG=* npx eleventy
```

## Bug reports, feature requests, etc

This is an ongoing project and I welcome any feedback, suggestions or contributions.

Please use the issue tracker to let me know about any bugs or feature requests, or alternatively make a pull request.

If you need any help with setting up Netlify CMS, you can reach out to the Netlify team in the [Netlify CMS Gitter](https://gitter.im/netlify/netlifycms).

## [Browser support](#browser-support)

This template uses relatively new features such as [CSS Grid layout](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Grid_Layout) and [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Variables) therefore browser support is still patchy. You should consider providing fallbacks for older or less capable browsers when using this template in a production environment.
