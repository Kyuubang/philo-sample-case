## Install Docker on all node

The Docker installation package available in the official Ubuntu repository may not be the latest version. To ensure we 
get the latest version, we’ll install Docker from the official Docker repository. To do that, we’ll add a new package 
source, add the GPG key from Docker to ensure the downloads are valid, and then install the package.

First, update your existing list of packages:

```shell
sudo apt update
```

Next, install a few prerequisite packages which let apt use packages over HTTPS:
```shell
sudo apt install apt-transport-https ca-certificates curl software-properties-common
```

Then add the GPG key for the official Docker repository to your system:
```shell
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
```

Add the Docker repository to APT sources:
```shell
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
```

This will also update our package database with the Docker packages from the newly added repo.
Make sure you are about to install from the Docker repo instead of the default Ubuntu repo:
```shell
apt-cache policy docker-ce
```

Notice that docker-ce is not installed, but the candidate for installation is from the Docker repository for Ubuntu 20.04 
(focal). Finally, install Docker:
```shell
sudo apt install docker-ce
```

Docker should now be installed, the daemon started, and the process enabled to start on boot. Check that it’s running:
```shell
sudo systemctl status docker
```

Installing Docker now gives you not just the Docker service (daemon) but also the docker command line utility, or the 
Docker client. We’ll explore how to use the docker command later in this tutorial.

## Task
- Install docker on all node
- Make suure docker is running on all node