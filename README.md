# Bioinformatics Applied Course Docker Environment
This Dockerfile sets up an extended Jupyter environment tailored for bioinformatics analysis. It includes various Python and system-level packages necessary for bioinformatics tasks.

## Description
This Docker environment is designed to support bioinformatics courses and analyses, providing a comprehensive set of tools and libraries commonly used in the field.

## Maintainer
Ezechiel B. TIBIRI
Email: ezechiel.tibiri@ujkz.bf

## Docker installation and configuration
* On Linux 

```bash
sudo apt update && sudo apt upgrade -y
```
Installation of Docker

```bash
sudo apt install docker.io
```

```bash
sudo systemctl start docker
```
Chech installation

```bash
docker --version
```
```bash
sudo usermod -aG docker $USER
```

* On WSL (Windows Subsystem for Linux):
*Activating WSL:* Before installing Docker on WSL, ensure that WSL is enabled on your Windows system. You can enable WSL by following the instructions provided by Microsoft: Install WSL on Windows 10

*Installing Docker Desktop for Windows:* On Windows, the simplest way to use Docker with WSL is to install Docker Desktop for Windows, which supports WSL 2. You can download Docker Desktop from the official Docker website: Docker Desktop for Windows

*Configuring Docker with WSL:* Once Docker Desktop is installed, ensure that it is configured to use WSL. You can configure Docker Desktop to use WSL by selecting "Settings" in the Docker taskbar, then enabling "Use the WSL 2 based engine".

*Verification of installation:* You can verify if Docker is working correctly with WSL by opening a WSL terminal and running the following command:

```bash
docker --version
```

## Usage
* To build the Docker image, use the following command:

```bash
docker build -t bioinformatics-course .
```
* For our course, we will use an already available docker image
```
docker load -i bioinformatics-course.tar
```
* Load your docker image
```bash
docker run -p 8888:8888 bioinformatics-course
```

* Copy a directory from the host system to a Docker container:

```bash
docker cp directory/ container_name:/path/destination/
```

* Copy a directory from a Docker container to the host system:

```bash
docker cp container_name:/path/source/ directory/
```
