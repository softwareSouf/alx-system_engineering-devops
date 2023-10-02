# High Availability Web Stack

In this project, we aim to enhance the availability and redundancy of our web stack by introducing a second web server and configuring load balancing. This improvement will allow us to handle more web traffic and enhance the reliability of our infrastructure. In the event of one web server failure, the other server will continue to handle requests.

## Project Overview

The project involves setting up the following components:

1. **Web Servers**: We will configure two web servers:
   - `gc-[STUDENT_ID]-web-01-XXXXXXXXXX`
   - `gc-[STUDENT_ID]-web-02-XXXXXXXXXX`
   
   Both servers will serve web content.

2. **Load Balancer**: We will set up a load balancer:
   - `gc-[STUDENT_ID]-lb-01-XXXXXXXXXX`
   
   The load balancer will distribute incoming web traffic evenly between the two web servers, ensuring high availability and load distribution.

## Resources and Requirements

### Resources

Before proceeding, review the following resources:

- **Introduction to Load-Balancing and HAProxy**: Understand the concept of load balancing and HAProxy, which we will use for load balancing.

- **HTTP Header**: Familiarize yourself with HTTP headers, as they may be relevant for configuration.

- **Debian/Ubuntu HAProxy Packages**: Review the documentation for HAProxy packages on Debian/Ubuntu systems, as we will use HAProxy for load balancing.

### Requirements

- **Operating System**: All tasks will be executed on Ubuntu 16.04 LTS.

- **File Endings**: Ensure that all files end with a new line.

- **README.md**: A README.md file at the root of the project folder is mandatory. This file will document the project and its components.

- **Executable Bash Scripts**: All Bash script files must be executable.

- **Shellcheck**: Your Bash scripts must pass Shellcheck (version 0.3.7) without any errors. This ensures that your scripts adhere to best practices and avoid common scripting issues.

- **Script Comments**: The first line of all Bash scripts should begin with `#!/usr/bin/env bash`, and the second line should contain a comment explaining the purpose of the script.

## Project Tasks

The tasks for this project include configuring the web servers, setting up HAProxy for load balancing, and ensuring that the web stack is highly available. Each task will be automated using Bash scripts to configure a brand new Ubuntu server as required.

## Conclusion

By the end of this project, our web stack will be more robust, capable of handling increased web traffic, and less susceptible to failures due to the redundancy of web servers and load balancing. The README.md file will provide detailed documentation to help understand the project components and configuration steps.
