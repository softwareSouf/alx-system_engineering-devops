
# Application Server vs Web Server Infrastructure

This README explains the distinction between an Application Server and a Web Server within a specific infrastructure, while also outlining the setup requirements.

## Infrastructure Overview

The infrastructure includes the following components:
- **1 Server:** The primary machine hosting the entire application.
- **1 Load-Balancer (HAproxy):** Configured as a cluster with another HAproxy for load distribution.
- **Split Components:** The infrastructure is divided into separate servers for the Web Server, Application Server, and Database.

## Application Server

The Application Server's role is to execute the dynamic application logic and process user-specific requests. It handles tasks such as data processing, authentication, and generating personalized responses.

## Web Server

The Web Server is responsible for serving static content to users, handling incoming HTTP requests, and routing them to the appropriate components. It can also act as a reverse proxy to forward dynamic requests to the Application Server.

## Why Split Components?

- **Scalability:** Separating components onto different servers allows for independent scaling. For example, the Web Server can be scaled independently from the Application Server or Database.
- **Resource Allocation:** Different components have varying resource requirements. Separation ensures optimal allocation of resources.
- **Isolation:** Separation prevents issues in one component from affecting others. A problem in the Web Server won't necessarily impact the Application Server.

## Load-Balancer (HAproxy)

The HAproxy Load-Balancer is a critical component for distributing incoming traffic across multiple servers. By configuring it as a cluster with redundancy, we ensure high availability and fault tolerance.

## Additional Element Explanation

- **Server:** Added as the primary hosting machine to run the entire application.
- **Load-Balancer (HAproxy):** Ensures even distribution of incoming traffic, preventing server overload.
- **Split Components:** Dividing the infrastructure into separate servers enhances resource utilization and isolation.

