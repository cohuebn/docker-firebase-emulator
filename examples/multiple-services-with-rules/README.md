# Multiple services example

This example shows how to mount a custom Firebase config to run more than just the authentication service.
This example includes:

1. The authentication service
2. Firestore with custom access rules
3. Pub/Sub

To run this example, run `docker compose up` from this directory.

## How does it work?

1. See the [docker-compose.yml](./docker-compose.yml) file
   for the environment setup required to mount custom config and setup port-access
2. Note this volume in that [docker-compose.yml](./docker-compose.yml) file: `- ${PWD}/config:/firebase`. That mounts [the custom config](./config/).
3. In the [the config directory](./config/), the [firebase.json](./config/firebase.json) file configures settings for all three emulated services
4. In that [firebase.json](./config/firebase.json), there
   is a reference to a [firestore.rules](./config/firestore.rules) file which configures access rules for
   the emulated Firestore instance
