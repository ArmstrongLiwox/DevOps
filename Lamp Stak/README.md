# LAMP STACK IMPLEMENTATION

## WEB STACK IMPLEMENTATION (Lamp stack) in AWS

What is a technology stack?
A technology stack is a set of frameworks and tools used to develop a software product.

some examples are as follows:
1. **LAMP** (Linux, Apache, MySQL, PHP or Python or Perl)
1. **LEMP** (Linux, Nginx, MySQL, PHP or Python or Perl)
1. **MERN** (MongoDB, ExpressJS, ReactJS, NodeJS)
1. **MEAN** (MongoDB, ExpressJS, AngularJS, NodeJS)

## Side Self Study

### 1. what is SDLC

According to wikipedia:

In systems engineering, information systems and software engineering, the systems development life cycle (SDLC), also referred to as the 
application development life cycle, is a process for planning, creating, testing, and deploying an information system. 
The SDLC concept applies to a range of hardware and software configurations, as a system can be composed of hardware only, software only, 
or a combination of both. 
There are usually six stages in this cycle: requirement analysis, design, development and testing, implementation, documentation, and evaluation.

### 2. what is LAMP stack

LAMP (Linux, Apache, MySQL, PHP/Perl/Python) is an acronym denoting one of the most common software stacks for many of the web's most popular applications. 
However, LAMP now refers to a generic software stack model and its components are largely interchangeable.
Each letter in the acronym stands for one of its four open-source building blocks:

>**Linux** for the operating system
>**Apache** HTTP Server
>**MySQL** for the relational database management system
>**PHP, Perl, or Python** programming language.

The components of the LAMP stack are present in the software repositories of most Linux distributions.

### 3. what is *chmod* and *chown* commands in Linux

### chmod

In Unix and Unix-like operating systems, **chmod** is the command and system call used to change the access permissions and the special mode flags ***(the setuid, setgid, and sticky flags)*** of file system objects (files and directories). 
Collectively these were originally called its modes, and the name chmod was chosen as an abbreviation of change mode.

### chown

The command **chown**, an abbreviation of change owner, is used on Unix and Unix-like operating systems to change 
the owner of file system files, directories. 
Unprivileged (regular) users who wish to change the group membership of a file that they own may use ***chgrp***.
The ownership of any file in the system may only be altered by a super-user. A user cannot give away ownership of a file, even when the user owns it. 
Similarly, only a member of a group can change a file's group ID to that group.
The command is available as a separate package for Microsoft Windows as part of the UnxUtils collection of native Win32 ports of common GNU Unix-like utilities. The chown command has also been ported to the IBM i operating system.

### 3. what is TCP and UPD

### TCP : tansmission control protocol

The ***Transmission Control Protocol (TCP)*** is one of the main protocols of the Internet protocol suite. It originated in the initial network implementation in which it complemented the ***Internet Protocol (IP)***. Therefore, the entire suite is commonly referred to as ***TCP/IP***. ***TCP*** provides reliable, ordered, and error-checked delivery of a stream of octets (bytes) between applications running on hosts communicating via an IP network. 
Major internet applications such as the World Wide Web, email, remote administration, and file transferrely on TCP, which is part of the Transport Layer of the TCP/IP suite. SSL/TLS often runs on top of TCP.

### UDP : user datagram protocol

In computer networking, the ***User Datagram Protocol (UDP)*** is one of the core communication protocols of the Internet protocol suite used to send messages (transported as datagrams in packets) to other hosts on an Internet Protocol (IP) network. 
Within an IP network, UDP does not require prior communication to set up communication channels or data paths.

There are several ports commonly used in web-related services and protocols. Here are some of the most common ones:

1. **HTTP (Hypertext Transfer Protocol)**
   - Port 80: This is the default port for unencrypted web traffic.

2. **HTTPS (Hypertext Transfer Protocol Secure)**
   - Port 443: This is the default port for secure, encrypted web traffic. It is used for secure communication over SSL/TLS.

3. **FTP (File Transfer Protocol)**
   - Port 21: FTP control port for sending commands.
   - Port 20: FTP data port for sending data.

4. **SMTP (Simple Mail Transfer Protocol)**
   - Port 25: Used for sending email messages.

5. **POP3 (Post Office Protocol version 3)**
   - Port 110: Used for receiving email from a mail server.

6. **IMAP (Internet Message Access Protocol)**
   - Port 143: Used for retrieving email messages from a mail server.
   - Port 993: IMAPS (IMAP over SSL/TLS) for secure email retrieval.

7. **DNS (Domain Name System)**
   - Port 53: Used for translating domain names into IP addresses and vice versa.

8. **SSH (Secure Shell)**
   - Port 22: Used for secure remote access and administration of servers.

9. **Telnet**
   - Port 23: Used for unencrypted remote access and administration of servers (considered insecure and often replaced by SSH).

10. **RDP (Remote Desktop Protocol)**
    - Port 3389: Used for remote desktop access on Windows-based systems.

11. **HTTP/2**
    - Port 8080: An alternate port for HTTP traffic, often used for proxy servers and testing.

12. **HTTP/3 (QUIC)**
    - Port 443: It can also use port 443 for secure, encrypted communication. HTTP/3 is a newer protocol that uses QUIC (Quick UDP Internet Connections) for improved performance.

13. **WebSocket**
    - Port 80 (ws) and Port 443 (wss): Used for full-duplex communication channels over a single TCP connection.

14. **NTP (Network Time Protocol)**
    - Port 123: Used for time synchronization between computers on a network.

15. **SNMP (Simple Network Management Protocol)**
    - Port 161: Used for network management and monitoring.

16. **LDAP (Lightweight Directory Access Protocol)**
    - Port 389: Used for directory services.

These are some of the commonly used ports in web-related services and protocols. Keep in mind that there are many other ports used for various specific applications and services, and some applications may use non-standard ports for communication.
