# xml-json

convert xml to json on the command line. not streaming, pure javascript

[![NPM](https://nodei.co/npm/xml-json.png?global=true)](https://nodei.co/npm/xml-json/)

## usage

```
npm install xml-json -g
xml-json <file>
```

or `cat something.xml | xml-json`

## example

```
curl "http://webservices.nextbus.com/service/publicXMLFeed?command=vehicleLocations&a=actransit" | xml-json
{
  "body": {
    "$": {
      "copyright": "All data copyright AC Transit 2014."
    },
    "Error": [
      {
        "_": "\n  last time \"t\" parameter must be specified in query string\n",
        "$": {
          "shouldRetry": "false"
        }
      }
    ],
    "vehicle": [
      {
        "$": {
          "id": "5005",
          "routeTag": "31",
          "dirTag": "31_51_0",
          "lat": "37.8046264",
          "lon": "-122.2770156",
          "secsSinceReport": "51",
          "predictable": "true",
          "heading": "206",
          "speedKmHr": "0"
        }
      },
      // etc
    ],
    "lastTime": [
      {
        "$": {
          "time": "1403999101266"
        }
      }
    ]
  }
}
```
