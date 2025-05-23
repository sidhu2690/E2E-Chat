E2E-Chat
E2E-Chat is a secure, peer-to-peer chat application built with PeerJS and WebRTC, designed for end-to-end (E2E) encrypted messaging and file sharing between two users. One user creates a chat room, another joins, and they communicate directly with no server storing their data. The app features a clean, responsive interface using Tailwind CSS.
Features

E2E Encrypted Messaging: Messages are secured with WebRTC’s DTLS and SRTP protocols, ensuring only the two connected users can read them.
E2E Encrypted File Sharing: Send images, PDFs, or other files securely with WebRTC encryption.
Two-User Limit: Only two users can connect per room, blocking third-party intrusions even if the room name is guessed or brute-forced.
Minimal Server Role: The PeerJS signaling server only sets up the initial connection (exchanging metadata like IP addresses) and then has no further involvement.
No Server Attacks: Serverless design prevents SQL injection and similar attacks.
XSS Protection: Input sanitization blocks cross-site scripting (XSS) attacks.
Responsive Design: Built with Tailwind CSS for a modern, mobile-friendly UI.

Demo
Try it out here: https://sidhu2690.github.io/E2E-Chat/
Prerequisites

A modern web browser (e.g., Chrome, Firefox, Edge) with WebRTC support.
Internet connection for accessing the PeerJS signaling server.

Setup

Clone the repository:git clone https://github.com/sidhu2690/E2E-Chat.git
cd E2E-Chat


Open index.html in a browser or host it on a secure web server (must use HTTPS for WebRTC compatibility).

Usage
Open the Application
Access the hosted app via a secure web server (HTTPS required for WebRTC).
Create a Room (Host)

Enter a unique room name (e.g., room-x7b9p3q8r2) in the input field.
Click Create Room to host a new chat room.
Share the room name privately with your friend (e.g., via a secure channel like Signal or WhatsApp).

Join a Room (Participant)

Enter the room name provided by the host.
Click Join Room to connect directly to the host via WebRTC.

Chat and Share Files

Once connected, type messages in the input field and click Send or press Enter.
To share a file, click the 📎 button, select a file (e.g., image or PDF), and send it.
Messages and files appear in the chat window, with your messages on the right and the other user’s on the left.
Only the two connected users can send and receive messages or files.

How File Sharing Works

Upload: Click the 📎 button to select a file.
Transfer: The file is split into chunks, encrypted with WebRTC’s DTLS protocol, and sent directly to the other user.
Receive: Files appear in the chat for viewing or downloading, fully encrypted.

Security
E2E-Chat is built for secure, private communication with minimal server involvement:

End-to-End Encryption: Messages and files are encrypted using WebRTC’s DTLS for key exchange and SRTP for data transfer. Only the two connected users can decrypt them.
Server Only for Setup: The PeerJS signaling server facilitates connection setup (exchanging room names and IP addresses) and then steps out completely. It cannot access or store messages or files.
Two-User Lock: Only two users can connect per room. If a third party tries to join (even with the correct room name), they’re blocked, preventing intrusions.
No Server Storage: With no server-side data storage, attacks like SQL injection are impossible.
XSS Protection: User inputs are sanitized to prevent cross-site scripting (XSS) attacks.
Metadata Exposure: The signaling server can see room names and IP addresses, but message and file content remains E2E encrypted.

Recommendations for Secure Use

Share room names only through secure channels (e.g., encrypted messaging apps like Signal).
Use long, random room names (10+ characters, e.g., room-x7b9p3q8r2) to prevent guessing or brute-forcing.


Contributing
Contributions are welcome to improve security and features! To contribute:

License
This project is licensed under the MIT License. 
See the LICENSE file for details.
