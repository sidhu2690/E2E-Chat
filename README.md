# E2E Chat
E2E Chat is a peer-to-peer chat application built with PeerJS and WebRTC, designed for secure, end-to-end (E2E) encrypted messaging between two users. It allows one user to create a chat room and another to join it, with no server-side storage or access to message content beyond connection setup. The application uses Tailwind CSS for a clean, responsive interface.
Features

E2E Encrypted Messaging: Messages are encrypted using WebRTC's DTLS and SRTP protocols, ensuring only the two connected users can read them.
Two-User Communication: Supports one host and one participant per room for private, direct messaging.
Minimal Server Role: The PeerJS signaling server only facilitates connection setup (exchanging metadata like IP addresses) and cannot access message content.
Responsive Design: Built with Tailwind CSS for a modern, mobile-friendly UI.

## Demo
Try it out here:
https://sidhu2690.github.io/E2E-Chat/


Prerequisites

A modern web browser (e.g., Chrome, Firefox, Edge) with WebRTC support.
Internet connection for accessing the PeerJS signaling server.

Setup

Clone the Repository:git clone https://github.com/sidh2690/E2E-Chat.git
cd E2E-Chat



Usage

Open the Application:

Access the hosted app via a secure web server (must use HTTPS for WebRTC compatibility).


Create a Room (Host):

Enter a unique room name (e.g., room1234) in the input field.
Click Create Room to host a new chat room.
Share the room name privately with the intended recipient (e.g., via a secure channel like email or encrypted messaging).


Join a Room (Participant):

Enter the room name provided by the host.
Click Join Room to connect to the host's room.


Chat:

Once connected, type messages in the input field and click Send or press Enter.
Messages appear in the chat window, with your messages on the right and the other user's on the left.
Only the two connected users can send and receive messages in the room.



Security
E2E Chat is designed for E2E secure messaging with minimal server involvement:

End-to-End Encryption: Messages are encrypted using WebRTC's DTLS for key exchange and SRTP for data transfer. Only the two connected users can decrypt and read the messages.
Signaling Server Role: The PeerJS signaling server facilitates connection setup by exchanging metadata (e.g., room names, IP addresses). It cannot access or store message content.
Current Limitations:
XSS Vulnerability: User messages are not sanitized, potentially allowing malicious code execution. Do not use in production without fixing this (see Contributing).
No Room Authentication: Anyone with the room name can join. Use strong, unique room names and share them securely.
Metadata Exposure: The signaling server can see room names and IP addresses, though message content remains E2E encrypted.


Recommendations for Secure Use:
Share room names only through secure channels (e.g., encrypted messaging apps).
Use long, random room names to prevent guessing (e.g., room-x7b9p3q8r2).



Contributing
Contributions are welcome to enhance security and functionality! To contribute:


License
This project is licensed under the MIT License. See the LICENSE file for details.

![Visitor Count](https://profile-counter.glitch.me/sidhu2690/E2E-Chat/count.svg)

