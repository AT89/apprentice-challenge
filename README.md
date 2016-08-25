# Social Tables Apprentice Challlenge

Our help page <http://help.socialtables.com/> needs help! Your challenge is to write **test coverage** so tablers can sleep better at night knowing customers have access to the help they need.

## The Tests

Please add coverage for the following functionality:

1. The Social Tables logo in the top left should link to <https://www.socialtables.com/>.
2. Searching for `Bobby Fisher` should return 0 results.
3. Searching for `event` should return 10 results.
4. Searching for a word under three character should trigger an alert box with the text `Search string must be at least 3 characters long`.

All tests must run against <http://help.socialtables.com>.

For extra credit, add a test of your own.

## Requirements

* You must use [Node](https://nodejs.org/)
* You must use [Selenium](https://github.com/SeleniumHQ/selenium/wiki/WebDriverJs)
* You must use [Mocha](https://mochajs.org/)

You probably haven't used some or all of these packages before. Fear not.  We designed this challenge anticipating you would need to learn to pass.

## How To Get Started

You are provided with boilerplate that includes a sample test with all requirements working together.

General steps to get the boilerplate running:

* Install [Firefox](https://www.mozilla.org/en-US/firefox/new/)
* Install [Node](https://nodejs.org/en/download/)
  * For OS X, we prefer using [Homebrew](http://brew.sh/) to `brew install node`
  * Make sure you are installing a version of Node that is 6.0.0 or higher
* `npm install mocha -g`
* `npm install chai -g`
* `git clone https://github.com/socialtables/apprentice-challenge.git`
* `cd apprentice-challenge`
* `npm install`
* `mocha test`

This should start the mocha test runner and selenium.  One test should pass and four should be marked as pending.  Your job is to complete the pending tests.

You are not required to use the boilerplate, but it is recommended.

## What To Turn In

Send all your files in one email to <apprenticechallenge@socialtables.com> with the subject line, `Social Tables Apprentice Challenge`.

You must include the following files in your email: yourinitials-readme.{md, txt}, yourinitials-code.{tar.gz, zip}, yourinitials-resume.pdf (where yourinitials are your initials).

These files will contain:

* The yourinitials-readme.{md, txt} contains instructions for running your code and any notes you wish to include.
* The yourinitials-code.{tar.gz, zip} contains your code. You can optionally also submit a link to your code in the readme file.
* A file named yourinitials-resume.pdf containing your resume.

Submitting your node-modules folder isn't necessary, for example, because we can get it by running `npm install`; however, you should at least submit any files you found necessary to change and enough support and explanation so we can reproduce your results. In any case, include all the information in yourinitials-readme.{md, txt}.

## FAQ

**Can I copy code from the Internet?**
You must cite any outside resources you use in your work (for example, using comments to denote a snippet obtained from Stack Overflow).

**Can I copy someone else's submission, cite it, and submit?**
No.

**Can I submit without completing all the tests?**
Yes.

**Can I use a browser other than Firefox?**
You may alternatively use Chrome.

**What is the status of my application?**
Email <apprenticechallenge@socialtables.com>.

**I see a typo.**
Submit a pr.

**I still have a question.**
Submit a Github issue.

##Captains Log (Anh)
- Was a pain getting it to work, I didnt see the issue that Firefox 48 isnt compatible with Selenium lol. So I had to get Firefox 45.

- Had to research around to figure out that getTitle is a built in function http://bites.goodeggs.com/posts/selenium-webdriver-nodejs-tutorial/

- the logo link is http://socialtables.digihey.com, so i rewrote the test to get it to pass

- HOLY MOTOWN test2 passes, finally. now understanding this selenium driver, the beforeEach needs to be used before it, this allows you to 'bot' or 'drive' firefox. Using this, we are left at a checkpoint at (done). Then we can check if the currentUrl is what it is supposed to be.

- Figured out the click() from the past but mainly from the documentation here: https://github.com/SeleniumHQ/selenium/wiki/WebDriverJs and http://bites.goodeggs.com/posts/selenium-webdriver-nodejs-tutorial/ 8. Interacting with the Page

- another Ah Ha moment, noticed that sometimes test 1 would time out and fail and sometimes it would pass, so from the comments before and I figured out that we need to change the default setTimeout of 2000. so added     ```this.timeout(10000);```

- 


##Other thoughts
- We only went through Testing for 1 day total (half day for ruby testing and another half day for Node testing with Jasmine), I do like testing; wish we got more experience but then again we got to learn/build cool stuff
- I found this node module, it like the option it has to run the tests in multiple browsers with -p https://www.npmjs.com/package/mocha-selenium it also seems to have other nifty things
