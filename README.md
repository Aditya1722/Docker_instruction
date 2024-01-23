# Docker_Presto_instruction
* Step 1 - Pull the image from docker hub - `sudo docker pull adii1722/presto:presto`
  This image will be used as a base for making containers  where changes can be saved
  Note - Changes made in image wont be saved that's why there is a need to create container.  
* Step 2 - To start a docker container with name - presto and effectively use GUI interation use this command -
  name of container = presto(choose yourself)
  name of repository = adii1722/mwa_sps_pipeline:presto
  `sudo docker run -it --privileged --network host -e DISPLAY=:1 --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" --name presto adii1722/presto:presto /bin/bash`  
* Step 3 - After getting inside the container exit by typing exit and enter
* Step 4 - Start the container by using command - `sudo docker start presto`
* Step 5 - For entering the docker container using - `sudo docker exec -it  presto /bin/bash`
* Step 6 - Check gui interaction is working using command - xeyes.
  After completing now you can use PRESTO.

# Use docker without sudo or root access 
* Step 1 - Install docker and pull the image in your root access machine
* Step 2 - execute comman - `sudo groupadd docker`
* Step 3 - execute command `sudo usermod -aG docker $USER`
    Replace $USER with the user you want to add.
* Step 4 - Go to user account and enjoy docker without sudo  

(optional steps if you hvae a server with hight security ) 
* Step 5 - repeat till step 3  
* Step 6 - ls -l /var/run/docker.sock  
    Check if the output looks like - srw-rw---- 1 root root 0 Jan 23 10:08 /var/run/docker.sock  
    you have to change the root user of group to docker and to do that execute command - `sudo chown root:docker /var/run/docker.sock`
* Step 7 - Repeat step 3 and you're good to go !!!

 


 ## For copying
docker to local machine - `sudo docker cp container_name:/path/to/your/file.txt /path/to/destination/`
local machine to docker - `sudo docker cp /path/to/your/file.txt aditya:/path/to/destination/in_docker`
