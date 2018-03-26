# Data Days Session: Advanced Docker
Creating portable, infra-agnostic projects using Docker and Docker-compose capable of running in production using Docker Swarm.
Swarm
Repos
CI/CD
- Dockerfile: define your own images
- docker-compose files: std, override, test, prod
 - `.env`
 - config to combine for prod
- Swarm
## Contents
- Showcase: 'living the dream'
- Architectural overview
 - 
- Dockerfile
 - FROM
 - LABEL
 - Entrypoints: CMD vs ...
 - versions: always specify
- Docker-compose
 - Networking: VNet, only publish a single port for Jupyter
 - Services
 - Links
 - Ports
 - Context
 - `.env`
- Docker prune
## Pre-requirements
- have Docker and Docker-compose installed
 - if on Linux, Docker Swarm
- be familiar with pulling images
- be familiar with running containers
# Cases
## Project composing
- Projects need their own data
- 'static data' in named volumes
- Codebase in 
## Streaming
- pipeline with kafka(?) to Database using Docker-compose
## CI/CD on Swarm
- Different Docker compose files: `docker-compose.yml`, `docker-compose.override.yml`, `docker-compose.test.yml`, `docker-compose.prod.yml`
- `docker-compose config -f docker-compose.yml -f docker-compose.prod.yml`
- repo management
## App deployment

# Udemy Course

## Sectie 1: Course Intro and Docker Setup

### 1. Course Roadmap (overview) 

### 2. Meet Your Instructor 

### 3. Getting Course Resources (GitHub Repo) 
Docker_CheatSheet_08.09.2016_0.pdf  
GitHub Repository For This Course  
Slides Section 1-5.pdf  

### 4. Course Slack Room: Chat Live With Me and Other Students 

### 5. Docker Editions: Which Do I Use? 

### 6. Installing Docker: The Fast Way 

### 7. Windows Docker Options 
### 8. Docker for Windows 10 Pro/Ent: Setup and Tips c
## Sectie 2: Creating and Using Containers Like a Boss
Check Our Docker Install and Config  

### 16. Starting a Nginx Web Server 

### 17. Debrief: What Happens When We Run a Container 

### 18. Container VS. VM: It's Just a Process 
Mike Coleman (Docker Employee) "Docker for the Virtualization Admin" eBook 
Docker Internals: cgroups, namespaces, and beyond (YouTube) 
Docker for Mac Commands for Getting Into Local Docker VM 

### 19. Windows Containers: Docker Is No Longer Just Linux 

### 20. Assignment: Manage Multiple Containers 

### 21. Assignment Answers: Manage Multiple Containers 

### 22. What's Going On In Containers: CLI Process Monitoring 

### 23. Getting a Shell Inside Containers: No Need for SSH 
Package Management Basics: apt, yum, dnf, pkg 

### 24. Docker Networks: Concepts for Private and Public Comms in Containers 
Docker's --format option for filtering cli output 

### 25. FIXME: Change In Official Nginx Image Removes Ping 

### 26. Docker Networks: CLI Management of Virtual Networks 

### 27. Docker Networks: DNS and How Containers Find Each Other 

### 28. Assignment: Using Containers for CLI Testing 

### 29. Assignment Answers: Using Containers for CLI Testing 

### 30. Assignment: DNS Round Robin Test 
### 31. Assignment Answers: DNS Round Robin Test 
## Sectie 3: Container Images, Where To Find Them and How To Build Them
What's In An Image (and What Isn't) 

Official Docker Image Specification 

### 33. The Mighty Hub: Using Docker Hub Registry Images 
List of Official Docker Images 

### 34. Images and Their Layers: Discover the Image Cache 
Images and Containers From Docker Docs 

### 35. Image Tagging and Pushing to Docker Hub 

