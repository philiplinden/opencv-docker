# opencv-docker

Docker image of [OpenCV 4.2.0](https://github.com/opencv/opencv/releases/tag/4.2.0) built from [Python3.6-alpine](https://hub.docker.com/_/python)

![Docker](https://github.com/philiplinden/opencv-docker/workflows/Docker/badge.svg)

Also includes:

- [OpenCV Contrib 4.2.0](https://github.com/opencv/opencv_contrib/releases/tag/4.2.0) (`OPENCV_ENABLE_NONFREE=True`)
- Python 3 examples
- [NumPy](https://numpy.org/)

For educational use only.

## Install

Pull the latest version of the image:

```bash
docker pull philiplinden/opencv:latest
```

Or pull a specific [tagged version](https://github.com/philiplinden/opencv-docker/tags)):

```bash
docker pull philiplinden/opencv:tag
```

Or build it yourself (this will take 2+ hours!):

```bash
docker build . --file Dockerfile
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
