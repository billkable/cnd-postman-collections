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
    collection file.

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

Use the Postman Runner to