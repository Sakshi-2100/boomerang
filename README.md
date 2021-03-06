GDG-X Boomerang
=========

[![Build Status](https://travis-ci.org/gdg-x/boomerang.svg)](https://travis-ci.org/gdg-x/boomerang) [![Join the chat at https://gitter.im/gdg-x/boomerang](https://badges.gitter.im/Join%20Chat.svg)](https://gitter.im/gdg-x/boomerang?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Boomerang is a template for a dynamic material design GDG chapter web site that can be deployed
within 30 minutes. It is built using [AngularJS](https://angularjs.org/) and 
[AngularJS Material](https://material.angularjs.org).

See it in action: http://gdg-x.github.io/boomerang

Configuration!!!
---------------
Update `app/services/configService.js` with values appropriate for your group:

1. **name**: The name of your GDG
1. **twitter**, **facebook**, **meetup**: Update these with your chapter's social network handles. Setting them to '' will hide the icon.
1. Create your Google Analytics account and modify the Google Analytics tracking code in **index.html**.

Additional Optional Config
---------------
1. **domain**: Your custom domain name (or base appspot URL).
1. **cover.title**: An announcement that will appear on the landing page.
1. **cover.subtitle**: More text to support the landing page announcement.
1. **cover.button.text**: Text for the announcement button.
1. **cover.button.url**: The URL that the announcement button will open in another window.
1. **cover.url**: If the cover image drawn from your Google+ page does not work with the default layout,
   you can specify a URL for a specific image instead.
1. Edit the snippet details in the **index.html** to change how your page looks when it is shared.
1. Modify the images in war/app/images/sponsor1 and war/app/images/sponsor2 to be your sponsor images.
1. Modify the sponsor links in **about.html**.

Building
---------------
Here you will install dependencies and tooling, build, minify, run static analysis, and more.
You must have Node.js installed to use the build tools. Download it [here](http://nodejs.org/download/).
From the boomerang directory, run the following:

1. `npm install`
1. `gulp`

Automated Testing
---------------
1. Unit tests can be run once via `gulp karma` or constantly via `gulp karma-watch`.
1. Integration tests can be run via:
  1. `node node_modules/protractor/bin/webdriver-manager update`
  1. `node node_modules/protractor/bin/webdriver-manager start`
  1. Then in a separate terminal: `node node_modules/protractor/bin/protractor test/e2e/conf.js`
1. WebStorm or IntelliJ IDEA can make this testing a lot easier if you configure the idea to do it for you.

Testing locally
---------------
You should be able to test locally with Node.js using the following:

1. `npm start`

Deployment
---------------
Deploy on your web server of choice (Apache, Nginx, etc).
If you need a web server, Google App Engine's free tier should be more than sufficient for your
chapter's needs.

Development Details
---------------
Make sure that you do the following successfully before committing:

1. `gulp prod`
2. `gulp karma` - Make sure that you fix any broken tests.
3. Protractor tests - Make sure that you fix any broken tests.
4. If you changed any dependency versions in `bower.json`, make sure that `config/CDN.json` is
   updated to match.

Sites using this template
---------------
* http://gdgspacecoast.org/
* http://www.gdg-bodensee.de/
* http://www.gdgfresno.com/
* http://gdg-brussels.org/
* http://www.gdgschaumburg.com/
* http://gdgdubai.com/
* http://gdga-site.appspot.com/
* http://gdg.nz/

### Contributors
See [list of contributors](https://github.com/gdg-x/boomerang/graphs/contributors)

Maintainer: [Splaktar](https://github.com/Splaktar).

###### GDG Apps, GDG[x] are not endorsed and/or supported by Google, the corporation.

License
--------

    © 2013-2019 GDG[x]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

       http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
