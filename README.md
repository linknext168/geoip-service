geoip-service
=============

A fast in-memory http microservice for looking up MaxMind GeoIP2 and GeoLite2 database.

This allows you to have your own IP to location lookup.

This implementation has been tested and handles more than 30,000(uncached)/110,000(cached) requests per second, and uses less than 100MB memory with no cache.

[![Build Status][1]][2]
[1]: https://travis-ci.org/klauspost/geoip-service.svg
[2]: https://travis-ci.org/klauspost/geoip-service

#Prerequisites
Requires a [go installation](https://golang.org/dl/).

A Database (choose one):
* [Free GeoLite 2 database](http://dev.maxmind.com/geoip/geoip2/geolite2/). Download the "MaxMind DB binary, gzipped" and unpack it.
* [GeoIP2 Downloadable Database](http://dev.maxmind.com/geoip/geoip2/downloadable/). This is a more detailed database and should be compatible, but since I don't have access to that, I have been unable to verify this.

##Building the service
```go get github.com/klauspost/geoip-service```

This should build a "geoip-service" executable in your gopath.
##Binary distributions

You can download binaries for Windows, Linux, OS X and BSD platforms on the [Releases page](https://github.com/klauspost/geoip-service/releases).

##Running the service
Unpack the database to your current directory. Execute ```geoip-service -db=GeoLite2-City.mmdb```. This will start the service on port 5000 on your local computer.
