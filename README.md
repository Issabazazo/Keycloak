## Setup
Install docker

## Start and configure Keycloak

### Start Keycloak:

#### Docker
Using the image from https://hub.docker.com/r/jboss/keycloak/
```
docker run -p 8080:8080 -e KEYCLOAK_USER=admin -e KEYCLOAK_PASSWORD=admin jboss/keycloak
```
#### Standard
```
/<Path-To-Keycloak>/bin/standalone.sh
```

Open the Keycloak admin console, click on Add Realm, click on import 'Select file', 
select nodejs-example-realm.json and click Create.

Install the dependencies and start NodeJS example by running:

```
npm install
npm start
```

Open the browser at http://localhost:3000/ and login with username: 'user', and password: 'password'.

The issue happening is that after logging in the user is not redirected to the main screen and receiveing error "Could not obtain grant code: Error: 404:Not Found"