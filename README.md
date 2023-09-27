# SHORTEN URL

## tiny url API

A command-line tool to shorten url and still function effectively. The main aim behind this is to get rid of extremely long URLs  [*Lovely right?*]

This is a very simple Golang project for efficiency, Couldn't guess further more.

## Concept
This simple project seems to make use of the [os](https://pkg.go.dev/os) package. Personally,it was my first time using the [net/http](https://pkg.go.dev/net/http) locally.

## Code Reference
```Go
baseUrl := "http://tinyurl.com/api-create.php?url="
	urlToShorten := os.Args[1]
	getReqUrl := baseUrl + urlToShorten

```

```Go
response, err := http.Get(getReqUrl)
	if err != nil {
		log.Fatal(err)
	}
```


## Run
Program must take not less than two arguments, i.e should include program name and url to be shortened.

My link here to be shortened is: https://github.com/fiificoder/CLI-calculator/blob/master/README.md


```Terminal
./urlToShort www.https://github.com/fiificoder/CLI-calculator/blob/master/README.md
```

```Terminal
go run main.go https://github.com/fiificoder/CLI-calculator/blob/master/README.md
```