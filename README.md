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

### Option 3. Install Minified CSS

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
// Regular
@font-face {
  font-family: "FuturaPT";
  src: url("/fonts/FuturaPT-Book.eot");
  src: url("/fonts/FuturaPT-Book.eot?#iefix") format("embedded-opentype"), url("/fonts/FuturaPT-Book.woff2")
      format("woff2"), url("/fonts/FuturaPT-Book.woff") format("woff"), url("/fonts/FuturaPT-Book.ttf")
      format("truetype");
}

// Bold
@font-face {
  font-family: "FuturaPT";
  src: url("/fonts/FuturaPT-Heavy.eot");
  src: url("/fonts/FuturaPT-Heavy.eot?#iefix") format("embedded-opentype"), url("/fonts/FuturaPT-Heavy.woff2")
      format("woff2"), url("/fonts/FuturaPT-Heavy.woff") format("woff"), url("/fonts/FuturaPT-Heavy.ttf")
      format("truetype");
  font-weight: 700;
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

Prepare a PR with a new version number that follows [semantic versioning](http://semver.org/) - this is really important!

Build the latest website by running (it will create `_site` directory):

```sh
$ bundle exec jekyll server
```

Commit all changes, then push the changes to `gh-pages` branch with:

```sh
$ grunt publish
```

Changes should be live in around 30 seconds.

#### Creating a new release

- Go to the ['releases'](https://github.com/wealthsimple/fabric/releases) tab in github.
- Hit the 'draft new release button'. Use the master branch only please. This does two things:
  - it prompts you to enter some info about what's in the new release. Be descriptive! This serves as our changelog, and your colleagues will thank you. Screenshots of new controls/features are handy too.
  - It creates the git tag that bower will use.

For npm you need to manually publish. Go to your terminal, rebase latest master, and run:

```sh
$ npm login
$ npm publish
```

You will need to be added to our organization to publish the package.

## Credits

Boilerplate for this repository was heavily reused from [GitHub's CSS toolkit](https://github.com/primer/primer).
