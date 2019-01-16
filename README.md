# imodel-query-agent

Copyright © 2019 Bentley Systems, Incorporated. All rights reserved.

imodel-query-agent is an example of an [agent](https://imodeljs.github.io/iModelJs-docs-output//learning/app/#imodel-agents) that illustrates use of the iModel.js API to listen and query changes made to iModels on the iModelHub. A separate optional [imodel-changeset-test-utility](https://github.com/imodeljs/imodel-changeset-test-utility) can be used to generate sample change sets that can then be consumed by this sample.

More specifically, this sample application demonstrates use of iModel.js API to:

* Listen to 'Change Sets' posted to the iModels on the iModelHub.
* Listen to 'Named Versions' created for iModels on the iModelHub.
* Query and download these Change Sets from the iModelHub.
* Parse the Change Sets to construct a 'Change Summary' of useful information contained in them.
* Iterate and query the information contained in the Change Summary.

See http://imodeljs.org for comprehensive documentation on the iModel.js API and the various constructs used in this sample.

## Development Setup

1. (Optional) Create a sample project using the procedure at [Developer Registration](https://imodeljs.github.io/iModelJs-docs-output/getting-started/#developer-registration).  This step is not needed if you already have a project to test with.

1. (Required) Register your application at [Developer Registration](https://imodeljs.github.io/iModelJs-docs-output/getting-started/#developer-registration). For more information, see the section on [authorization](https://imodeljs.github.io/iModelJs-docs-output/learning/common/accesstoken/).

1. Edit [src/QueryAgentConfig.ts](./src/QueryAgentConfig.ts) to set the values you obtained from registration.

1. Install the dependencies with `npm install`

1. Build the source with `npm run build`

1. (Optional) Follow the Development Setup process to setup the [imodel-changeset-test-utility](https://github.com/imodeljs/imodel-changeset-test-utility/blob/master/README.md). The utility can be used to generate and push sample change sets to the iModelHub that can then be consumed by this sample.

## Run Query Agent

1. Start this sample application with `npm start`. Watch the console for various messages that show the progress:
    * Register event handlers that listen to Change Sets being posted to the iModelHub.
    * Register event handlers that listen to Named Versions created on the iModelHub.
    * Receive notification of a new Change Set posted to the iModelHub.
    * Receive notification of a new Named Version created on the iModelHub.
    * Extract Change Summary information from the Change Set.
    * Dump the contents of the Change Summary as a JSON file to disk.

1. (Optional) Immediately start the imodel-changeset-test-utility to generate and push change sets by following the procedure documented in it's [README](https://github.com/imodeljs/imodel-changeset-test-utility/blob/master/README.md).

## Run automated tests

The sample includes some tests to validate it's behavior - these are useful for internal testing:

* Use `npm test` to run unit tests
* Use `npm run test:integration` to run integration tests

## Debugging

To debug the Query Agent Code click the launch configuration `Attach to Main.js` in the debug menu for VS code. Then in your terminal run `npm run start:debug` and wait for breakpoints to be hit.

## Contributing

[Contributing to iModel.js](https://github.com/imodeljs/imodeljs/blob/master/CONTRIBUTING.md)
