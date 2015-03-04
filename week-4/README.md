# simple-html-and-css

This week is different than the previous weeks. It introduces some new libraries and concepts, but also has no visual goal to strive towards (just a small bit of functionality). You're at the point now where you can determine what your page will look like. Make it look visually appealing, but that's not the focus. The focus is on building up your developer toolset by learning some new tools that every frontend developer needs to know.

- **SASS** a CSS-like language (.scss files) that make it easy to write CSS (http://sass-lang.com/)
- **jQuery** a javascript library for adding behavior to your sites (http://jquery.com/)
- **Grunt** for automating frontend tasks. (http://gruntjs.com/)
  - These tasks include:
    - Reloading your website when you make changes to files
    - Allowing you to write standards-based CSS by auto-adding browser prefixes as needed to certain CSS rules (like -webkit- for example)
    - Combining and optimizing files so that the browser doesn't have to request and download tons of different CSS and javascript files
    - Much more
- Package managers (npm and bower)
- Source code vs. distribution code (Grunt helps you transform from /app to /dist)
  - Also known as development vs. production
  - For this week-4 project, consider the week-4/app folder to be your source code and the week-4/dist folder to be your production code
- Bootstrap (http://getbootstrap.com/)
  - Components based on HTML, JS and CSS originally created by Twitter engineers
  - SASS version
- AJAX
  - http://en.wikipedia.org/wiki/Ajax_(programming)
  - http://api.jquery.com/jquery.ajax/

The goal this week is to create a "latest tweets" component. This requires:
- adding a text input that takes a Twitter username
- adding a button to initiate the request to Twitter
- displaying a list of the 5 latest tweets
- displaying a loading indication while the AJAX request waits to complete (http://www.ajaxload.info/)
- functions well and looks decent for mobile and desktop

The final deliverable must be compiled into the week-4/dist folder and pushed to the remote on github.

HINTS:
- The command line (Terminal) is your friend, and you can't start this week without it
  1. Install NodeJS and npm which will allow you to utilize the new tools
    - https://docs.npmjs.com/getting-started/installing-node
  2. Install bower, which is a frontend library manager (package manager) created by Twitter engineers
    - http://bower.io/#install-bower
  3. After pulling week-4, you'll want to install its dependencies
  4. Dependencies can be installed via npm and bower commands, two package managers. In Terminal, navigate to /week-4/ folder and run:
    - npm install
    - bower install
- Grunt commands will drive your debug/preview workflow
  - Running `grunt serve`will compile your SASS (`styles/main.scss`) into plain CSS and open the site in your default browser
  - Running `grunt build` will compile everything into the /dist/ folder, ready for sending to production! (only needed when done)
  - Errors in your files will show up in yellow/red text in grunt output in Terminal
- You'll need to reference the SASS, Bootstrap and jQuery documentation heavily while developing the component
- Components can be broken down conceptually into 3 parts:
  1. **Structure**: the HTML markup describing the component (text `<input>`, `<button>`, etc.)
  2. **Style**: the CSS (compiled from SASS/scss in this case) (layout, colors, font size, etc.)
  3. **Behavior**: the javascript (jquery in this case) allowing for interactive behavior (click handler, AJAX request, etc)
- Twitter's API doc for user timeline: https://dev.twitter.com/rest/reference/get/statuses/user_timeline
