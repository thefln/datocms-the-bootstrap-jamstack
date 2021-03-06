## The Bootstrap Jamstack (Website) [WIP] [![Netlify Status](https://api.netlify.com/api/v1/badges/b4d4851c-b743-4034-8f20-293d2ca9396e/deploy-status)](https://app.netlify.com/sites/bootstrapjamstack/deploys)

![The Bootstrap Jamstack](https://snipcart.com/media/205586/the-bootstrap-jamstack.png?width=1600&format=webp&quality=80&upscale=false)

I'm working on creating an index of bootstrapped Jamstack companies.

The idea came from [this post](https://snipcart.com/blog/bootstrap-jamstack), [this video](https://www.youtube.com/watch?v=aegc7A9v3OM&lc), and [this meetup](https://www.youtube.com/watch?v=wmFBZ_SnZns).

---

# Hugo Portfolio Website

This repo contains a working static website written with [Hugo](http://gohugo.io/), integrated with content coming from DatoCMS.

You can check the [live version deployed on Netlify](https://portfolio-datocms-hugo.netlify.com/), that looks like this:

![Screenshot of the porfolio website](./screenshot.png)

or you can deploy your own, together with the administrative area, with this button:

[![Deploy with DatoCMS](https://dashboard.datocms.com/deploy/button.svg)](https://dashboard.datocms.com/projects/new-from-template/static-website/hugo-portfolio)


## Usage

First, install the dependencies of this project:

```
npm install
```

Add an `.env` file containing the read-only API token of your DatoCMS site:

```
echo 'DATO_API_TOKEN=abc123' >> .env
```

Then, to run this website in development mode (with live-reload):

```
npm start
```

To build the final, production ready static website:

```
npm run build
```

The final result will be saved in the `public` directory.

## About

The goal of this project is to show how easily you can create static sites using the content (text, images, links, etc.) stored on [DatoCMS](https://www.datocms.com). This project is configured to fetch data from a specific administrative area using [the API DatoCMS provides](https://docs.datocms.com/api/reference.html).

This websites uses:

* [Yarn](https://yarnpkg.com/) as package manager;
* [Webpack](https://webpack.github.io/) to compile and bundle assets (Sass/ES2015 JS);
* [datocms-client](https://github.com/datocms/js-datocms-client) to integrate the website with DatoCMS.

## The `dato.config.js` file

To convert the content stored on DatoCMS into local Markdown files that can be digested by Hugo, the datocms-client plugin requires an explicit mapping file called [`dato.config.js`](https://github.com/datocms/hugo-portfolio/blob/master/dato.config.js). You can read more about the commands available in this file [in the official documentation](https://docs.datocms.com/hugo/overview.html).


