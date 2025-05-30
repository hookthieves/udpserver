UDP Server
A simple UDP server written in C that listens for incoming messages on a specified port and prints them to the console. This project is designed for red teaming exercises to test network communication and message handling.
Features

Listens for UDP messages on port 8080.
Displays the sender's IP address, port, and message content.
Includes basic error handling for socket creation and binding.

Prerequisites

A C compiler (e.g., gcc)
Linux/Unix-based system with standard networking libraries

Installation

Clone the repository:git clone https://github.com/yourusername/udp-server.git


Navigate to the project directory:cd udp-server


Compile the code:gcc udp_server.c -o udp_server



Usage

Run the server:./udp_server


The server will listen on port 8080 for incoming UDP messages.
Send a test message using a tool like netcat:echo "Test message" | nc -u 127.0.0.1 8080


The server will print the received message along with the client's IP and port.

Notes

The server runs indefinitely until manually stopped (Ctrl+C).
The port number (8080) is defined in the code (PORT macro) and can be modified as needed.
Ensure the port is not blocked by a firewall or already in use.

License
MIT License
Contributing
Feel free to submit issues or pull requests for improvements or bug fixes.
