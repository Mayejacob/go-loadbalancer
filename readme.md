# Go Load Balancer

This Go project implements a simple load balancer that distributes incoming HTTP requests among multiple backend servers.

## Table of Contents

- [Overview](#overview)
- [Usage](#usage)
- [Server Configuration](#server-configuration)
- [Load Balancer Configuration](#load-balancer-configuration)


## Overview

The Go Load Balancer project consists of a simple load balancing algorithm that evenly distributes HTTP requests among multiple backend servers. It uses a round-robin approach to route incoming requests to available servers.

## Usage

To use the load balancer, follow the steps below:

1. Clone the repository:

    ```bash
    git clone https://github.com/Mayejacob/go-loadbalancer.git
    ```

2. Change to the project directory:

    ```bash
    cd go-load-balancer
    ```

3. Run the load balancer:

    ```bash
    go run main.go
    ```

4. The load balancer will be accessible at `http://localhost:8000`.

## Server Configuration

The backend servers are defined in the `main.go` file. You can add or remove servers as needed:

```go
servers := []Server{
    newSimpleServer("https://www.facebook.com"),
    newSimpleServer("https://www.bing.com"),
    newSimpleServer("https://www.duckduckgo.com"),
}
