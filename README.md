# Documentation

## Project setup and Gulp installation
This boilerplate was created off [Fastshell](https://github.com/HosseinKarami/fastshell). This boilerplate utillizes open source componenets running on the Terminal/command-linefor it's workflow.

1. Install [Node.js](http://nodejs.org/download), [Sass](http://sass-lang.com/tutorial.html) and [Git](http://git-scm.com) on your machine. If you're a Windows user you'll also need to install [Ruby](http://rubyinstaller.org/downloads).
2. [Install Gulp](http://Gulpjs.com/) using `npm install -g gulp`. You may need to use `sudo` in front of the Gulp install command to give it permissions.
3. Fork/Clone/Download the FastShell repository into your machine, you should hopefully see all the files and folders.
4. Open Terminal and run `npm install` in your project directory in order to download your `node_modules`. You don't need `sudo` to do this.
5. Run `gulp` (again in your project directory) to start a local server that automatically reloads when changes are made in your project. The default port is `localhost:3002`.
6. Onward, just run `gulp` in your project directory to automatically run your Gulp tasks.

````js
/*!
 * @author Adeyemi Oluwapelumi
 * @version 1.0.0
 * Copyright 2018. MIT licensed.
 */
````



## Why just style.min.css and scripts.min.js?
Including only two of your custom CSS and JavaScript files in your HTML aligns with best practices in modern web development, minifying your code and limiting HTTP requests is a huge performance enhancer.

## Sass/SCSS setup
FastShell comes with a `.scss` file setup and existing `@import` declarations to the very common web components. FastShell hopes to help those out who aren't sure about structuring a CSS project confidently as well as getting them setup with using a CSS PreProcessor. The basic idea:

* `mixins` holds all Sass/SCSS mixins, FastShell ships with a few helpers
* `module` holds modules, more Object-Orientated components and a generic `app.scss` for everything else, all file names should be modular/OO.
* `partials` holds the blueprints for the project, the header, footer, sidebar and so on.
* `vendor` holds any files that are third party, such as the font awesome icons CSS
* `style.scss` imports all the necessary files from the above folders, when adding new files be sure to add it inside this file.

## Hidden files explained

It's a good idea to expose hidden files so you can configure your `.editorconfig`, `.jshintrc`, `.gitignore` files. On the command line, enter:

````
defaults write com.apple.Finder AppleShowAllFiles YES
````

To hide hidden files enter:

````
defaults write com.apple.Finder AppleShowAllFiles NO
````

### .editorconfig
EditorConfig helps developers define and maintain consistent coding styles between different editors and IDEs. The `.editorconfig` file consists of a format for defining coding styles and a collection of text editor plugins that enable editors to read the file format and adhere to defined styles.

### .gitignore
Ignores minified and generated files, this is best for working in teams to avoid constant conflict, only the source files are needed.

### .travis.yml
This is used on [travis-ci.org](http://travis-ci.org) for continuous integration tests, which monitors build.
