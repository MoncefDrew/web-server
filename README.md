# a simple web server

this is a small http web server i built in pure c using low-level socket programming.
i made this project to better understand how web servers actually work behind the scenes without using frameworks or external libraries.

## features

- handles basic http requests
- serves static html files
- supports content-length for response bodies
- runs on linux, macos, and windows

## how it works

1. the server creates a tcp socket
2. binds it to a port
3. listens for incoming connections
4. accepts a client connection
5. reads the http request from the client
6. parses the request method and headers
7. sends back an http response with a file from the `www` directory

## build instructions

make sure you have `gcc` installed.

using make:

make

or compile manually:

gcc main.c -o webserver

## running the server

./webserver

by default, the server runs on:

http://localhost:8080

open this address in your browser.

## serving files

place your html files inside the `www` directory:

www/
├── index.html
├── about.html
└── style.css

the server will return these files when requested by a browser.

