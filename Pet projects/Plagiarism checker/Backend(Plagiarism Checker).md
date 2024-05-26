---
Date: 2024-04-13
tags:
  - project
  - programming
  - backend
  - rust
  - web
---
# Simple HTTP Server in Rust using Tokio

This is a simple HTTP server implemented in Rust using the Tokio framework for asynchronous I/O. It listens for incoming TCP connections on `127.0.0.1:8080` and handles each connection in a separate asynchronous task.

## Dependencies
- `std::error::Error` for error handling
- `tokio::io::{AsyncReadExt, AsyncWriteExt}` for asynchronous I/O operations
- `tokio::net::{TcpListener, TcpStream}` for TCP networking
- `tokio::fs::File` for file operations

## main Function
- Binds the server to `127.0.0.1:8080` and starts listening for incoming connections
- For each incoming connection, spawns a new asynchronous task to handle the client using `handle_client`
- Prints errors encountered while handling clients
## handle_client Function
- Accepts a `TcpStream` representing a client connection
- Writes HTTP response headers to the client, allowing cross-origin requests
- Reads the client's request data until an empty line is encountered, limiting the request size to a certen line
- Extracts the body of the request and saves it to a file named `tmp.txt`
- Closes the client stream

To run the server, compile the code using `cargo build` and then run the executable. Access the server at `http://127.0.0.1:8080` in a web browser or use a tool like `curl` to make HTTP requests.
