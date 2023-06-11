# docker dev container for rust language development

## Get Start

1. Create compose-dev.yaml in your project root dir or an empty dir, following config bind ./ to /com.docker.devenvironments.code, docker  makes /com.docker.devenvironments.code the default working dir.

    ```yaml
    services:
    app:
        entrypoint:
        - sleep
        - infinity
        image: wgetmeoh/rust-lang-dev-env:debian
        init: true
        volumes:
        - type: bind
        source: ./
        target: /com.docker.devenvironments.code
    ```

2. Use docker dashboard create dev environment

    Note that your project needs to include the compose-dev.yaml that mentioned above.

    ![Alt text](image.png)

## Container content

This container is from image: dibian:lastest, what I prepare for rust dev environment by following steps.

* install git
* install curl
* install zsh
* install oh-mu-zsh and some plugins
* install gcc
* install rust
* install container vscode extensions: rust-analyzer and codeLLdb
