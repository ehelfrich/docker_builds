# VSCode server running on a CentOS container

Container to test install of code-server on a CentOS server.  

## To Run
1. docker pull ehelfri/centos-code-server:latest
2. docker container run -p 8080:8080 ehelfri/centos-code-server:latest
3. Navigate to localhost:8080
3. Default password is "test_password"

## To Build & Run
1. Clone the repo
2. Navigate to centos-vscode-server directory
3. (Optional) Change password in config.yaml
3. Run the command `docker build -t <docker_name> .` where <docker_name> is what you the container to be called
4. docker container run -p 8080:8080 <docker_name>