### Jedi Knight II: Jedi Outcast Dedicated Server Container

This is a container for hosting a Jedi Knight II: Jedi Outcast dedicated server (jk2mv v1.4.1)

#### Method

The exposes the necessary ports to run the server and installs some dependencies. This repository contains the native shared library needed to host the fastest server possible.

#### Launching

Copy your .pk3 files from your copy of Jedi Outcast's base folder and paste them into `jk2-server/base`.
Copy your amd64 or i386 jk2mvded binary to `jk2-server` and verify it is executable

##### Manual Launch

If you need to pass other launch parameters you can launch the container with this command:

```docker run -d -v /path/to/docker-jk2/jk2-server:/root docker-jk2```

If you're running multiple instances on the same box you can remap the ports by using parameters:

```docker run -d -v /path/to/docker-jk2/jk2-server:/root docker-jk2 +set net_port 28060```

#### Version changing

You can specify the version of JK2 used on the server by editing the server.cfg file and changing the line "seta mv_serverversion" to 1.02, 1.03 or 1.04. Be aware that your clients must be on the same version.

#### Customizing

Included in this repository is a server.cfg file in the `base` folder. You can use this to customize server settings.

A lot more options are available for JK2MV, just checkout [their documentation.](https://github.com/mvdevs/jk2mv/wiki/Server-hosting)

* [JK2MV](https://jk2mv.org/)