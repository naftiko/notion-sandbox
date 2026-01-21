# Notion Sandbox
This is an API sandbox for the [Notion API](https://developers.notion.com/), using an OpenAPI specification with examples, Microcks and Bruno as the sandbox interface, and this GitHub repository as the vehicle for delivering a localized sandbox.

## Capability-Driven
This sandbox is capability-driven, using an early [prototype of the Naftiko capability schema as the manifest](capability-notion-sandbox.yml). The manifest provides the mapping to the OpenAPI source for the sandbox and guides the evolution of the sandbox, aligning with business outcomes—something we will keep iterating upon.

## OpenAPI
This sandbox uses OpenAPI as the definition, providing [a complete definition of all available paths for the Notion API](openapi/notion-openapi.yml). This OpenAPI uses examples and Microcks extensions to mock the requests and responses for each API operation, something we will iterate and expand upon with richer examples as we move forward.

## Microcks
This sandbox uses Microcks to deliver the mock API. [You just install Microcks, with the Docker extension being the easiest](https://microcks.io/documentation/guides/installation/docker-desktop-extension/), [import the OpenAPI as a service](openapi/notion-openapi.yml), and you have a mocked API for the entire Notion API, available via REST and MCP APIs--providing a multi-protocol sandbox.

## Bruno
This sandbox [uses Bruno as the client](https://www.usebruno.com/), leveraging a [Bruno Collection](bruno/Notion+API/) pre-generated from the OpenAPI and a [Bruno environment](bruno/Notion+API/environments/) that uses the localhost and port of Microcks to work with the mocked API. You just have to install Microcks, then open the collection provided in this repository, select the available environment, and begin calling the Notion API via the sandbox.

## Resources
These are the resources available via the Notion API, which are made available via this sandbox API, which are applied as tags to each operation in the OpenAPI.

  - Authentication
  - Blocks
  - Comments
  - Data Sources
  - Databases
  - File Uploads
  - Notion
  - Pages
  - Search
  - Users

## Operations
These are all of the available operations in this sandbox, providing a complete view of what you can do within this sandbox using the mocked Notion API.

  - Create Comments
  - Create Databases
  - Create Datasources
  - Create Datasources Query
  - Create File Uploads
  - Create File Uploads Complete
  - Create File Uploads Send
  - Create Oauth Token
  - Create Oauth Token Introspect
  - Create Oauth Token Refresh
  - Create Oauth Token Revoke
  - Create Pages
  - Create Pages Move
  - Create Search
  - Delete Blocks
  - Patch Blocks
  - Patch Blocks Children
  - Patch Databases
  - Patch Datasources
  - Patch Pages
  - Retrieve Blocks
  - Retrieve Blocks Children
  - Retrieve Comment
  - Retrieve Comments
  - Retrieve Data Sources Template
  - Retrieve Databases
  - Retrieve Datasources
  - Retrieve File Upload
  - Retrieve File Uploads
  - Retrieve Pages
  - Retrieve Page Properties
  - Retrieve User
  - Retrieve Users
  - Retrieve Users Me

## Backstage
We provide a Backstage software catalog entity for the Notion API Sandbox, allowing this sandbox to be registered with any catalog, making it discoverable by team and across an organization--allowing anyone to fork and deploy locally within the enterprise.

## Open Work
This is the current work on the table to keep improving this sandbox, but it is currently 100% functional and ready to use, but will be even better once we tackle the work on this list.

- **Examples** - Continue refining the available examples and make them reflect different business scenarios, and industries.
- **Tests** - Setup a test suite to run automated test against each of the operations, ensuring that each mock operation works.
- **Documentation** - What can we use alongside Microcks, Bruno, and Backstage to help any user see the operations and schema.
- **Un-Happy Paths** - Need to document and continue to standardize how you trigger the un-happy paths for each operation.
- **What Else?** - What else can we do with this sandbox to make it easier to use as part of integration into any developoment workflow.

## Support
Please provide any questions or feedback via GitHub issues, or just email kinlane@naftiko.io with feedback. The goal is to keep iterating upon this sandbox using existing OpenAPI, Microcks, and Bruno features, offering value out of the box via this forkable third-party Notion API sandbox.


