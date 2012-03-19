Mono Heroku Buildpack
=====================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpack) for Mono that will run ASP.NET applications (and other frameworks too).

It serves files using [XSP](http://www.mono-project.com/ASP.NET#ASP.NET_hosting_with_XSP).

Usage
-----

Example usage:

    $ heroku create --stack cedar --buildpack http://github.com/rodrigoi/heroku-buildpack-mono.git
    $ git push heroku master

The buildpack will detect your app as Mono if it has the file `global.asax` in the root or at one directory depth.

TODO
----

1. Add kayak as a lightweight, event based web server.
2. Add nuget.exe to pull dependencies on commit
3. Make deploy conditional to unit test success