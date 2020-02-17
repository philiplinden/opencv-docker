# opencv-docker

Docker image of OpenCV 4.2.0 built from Python3.6-alpine ![Docker](https://github.com/philiplinden/opencv-docker/workflows/Docker/badge.svg)

## Install

Pull the latest version of the image:

```bash
docker pull philiplinden/opencv:latest
```

Or pull a specific tagged version (see git tags):

```bash
docker pull philiplinden/opencv:tag
```

## Usage

Run the image:

```bash
# run the image (with options)
docker run --name opencv philiplinden/opencv -v /host/directory:/container/directory --other --options command_to_run

# check if the container is running
docker ps | grep opencv
```

For example,

```bash
# run the container and mount the local directory with the container
docker run --name opencv philiplinden/opencv -v $(pwd_):/usr/src/opencv -it

# open an interactive bash terminal on the running container
docker exec -it opencv bash
```
