# Web-component-tester issue with dynamic HTML Imports with Polymer

This is the test-case for a strange issue with web-component-tester
[#354](https://github.com/Polymer/web-component-tester/issues/354).

In polyfilled browsers (IE, Safari) an exception is thrown, when a test-suite loads HTML Import with Polymer dynamically.
It only happens when run on [polyserve](https://github.com/PolymerLabs/polyserve).

## Steps to reproduce:

1. Clone the repo,
2. Install polyserve `npm install -g polyserve`,
3. Run `polyserve`,
4. Open IE/Safari with devtools opened,
5. Open http://localhost:8080/components/WCT-HTML-Imports-issue/

## Expected behavior
Everything should execute silently. See Chrome.

## Result

You will see `Object expected` error
![Error thrown](https://raw.githubusercontent.com/tomalec/WCT-HTML-Imports-issue/gh-pages/error.png)
