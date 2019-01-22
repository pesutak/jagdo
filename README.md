# Jenkins JNLP Agent CI build stack
contains:
- [Jenkins JNLP Agent](https://hub.docker.com/r/jenkins/jnlp-slave) (latest)
- [Docker CE](https://docs.docker.com/install/) (latest)
- [Node.js](https://nodejs.org/en/) 8.x 
- [.NET Core 2.2 SDK](https://www.microsoft.com/net/download?initial-os=linux)
- [Angular CLI](https://cli.angular.io/) (latest)

to run, just type:
```
docker run -d --restart always \
  -v /var/run/docker.sock:/var/run/docker.sock \
  -v jenkins_agent_home:/home/jenkins \
  --name jenkins-agent fixerapps/jagdo \
  -url https://jenkins-server:port \
  -workDir=/home/jenkins \
  -disableHttpsCertValidation <secret> <agent name>
```

Have a Fun ;)
