# Call your code from another module

## Run


```
$ cd hello
$ go run .
hello.go:6:5: no required module provides package example.com/greetings; to add it:
        go get example.com/greetings
```
## Redirect module

Use the go mod edit command to edit the example.com/hello module to redirect Go tools from its module path (where the module isn't) to the local directory (where it is).
  
```
$ go mod edit -replace example.com/greetings=../greetings
```
## Synchronize module's dependencies

```
$ go mod tidy
```
## Running

```
$ go run .
Hi, Gladys. Welcome!
```

## Reference
- https://golang.org/doc/tutorial/call-module-code
