# Docker Firebase Emulator

A Docker image containing [the Firebase emulator](https://firebase.google.com/docs/emulator-suite).
This can be used to setup Firebase emulation in your environment alongside other Docker resources
(e.g. Postgres, Mongo, etc.).

This is useful when you want to develop an application using Firebase, but want a completely local
environment running in Docker for testing

## Configuration

By default, this emulator only runs the Firebase authentication service. However,
you can add your own configuration file and mount it
