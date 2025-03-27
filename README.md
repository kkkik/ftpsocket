
<img src="https://static.pepy.tech/badge/ftpsocket" height="30" /> <img src="https://static.pepy.tech/badge/ftpsocket/month" height="30" />

## About:
**ftpsocket** is a Python library designed to implement FTP server and client functionality using sockets for transferring files over the network. It allows you to send and receive files securely between devices connected to the same network.

---

## Installation:
To install the **ftpsocket** library, run the following command:

```bash
pip install ftpsocket
```

---

Usage Examples

1. Starting the FTP Server:

In this example, we'll create and run an FTP server.

from ftpsocket.server import FTPServer

# Create and start the FTP server on the desired address and port
ftp_server = FTPServer(host='0.0.0.0', port=21)
ftp_server.start()

2. FTP Client Example:

The client connects to the server and sends a file.

from ftpsocket.client import FTPClient

# Connect to an FTP server on a specific address and port
ftp_client = FTPClient(host='127.0.0.1', port=21)  # the local hosted server
ftp_client.connect()

# Send a file to the server
ftp_client.send_file('example.txt')

# Close the connection after the file is sent
ftp_client.close()


---

Explanation:

FTPServer: This class allows you to start an FTP server that listens for incoming client connections, handling file uploads and downloads within the local network.

FTPClient: The client connects to the server, sends files, and manages the connection.



---

Features:

FTP-like server-client file transfer over the network.

Secure connections using Python sockets.



---

Note:
To secure your connection, you can use ftpsocket for FTP-like operations over the network.
