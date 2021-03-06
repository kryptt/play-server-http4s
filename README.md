# play-server-http4s

[![Build Status](https://travis-ci.org/knshiro/play-server-http4s.svg)](https://travis-ci.org/knshiro/play-server-http4s)

Experimental [http4s](http://http4s.org/) backend for [Play framework](https://www.playframework.com/).
This is just a proof of concept for the moment and needs work.

## How to use
To use the Akka HTTP server backend you first need to disable the Netty server and add the http4s HTTP server dependency to your project:

```scala
lazy val root = (project in file("."))
  .disablePlugins(PlayNettyServer)

resolvers += "Knshiro's repository" at "https://dl.bintray.com/knshiro/maven"

libraryDependencies += "me.ugo" %% "play-server-http4s" % "0.0.3"
```

## TODO

- SSL
- Websockets
- Better enumerator to stream (and vice-versa) transformations.
