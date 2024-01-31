

# Runway Example java App

This is an example app demonstrating how to deploy a java app
to [runway](https://runway.planetary-quantum.com/).

* clone this repo, and navigate into that directory
* `runway app create`
* `runway app deploy`
* `runway open`

You can then deploy changes by `git commit`ing them, and running `runway app
deploy` again.

## Tuning Memory Usage

In order for the app to fit into the smaller runway plans, you'll need to adjust
some runtime config options, via something like:

* `runway app config set BPL_JVM_THREAD_COUNT=3 JAVA_TOOL_OPTIONS=-XX:ReservedCodeCacheSize=16M`

(additional documentation is available at https://github.com/paketo-buildpacks/bellsoft-liberica?tab=readme-ov-file#configuration)

---

This app uses Gradle and Spring Boot - additional documentation for other kinds
of java apps is available at https://paketo.io/docs/howto/java/.

You can run the application with the following command on localhost:

```sh
./gradlew bootRun # (or just "gradle bootRun" if you have gradle installed)
```

(and then go to http://localhost:5000/)

