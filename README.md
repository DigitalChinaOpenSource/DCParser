# DCParser - SQL Parser optimized based on PingCAP/parser

[![Go Report Card](https://goreportcard.com/badge/github.com/DigitalChinaOpenSource/DCParser)](https://goreportcard.com/report/github.com/DigitalChinaOpenSource/DCParser)
[![GoDoc](https://godoc.org/github.com/DigitalChinaOpenSource/DCParser?status.svg)](https://godoc.org/github.com/DigitalChinaOpenSource/DCParser)
[![codecov](https://codecov.io/gh/DigitalChinaOpenSource/DCParser/branch/main/graph/badge.svg?token=6MGSRZAQE0)](https://codecov.io/gh/DigitalChinaOpenSource/DCParser)

## Introduction

DCParser is a single project built for compatibility with TiDB for PostgreSQL. It is based on PingCAP/parser, but it is difficult to merge into the original parser repository because there are many changes. So a new project is created to provide parsing abilities for TiDB for PostgreSQL.

## Development

The current development is driven by the implementation of TiDB for PostgreSQL. The implements of Schema structure, system functions, system views and other functions of TiDB for PostgreSQL depend on the parser modification. Currently, the DCParser can fully meet the functional requirements of the TiDB for PostgreSQL. If TiDB for PostgreSQL needs new system functions, system views and other functions, you also need to modify them in DCParser.

## Quick start

DCParser project is the sql parser of TiDB for PostgreSQL. The most common way to use it is to import it into the TiDB for PostgreSQL project and play its role by parsing sql statements.

DCParser is written in Go language. SO to use DCParser, you need to ensure that the Go environment is installed.

In the TiDB for PostgreSQL project, it has been declared that DCParser needs to be pulled. You can use the vendor command to get the project before compiling the project.

In the GOPATH of the development environment, there will be the source files of the DCParser project that TiDB for PostgreSQL depends on. Modify the parser.y file, and then use the following command to compile the new parser.go file.

```shell
goyacc -o parser.go parser.y 
```





## Contributing

We greatly welcome and appreciate developers to contribute to DCParser to realize other features of TiDB for PostgreSQL.

## License

The license is pending.
