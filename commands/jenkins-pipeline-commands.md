# Jenkins Pipeline Lab Commands

This document contains the commands used during the Jenkins CI/CD Pipeline lab.

---

# System Update

```bash
sudo apt update
sudo apt upgrade -y
```

---

# Install Java

```bash
sudo apt install fontconfig openjdk-21-jre -y
java -version
```

---

# Add Jenkins Repository

```bash
curl -fsSL https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key | \
sudo tee /etc/apt/keyrings/jenkins-keyring.asc > /dev/null

echo "deb [signed-by=/etc/apt/keyrings/jenkins-keyring.asc] https://pkg.jenkins.io/debian-stable binary/" | \
sudo tee /etc/apt/sources.list.d/jenkins.list > /dev/null
```

---

# Install Jenkins

```bash
sudo apt update
sudo apt install jenkins -y
```

---

# Enable Jenkins

```bash
sudo systemctl enable jenkins
sudo systemctl start jenkins
sudo systemctl status jenkins
```

---

# Get Initial Admin Password

```bash
sudo cat /var/lib/jenkins/secrets/initialAdminPassword
```

---

# Install Docker

```bash
sudo apt install docker.io -y
```

---

# Enable Docker

```bash
sudo systemctl enable docker
sudo systemctl start docker
sudo systemctl status docker
```

---

# Add Users to Docker Group

```bash
sudo usermod -aG docker $USER
sudo usermod -aG docker jenkins
```

Apply group changes

```bash
newgrp docker
```

---

# Verify Docker

```bash
docker --version
docker ps
docker images
```

---

# Clone Repository

```bash
git clone https://github.com/Mohamed-Mosad-98/sourcecode.git

cd sourcecode
```

---

# Configure Git

```bash
git config --global user.name "Mohamed Mosad"

git config --global user.email "YOUR_EMAIL"
```

---

# Build Docker Image

```bash
docker build -t nodeapp:latest .
```

---

# Run Docker Container

```bash
docker run -d --name nodeapp -p 3000:3000 nodeapp:latest
```

---

# Stop Container

```bash
docker stop nodeapp
```

---

# Remove Container

```bash
docker rm nodeapp
```

---

# Remove Docker Image

```bash
docker rmi nodeapp:latest
```

---

# Verify Running Container

```bash
docker ps
```

---

# Verify Jenkins

```bash
sudo systemctl status jenkins
```
