# docker-bamboo-android-agent

Docker image that installs and configures Android and Bamboo agent

## Building

```
$ sudo docker build -t mcarr/docker-bamboo-android-agent .
```

## Running

```
sudo docker run -e HOME=/root/ -e BAMBOO_SERVER=http://hostname:port/bamboo -i -t atlassian/bamboo-java-agent:latest
```

Replace hostname:port with your Bamboo server's name and port (typically 8085).

Don't use localhost as the server address because for Docker, localhost is in the Docker container, not the host machine.

Go back to Administration > Agents (or refresh that page) and notice that your remote agent has registered itself.



### References

* https://registry.hub.docker.com/u/webratio/android-sdk/
* https://confluence.atlassian.com/display/BAMBOO/Getting+started+with+Docker+and+Bamboo


