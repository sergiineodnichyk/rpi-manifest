# YoctoRaspberryPI
RaspberryPI distro build using Yocto(dunfell)

Based on Mender integration layer for Raspberry Pi family of boards.
The supported and tested boards are:

- [Raspberry Pi 4 Model B](https://hub.mender.io/t/raspberry-pi-4-model-b/889/2)
- [Raspberry Pi 3 Model B/B+](https://hub.mender.io/t/raspberry-pi-3-model-b-b/57)
- [Raspberry Pi CM3](https://hub.mender.io/t/raspberry-pi-compute-module-3/110/2)
- [Raspberry Pi 0 Wifi](https://hub.mender.io/t/raspberry-pi-0-wifi/78)

#### Install repo

	# curl https://storage.googleapis.com/git-repo-downloads/repo > /usr/local/bin/repo
	# chmod a+x /usr/local/bin/repo


#### Get project

	repo init -u git@github.com:sergiineodnichyk/rpi-manifest.git -b master
	repo sync -c

#### Build project

source setup-environment raspberrypi

MACHINE=raspberrypi4 bitbake core-image-base

#### Yocto required

    # apt-get install gawk wget git-core diffstat unzip texinfo gcc-multilib build-essential chrpath socat libsdl1.2-dev xterm

