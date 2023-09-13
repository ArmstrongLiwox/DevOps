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

### 4. what is TCP and UPD

### TCP : tansmission control protocol
The ***Transmission Control Protocol (TCP)*** is one of the main protocols of the Internet protocol suite. It originated in the initial network implementation in which it complemented the ***Internet Protocol (IP)***. Therefore, the entire suite is commonly referred to as ***TCP/IP***. ***TCP*** provides reliable, ordered, and error-checked delivery of a stream of octets (bytes) between applications running on hosts communicating via an IP network. 
Major internet applications such as the World Wide Web, email, remote administration, and file transferrely on TCP, which is part of the Transport Layer of the TCP/IP suite. SSL/TLS often runs on top of TCP.

### UDP : user datagram protocol
In computer networking, the ***User Datagram Protocol (UDP)*** is one of the core communication protocols of the Internet protocol suite used to send messages (transported as datagrams in packets) to other hosts on an Internet Protocol (IP) network. 
Within an IP network, UDP does not require prior communication to set up communication channels or data paths.

### Difference between TCP and UDP
TCP is reliable, ordered, and connection-oriented. It guarantees data delivery and order but has higher overhead.

UDP is unreliable, unordered, and connectionless. It has lower overhead but doesn't guarantee delivery or order. 

Choose based on your application's needs: TCP for reliability, UDP for low latency.

### List of ports commonly used in Web
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

### 5. What is VIM

Vim is a powerful and extensible text editor known for its efficiency and keyboard-centric approach. 
It operates in different modes, offers syntax highlighting, and is commonly used by programmers and system administrators for text and code editing.


___

## Preparing prerequisites

### Step 0 - preparing prerequisites

> Register  a new AWS account

![register AWS](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/8ce03528-fb3c-438b-9964-71e9864d09cf)

> Select London region

![select region](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/f9aba5c6-66c1-4db9-b823-c1f17d77e44c)

> Create instance, and download key to PC.
> Lanunch EC2 instance of t2micro family with Ubuntu server 22.04 LTS (HVM)

![launch instance](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/c9a15609-c30d-439b-a897-349aeea5ae0f)

### Connecting to EC2 using the terminal

> go to download location of private key

![key location](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/6b5bd92f-c66a-46dc-89af-31b4e0516f04)

> pick instance and click connect

![connect](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/6d76137c-3abb-400d-bf5e-433b410f875a)

> choose SSH client and copy SSH address

![SSH copy](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/c44d93dc-0ed1-4990-a864-e5e30e63b7b2)

> paste SSH address into git bash at the key location. press enter.

![connect with git](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/33b8b508-69d1-4753-af4b-a74be2c0fa4f)

---

## Installing Apache and Updating the Firewall

### Step 1 - Installing Apache and Updating the Firewall
Apache is a widely used, open-source web server software that serves web content to users' web browsers. It's known for its flexibility, security features, and scalability, making it a popular choice for hosting websites and web applications.

> Insalling Apache using Ubuntu's package manager
```
sudo apt update
```

![sudo apt update](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/9fe7b05b-2482-4603-be80-1186995a9040)

> Run apache2 installation package
```
sudo apt install apache2
```

![rebooting](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/45aa7e80-6c28-481a-86e0-ca00caea490e)

![rebooting services](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/527683c6-1ae7-48a7-8e5e-59dddf4953db)

![apache install done](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/36277dc5-808e-480d-a998-8a42b6be1fae)


> Verify apache2 is running as a service in the OS
```
sudo systemctl status apache2
```

![apache running](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/6c6d72ec-b3da-4c8d-9263-778ceb83ee03)


> Check how we can access it locally in our Ubuntu shell
```
curl http://localhost:80
```

![check localhost](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/6eb48c85-6e57-4f3f-a886-4c083e92d6d4)


```
curl http://127.0.0.1:80
```

> Test how Apache HTTP server can respond to request from the internet.

http://35.179.92.176:80

![check apache on web](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/09c5f4ac-33e8-46f4-bcec-5a8219d8a583)

> Check Public IP address with command
```
curl -s http://169.254.169.254/latest/meta-data/public-ipv4
```

![check apache with command](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/cac20b68-acab-4ebb-b625-cc0a9992afbf)

---

## Installing MySQL

### Step 2 - Installing MySQL
> MySQL is relational database management system used within PHP environments.
>Install MySQL server
```
sudo apt install mysql-server
```

![install mysql](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/08aafd52-7d18-40af-a14e-3a43d89feefa)

![mysql reboot](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/8c072496-6021-4cbb-8a77-1bdd1b7869b3)

![mysql installed ](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/b4ebce74-a193-4b1c-ac64-54fb7e53f4f7)

> login to mysql console
```
sudo mysql
```

![mysql login](<images/mysql login.png>)

> Run security script
```
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY 'PassWord.1';
```

![secure mysql](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/13a18210-a69c-4fa4-ae53-9fe65c4f905b)

> Exit MySQL shell
```
exit
```

![exit mysql](https://github.com/ArmstrongLiwox/DevOps/assets/143335106/9510524a-7ecf-4b9a-b897-7f1c886d087c)




