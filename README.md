karma-bamboo-reporter
=====================

This Karma reporter will create a report file readable by the *Mocha Test Parser* task. You will need the [Bamboo Node.js Support plugin](https://marketplace.atlassian.com/plugins/com.atlassian.bamboo.plugins.bamboo-nodejs-plugin).

Install
-------
`npm install --save-dev Dashlane/karma-bamboo-reporter`

Usage
-----

You need to add the reporter to your Karma config.

```js
// …

reporters: ['bamboo'],

bambooReporter:{
    filename: 'util.mocha.json' // optional, defaults to "mocha.json"
},

plugins: ['karma-bamboo-reporter']

// …
```

In your Bamboo job, you need to add the *Mocha Test Parser* task after the execution of your tests.

**Beware**: Your tests' full names will have to be unique otherwise they might not appear in Bamboo's Tests report.


Credits
-------

Forked from a project started by [Evan Sharp](https://github.com/TheSharpieOne): https://github.com/TheSharpieOne/karma-bamboo-reporter
