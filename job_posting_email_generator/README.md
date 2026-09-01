# Email generator
- It's used to generate the different variants of emails based on provided text (like job post).

## How To Run
1. Pull the docker image <a href="https://hub.docker.com/r/saiamarendrareddy/job-posting-email-generator">Docker Hub Image</a><br/>
**CMD to pull docker Image:**`docker pull saiamarendrareddy/job-posting-email-generator:1.0.0`, 

2. Clone the github `git clone --branch job-posting-email-generator --single-branch https://github.com/SaiAmarendraReddy/docker_hub.git`

3. Create `.compose.env` file inside cloned folder.

4. We need **Ollama API Key** (it provide free **gemma4:31b-cloud**) model.
    1. Open ollama in browser <a href="https://ollama.com/">Ollama</a>.
    2. Sign in and then click on **profile** section.
    3. Click on **keys** --> create API key and place it in **.compose.env** file.
5. Open the terminal run the commnad:
   > **CMD : 1** `docker compose --env-file=.compose.env -f docker-compose.yml build --no-cache`<br />
   > **CMD : 2**`docker compose --env-file=.compose.env -f docker-compose.yml up -d`