### sigp/lighthouse beaconchain node docker-compose
##### Note: 
* this container persists data in $HOME/.lighthouse

1) install docker

    ```zsh 
    brew install --cask docker
    ```
2) login to docker

    ```zsh
    docker login
    ```
3) clone down [the repo](../..)

    ```zsh
    git clone <repo_url>
    ```
4) bring up the docker container

    ```zsh
    docker-compose -f bn-docker-compose.yml up -d
    ```
5) follow the container logs

    ```zsh 
    docker logs -f bn
    # exit with <ctrl+c>
    ```
6) jump into container environment

    ```zsh
    docker exec -it bn bash
    ```
7) stop the container
    ```zsh
    docker stop bn
    ```
8) remove the image
    ```zsh
    docker images
    # grab the image id
    docker rmi -f <your image id>
    ```