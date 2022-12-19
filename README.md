# API Catalog - Continuous Integration Example

This example shows how to implement a Continuous Integration (CI) solution for cataloging APIs using API Cataloging CLI.

In this display, we are automating the cataloging process of a single API as part of its deployment using a Jenkins pipeline. We provide a baseline catalog.yaml file and a documentation structure that can be adapted or extended as needed.

## Prerequisites

1. A valid version of Jenkins is installed and ready to be used
2. A valid version of Node.js is installed and configured to be used by Jenkins.

## How to use it

1. Clone the contents of this github repository
2. Review and adapt the content of the markdown documents (.md) presented inside the /api/documentation directory
3. Review and adapt the content of the descriptor file named catalog.yaml presented inside the /api directory
4. Review and adapt the content of the Jenkisfile named anypoint-api-cataloging-example-ci.jenkinsfile presented inside the /jenkins directory
5. Define the following Jenkins secrets within your Jenkins instance:
* anypoint.platform.org.id=\<Your Anypoint Platform Org ID value\>
* anypoint.platform.cataloging.clientId=\<Your Connected App Client ID value\>
* anypoint.platform.cataloging.clientSecret=\<Your Connected App Client Secret value\>
6. Run the pipeline

The pipeline consists of 3 main stages:
* Stage 1: Checkout the release code
* Stage 2: Downloading Anypoint Cataloging CLI. This stage can be skipped if the tool is already installed within the worker running the jenkins pipeline
* Stage 3: Cataloging the API in Anypoint Platform