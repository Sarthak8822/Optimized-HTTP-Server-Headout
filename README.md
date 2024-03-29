# HTTP Server Assignment

This repository contains the code for a simple HTTP server that fulfills specific requirements. The server is implemented using Node.js and Express and is designed to handle GET requests with specific query parameters.

## Assignment Requirements

- [x] Set up an HTTP server to respond to GET requests on the endpoint `/data`.
- [x] Accept 2 query parameters, `n` (file name) and `m` (line number).
- [x] If both `n` and `m` are provided, return the content of file `/tmp/data/n.txt` at line number `m`.
- [x] If only `n` is provided, return the entire contents of file `/tmp/data/n.txt`.
- [x] Each file should be around 100MB in size, and there will be more than 30 different files (e.g., `1.txt`, `2.txt`, ..., `30.txt`, ..., `n.txt`).



## Runtime Requirements

- Bundle everything inside a Docker image (Dockerfile provided).
- Docker container should be compatible with ARM architecture and x86.
- Expose port 8080.
- Allocate a maximum of 1500 MB RAM and 2000m/2 Core CPU to the Docker container.

## How to Run

1. Clone this repository using:
    ```bash
    git clone https://github.com/Sarthak8822/Headout-Assignment
2. Install the libraries  that are in the project using:
    ```bash
    npm install
3. [***MANDATORY***]Also run the python script to generate all the txt files in your directory using:
    ```bash
    python generate_files.py
4. Build the Docker image using:
   ```bash
   docker build -t data-image .
5. Running docker image on your pc on port :8080 using:
    ```bash
    docker run -p 8080:8080 --memory 1500m --cpus 2 data-image
6. You can also test this application on POSTMAN using this endpoint
    `http://localhost:8080/data?n=1&m=2`
