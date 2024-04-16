+++
title = 'Effortlessly Manage Docker With Portainer: A Step by Step Guide'
date = 2024-04-14T13:02:04+10:00
draft = false
[params]
  author = 'Eason Li'
  description = 'How to install Portainer using Docker. Portainer is a web UI tool for Docker that allows you to manage Docker containers, Kubernetes clusters, and Docker Compose stacks all in one convenient interface.'
+++

**Portainer: A Web UI for Docker Management**

Portainer is a web UI tool for Docker that allows you to manage Docker containers, Kubernetes clusters, and Docker Compose stacks all in one convenient interface. In this blog post, I'll show you how to install Portainer using Docker.

**Prerequisites**

- Ensure Docker is installed and running on your system.
- You'll need root privileges to create the Docker volume.
- (Optional) Configure a firewall whitelist rule for Portainer's access (if applicable).

**Installation Guide**

1. **Create a Portainer Volume:**

```
docker volume create portainer_data
```

This command creates a Docker volume named `portainer_data` to store Portainer's persistent data.

2. **Run the Portainer Container:**

```
docker run -d -p 8000:8000 -p 9443:9443 --name portainer --restart=always -v /var/run/docker.sock:/var/run/docker.sock -v portainer_data:/data portainer/portainer-ce:latest
```

This command runs a Portainer container in detached mode (`-d`) and maps the container's ports to your host's ports:

- `8000:8000` - Maps the container's port 8000 to the host's port 8000 (optional, for future use)
- `9443:9443` - Maps the container's port 9443 (Portainer's UI) to the host's port 9443

The `--name portainer` assigns a name to the container for easier management.

The `--restart=always` option ensures Portainer automatically restarts if the system reboots.

The `-v` flags mount two volumes:

- `/var/run/docker.sock:/var/run/docker.sock` - Mounts the Docker socket from the host system to the container, allowing Portainer to interact with Docker.
- `portainer_data:/data` - Mounts the `portainer_data` volume created earlier, allowing persistent storage of Portainer data.

**Login and Configure Portainer**

1. Access Portainer's web interface in your browser using the following URL, replacing `192.168.199.199` with your server's IP address or FQDN:

```
https://192.168.199.199:9443
```

> By default, Portainer uses a self-signed SSL certificate, which may trigger a security warning in your browser. You can proceed by accepting the risk (not recommended for production environments) or configure a trusted certificate for Portainer.

2. Create a username and a strong password for your Portainer account. You can change the password later if needed.

3. Upon successful login, you should land on the Portainer homepage with a "local" environment.

4. Click "Local" and then "Live Connect" to establish a connection to your local Docker daemon.

Now you're ready to use Portainer's web UI to deploy containers, manage stacks (Docker Compose), and perform other Docker-related tasks.

> Note: This blog post is written by Eason Li and edited by google bard.
