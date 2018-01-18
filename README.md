# Template for Angular apps

This template is a very basic Angular App created using Angular CLI. It is basically just the default project created using `ng new` but with a few extra features:
* A test environment has been added in addition to dev and prod.
* When build by Jenkins, both a test artifact and a prod artifact will be build. They are both built using the `-prod -sm` flags and only differ by the environment they include. The will be output in `/dist/test` and `/dist/prod' accordingly.
* The image built with Docker will accept the environment variable `PROFILE` for choosing either `test`(default) or `prod`. The chosen profile is injected into nginx in order for it to serve the correct artifact.
