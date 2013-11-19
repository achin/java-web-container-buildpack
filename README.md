# Buildpack: Java Web Container
This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for Java web applications. It accepts a pre-built war file and uses OpenJDK to run it.

This build pack currently supports the following containers.

* [JBoss AS 7.1.1](http://www.jboss.org/jbossas) -- keyword: `jboss-as-7`

## Choose a Container
Create a `container.properties` file in the root of your project directory and set `container` to the keyword for the container you want. e.g. `jboss-as-7`.

## Choose a WAR to Deploy
In the same `container.properties` file from above, set `war` to the name of the warfile in the `webapps` directory. Subdirectories are not allowed. This webapp will be deployed to the root context of the container.

## Choose a JDK (optional)
Create a `system.properties` file in the root of your project directory and set `java.runtime.version` to, for example, `1.7`.

# Future Work

* Deploying multiple WARs
* Defining contexts for each WAR
