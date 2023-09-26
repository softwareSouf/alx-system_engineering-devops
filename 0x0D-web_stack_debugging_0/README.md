# Webstack Debugging Basics

Welcome to the Webstack Debugging Basics project! This series is designed to help you master the art of debugging, an essential skill for Full-Stack Software Engineers. Computers and software don't always behave as expected, and that's where debugging comes in.

## Project Overview

In this project, you will be given a broken or bugged webstack, and your goal is to fix it. Your ultimate objective is to create a Bash script that, when executed, will bring the webstack to a working state. However, before writing this Bash script, you should first identify the issues and fix them manually.

## Getting Started

Let's start with a simple example. Your server must meet the following criteria for the web application to work:

1. Have a copy of the `/etc/passwd` file in `/tmp`.
2. Have a file named `/tmp/isworking` containing the string "OK".

Without these two elements, the web application cannot function.

```bash
vagrant@vagrant:~$ docker run -d -ti ubuntu:14.04
# Output...
vagrant@vagrant:~$ docker ps
# Output...
vagrant@vagrant:~$ docker exec -ti 76f44c0da25e /bin/bash
root@76f44c0da25e:/# ls /tmp/
root@76f44c0da25e:/# cp /etc/passwd /tmp/
root@76f44c0da25e:/# echo OK > /tmp/isworking
root@76f44c0da25e:/# ls /tmp/
isworking  passwd
root@76f44c0da25e:/#
```

In this example, you manually fixed the server, and your answer file would contain:

```bash
sylvain@ubuntu:~$ cat answerfile
#!/usr/bin/env bash
# Fix my server with these magic 2 lines
cp /etc/passwd /tmp/
echo OK > /tmp/isworking
sylvain@ubuntu:~$
```

**Note:** You cannot use interactive software such as emacs or vi in your Bash script; everything needs to be done from the command line, including file editing.

## Installing Docker

For this project, you will be provided with a Docker container to solve the task. However, if you want to experiment locally, you can install Docker on your machine. Here are some installation resources:

- [Mac OS](https://docs.docker.com/desktop/install/mac-install/)
- [Windows](https://docs.docker.com/desktop/install/windows-install/)
- [Ubuntu 14.04](https://docs.docker.com/install/linux/docker-ce/ubuntu/)
- [Ubuntu 16.04](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

## Resources

You can refer to the `man` or `help` command for information on:

- `curl`

## Requirements

General:

- Allowed editors: vi, vim, emacs
- All your files will be interpreted on Ubuntu 14.04 LTS
- All your files should end with a new line
- A README.md file, at the root of the folder of the project, is mandatory
- All your Bash script files must be executable
- Your Bash scripts must pass Shellcheck without any error
- Your Bash scripts must run without error
- The first line of all your Bash scripts should be exactly `#!/usr/bin/env bash`
- The second line of all your Bash scripts should be a comment explaining what the script is doing

Happy debugging! 🐞🔍
