
- allows you to configure your docker container via json file
- expected in the rot of your project

## Structure of a Dev Container Configuration File (devcontainer.json)

1\. Provide a remote image
```json
{
	"image": "mcr.microsoft.com/vscode/devcontainers/base:0-focal"
}
```
- the above is the base image for microsoft
- you can supply your own images


2\. Specify features:
```json
{
  "image": "mcr.microsoft.com/vscode/devcontainers/base:0-focal",
  "features": {
    "github-cli": "latest",
    "node": {
      "version": "lts"
    },
    "python": {
      "version": "3.8"
    }
  }
}
```
- features allow you to quickly install applications, etc. These features should be for the common base image
- to custom configure programs, you would need a custom Dockerfile
  ![[Pasted image 20250629123521.png]]

3\. Settings:
- allow you to change the settings of VSCode
```json
{
  "settings": {
    "terminal.integrated.shell.linux": "/bin/bash",
    "python.pythonPath": "/usr/local/bin/python"
  },
  "extensions": [
    "ms-python.python",
    "ms-vscode.cpptools",
    "github.vscode-pull-request-github"
  ]
}
```
- this makes it so that codespaces recognizes these settings, and remembers the extensions that you require

4\. Ports to forward to:
```json
"forwardPorts": [3000, 5000]
```
- useful when running web servers

5\. Command flags:
- specify command flags and their values to pass when using docker run command
```json
{
  "runArgs": [
    "-e", "MY_ENV_VAR=myvalue",
    "-e", "ANOTHER_ENV_VAR=anothervalue",
    "-v", "/my/host/folder:/container/folder",
    "--network=host",
    "--user=$(id -u):$(id -g)",
    "--cpus=2.0",
    "--memory=2g",
    "--shm-size=1g",
    "--add-host=example.com:192.168.1.10",
    "--privileged",
    "--security-opt", "seccomp=unconfined",
    "--network-alias=myalias",
    "-e", "TZ=Europe/London",
    "-v", "/var/run/docker.sock:/var/run/docker.sock"
  ]
}
```

6\. Environment Variables:
- set them in the containerEnv property
```json
  "containerEnv": {
    "NODE_ENV": "development",
    "PYTHONUNBUFFERED": "1",
    "TZ": "America/New_York",
    "LANG": "en_US.UTF-8",
    "HTTP_PROXY": "http://proxy.example.com:8080",
    "HTTPS_PROXY": "http://proxy.example.com:8080",
    "NO_PROXY": "localhost,127.0.0.1,.example.com",
    "JAVA_HOME": "/usr/lib/jvm/java-11-openjdk-amd64",
    "MAVEN_HOME": "/usr/share/maven",
    "DOCKER_TLS_VERIFY": "1",
    "DOCKER_HOST": "tcp://docker.example.com:2376",
    "DOCKER_CERT_PATH": "/certs/client",
    "DATABASE_URL": "postgresql://user:password@localhost:5432/mydatabase",
    "REDIS_URL": "redis://localhost:6379",
    "API_KEY": "your-api-key",
    "LOG_LEVEL": "debug"
  }
```

7\. Mounts:
- set up mounts to map files and folders to your container:
```json
{
  "mounts": [
    "source=${localWorkspaceFolder}/data,target=/container/data,type=bind,consistency=cached",
    "source=myvolume,target=/container/volume,type=volume",
    "source=/var/run/docker.sock,target=/var/run/docker.sock,type=bind",
    "source=${localWorkspaceFolder}/config/settings.json,target=/container/settings.json,type=bind,consistency=cached",
    "source=${localWorkspaceFolder}/docs,target=/container/docs,type=bind,consistency=cached,readonly"
  ]
}
```

8\. postCreateCommand:

- the command that runs after creation automatically is the `postCreateCommand`, you can set this command to run a custom command
```json
{
  "postCreateCommand": "echo 'Container ready!'",
  "remoteUser": "vscode"
}
```