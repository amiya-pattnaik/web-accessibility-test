## Web Accessibility Testing

This repository contains common methods for  Web Accessibility Testing recommended by WCAG. It uses `axe-core` which is an accessibility testing engine for websites and other HTML-based user interfaces. It's fast, secure, lightweight, and was built to seamlessly integrate with any existing test environment so you can automate accessibility testing alongside your regular functional testing. It shows hints which internally run the recommended set of WCAG 2.1 Level A and Level AA rules from axe-core. For complete E2E testing using `webdriver.io` and `Allure` reporting please refer to the [WebAccessibilityTestTool](https://github.com/amiya-pattnaik/WebAccessibilityTestTool).

## Installation

Download this package:

`npm install web-accssbility-test --saveDev`

## Example
These are few examples below on how to use:

```
var wat = require('web-accssbility-test');

// to get WCAG Violations
let result = wat.getViolations();
console.log(result);

// to list out WCAG rules
let result = wat.getRules();
console.log(result);

// to run script with custom tag
let result = wat.analyseWithTag(["your-custom-tag"]);
console.log(result);

// to run script with with context enabled
let wat = require('web-accssbility-test');
wat.analyseWithContext([{include: [['#iframe']]}]);

// to get the WCAG recommended best practice

let result = wat.getBestPractice();
console.log(result);

```
### References
[Web Accessibility Initiative (WAI)](https://www.w3.org/WAI/)
[axe-cre](https://github.com/dequelabs/axe-core)


### License
ISC
