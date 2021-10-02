---
title: Containers Deep Dive
author: Stack Underflow
date: '2021-09-01'
slug: containers-deep-dive
categories: 
  - Linux
tags: 
  - container
image: images/future-world.jpg
---

This is a collection of resources and posts about containers.

## Linux namespaces

The series [Namespaces in operation](https://lwn.net/Articles/531114/) on LWN covers the underlying technology of containers: Linux namespaces. Some code examples are outdated because of new Linux kernel releases and the author provides updates in the comments. If the programs in the article do not work, do refer to the comments to see what should be modified.

The author also has a two-videos series about namespaces:

- [Containers unplugged: Linux namespaces](https://youtu.be/0kJPa-1FuoI)
- [Containers unplugged: understanding user namespaces](https://youtu.be/73nB9-HYbAI)

## Container networking

This is a series of blog posts explaining how container networking behaves. If you are not familiar with Linux networking, check out [Linux Networking Fundamentals](/p/linux-networking-fundamentals/) first.

- [Network Namespaces and Docker](/p/network-namespaces-and-docker/)
- [Kubernetes Pods Networking](/p/kubernetes-pods-networking/)
- Kubernetes Services Networking (todo)
- Kubernetes DNS (todo)

### Resources

#### Services networking

[Kubernetes Services and Iptables](https://msazure.club/kubernetes-services-and-iptables/)

#### DNS

[Understanding CoreDNS in Kubernetes](https://youtu.be/qRiLmLACYSY)

## The containers ecosystem

The Udemy course [Dockerless: Deep Dive Into What Containers Really are About](https://www.udemy.com/course/dockerless/) ([How to get Udemy courses for free](/resources/#tricks-to-get-them-for-free-or-at-a-low-cost)) explains the containers ecosystem in great detail, including:

- Low level container standard (OCI) and tools (like `runc`)
- Tools other than Docker to work with containers (like `buildah` and `podman`)

## Rootless containers

Docker by default requires root privilege, this is not desirable from the security perspective. In contrast, Podman runs containers rootlessly using user namespaces. The article series written by [Daniel J Walsh](https://opensource.com/users/rhatdan) explains how rootless containers are implemented:

- [Podman and user namespaces: A marriage made in heaven](https://opensource.com/article/18/12/podman-and-user-namespaces)
- [How does rootless Podman work?](https://opensource.com/article/19/2/how-does-rootless-podman-work)
- [How rootless Buildah works: Building containers in unprivileged environments](https://opensource.com/article/19/3/tips-tricks-rootless-buildah)
- [The shortcomings of rootless containers](https://opensource.com/article/19/5/shortcomings-rootless-containers)

