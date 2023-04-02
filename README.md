# docker-aws-cli
Some amazing Docker images to work with aws-cli Out Of The Box

[![Docker Hub](https://img.shields.io/static/v1.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=flat&label=lcaparros/aws-cli&message=Docker%20Hub&logo=docker)](https://hub.docker.com/r/lcaparros/aws-cli)
[![Docker Pulls](https://img.shields.io/docker/pulls/lcaparros/aws-cli.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=flat&label=pulls&logo=docker)](https://hub.docker.com/r/lcaparros/aws-cli)
[![GitHub Repository](https://img.shields.io/static/v1.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=flat&label=lcaparros/docker-aws-cli&message=GitHub%20Repo&logo=github)](https://github.com/lcaparros/docker-aws-cli)
[![GitHub](https://img.shields.io/static/v1.svg?color=4edafc&labelColor=555555&logoColor=ffffff&style=flat&label=lcaparros&message=GitHub&logo=github)](https://github.com/lcaparros "view the source for all of our repositories.")

## Usage
Run the command below and begin using the cli as if aws-cli was installed.

```
docker run -it --name aws lcaparros/aws-cli
```

# Contribution

## Pull Requests

Create a new Pull Request with the necessary changes. After being reviewed and merged a new tag will be generated, creating a new Release and publishing the new version.

```shell
$ git tag -a v1.0.9 -m "This is my new amazing version"
$ git push origin v1.0.9
```

## How to push a new version of the image manually

```shell
$ docker build --build-arg VERSION=<version> --build-arg BUILD_DATE="$(date +%Y/%m/%dT%H:%M:%S)" -t aws-cli .
$ docker tag terraform lcaparros/aws-cli:<version>
$ docker push lcaparros/aws-cli:<version>