# Notion Sandbox
This is an API sandbox for the [Notion API](https://developers.notion.com/), using an OpenAPI specification with examples, Microcks and Bruno as the sandbox interface, and this GitHub repository as the vehicle for delivering a localized sandbox.

## Capability-Driven
This sandbox is capability-driven, using an early [prototype of the Naftiko capability schema as the manifest](capability-notion-sandbox.yml). The manifest provides the mapping to the OpenAPI source for the sandbox and guides the evolution of the sandbox, aligning with business outcomes—something we will keep iterating on.

## OpenAPI
This sandbox uses OpenAPI as the definition, providing [a complete definition of all available paths for the Notion API](openapi/notion-openapi.yml). This OpenAPI uses examples and Microcks extensions to mock the requests and responses for each API operation, something we will iterate and expand upon with richer examples as we move forward.

## Microcks
This sandbox uses Microcks to deliver the mock API. [You just install Microcks, with the Docker extension being the easiest](https://microcks.io/documentation/guides/installation/docker-desktop-extension/), [import the OpenAPI as a service](openapi/notion-openapi.yml), and you have a mocked API for the entire Notion API, available via REST and MCP APIs--providing a multi-protocol sandbox.

## Bruno
This sandbox [uses Bruno as the client](https://www.usebruno.com/), leveraging a [Bruno Collection](bruno/Notion+API/) pre-generated from the OpenAPI and a [Bruno environment](bruno/Notion+API/environments/) that uses the localhost and port of Microcks to work with the mocked API. You just have to install Microcks, then open the collection provided in this repository, select the available environment, and begin calling the Notion API via the sandbox.

## Work
This is just the initial draft of this repository, and there is more work to be done to make it deliver everything possible using these open-source specifications and tooling:

- **Examples** - More work is needed to continue refining the available examples and make them reflect different scenarios.
- **Microcks Examples** - I'd like to evolve the examples to use Microcks examples to more easily allow them to be independently evolved and iterated upon.
- **Defaults** - More work is needed on the default values for the OpenAPI parameters and bodies to make everything work smoothly.
- **Errors** - More Dispatcher work is needed to get all the unhappy path responses to work as expected for 4xx and 5xx errors.
- **Backstage** - We will add a Backstage software catalog entity for the sandbox, allowing it to be distributed to Backstage.

## Support
Please provide any questions or feedback via GitHub issues, or just email kinlane@naftiko.io with feedback. The goal is to keep iterating upon this sandbox using existing OpenAPI, Microcks, and Bruno features, offering value out of the box via this forkable third-party Notion API sandbox.


