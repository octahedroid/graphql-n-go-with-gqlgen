# graphql-n-go-with-gqlgen
This is the roadmap to learn GraphQL implemented on Go (golang) with gqlgen.

* Setup gqlgen
  * Setup the graphql server
* Code slightly more realistic
  * Complete the example from "getting started" documentation
* Custom example (may the force be with you)
  * Create a custom types and resolvers, with the Starwars example
* Handling errors
  * Make more robust our code, handling errors
* Apollo Federation
  * Create more graphql servers, and connect between that
* Connect with a persistent layer
  * Now add a database server to save the data
* Make testing scripts
  * Script with bash to test all steps until this point


Instructions. This repo is organized in steps to demonstrate, one by one, the progress in learning of gqlgen. Each of these steps is related to one tag or release of this repo, so you can jump to the tag of your interest or go one by one.
## Step 1. Setup gqlgen

First you can starting here https://gqlgen.com/getting-started/ the code what is demonstrated on this step.

```bash
$ mkdir learn-gqlgen
$ cd learn-gqlgen/
$ go mod init github.com/eisenheimjelid/learn-gqlgen
$ go get github.com/99designs/gqlgen
$ go run github.com/99designs/gqlgen init
Exec "go run ./server.go" to start GraphQL server
$ go run server.go 
2021/03/02 16:29:48 connect to http://localhost:8080/ for GraphQL playground
```


## Step 2. Add code slightly more realistic

Add new `graph/model/todo.go`, regenerate the code and implement the new resolver into `graph/schema.resolvers.go`.

```bash
$ go generate
$ go run server.go 
2021/03/02 20:35:39 connect to http://localhost:8080/ for GraphQL playground
```

Tip. Add this comment to `resolver.go` for reduce time, and avoid the `go generate` command.
`//go:generate go run github.com/99designs/gqlgen`

