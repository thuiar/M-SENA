[![](https://badgen.net/badge/license/GPL-3.0/green)](#License) [![](https://badgen.net/badge/contact/THUIAR/purple)](https://thuiar.github.io/)

**M-SENA: An All-in-One Platform for Multimodal Sentiment Analysis**

The M-SENA Platform supports AI-assisted data labeling, data and model management, as well as model training and evaluation. It aims to help researchers save effort on insignificant details and focus more on analyzing data and models. 

The platform is developed with frontend and backend seperated into two repos:

- [M-SENA Frontend](https://github.com/FlameSky-S/M-SENA-frontend)
- [M-SENA Backend](https://github.com/iyuge2/M-SENA-Backend)

# Installation

## Docker

For demonstration, we provide a [docker image](https://hub.docker.com/repository/docker/flamesky/m-sena-platform) with one chinese dataset and two pretrained models integrated. To reduce image size, there's also an image with no datasets included.

> Note: The docker images are for demonstration purposes only. There's no guarantee on performance(no cuda support) or stability. For production purposes, please refer to [Build from Scratch](#build-from-scratch).
 
Follow below steps to use the docker image:

- Download docker image from [Docker Hub](https://hub.docker.com/repository/docker/flamesky/m-sena-platform) or use the command-line tool:

```shell
$ docker pull flamesky/m-sena-platform:latest
```

- Run the following command:

```shell
$ docker run -itd -p 5000:5000 -p 80:80 -p 8096:8096 --env BASE_URL="your_server_ip" flamesky/m-sena-platform:latest
```

The `-p` arguments foward 3 ports from docker to the host machine. Do not alter the mappings unless you know what you're doing. 

The `--env` argument sets a global environment variable `BASE_URL`. You should change `your_server_ip` into your server's ip address.

- Open browser and visit your server's ip address.

## Build from Scratch

Follow the instructions on these pages to set up frontend and backend on your server:

- [Frontend](https://github.com/FlameSky-S/M-SENA-frontend#installation)
- [Backend](https://github.com/iyuge2/M-SENA-Backend#installation)

You can deploy frontend and backend on separate servers. 

# Collaboration

For commercial collaborations (model customization, data customization, end-to-end function development, etc.), please contact THUIAR Team at xuhua@tsinghua.edu.cn

# License

M-SENA Platform is published under the GNU GPL 3 license.
