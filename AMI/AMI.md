# AMI with Dockerized React Website

## Overview

This AMI is configured to host a Docker container running a React website. It is designed for use in an AWS Auto Scaling Group with an Application Load Balancer (ALB) to handle incoming traffic. The AMI was built to speed up instance launches by pre-packaging the Docker environment and the React application.

## Features

- Pre-installed Docker engine and Docker Compose
- Docker container running a React website
- Configured to start the container automatically on instance launch
- Lightweight and optimized for rapid deployment

## AMI Configuration

### Base OS

The AMI uses a Dockerfile to build a image which runs on Node (to create the build of React project) and nginx which acts as a webserver to run the website.

### Docker Installation

Docker is installed via the official Docker repository to ensure the latest stable version. ## OR
Run script on your terminal that pulls the docker image: curl https://get.docker.com/ | bash

### React Website

The React application is built and containerized using a Dockerfile. The container is configured to expose the necessary port (usually 80 or 3000) for HTTP traffic.

- Project Repo:[GIT](https://github.com/Thelaxman/UTELL-PORTFOLIO.git)

### Container Auto-Start

The AMI includes a systemd service file to automatically start the Docker container upon instance launch. This ensures that the website is immediately accessible once the instance is running.

## Usage

1. Launch an EC2 instance using this AMI.
2. Ensure that the security group allows HTTP/HTTPS traffic.
3. Use an Auto Scaling Group to manage instance scaling based on load.
4. Attach the instances to an Application Load Balancer for traffic distribution.

## Troubleshooting

- Check Docker service status:
  ```bash
  sudo systemctl status docker
  ```
