# vscodedc-java11-gradle

OpenJDK 11 Gradle VSCODE Docker development container (devcontainer)

## References
1. [Microsoft Docs](https://code.visualstudio.com/docs/devcontainers/containers)
1. [CyberBok](https://github.com/dewcservices/CyBOK/content/en/docs/sofware-practices/devcontainers/index.md)

## What is it

|Name|Description|Additional|
|--|--|--|
|Base Image|openjdk:11-jdk| |
|openJdk11| openJDK v11 | |
|gradel| v7.2||

## How to use

General instructions including general concepts, setting up you linux environment, and cloning as a submodule are provided at [reference 2](https://github.com/dewcservices/CyBOK/content/en/docs/sofware-practices/devcontainers/index.md).

The following are specific commands for this devcontainer

### Add devcontainer to a project for the first time

```shell
git submodule add ssh://<submodule-repo>.git ./.devcontainer
```

#### Expected result

/.gitmodules
```shell
[submodule ".devcontainer"]
    path = .devcontainer
    url = ssh://<submodule-repo>.git
```

### Cloning a project with submodules

```shell
git clone --recurse-submodles ssh://<submodule-repo>.git
```


### Customising the devcontainer for your project

It is likely you will want to extend the docker-compose.yml file to include containers to develop against (kafka, databases ...).
To do this you should create a branch of this project and use the branch as a sub-module within your project.

## TODO
- Make the openJDK and gradle verions configurable