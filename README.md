# README

## Postman scripts for Cloud Native Developer course

For the PAL tracker distributed application, it is cumbersome
to use curl, and correlate requests for all the 4 apps.

You can use the Postman collection and associate environments
here to verify or experiment with your local or PCF hosted
running apps.

## Prerequisites

-   Postman v2.1 or above
-   Pal Tracker Distributed application running locally and/or
    Remotely on PCF.

## Installation

1.  Clone or fork this repo, or download the individual files.

1.  Replace the `{unique-identifier}` and `{your-domain}`
    tags in the `pal-tracker-distributed-pcf.postman_environment.json`
    environment file with the values of running PAL Tracker distributed running on PCF (or PWS) you configured
    in the associated manifest files.

1.  Import the `PAL-Tracker-Distributed.postman_collection.json`
    collection file for labs before *Securing a Distributed System*.
    For *Securing a Distributed System* and *Config Server* labs,
    import the `PAL-Distributed-Oauth-PWS.postman_collection.json`
    collection.
    You will need to generate the access token and set the `Bearer`
    token header through postman for successful authentication.

1.  Import both the environment files:

    `pal-tracker-distributed-local.postman_environment.json`

    and

    `pal-tracker-distributed-pcf.postman_environment.json`

## Usage

You can run the collection out-of-box with no additional
updates; however, you may want to customize the user, project
or story name prefixes.
You can customize in the local and/or pcf environments
for the following variables:

-   Project Name:
    `projectNamePrefix`

-   Project Name:
    `userNamePrefix`

-   Project Name:
    `storyNamePrefix`

### Automated Test

Use the Postman Collection Runner to run the automated tests:

1.  Launch the Runner.

1.  Select the `PAL-Tracker-Distributed` collection.

1.  Select the `Primary Workflow` folder.

1.  Select `pal-tracker-distributed-local` environment for running
    against your local running deployment.

    OR

1.  Select `pal-tracker-distributed-pcf` environment for running
    against your remote PCF running deployment.

1.  Click `Run PAL Tracker...` button.

The Operations in the Primary Workflow and sub folders are set up
to correlate requests automatically, and assert the expected
Http return status codes.

You can use Postman runner to verify success or failures, and the
Postman console to troubleshoot request failures.