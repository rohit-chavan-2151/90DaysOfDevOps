## Task 1
### Install Docker and Jenkins in the system

- To install docker in the system, use command `sudo apt install docker`

- To install jenkins, please refer this [installation guide link](https://pkg.jenkins.io/debian-stable/)
 
![install-jenkins](https://user-images.githubusercontent.com/42653667/211163533-1e446e8b-0a38-4e96-b232-307a4e5088d3.png)

The jenkins service is started by system. To check the status of service, use command `service jenkins status`

![service-jenkins](https://user-images.githubusercontent.com/42653667/211163792-15163624-90bb-40a1-8db5-2bde0fe2c805.png)

To stop the service, use command `service jenkins stop` You can see the status of jenkins as stopped.

![service-jenkins-stop](https://user-images.githubusercontent.com/42653667/211163861-27e599eb-168a-4b9c-a4fb-c51c25b0a323.png)

### Systemctl vs Service

You can check Docker’s status with systemctl on distributions that use Systemd for service management. This covers the majority of popular operating systems including Debian, Ubuntu, CentOS, and Red Hat.

``sudo systemctl status docker``

![systemctl-docker](https://user-images.githubusercontent.com/42653667/211164061-33e3ba94-78e8-4348-bf77-0f9dbcbf2e23.png)

Check what’s displayed under “Active.” If you see active (running) in green, the Docker daemon is running and your containers should be up. An active state of inactive indicates the service has stopped. Try to bring it up by running sudo systemctl start docker. The status should change to active (running) after the daemon starts.

If you see a status of failed in red, the daemon couldn’t start due to an error. You should review the service’s startup logs shown later in the systemctl command output as these usually contain hints that let you work out what went wrong.

When there’s no obvious resolution available, manually start the daemon in debugging mode to get more information on its startup routine.

``sudo dockerd --debug``

Rebooting your host machine or restarting the Docker service with systemctl restart docker can help alleviate transient issues too.

- Working with systemd

Systemd stores configuration for services in two places. The first is /lib/systemd/system/, where you’ll find configuration for many services on your system. Most software installs install services here. The second is /etc/systemd/system/, which overrides the /lib/systemd directory and is generally used to place user-created services in. There’s also /etc/systemd/users/, which runs services for individual logged-in users, such as fetching mail.
