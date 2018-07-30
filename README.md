# Eleventy Netlify Boilerplate

## What is it?

An extremely simple and lightweight template for building a website with blog using the [Eleventy](https://www.11ty.io/) static site generator, with deployment to [Netlify](https://www.netlify.com).

Based on the [Eleventy Base Blog](https://github.com/11ty/eleventy-base-blog) repo (see there for more info on usage).

## Features

* 100% pre-built and minified HTML pages
* CSS 2kb minified, inline for fastest page render
* CSS Grid layout with fallbacks
* Sample pages and a blog with posts and tag support
* Uses Markdown files for content
* Uses Liquid and/or Nunjucks templates for layout
* Optional Javascipt pipeline for minified inline scripts
* Continuous Integration (CI) workflow via Netlify

## [Demo Site](https://eleventy-netlify-boilerplate.netlify.com//)

## Want to just try it out?

* [Get your own copy on Netlify](https://app.netlify.com/start/deploy?repository=https://github.com/danurbanowicz/eleventy-netlify-boilerplate) in just a few clicks.

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
