# Eleventy Netlify Boilerplate

## What is it?

An extremely simple and lightweight template for building a website with blog using the [Eleventy](https://www.11ty.io/) static site generator, with deployment to [Netlify](https://www.netlify.com).

Use it as a basis for your own projects or as a way to get started building static sites with Eleventy.

Based on the [Eleventy Base Blog](https://github.com/11ty/eleventy-base-blog) repo (see there for additional info on usage).

## Features

* Pre-builds and minifies your HTML
* CSS 2kb minified, inline for fastest page render
* Responsive CSS Grid layout, with fallbacks
* Sample pages and blog with tag support
* Uses Markdown files for content (works with Netlify CMS)
* Uses Liquid and/or Nunjucks templates for layout
* Contains no boilerplate JS (100% framework free)
* Optional Javascipt pipeline for minified inline scripts
* Continuous Integration (CI) workflow

## [Demo Site](https://eleventy-netlify-boilerplate.netlify.com//)

## Want to just try it out?

* [Deploy this project now to Netlify](https://app.netlify.com/start/deploy?repository=https://github.com/danurbanowicz/eleventy-netlify-boilerplate) in just a few clicks.

## Getting Started

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

### 5. Run Eleventy

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
