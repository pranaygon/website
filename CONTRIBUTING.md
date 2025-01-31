# Contributing to Verdaccio Website

## Translations

If you are willing to contribute with translations you need to fullfil some requirements:

* You need a [crowdin](https://crowdin.com/project/verdaccio) account.
* Chose the target language if exist otherwise request to be enabled.

## Source Code Documentation

The language by default is English, all source code is under the `docs` folder.

[https://github.com/verdaccio/website/tree/master/docs](https://github.com/verdaccio/website/tree/master/docs)

## Source Code Website

We use [Docusaurus](https://docusaurus.io) to publish the website, it is based on React. The source code is under the folder

[https://github.com/verdaccio/website/tree/master/website](https://github.com/verdaccio/website/tree/master/website)

🚨🚨 Some caveats you need to keep on mind 🚨🚨:

* Do not update files in the following folders due are autogenerated by crowdin
  * `website/website/translated_docs`
  * `website/website/versioned_docs`
  * `website/website/versioned_sidebars`
  * `website/i18n/!en.json` (only update en.json, the other files are autogenerated)


# Development

## Running website locally

Install [`pnpm`](https://pnpm.js.org/)

```
npm i -g pnpm
```

Go to `cd website` that include the docusaurus source code

## Scripts

Start the dev server (browser will open)
```
pnpm run start
```

Build the website on `build/` folder
```
pnpm run build
```

# Pull Request

For this repository there is no strict rules, please follow the basics:

* Document and explain your changes for faster code reviews
* Verify with Netlify preview (see the checks clicking on Details) to open the preview URL

# How to add a new page

1. Add a new markdown document on [this location](https://github.com/verdaccio/website/tree/master/docs)
2. Define the header for the markdow like this:

```
---
id: idOfTheArticlePleaseUseCamelCase
title: "The Title of my article"
---

your content ...
````
3. Edit [(`sidebar.json`](https://github.com/verdaccio/website/blob/master/website/sidebars.json) and add the reference **using the ID in the previous section**.
4. PR your changes
5. Wait until finish the build and preview your changes

<img width="1130" alt="New_Crowdin_updates_by_juanpicado_·_Pull_Request__304_·_verdaccio_website" src="https://user-images.githubusercontent.com/558752/97103693-57e9e900-16ae-11eb-8a3b-5728f211e052.png">
