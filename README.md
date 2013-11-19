# Buildpack: Java Web Container
This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for Java web applications. It accepts a pre-built war file and uses OpenJDK to run it.

This build pack currently supports the following containers.

* [JBoss AS 7.1.1](http://www.jboss.org/jbossas) -- keyword: `jboss-as-7`

## Choose a Container
Create a `container.properties` file in the root of your project directory and set `container` to the keyword for the container you want. e.g. `jboss-as-7`.

```
$ echo 'container=jboss-as-7' > container.properties
```

The buildpack automatically deploys all wars in the `webapps` directory of your project. If you want to deploy a war to the root context, name it `ROOT.war`.

## Choose a JDK (optional)
Create a `system.properties` file in the root of your project directory and set `java.runtime.version` to your desired version, for example, `1.7`.

```
$ echo 'java.runtime.version=1.6' > system.properties
```
