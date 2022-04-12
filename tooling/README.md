User must have gitbook-cli installed with version 4.2.0 of graceful-fs
This means going to this repo's node_modules/gitbook-cli/node_modules/npm/node_modules and running `npm install graceful-fs@4.2.0`

See https://stackoverflow.com/questions/64211386/gitbook-cli-install-error-typeerror-cb-apply-is-not-a-function-inside-graceful

Local testing: `npm run docs:serve` (http://localhost:4000)
Build: `npm run docs:build`
