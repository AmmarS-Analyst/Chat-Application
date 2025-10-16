# Chat Application

A simple Java-based peer-to-peer chat application with GUI that allows users to connect as either host or client and exchange messages in real-time.

![Java](https://img.shields.io/badge/Java-17+-blue)
![Swing](https://img.shields.io/badge/GUI-Swing-orange)

## Features

- 🖥️ **Graphical User Interface** - Built with Java Swing
- 🔄 **Dual Mode Support** - Act as either Host or Client
- 🌐 **Network Communication** - TCP socket-based messaging
- 💬 **Real-time Chat** - Instant message sending and receiving
- 👤 **User Identification** - Personalize with usernames
- 🔌 **Connection Management** - Easy connect/disconnect functionality
- 🎨 **Clean Interface** - Intuitive and user-friendly design


+-----------------------------------------------+
|             Lets Chat                         |
+-----------------------------------------------+
| [Settings Panel]      | [Reply Received]      |
|                       |                       |
| Name: [ Wahaj   ]     | +-------------------+ |
| IP:   [ localhost ]   | | Client: Hello!    | |
| Port: [ 8080     ]    | | You: Hi there!    | |
|                       | | Client: How are u?| |
| ● Host ○ Client       | +-------------------+ |
|                       |                       |
| [Connect] [Disconnect]| [Your Message]       |
|                       | +-------------------+ |
| Status: Connected     | | [Type here...] [S] | |
| To: Ammar             | +-------------------+ |
+-----------------------------------------------+


## Prerequisites

- Java Runtime Environment (JRE) 8 or higher
- Network connectivity between chat participants

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/AmmarS-Analyst/Chat-Application.git
   cd chat-application
   ```

2. **Compile the application**
   ```bash
   javac ChatApp.java
   ```

3. **Run the application**
   ```bash
   java ChatApp
   ```

## Usage

### Starting as Host:

1. Select the **"Host"** radio button
2. Enter your **name** in the "Your Name" field
3. Enter your **IP address** (or use "localhost" for local testing)
4. Enter a **port number** (e.g., 8080)
5. Click **"Connect"**
6. Wait for a client to connect

### Starting as Client:

1. Select the **"Client"** radio button  
2. Enter your **name** in the "Your Name" field
3. Enter the **host's IP address**
4. Enter the **same port number** as the host
5. Click **"Connect"**
6. You'll be connected to the host

### Chatting:

- Type your message in the bottom text area
- Click **"Send"** or press Enter to send messages
- Received messages appear in the top text area
- Click **"Disconnect"** to end the session

## Configuration

| Field | Description | Example |
|-------|-------------|---------|
| **Your Name** | Your display name | `Ammar` |
| **IP Address** | Host IP address | `localhost` or `192.168.1.100` |
| **Port Number** | Communication port | `8080`, `1234` |

## Network Setup

### For Local Testing:
- Use `localhost` as IP address for both host and client
- Ensure both instances use the same port number

### For Network Testing:
- Host should use their local IP address (e.g., `192.168.1.100`)
- Client should connect to the host's IP address
- Ensure firewall allows connections on the specified port

## Project Structure

```
chat-application/
├── ChatApp.java          # Main application class
├── icon.png             # Application icon (optional)
├── README.md           # This file
└── LICENSE             # MIT License
```

## Technical Details

- **Framework**: Java Swing for GUI
- **Networking**: Java Sockets (TCP)
- **Streams**: DataInputStream/DataOutputStream
- **Threading**: Multi-threaded for non-blocking UI
- **Compatibility**: Java 8 and above

## Troubleshooting

### Common Issues:

1. **Connection Refused**
   - Ensure host is running before client connects
   - Verify IP address and port number match
   - Check firewall settings

2. **Port Already in Use**
   - Choose a different port number
   - Ensure previous instance is closed

3. **Messages Not Delivered**
   - Verify both users are connected
   - Check network connectivity

## Development

### Built With:
- [Java Swing](https://docs.oracle.com/javase/8/docs/technotes/guides/swing/) - GUI Toolkit
- [Java Networking](https://docs.oracle.com/javase/8/docs/api/java/net/package-summary.html) - Socket Communication

### Code Overview:
- Single-class design for simplicity
- Event-driven architecture
- Separate threads for network operations
- Exception handling for robust operation



---

**Note**: This is a educational project demonstrating basic networking and GUI concepts in Java. For production use, consider adding security features like encryption and authentication.
