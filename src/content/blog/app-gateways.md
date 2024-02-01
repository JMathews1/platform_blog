---
author: James Mathews
pubDatetime: 2024-02-01T09:05:53Z
modDatetime: 2024-02-01T13:09:05.066Z
title: Demystifying App Gateways in Azure
slug: azure-app-gateways
featured: true
draft: false
tags:
  - networking
  - cloud
  - Azure
  - Az-204
description: A Comprehensive Guide to Azure Application Gateways
---

## Table of contents

This blog post delves into what Azure Application Gateway is, its core features, benefits, and how it stands as a cornerstone for modern web application architectures.

# Intro to app gateways

Azure Application Gateway is a web traffic load balancer that enables you to manage traffic to your web applications. Traditional load balancers operate at the transport layer (OSI layer 4 - TCP and UDP) and route traffic based on source IP address and port, to a destination IP address and port. However, Azure Application Gateway operates at the application layer (OSI layer 7), providing advanced routing features, SSL termination, and other essential capabilities designed to enhance application scalability, security, and performance.

# Operating at the Application Layer (OSI Layer 7)

The OSI model is a conceptual framework used to understand network interactions in seven layers, from physical (Layer 1) up to application (Layer 7). By operating at Layer 7, Azure Application Gateway can inspect, process, and make routing decisions based on the content of the web traffic, such as URLs, headers, or cookies. This ability goes beyond simple IP address and port (Layer 4) routing, offering more granular control over traffic distribution.

# Advanced Routing Features

Azure Application Gateway can direct user requests based on the requested URL or path. For instance, it can route requests for www.example.com/video to one set of servers in a pool and www.example.com/images to another. This URL-based routing is particularly beneficial for applications composed of microservices, where different components or services may reside on separate servers.

# Core Features of Azure Application Gateway

1. SSL Termination
Azure Application Gateway simplifies the management of SSL certificates and offloads the SSL processing workload from the web servers, thereby improving the performance and scalability of web applications.

2. Autoscaling
The autoscaling feature allows the Application Gateway to scale up or down based on web traffic, ensuring that the application can handle sudden traffic spikes without manual intervention.

3. Web Application Firewall (WAF)
Integrated with Azure's Web Application Firewall, the Application Gateway provides centralized protection of your web applications from common exploits and vulnerabilities. WAF comes with pre-configured rules set based on OWASP core rule sets that automatically protect web apps from vulnerabilities and attacks.

4. URL-based Routing
This feature routes traffic to different backend pool endpoints based on URL paths. It allows a single gateway to route requests to multiple microservices or web applications based on the URL.

5. Session Affinity
Azure Application Gateway supports session affinity, which is critical for ensuring that all requests from a particular user session are directed to the same server for processing.

6. Custom Health Probes
Customizable health probes allow Azure Application Gateway to monitor the health of the backend servers and ensure traffic is only routed to healthy servers.

# Benefits of Using Azure Application Gateway

Enhanced Security
With its built-in WAF, Azure Application Gateway provides robust security features that protect your applications from web vulnerabilities and attacks without the need for additional devices or services.

# Improved Application Performance

SSL termination offloads the SSL processing work from your web servers, reducing the load on them and thereby improving the overall application performance.

# Operational Simplicity
Azure Application Gateway simplifies operations by providing a single point of control for managing web traffic, SSL certificates, and other crucial web application functionalities.

# Cost-Effectiveness
By providing autoscaling capabilities, Azure Application Gateway ensures that you only pay for the resources you need when you need them, optimizing your cloud spending.


# Conclusion 

Azure Application Gateway stands out as a comprehensive solution for managing web application traffic in the Azure ecosystem. By offering features like SSL termination, autoscaling, WAF, and URL-based routing, it addresses the core needs of modern web applications, including security, performance, and scalability. Whether you're deploying new applications or migrating existing ones to the cloud, Azure Application Gateway provides a secure, efficient, and cost-effective path to achieving your objectives.