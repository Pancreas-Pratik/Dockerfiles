# Dockerfile Collection for DGX-230

## Master branch

Here we provide a submodule `noVNCbin` cloned from 

[https://github.com/novnc/noVNC](https://github.com/novnc/noVNC)

and we also provide a wrapping script `noVNC` which calls the `noVNCbin` scripts here.

To make use of this service, just copy this branch to your `/usr/local/bin/` like

```Bash
/etc/ssl/
`---vncssl.cnf

/usr/local/bin/
|---noVNC
`---noVNCbin
    |---utils
    |   |---launch.sh
    |   `---...
    `---...
```

And you could use such simple command on your Bash:

```Bash
noVNC IP=192.168.127.128:5901 PORT=6080
```

where `5901` is the entry (input) port and `6080` is the service (output) port.

## Dockerfile list

To view the manual, please check [here](./manual).

To view the detailed graphic guides, click [here](./manual-session).

To view extra manuals about xUbuntu, please check [here](./manual-xubuntu).

To view our dockerfile list, please check [here](./dockerlist).

## Dockerfiles

Here is the list of each dockerfile:

1. xubuntu at the branch [**xubuntu**](https://github.com/cainmagi/Dockerfiles/tree/xubuntu)

    Run such a command to build the newest image online:

    ```Bash
    docker build -t xubuntu:1.0 https://github.com/cainmagi/Dockerfiles.git#xubuntu
    ```

2. jupyterlab at the branch  [**jupyterlab**](https://github.com/cainmagi/Dockerfiles/tree/jupyterlab)

    Run such a command to build the newest image online:

    ```Bash
    docker build -t jlab:1.0 https://github.com/cainmagi/Dockerfiles.git#jupyterlab
    ```

## Update records

### ver 1.5 @ 4/20/2022

1. Finish the re-crafted `xubuntu` dockerfile and `jupyterlab` dockerfile.
2. Update the submodule `noVNC` to newest version.
3. Write some new guides.

### ver 1.45 @ 2/2/2021

1. Add `openssl` support.
2. Update the submodule `noVNC` to newest version.

### ver 1.4 @ 1/11/2021

1. Finish the re-crafted `xubuntu` dockerfile.
2. Update the submodule `noVNC` to newest version.
3. Add tips and comments.
4. Change the `gitpage` path.

### ver 1.3 @ 20191114

Finish the `xubuntu-tf2` dockerfile.

### ver 1.2 @ 20180820

Update master branch. This update includes:

1. Update the submodule `noVNC` to newest version.
2. Update the start script so that it could be appiled to both `Ubuntu 16.04` and `Ubuntu 18.04`.

### ver 1.16 @ 20180820

Update xubuntu-tf to 1.2 version.

### ver 1.15 @ 20180819

1. Revise the `xubuntu-tf` dockerfile for fixing some bugs in the installation scripts.
2. Revise the `xubuntu` dockerfile, upgrade its dependencies and make a good preparation for installing caffe with gcc-6.3.0 in this image.

### ver 1.12 @ 20180816

1. Revise the `xubuntu-tf` dockerfile and upgrade its dependencies.
2. Revise `noVNC`, now we do not need to change anything but just copy it for the installation.
3. Arrange the page of this project.

### ver 1.1 @ 20180815

Add the `xubuntu-tf` dockerfile.

### ver 1.0 @ 20180605

Create the branch, add the noVNC submodule and add the `xubuntu` dockerfile.