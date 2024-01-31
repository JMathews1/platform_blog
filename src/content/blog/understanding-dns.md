---
author: James Mathews
pubDatetime: 2024-01-31T16:36:06Z
modDatetime: 2024-01-31T16:39:06Z
title: Understanding DNS and Its Operation in the Cloud
slug: understanding-dns
featured: true
draft: false
tags:
  - cloud
  - networking
description:
  Blog post to outline the workings of DNS in a simple way 
---

# Understanding DNS and Its Operation in the Cloud

DNS, or Domain Name System, is often likened to a phonebook for the internet. It translates human-friendly domain names (like `www.example.com`) into IP addresses that computers use to identify each other on the network. Let's break down this concept and explore how it functions in cloud environments, particularly focusing on changing DNS settings in an Azure DevOps subscription from an IBM DNS to a local DNS system.

## What is DNS?

Imagine typing `www.example.com` in your browser. Your computer doesn't understand this human-readable address. It needs the numerical IP address to locate the website. Here's where DNS comes in – it converts `www.example.com` (domain) into an IP address like `192.0.2.1`.

## How Does DNS Work in the Cloud?

In cloud environments, DNS plays a crucial role. It ensures that cloud-based services and resources are easily accessible and reliably connected. When you use cloud services, such as Azure, AWS, or IBM Cloud, they offer their own DNS services, which manage the mapping of domain names to IP addresses within their networks.

## Changing DNS Settings in Azure DevOps

Suppose you have your Azure DevOps subscription initially configured with IBM's DNS and now you wish to switch to a local DNS system. Here’s a simplified explanation of the process:

1. **Access Azure Portal**: Log in to your Azure portal where your DevOps subscription is managed.
2. **Navigate to DNS Settings**: Find the DNS management section. This is typically located in the networking or domain management area.
3. **Modify DNS Records**: Replace the IBM DNS records with those of your local DNS system. This usually involves updating nameservers or A/CNAME records.
4. **Save and Propagate**: After saving your changes, they will propagate across the internet. This process can take anywhere from a few minutes to 48 hours.
5. **Verify the Changes**: Once the changes have propagated, verify that your domains are correctly resolving to the new DNS.


