# 🌀 GRB - Load Balancer 

A simple round-robin load balancer implemented in Go using the `net/http` and `httputil` packages. It forwards incoming requests to a pool of upstream servers.

## ✅ Requirements

- Go 1.16 or higher → [https://golang.org/dl/](https://golang.org/dl/)

### Optional for testing:
- `curl` or Postman

## 📦 Setup

### 1. Clone the repository

```bash
git clone https://github.com/DinethDilhara/grb-loadbalancer.git
```
```
cd grb-loadbalancer/src
```

### 2. Run the server

```bash
go run main.go
```

This will start the load balancer on `http://localhost:8080`.

## 🔁 How It Works

- The load balancer maintains a list of backend servers.

This example proxies to:

 `https://github.com`
 `https://www.facebook.com`
 `https://www.google.com`

> ⚠️ These are public websites and may block or redirect reverse proxy traffic. Use internal or test servers in a real-world scenario

- Each incoming request is forwarded to the next available server using round-robin logic.
- You can modify the list of backend servers in the `main()` function.

