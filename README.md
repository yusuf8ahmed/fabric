# Fabric

Fabric is the CSS toolkit that powers Wealthsimple's front-end design. It's purposefully limited to common components to provide our developers with the most flexibility. It's built with SCSS and available via Bower, so it's easy to include all or part of it within your own project.

[**Read the Fabric documentation**](http://fabric.wealthsimple.com/) to learn more.

## Install

There are three options for installing Fabric on your own project.

### Option 1. Install with npm or yarn

If you are using a `import`- or `require`- aware javascript bundler like [webpack](http://webpack.js.org), we recommend installing using `npm` or `yarn`:

```sh
npm install --save @wealthsimple/fabric
```

or

```sh
yarn add @wealthsimple/fabric
```

### Option 2. Install with Bower

If your project setup isn't capable of processing npm-based modules, we also publish to [bower](http://bower.io/).

First, create a `bower.json` in your project root directory if you dont have one yet:

```json
{
  "name": "your-project-name",
  "private": true
}
```

Optionally specify a `.bowerrc` config file to control the directory where the assets get pulled into:

```json
{
  "directory": "vendor/assets/bower_components"
}
```

Then, to install the latest version of Fabric, run:

```sh
$ bower install --save https://github.com/wealthsimple/fabric.git
```

To update the package once installed:

```sh
$ bower update wealthsimple-fabric
```

### Option 2. Install Minified CSS

The concatenated and minified CSS is available in https://github.com/wealthsimple/fabric/blob/master/css/fabric.css

Note: this is **not recommended**, as you won't have access to any of the SCSS variables or mixins.

## Usage

Once installed with bower, simply `@import` either the master SCSS file, or the individual files as you need them.

```scss
// Example: All of Fabric
@import "wealthsimple-fabric/scss/fabric";

// Example: Individual files
@import "wealthsimple-fabric/scss/variables";
@import "wealthsimple-fabric/scss/mixins";
@import "wealthsimple-fabric/scss/base";
```

## Fonts

Since font installation may vary based on the asset compilation framework you're using (e.g. Sprockets for Rails, Grunt for Ghost.org), Fabric does not include `@font-face` definitions. You must include these yourself.

Example below. Note: for Sprockets-based compilation, you'll want to replace `url` with `font-url`.

```scss
@font-face {
  font-family: 'FuturaBT-Light';
  src: url('/fonts/FuturaBT-Light.eot');
  src: url('/fonts/FuturaBT-Light.eot?#iefix') format('embedded-opentype'),
       url('/fonts/FuturaBT-Light.woff2') format('woff2'),
       url('/fonts/FuturaBT-Light.woff') format('woff'),
       url('/fonts/FuturaBT-Light.ttf') format('truetype');
}

@font-face {
  font-family: 'FuturaBT-Book';
  src: url('/fonts/FuturaBT-Book.eot');
  src: url('/fonts/FuturaBT-Book.eot?#iefix') format('embedded-opentype'),
       url('/fonts/FuturaBT-Book.woff2') format('woff2'),
       url('/fonts/FuturaBT-Book.woff') format('woff'),
       url('/fonts/FuturaBT-Book.ttf') format('truetype');
}

@font-face {
  font-family: 'FuturaBT-Heavy';
  src: url('/fonts/FuturaBT-Heavy.eot');
  src: url('/fonts/FuturaBT-Heavy.eot?#iefix') format('embedded-opentype'),
       url('/fonts/FuturaBT-Heavy.woff2') format('woff2'),
       url('/fonts/FuturaBT-Heavy.woff') format('woff'),
       url('/fonts/FuturaBT-Heavy.ttf') format('truetype');
}

@font-face {
  font-family: 'CaslonGraD';
  src: url('/fonts/CaslonGraD.eot');
  src: url('/fonts/CaslonGraD.eot?#iefix') format('embedded-opentype'),
       url('/fonts/CaslonGraD.woff2') format('woff2'),
       url('/fonts/CaslonGraD.woff') format('woff'),
       url('/fonts/CaslonGraD.ttf') format('truetype');
}

@font-face {
  font-family: "SSSocialCircle";
  src: url('/fonts/SSSocialCircle.eot');
  src: url('/fonts/SSSocialCircle.eot?#iefix') format('embedded-opentype'),
       url('/fonts/SSSocialCircle.woff') format('woff'),
       url('/fonts/SSSocialCircle.ttf')  format('truetype');
}
```

## Running locally and making changes

- Grunt is used for SCSS compliation, vendor prefixing, CSS reporting, and publishing the documentation to GitHub Pages.
- The docs are written in Markdown and compiled to HTML by [Jekyll](https://jekyllrb.com/), a static site generator.

### First-time setup

To get this setup working locally, you must first have Node.JS and Ruby installed.

Next, install dependencies with the following commands:

```sh
bundle install
npm install
npm install -g grunt-cli
```

Then, you may have to open a new Terminal window or run `source ~/.bash_profile` to have access to the new `grunt` and `jekyll` binaries.

### Running locally

1. Make sure dependencies are installed as described in "First-time setup"
2. Run `grunt watch` to have the CSS recompiled when any file in `scss` is changed
3. Boot up a Jekyll server with `bundle exec jekyll server`
4. Open [http://localhost:4000](http://localhost:4000) to view the documentation locally

### Publishing changes

The public documentation is hosted on GitHub pages. To push new changes, first compile the CSS:

```sh
$ grunt
```

Commit all changes, then push the changes to `gh-pages` branch with:

```sh
$ grunt publish
```

Changes should be live in around 30 seconds.

## Credits

Boilerplate for this repository was heavily reused from [GitHub's CSS toolkit](https://github.com/primer/primer).
