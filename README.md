

# Runway Example java App

This is an example app demonstrating how to deploy a java app
to [runway](https://runway.planetary-quantum.com/).

* clone this repo, and navigate into that directory
* `runway app create`
* `runway app deploy`
* `runway open`

You can then deploy changes by `git commit`ing them, and running `runway app
deploy` again.

You can run the application with the following command on localhost:

```sh
./gradlew bootRun
```

