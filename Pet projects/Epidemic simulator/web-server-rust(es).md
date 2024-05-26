---
Date: 2024-04-14
tags:
  - project
  - programming
  - rust
  - backend
links: https://github.com/vvtttvv/Epidemic-Simulator/blob/backend/back/src/main.rs
---
## Overview
It s a web server written in [[Rust]] that uses [[WebSockets]] protocol 
## Parts
### Main

The `WebSocket` part contains the main server logic. It handles incoming TCP connections, reads data from clients, processes the data using the algorithm part, and sends back responses.
### Algorithm

The `algorithm` part contains the logic for processing the data received from the frontend. It simulates an algorithm that generates a vector of structures representing the responses. The algorithm's behavior can be customized by changing the parameters.

## Usage

1. Start the server by running the executable.
2. Send data to the server using a TCP client (e.g., telnet, curl).
3. The server will process the data and send back responses in json format.

## Example

### Sending Data

Sent data should be in this format:
```json
{
	"parametr_name": "parametr_value",
	... ,
	...,
}
```
In the list should be all the parameters needed for algorithm
### Response

The server will respond with a json array containing the algorithm's simulated responses:
```json
[     
{  "id": "value", "position_x": "value", "position_y": "value", "infected": "value", "dead": "value"},     
{.....},
... ,
]
```

For all points that are simulated(the response will be sent several times per second, depending of frame rate)
## Dependencies
```rust
// Cargo.toml
tokio = { version = "1", features = ["full"] }
tokio-tungstenite = "0.14"
futures = "0.3"
serde = { version = "1.0", features = ["derive"] }
serde_json = "1.0"
rand = "0.8"
```
## Code explanation

### Imports
The code imports several libraries used for various functionalities:
- `tokio` and `tokio_tungstenite` for handling asynchronous tasks and WebSocket communication.
- `rand` for random number generation.
- `serde` for JSON serialization.

### Individual Struct
Defines a struct `Individual` to represent an individual in a population:
- Fields: `id`, `position`, `movement_speed`, `grid_size`, `is_infected`, `infected_time`, `alive`.
- Methods: `new`, `move_ind`, and `dead_treated` to initialize, move, and handle life status of individuals.

### distance Function
Defines a function `distance` to calculate the Euclidean distance between two points.

### Main Function
Sets up a TCP listener on port 8080 and accepts incoming connections:
- Spawns a new asynchronous task (`handle_connection`) for each connection.

### handle_connection Function
Handles the WebSocket connection with each client:
- Parses incoming messages as JSON.
- Initializes a population of individuals and simulates their movements and interactions.
- Sends the updated population as a JSON message back to the client every 17 milliseconds.

### get_local_ip Function
Retrieves the local IPv4 address of the server:
- Binds a UDP socket to a random port and connects to a known IP address (`8.8.8.8`).
- Retrieves the local address of the socket.

Overall, the code demonstrates a simple simulation of a population where individuals can move, become infected, and potentially die based on certain probabilities. The simulation is run over a WebSocket connection, with the server sending updates to the client periodically.
