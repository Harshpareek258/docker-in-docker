
# docker-in-docker

# 🐳 Docker Inside Docker (DIND)

## 📖 About the Project

This project demonstrates how to run **Docker Inside Docker (DIND)** — a DevOps concept where a Docker container itself runs Docker commands. It's commonly used in CI/CD pipelines, container testing, and learning environments.

Using the official `docker:dind` image, we launched a Docker container capable of running other Docker containers inside it.



## ⚙️ Commands Used

###                                             🔹 Step 1: Pull the official DIND image

docker pull docker:dind


                                               🔹 Step 2: Run the Docker-in-Docker container in privileged mod
docker run --privileged -dit --name dind-test docker:dind

                                                  

                                              🔹 Step 3: Enter the container shell
docker exec -it dind-test sh
                                             
                                              🔹 Step 4: Inside the container 

docker info

                                               🔹 Step 5: Run a test container from inside DIND

docker run hello-world

 
                                               OUTPUT
Hello from Docker!
This message shows that your installation appears to be working correctly.
                           
                                               🔹 Step 6: View all containers 

docker ps -a

🧰 Tech Stack
Docker

Docker-in-Docker (docker:dind)

RHEL 9

VirtualBox

Linux CLI

 Author
Harsh Pareek
🎓 B.Tech CSE (2023–2027) | Arya College of Engineering
👨💻 DevOps & Cloud Intern at LinuxWorld Pvt. Ltd.
🏫 Learning under the guidance of Vimal Daga Sir

>>>>>>> 6eab631 (Added final clean and formatted README)
