# Golang gRPC demo
<br>

## Why?

In a REST or GraphQL architecture we have
Client sending request
Server giving response

But this process is

- Slow
- Synchronous
- Not Scalable
  
---

## How?

<p>How to make the client server intercation Scalable?
<div></div>For that we use Remote Procedure Calls (RPC)</div></p>

RPC directly calls functions from client to server Instead of JSON, we use protobuf files Here, payload size is small and accelerates communication

- Client Server communication can happen via Streaming (sequences of mesages)
- Stream is continous flow of data
- Its asynchronous
- Extremely scalable
  
Usecase: MICROSERVICES!, Blockchains

---

There are mainly 4 types of communications in GRPC
### 1. Unary API

- Regular request-response

### 2. Server Streaming

- Client sends a request to server

- Server sends a strea of data to client

### 3. Client Streaming

- Client sends a stream of data to server

- Server provides a siple response to client

### 4. Bi-Directional Streaming

- Both client and server can communicate via streaming.

- And they can do this parallely,

- Not like request response wehre client sneds first and then server gives response - not like this.

- Its like a two way-traffic

- Even though its a stream, not a queue, sequence of messages is preserved
  
---

## To Run the project
Install the dependencies
```bash
go mod tidy
```
Update the Path

```bash
export PATH="$PATH:$(go env GOPATH)/bin"
```

Run the server

```bash
go run server/main.go
```
Run the client
```bash
go run client/main.go
```
For Go-grpc check [Official docs](https://grpc.io/docs/languages/go/quickstart/)
