# Get Help Osage [![Build Status](https://travis-ci.org/Osage-Nation/GetHelpOsage.svg)](https://travis-ci.org/Osage-Nation/GetHelpOsage) [![Waffle.io - Columns and their card count](https://badge.waffle.io/Osage-Nation/GetHelpOsage.svg?columns=all)](https://waffle.io/Osage-Nation/GetHelpOsage)


## History
The project is based on Code for Lexington's GetHelpLex, which in turn is based on Code for Boston's [finda](https://github.com/codeforboston/finda) project. 

Osage Nation customized it with:
* WIP

Lexington customized it with:
 * The facilities [are read](https://github.com/Osage-Nation/GetHelpOsage/blob/gh-pages/src/data/geojson.js#L10) from a Google spreadsheet using the [Tabletop.js](https://github.com/jsoma/tabletop) library. This way our stakeholders have realtime ability to update facilities.
 * We hacked the [facet handling](https://github.com/Osage-Nation/GetHelpOsage/blob/gh-pages/src/ui/facet.js) to guide the user through a 'survey'. It narrows down the facilities based on type of treatment, the insurance they accept, etc.
 
## I want to help
Great, thank you for wanting to help with our project. Below we have categorized some of the various ways you can get started with assisting. **At this time we are actively looking for assistance with mapping out facilities in Osage, Kaw, Pawnee, Washington, and Tulsa Counties in Oklahoma.** 

### Developer
#### Install 
Quick setup:

    npm install
    npm install -g http-server
    npm start

Visit [localhost:8080](http://localhost:8080/) to see the app.

#### Test
You can run tests once by running: `npm test`

Keep test server running to speed up tests. Start test server:

    npm run test-server

Kick off a test run when the test server is running:

    npm run test-client

#### Submit Pull Request
    1. Please explain your effort in your pull request to make our review easier

### Content Editor
#### Add New Facility Information
 1. Add a column to the [facilities spreadsheet](https://docs.google.com/spreadsheets/d/1ubx07oylGxk5FDIjMnQo4cMNBd3a8QYiPm27rWuyByI/edit#gid=145432932) called smoking_permitted (or similar):

    * Make a copy of the existing spreadsheet
    * Copy-paste the new spreadsheet's key to the [Tabletop.js init](https://github.com/Osage-Nation/GetHelpOsage/blob/gh-pages/src/data/geojson.js#L12)
    * Update [config.json](https://github.com/Osage-Nation/GetHelpOsage/blob/gh-pages/config.json) [todo, flesh this step out more :)]

A lot of Code for Boston's [development documentation](https://github.com/codeforboston/finda/wiki/Developing-Finda) is still relevant. Add an issue or Pull Request if you hit any key differences for Osage Nation so we can update this readme.

#### Add map coordinates for new facilities
![Geocode facilites](./get-help-lex-geocode.gif)

### Everyone
Please look in the [waffle board](https://waffle.io/Osage-Nation/GetHelpOsage) for priority issues. Issues will be tagged with `first-timers-only` for issues that are beginner-friendly. See [Awesome for Beginners](https://github.com/MunGell/awesome-for-beginners) for more info.



## Analytics and feedback
GetHelpOsage uses Google Tag Manager to manage Google Analytics as described in the [Unified Analytics repository](https://github.com/laurenancona/unified-analytics).

GetHelpOsage posts feedback to a Google Spreadsheet [as described here](https://mashe.hawksey.info/2014/07/google-sheets-as-a-database-insert-with-apps-script-using-postget-methods-with-ajax-example/).
As a backup, feedback is tracked using the [ga-feedback approach](https://github.com/luckyshot/ga-feedback) managed by Google Tag Manager [as described here](http://erikschwartz.net/2016-01-23-google-analytics-events-in-google-tag-manager/).

Feedback is emailed to addresses defined in the script attached to the [feedback spreadsheet](https://docs.google.com/spreadsheets/d/1lP-OsypwXFkH-S3F3Re34fBPSYgpr1ZXY6bRD85w3V8/edit).

To make changes to the script that handles feedback requests:

* edit in the Appscript editor
* `Publish` > `Deploy as webapp` > `Version: new`