### 36. Building Images: The Dockerfile Basics 
Dockerfile Command Details (BOOKMARK AND REVIEW, lots of good details you'll use often when making Dockerfiles) 

### 37. Building Images: Running Docker Builds 

### 38. Building Images: Extending Official Images 

### 39. Assignment: Build Your Own Dockerfile and Run Containers From It 

### 40. Assignment Answers: Build Your Own Dockerfile and Run Containers From It 

## Sectie 4: Container Lifetime & Persistent Data: Volumes, Volumes, Volumes 

### 41. Container Lifetime & Persistent Data 
Intro to Immutable Infrastructure Concepts 
The 12-Factor App (Everyone Should Read: Key to Cloud Native App Design, Deployment, and Operation) 
12 Fractured Apps (A follow-up to 12-Factor, a great article on how to do 12F correctly in containers) 

### 42. Persistent Data: Data Volumes 

### 43. Persistent Data: Bind Mounting 

### 44. Assignment: Database Upgrades with Named Volumes 

### 45. Assignment Answers: Database Upgrades with Named Volumes 

### 46. Assignment: Edit Code Running In Containers With Bind Mounts 
Jekyll, a Static Site Generator (just as background info, no need to install) 

### 47. Assignment Answers: Edit Code Running In Containers With Bind Mounts 

## Sectie 5: Making It Easier with Docker Compose: The Multi-Container Tool 

### 48. Docker Compose and The docker-compose.yml File 
The YAML Format: Sample Generic YAML File 
The YAML Format: Quick Reference 
Compose File Version Differences (Docker Docs) 

### 49. Trying Out Basic Compose Commands 
docker-compose download for Linux via GitHub, Win/Mac already have it. 

### 50. Assignment: Build a Compose File For a Multi-Container Service 
Compose File Settings (BOOKMARK AND REVIEW). You'll use it often when making compose files. 

### 51. Assignment Answers: Build a Compose File For a Multi-Container Service 

### 52. Adding Image Building to Compose Files 
(Docker Docs) Compose file build options 

### 53. Assignment: Compose For Run-Time Image Building and Multi-Container Development 
### 54. Assignment Answers: Compose For Run-Time Image Building and Multi-Container Dev 
## Sectie 6: Swarm Intro and Creating a 3-Node Swarm Cluster 

### 55. Swarm Mode: Built-In Orchestration 
Docker 1.12 Swarm Mode Deep Dive Part 1: Topology (YouTube)  
Docker 1.12 Swarm Mode Deep Dive Part 2: Orchestration (YouTube)  
Heart of the SwarmKit: Topology Management (slides)  

### 56. Create Your First Service and Scale It Locally 
Deploy services to a swarm (Docker Docs) 

### 57. UI Change For Service Create/Update 

### 58. Creating a 3-Node Swarm Cluster 
Digital Ocean Coupon for $10 
Create and Upload a SSH Key to Digital Ocean 
Docker Swarm Firewall Ports 
## Sectie 7: Swarm Basic Features and How to Use Them In Your Workflow 

### 59. Scaling Out with Overlay Networking 

### 60. Scaling Out with Routing Mesh 
Use swarm mode routing mesh (Docker Docs) 

### 61. Assignment: Create A Multi-Service Multi-Node Web App 

### 62. Assignment Answers: Create A Multi-Service Multi-Node Web App 

### 63. Swarm Stacks and Production Grade Compose 
Features Not Supported In Stack Deploy 

### 64. Secrets Storage for Swarm: Protecting Your Environment Variables 

### 65. Using Secrets in Swarm Services 
Manage sensitive data with Docker secrets (Docker Docs) (Lots of good reading and examples) 

### 66. Using Secrets with Swarm Stacks 
Secrets In Compose Files (Docker Docs) 

### 67. Assignment: Create A Stack with Secrets and Deploy 

### 68. Assignment Answers: Create A Stack with Secrets and Deploy 

## Sectie 8: Swarm App Lifecycle 

### 69. Using Secrets With Local Docker Compose 

### 70. Full App Lifecycle: Dev, Build and Deploy With a Single Compose Design 
Using Multiple Compose Files (Docker Docs) 
Using Compose Files In Production (Docker Docs) 

### 71. Service Updates: Changing Things In Flight 
Service Update command (Docker Docs) 

### 72. Healthchecks in Dockerfiles 
PHP Laravel Good Defaults with Docker 
HEALTHCHECK in Dockerfile (Docker Docs) 
Healthcheck in Compose files (Docker Docs) 

## Sectie 9: Container Registries: Image Storage and Distribution 

### 73. Docker Hub: Digging Deeper 
Docker Hub 

### 74. Docker Store: What Is It For? 
Docker Store 

### 75. Docker Cloud: CI/CD and Server Ops 
Docker Cloud 

### 76. Use Docker Cloud for Easy Remote Swarm Management 

### 77. Understanding Docker Registry 
Registry Configuration Docs 
Registry Garbage Collection 
Use Registry As A "Mirror" of Docker Hub 

### 78. Run a Private Docker Registry 

### 79. Assignment: Secure Docker Registry With TLS and Authentication 

### 80. Using Docker Registry With Swarm 
### 81. Third Party Image Registries 
## Sectie 10: Bonus Section 

### 82. Bonus Lecture: $10 Coupon for Swarm Mastery 

### 83. Bonus Lecture: Bret's DockerCon 2017 Video: "Journey to Docker Production" 

### 84. Bonus Lecture: Swarm Raft Quorum and Recovery (Laura Frank from DockerCon 2017) 

### 85. Bonus Lecture: Bret's Docker and DevOps Newsletter 

### 86. Bonus Lecture: Using Prune to Keep Your Docker System Clean (YouTube) 

### 87. Bonus Lecture: What's New In Docker 17.06 (YouTube) 

### 88. Bonus Lecture: Node.js Good Defaults For Docker 
### 89. Bonus Lecture: About the DCA (Docker Certificated Associate) 
