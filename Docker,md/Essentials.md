# Install Docker on Ubuntu

Note: This demo was created using an Ubuntu 22.04 Jammy Jellyfish cloud server. 

1. Ensure no old versions are present on the system:

sudo apt remove -y docker docker-engine docker.io containerd runc

2. Ensure your apt package index is up to date, then upgrade your packages:

sudo apt update -y
sudo apt upgrade -y

3. Use the Tab key to toggle between fields and acknowledge any prompts.

4. Install the following apt packages to allow apt to use a repository over HTTPS:

sudo apt install -y ca-certificates curl gnupg lsb-release

5. Add Dockerâ€™s official GPG key:

sudo mkdir -m 0755 -p /etc/apt/keyrings
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg

6. Set up the repository:

echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

7. Update the apt package index:

sudo apt update -y

8. Install Docker Community Edition:

sudo apt install -y docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
 
9. Use the Tab key to toggle between fields and acknowledge any prompts.

10. Confirm Docker installed correctly:

sudo docker run hello-world

11. For best practices, do not use the root user. Instead, add your user to the Docker group:

sudo groupadd docker
sudo usermod -aG docker $USER

12. Run the command to activate the new group membership immediately:

newgrp docker

13. Verify you can now run the 'docker' command without 'sudo'.

docker run hello-world
