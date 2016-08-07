# Homework User Story

## User Story
As an instructor, I want to you to deploy the application to the Cloud Foundry
PaaS so you can see the level of simplicity and application management PaaS
provides over IaaS.

## Acceptance Criteria
* I should receive a single email per team
* The email should contain the name of the individuals on your team
* The email should contain a link to your Github repository
* The email should contain a link to your running application in Cloud Foundry
* I should be able to use the application to upload an image


# Pivotal's Cloud Foundry
Sign up for a free account -

http://run.pivotal.io/

# Download the Cloud Foundry CLI
You use Cloud Foundry's command line interface (CLI) to push applications -

https://docs.cloudfoundry.org/cf-cli/install-go-cli.html

# manifest.yml
The Cloud Foundry's CLI will use the manifest.yml file found in the image
gallery's directory.  You will need to change the name attribute to something
unique.

You can read more about the manifest files here -

https://docs.cloudfoundry.org/devguide/deploy-apps/manifest.html

# Pushing to Cloud Foundry

After the application's jar file is built, you will use the Cloud Foundry command
line interface to push the application.

Issue the login command to log into your Cloud Foundry account -

    cf login

You maybe asked for an API endpoint.  Use the following URL - https://api.run.pivotal.io

You can now push your application.  Here is a sample push command -

    cf push -p .\build\libs\image-gallery-0.1.0.jar -b https://github.com/cloudfoundry/java-buildpack.git

This push command could be simplified by adding the JAR file name and buildpack
to the application's manifest.yml.
