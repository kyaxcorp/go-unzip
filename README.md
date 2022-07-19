Package go-unzip
===================

Package go-unzip provides a very simple library to extract zip archive

## Installation
```shell
go get -u github.com/kyaxcorp/go-unzip
```

## Examples

```go
package main

import (
	"fmt"
	"github.com/kyaxcorp/go-unzip"
)

func main() {
	uz := unzip.New()

	files, err := uz.Extract("./data/file.zip", "./data/directory")
	if err != nil {
		fmt.Println(err)
	}

	fmt.Printf("extracted files count: %d", len(files))
	fmt.Printf("files list: %v", files)
}
```
