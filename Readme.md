# R + Docker: Reproducible Data Science Environment

This project demonstrates how to set up a portable and reproducible data science environment using **R** and **Docker**. It includes pre-installed packages like `tidyverse`, `readr`, `lubridate`, and more. The setup allows you to run R scripts that analyze CSV files, generate summaries, and save visual outputs — all inside a Docker container.

## 📁 Project Structure
```
r_docker_project/
├── Dockerfile # Defines the Docker environment
├── install_packages.R # Installs necessary R packages
├── myscript.R # Your main analysis script
```

## 🚀 Getting Started

### 1. Build the Docker image

```
docker build -t rfords_docker .


### 2. Run the container and execute your script

```
docker run -it -v "$(pwd)":/app -w /app rfords_docker
```
This mounts your local folder into the container and executes r_script.R. 

🧠 What’s Inside?

install_packages.R
This script installs all required R packages inside the container:

```
packages <- c("tidyverse", "data.table", "caret", "lubridate", "shiny", "readr", "readxl")
install.packages(packages, repos = "https://cloud.r-project.org")
```

r_myscript.R

After installation you'll see this message : 
```print ("R is working now... ready for analysis")
```

🌍 Why This Project?

As part of my learning journey in DevOps and reproducible science, I’ve created this Dockerized R setup to:

Eliminate dependency issues.
Simplify project sharing.
Keep my R workflows consistent across machines.


📬 Contact

If you're learning Docker + R or want to collaborate on data science projects, feel free to connect!

Built with curiosity, Docker, and some coffee ☕️
