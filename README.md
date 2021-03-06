# apiai-go

A simple wrapper over API.ai HTTP API. 

## To get this package

```
go get github.com/kamalpy/apiai-go
```


## Usage

Create an API.ai instance

```
    ai := apiaigo.APIAI{
		AuthToken: <API.ai Authentication Token>,
		Language:  "en-US",
		SessionID: <SessionID Here>,
		Version:   <Version latest: "20150910">,
	}
```

### To send a text query

```
	resp, err := ai.SendText("make me a sandwich")
```

`resp` is a `ResponseStruct` instance. It is defined in response.go.

### For text to speech
```
	// filepath to save the wav file
	err := ai.TTS("sudo make me a sandwich", <filepath>)

```

### Custom Query

You can also create your own `QueryStruct` instance and pass it directly to `ai.Response()`.
