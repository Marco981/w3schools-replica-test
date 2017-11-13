Pug starter

Starter package for pug (former jade) template based projects.

Note: When you want to make use of the automatically loaded JSON data, site.data has been replaced by data. On top of that, in templates, JSON data can be accessed with template (example: template.title or template.config.render)

Prerequisites

The project requires NodeJS v.4+ and gulp v4+

To install NodeJS visit nodejs download page

Install gulp v4 globally

$ npm i -g gulp-cli
If you already have gulp v3 or lower installed

$ npm rm -g gulp
$ npm i -g gulp-cli
To verify what version you have installed globally, you can run the below command (and should see a similar output)

$ gulp -v
CLI version 1.2.1
Install gulp 4 locally

Once globally installed, gulp v4 will then need to be installed on a per-project basis.

$ npm rm -D gulp
$ npm i -D gulpjs/gulp.git#4.0
Table of contents

Installation
Usage
Style
Installation

BEFORE YOU INSTALL: please read the prerequisites

$ npm i
or

$ npm install
Usage

To run the project in development mode and open a local server that synchronizes across multiple devices use:

npm run dev
To build the project for production use:

npm run prod
To automatically deploy your project to GitHub pages and make it available at https://[your-username].github.io/[your-project-name] use:

npm run deploy
Style

The project supports both inline and external style sheets. You can have none, one or the other, or both of them.

Single page application style

When you're building a single page app or website, there is no point in having the style sheets loaded from an external file and I'll explain why: the point of loading external style sheets is to allow the browser to cache those files and once you visit another web page of the same website, instead of making another request(s) for the style sheet file(s) to the server and having to download them, if there is no change, the browser will load them from the local drive. In a single page, there is no other page to go to therefore the external file technique doesn't apply.

Multi page application style

In this scenario you can have either both inline and external or just external. The most common scenario is to have only one external style sheet file to be loaded and most of the time that's just fine.

If you want to improve your SEO and user experience even further, I strongly recommend to use a combination of both inline and external. The inline style sheet should only contain the minimum amount of styles for the initial visible part of the page to render. The rest of the styles can be put in the external CSS file.
