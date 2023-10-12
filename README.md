# Docker Firebase Emulator

A Docker image containing [the Firebase emulator](https://firebase.google.com/docs/emulator-suite).
This can be used to setup Firebase emulation in your environment alongside other Docker resources
(e.g. Postgres, Mongo, etc.).

This is useful when you want to develop an application using Firebase, but want a completely local
environment running in Docker for testing

## Configuration

By default, this emulator only runs the Firebase authentication service. However,
you can add your own configuration file and mount it to emulate additional services.

- If you wish to only run the auth service, just run the container as-is (no custom config required).
- By default, the Firebase Emulator UI will be enabled and exposed at [http://localhost:8083/](http://localhost:8083/)
- Firebase config must be mounted at the location `/firebase` in the container
- At a minimum, the mounted config directory must contain a [firebase.json](https://firebase.google.com/docs/cli/#the_firebasejson_file)
  file. Additionally, the directory can contain referenced config, such as Firestore rules
- For an example of mounting custom config, see the [multiple-services-with-rules](./examples/multiple-services-with-rules/)
  example.
