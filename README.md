# FTP-Client-Server-System-C-Unix-Sockets-
FTP-like client/server application in C using TCP sockets, with a control channel for commands and an active-mode data connection for file transfers (get/put), plus basic authentication and filesystem operations.

Client FTP (C/Unix sockets)
Connects to server via control TCP (port 9119)
Reads one command per line and prints server reply codes/messages
Implements active-mode data transfers: client listens on 9120, server connects back for get/put
Supports commands: USER, PASS, PWD, LS, CWD/CD, MKDIR/RMDIR, DELE, GET, PUT, HELP, STATUS, QUIT

Server FTP (C/Unix sockets)
Control connection: client => server (command/reply, one line per command)
Data connection: server => client (active-mode, used for get/put)
Commands: USER, PASS, PWD, LS, CWD/CD, MKDIR/RMDIR, DELE, GET, PUT, HELP, STATUS, QUIT
