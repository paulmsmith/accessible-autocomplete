# Contributing

Contributions welcome, please raise a pull request.

If you want to help and want to get more familiar with the codebase, try starting with the ["good for beginners"](https://github.com/alphagov/accessible-autocomplete/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+for+beginners%22) issues. Feel free to request more guidance in the issue comments.

To develop locally:

```bash
npm install
npm run dev
```

Contributions will need to pass the linter and tests. To run everything once:

```bash
npm test
```

To run the functional tests in dev mode (automatically reruns when a file changes):

```bash
npm run karma:dev
```

To run the integration tests locally with Chrome (specified in [wdio.config.js](test/wdio.config.js)):

```bash
npm run wdio
```

To run the integration tests on [Sauce Labs](https://saucelabs.com/), create a `.env` file with the following:

```bash
SAUCE_ENABLED="true"
SAUCE_USERNAME="XXXXXXXX"
SAUCE_ACCESS_KEY="YYYYYYYY"
```

And run the same command:

```bash
npm run wdio
```

Failed integration tests should output screenshots to the `./screenshots/` folder.

## Cutting a new release

```bash
vim CHANGELOG.md # Update changelog, put all unreleased changes under new heading.
git commit -am "Update changelog"
npm version <major|minor|patch>
npm publish
```
