# WebExperiments
# About this project
This proyect was made for me to lear NodeJS, Express, MongoDB... and any future web technology that I throw into the mix. Each page in this website has it's own gimmick wich helps me learn a new technology or service.

## Install
For ease of use you can run the project in Docker.
## Install Docker

![Doker](https://1.bp.blogspot.com/-68aYf9ZNiZk/X33sbaV4AwI/AAAAAAAAFZo/Hf1BCsZT7KAIwbhmPx1yBitJ2LCpXQT-QCLcBGAsYHQ/s0/logo_docker.png)

- **Windows:** [Docker Desktop on Windows](https://docs.docker.com/docker-for-windows/install/)

- **MacOS:** [Docker Desktop on Mac](https://docs.docker.com/docker-for-mac/install/)

- **Linux:** [Choose your distro](https://docs.docker.com/engine/install/#server)
    
    - Or install using the convenience script (CentOS/ Debian/ Fedora/ Raspbian/ Ubuntu):

        ```bash
        curl -fsSL https://get.docker.com -o get-docker.sh
        sudo sh get-docker.sh
        ```
# Run
Once Docker is installed, go to the folder where **you cloned the repository** and run the following commands:
### Build Docker image
```bash
docker build -t magnitopic/server:1.0 .
```
### Run the MongoDB container
```bash
docker run --name=mongo -d -v /home/mag:/mongodb_data_volume -p 80:5000 mongo
```
### Run the NodeJS container
```bash
docker run --name node -d --net container:mongo magnitopic/server:1.0
```
## Server is now runing
Go to http://localhost to see the page.