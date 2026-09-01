# docker image loader:

- It's used to upload docker image file (i.e, .tar) and it will load that image into target machine. 
- we can combine multiple .tar and upload it a .zip file also.

#### use case
- Normal I need a docker image, in general we will clone the image from docker hub and it will load in our machine.
- There is another case i.e, I have docker image in locally and I don't want to push to docker hub, but my local image need to run on target machine, In that case we can use this.

### **Note :** 
clone this on the target machine, and it should have docker setup.

## How To Run:
1. Clone the git repo which contains docker-compose file.<br />
> **CMD :**`git clone --branch docker-image-load --single-branch https://github.com/SaiAmarendraReddy/docker_hub.git`

2. After cloning rename `.compose.env.sample` to `.compose.env`.
3. Run the compose file. <br /> 
> **CMD :**`docker compose --env-file=.compose.env -f docker-compose.yml up -d`

4. After successfull running, we will get an 
- Endpoint: `http://localhost:8000/upload`
- body: file (key is "file", value is upload zip or tar file.)
- Method: POST