[![Netlify Status](https://api.netlify.com/api/v1/badges/bbf28a84-4bdb-407b-a2fa-32628d27fa3d/deploy-status)](https://app.netlify.com/sites/eleventy-netlify-boilerplate/deploys)

# Eleventy Netlify Boilerplate

### Click the button below to try it out!

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/danurbanowicz/eleventy-netlify-boilerplate&stack=cms)

## What is it?

A simple template for building a fast, pre-generated HTML website using the [Eleventy](https://www.11ty.dev/) static site generator. With [Decap CMS](https://www.decapcms.org/) (formerly Netlify CMS) baked-in, ready to deploy to [Netlify](https://www.netlify.com) in a couple of clicks.

Use it as a starter for your own Jamstack projects, or as an easy way to get started building websites with Eleventy.

Based on the [Eleventy Base Blog](https://github.com/11ty/eleventy-base-blog) repo (see there for additional info on Eleventy usage).

## [Demo Site](https://eleventy-netlify-boilerplate.netlify.app/)

## Features

* Uses Eleventy v2.0.1
* Sample pages and a blog with tag support
* Decap CMS with editor previews (thanks [@biilmann](https://github.com/biilmann)!)
* Scores 100/100/100/100 in Lighthouse performance tests 🔥
* Maintenance-free post author archives
* Automatic navigation menus with [Eleventy Navigation](https://www.11ty.dev/docs/plugins/navigation/)
* Includes a working contact form
* CSS 2kb minified, inlined for fastest page render
* Optional pipeline for your minified inline JS
* Pre-builds and minifies your HTML too
* Uses Markdown files for content
* Uses Nunjucks (or Liquid) templates for layout
* 100% Javascript framework free
* Continuous Deployment workflow via Netlify

## Want to try it out now?

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/danurbanowicz/eleventy-netlify-boilerplate&stack=cms)

Clicking the button above will deploy a copy of the demo website to your Netlify
account (you can create an account during this process if you don't have one)
and everything needed for running the CMS:

* A new repository in your GitHub account with the code
* Full Continuous Deployment to Netlify's global CDN network
* Control users and access with Netlify Identity
* Manage content with Decap CMS
* Process form data with Netlify Forms

### Set Up Authentication

After deploying this project, Netlify Identity will add you as a CMS user and
will email you an invite. It is not necessary to accept this invite if you wish
to use an
[OAuth provider](https://www.netlify.com/docs/identity/#external-provider-login)
(e.g. Github) to manage authentication for your CMS.

It is recommended to use this method of authentication as it removes the need
for an email & password to log in to the CMS and is generally more secure. You
will need to add an OAuth provider in your Netlify app settings under
"Settings" > "Identity" > "External providers".

Once you've added an OAuth provider, navigate to `/admin` on your site, select your provider from the
list, and you should then be logged into your CMS. Cool huh?

### Set Up Identity Email Templates

In order for Netlify Identity service emails (Signup, Reset Password etc) to function correctly with Decap CMS, you will need to tell Netlify where your email templates are located.

Inside this repo under `/admin/email-templates/` are four Netlify Identity email templates. Inside your Netlify site settings, you will need to navigate to: "Site Settings > Identity" and look there for the four email template configuration boxes: Invitation template, Confirmation template, Recovery template, and Email change template. Inside each, edit the "Path to template" field to match the root-relative path to each template. For example:

`/admin/email-templates/invitation.html`

Now you're all set; you can invite new CMS users and begin editing content!

## Gotchas

If you change the repo that was created at deploy time from public to private, you'll need to regenerate your token,
as the token generated using the deploy to Netlify button can only access public repositories. To
regenerate your token, head to "Settings" in your Netlify site dashboard, go to the "Identity"
section, then scroll to "Services" where you'll see an "Edit settings" button. Click that and you'll
see a text link to "Generate access token in GitHub".

If you need any help with setting up Decap CMS, you can reach out to the Netlify team in the [Decap CMS Gitter](https://gitter.im/netlify/netlifycms).

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

### 3. Install dependencies locally

```
npm install @11ty/eleventy
```

### 4. Edit _data/metadata.json

This file contains your site title and author details, and can be used to store any other commonly used site data.

### 5. Run Eleventy (builds the site)

```
npx @11ty/eleventy
```

Or build automatically when a template changes:
```
npx @11ty/eleventy --watch
```

Or build and host locally for local development:
```
npx @11ty/eleventy --serve
```

Or in debug mode:
```
DEBUG=* npx @11ty/eleventy
```

## Bug reports, feature requests, etc

This is an ongoing project and I welcome contributions and suggestions! Feel free to submit a PR.

If you need any help with setting up Decap CMS, you can reach out to the Netlify team in the [Decap CMS Gitter](https://gitter.im/netlify/netlifycms).
