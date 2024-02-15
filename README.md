# koron-go/skkdict

[![PkgGoDev](https://pkg.go.dev/badge/github.com/koron-go/skkdict)](https://pkg.go.dev/github.com/koron-go/skkdict)
[![Actions/Go](https://github.com/koron-go/skkdict/workflows/Go/badge.svg)](https://github.com/koron-go/skkdict/actions?query=workflow%3AGo)
[![Go Report Card](https://goreportcard.com/badge/github.com/koron-go/skkdict)](https://goreportcard.com/report/github.com/koron-go/skkdict)

## Usage Example

```go
import skkdict "github.com/koron-go/skkdict"

f, err := os.Open("SKK-JISYO.utf-8.S")
if err != nil {
	panic(err)
}
defer f.Close()

r := skkdict.NewReader(f)
for {
	entry, err := r.Read()
	if err != nil {
		break
	}
	fmt.Printf("%+v\n", entry)
}
```

## Previous Work

<https://github.com/koron/go-skkdict>
