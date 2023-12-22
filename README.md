# Docker_Presto_instruction
* Step 1 - Pull the image from docker hub - `sudo docker pull adii1722/mwa_sps_pipeline:mwa`
  This image will be used as a base for making containers  where changes can be saved
  Note - image changes wont be saved that's why there is a need to create container.  
* Step 2 - To start a docker container with name - mwa and effectively use GUI interation use this command -
  name of container = mwa(choose yourself)
  name of repository = adii1722/mwa_sps_pipeline:mwa
  `sudo docker run -it --privileged --network host -e DISPLAY=:1 --volume="/tmp/.X11-unix:/tmp/.X11-unix:rw" --name mwa adii1722/mwa_sps_pipeline:mwa /bin/bash`  
* Step 3 - After getting inside the container exit by typing exit and enter
* Step 4 - start the container by using command - `sudo docker start mwa`
* Step 5 - for entering the docker container using - `sudo docker exec -it  mwa /bin/bash`
* Step 6 - Check gui interaction is working using command - xeyes.
  After completing now you can use PRESTO, SPEGID, FETCH & YOUR.
