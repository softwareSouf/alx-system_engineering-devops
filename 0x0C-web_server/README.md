# Web Server Configuration Project

Welcome to the Web Server Configuration project! In this project, you will be tasked with configuring an Ubuntu server (web-01) according to specific requirements. The goal is to automate server configuration tasks using Bash scripts to avoid manual intervention. This project aims to train you in the art of automating system administration tasks, which is a critical skill for any DevOps or System Administrator.

## Project Overview

Some of the tasks in this project will be graded based on two aspects:

1. **Is your web-01 server configured according to requirements?** - Your server should meet specific configuration requirements outlined in the project tasks.

2. **Does your answer file contain a Bash script that automatically performs commands to configure an Ubuntu machine to fit requirements (meaning without any human intervention)?** - You will need to create Bash scripts that automate the configuration tasks.

For example, if you need to create a file `/tmp/test` containing the string "hello world" and modify the configuration of Nginx to listen on port 8080 instead of 80, you should create a Bash script to perform these tasks.

```bash
#!/usr/bin/env bash
# Configuring a server with specification XYZ
echo hello world > /tmp/test
sed -i 's/80/8080/g' /etc/nginx/sites-enabled/default
```

The goal here is to automate tasks that are typically performed manually. Automating your work allows you to be more efficient and focus on more interesting and complex challenges. Keep in mind that the checker will execute your script as the root user, so you do not need to use the `sudo` command.

## Learning Objectives

By the end of this project, you should be able to:

### General
- Explain the main role of a web server.
- Understand the concept of child processes in the context of web servers.
- Describe why web servers usually have parent processes and child processes.
- Identify the main HTTP requests and their purposes.

### DNS
- Define what DNS stands for and its main role.
- Recognize different DNS record types, including A, CNAME, TXT, and MX.

## Resources

Before you begin, you may want to review the following resources:

- How the web works
- Nginx
- How to Configure Nginx
- Child process concept
- Root and subdomains
- HTTP requests
- HTTP redirection
- HTTP response codes (e.g., 404 - Not Found)
- Log files on Linux
- RFC 7231 (HTTP/1.1)
- RFC 7540 (HTTP/2)
- `man` or `help` for `scp` and `curl`

## Requirements

To successfully complete this project, ensure the following:

- Allowed editors: vi, vim, emacs
- All your files will be interpreted on Ubuntu 16.04 LTS
- All your files should end with a new line
- A README.md file, at the root of the folder of the project, is mandatory
- All your Bash script files must be executable
- Your Bash scripts must pass Shellcheck (version 0.3.7) without any error
- The first line of all your Bash scripts should be exactly `#!/usr/bin/env bash`
- The second line of all your Bash scripts should be a comment explaining what the script is doing
- You can't use `systemctl` for restarting a process

Remember, this project is not about copying and pasting solutions but about developing your skills in automating server configuration tasks. Be sure to meet the objectives and complete the tasks independently.

Let's automate and configure web-01! 🚀
