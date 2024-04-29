# Gin Quickstart Guide

In this quickstart guide, we'll walk you through the process of setting up a Gin web application, from installation to running your first server. Let's dive in!

## Requirements

Before we begin, ensure you have the following prerequisites installed:

- Go 1.13 or above

## Installation

To install the Gin package, follow these steps:

1. Download and install Gin:
   ```bash
   $ go get -u github.com/gin-gonic/gin
   ```

2. Import Gin in your code:
   ```go
   import "github.com/gin-gonic/gin"
   ```

3. (Optional) Import net/http if using constants such as http.StatusOK:
   ```go
   import "net/http"
   ```

## Getting Started

### Step 1: Create a Project Folder

Create your project folder and navigate inside it:
   ```bash
   $ mkdir -p $GOPATH/src/github.com/myusername/project && cd "$_"
   ```

### Step 2: Copy a Starting Template

Copy a starting template inside your project. For example, you can use the basic template from Gin's examples:
   ```bash
   $ curl https://raw.githubusercontent.com/gin-gonic/examples/master/basic/main.go > main.go
   ```

### Step 3: Write Your Code

Create a file called `example.go` and add the following code:

```go
package main

import "github.com/gin-gonic/gin"

func main() {
    r := gin.Default()
    r.GET("/ping", func(c *gin.Context) {
        c.JSON(200, gin.H{
            "message": "pong",
        })
    })
    r.Run() // listen and serve on 0.0.0.0:8080
}
```

### Step 4: Run Your Project

Run your project using the `go run` command:
   ```bash
   $ go run example.go
   ```

### Step 5: Test Your Server

Visit `0.0.0.0:8080/ping` on your browser to see the response "pong".

Congratulations! You've successfully set up and run your first Gin web application. Now you're ready to explore more features and build powerful web services with Gin.

For further learning and documentation, visit the [Gin GitHub repository](https://github.com/gin-gonic/gin).
```