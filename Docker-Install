# Docker and Docker Compose Installation Guide for Ubuntu

This guide provides step-by-step instructions to install Docker and Docker Compose on a fresh Ubuntu system.

---

## Prerequisites

Ensure your system is up-to-date and has the required tools installed.

### Update the System
Run the following commands to update your package list and install prerequisites:

```bash
sudo apt update
sudo apt upgrade -y
sudo apt install -y apt-transport-https ca-certificates curl software-properties-common
```

---

## Step 1: Add Docker’s Official GPG Key and Repository

1. Add Docker's GPG key:
   ```bash
   curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /usr/share/keyrings/docker-archive-keyring.gpg
   ```

2. Add the Docker repository:
   ```bash
   echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
   ```

---

## Step 2: Install Docker

1. Update the package list:
   ```bash
   sudo apt update
   ```

2. Install Docker:
   ```bash
   sudo apt install -y docker-ce docker-ce-cli containerd.io
   ```

3. Verify Docker installation:
   ```bash
   sudo docker --version
   ```

---

## Step 3: Enable and Start Docker

1. Enable Docker to start on boot:
   ```bash
   sudo systemctl enable docker
   ```

2. Start the Docker service:
   ```bash
   sudo systemctl start docker
   ```

---

## Step 4: Install Docker Compose

1. Download the latest version of Docker Compose:
   ```bash
   sudo curl -L "https://github.com/docker/compose/releases/latest/download/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
   ```

2. Set the correct permissions:
   ```bash
   sudo chmod +x /usr/local/bin/docker-compose
   ```

3. Verify Docker Compose installation:
   ```bash
   docker-compose --version
   ```

---

## Step 5: Optional - Run Docker Without `sudo`

To allow your user to run Docker commands without `sudo`:

1. Add your user to the `docker` group:
   ```bash
   sudo usermod -aG docker $USER
   ```

2. Log out and log back in for the changes to take effect.

---

## Verification

- Check Docker version:
  ```bash
  docker --version
  ```

- Check Docker Compose version:
  ```bash
  docker-compose --version
  ```

---

## Notes

- Always ensure you are installing the latest stable versions of Docker and Docker Compose.
- For more details, refer to the [official Docker documentation](https://docs.docker.com/).

---

You are now ready to use Docker and Docker Compose on your Ubuntu system!
