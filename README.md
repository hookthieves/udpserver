# UDP Server

**UDP Server** is a lightweight **C-based tool** that listens for incoming **UDP messages** on a specified port (default: `8080`) and prints the data to the console. This utility is designed for use in **red teaming scenarios**, **network testing**, and **message handling exercises**.

---

## Overview

This server helps assess UDP communication on target systems and provides a straightforward method to receive and inspect payloads, beacons, or test messages over the network.

---

## Features

- **UDP Listener**: Listens on port `8080` by default.
- **Message Logging**: Displays sender IP, port, and received message.
- **Lightweight**: Minimal external dependencies.
- **Error Handling**: Handles basic socket errors and binding failures.

---

## Prerequisites

- A **C compiler** (e.g., `gcc`)
- A **Linux/Unix-based system**
- Basic networking support (BSD sockets)

---

## Installation

Clone the repository:

```bash
git clone https://github.com/hookthieves/udp-server.git
cd udp-server
````

Compile the source code:

```bash
gcc udp_server.c -o udp_server
```

---

## Usage

Run the server:

```bash
./udp_server
```

The server will begin listening on **UDP port 8080**.

To test, use a tool such as `netcat` from another terminal or host:

```bash
echo "Test message" | nc -u 127.0.0.1 8080
```

### Example Output

```text
Received message from 127.0.0.1:54321
Message: Test message
```

---

## Notes

* The server runs **indefinitely** until manually terminated (`Ctrl+C`).
* The port number is defined as a macro (`PORT`) in the source file and can be modified to suit operational needs.
* Ensure **firewall rules** allow UDP traffic on the desired port.
* This server is **single-threaded** and handles messages sequentially.

---

## License

This project is licensed under the **MIT License**.
See the [LICENSE](LICENSE) file for more information.

---

## Contributing

Contributions are welcome. Submit issues or pull requests to:

* Improve performance
* Add features (e.g., multithreading, logging)
* Fix bugs or improve compatibility

