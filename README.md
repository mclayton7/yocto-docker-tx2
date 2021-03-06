# yocto-docker-tx2
This is a repository for a baseline NVIDIA Jetson TX2 with Docker (not NVIDIA docker yet, see [https://github.com/madisongh/meta-tegra/pull/248](https://github.com/madisongh/meta-tegra/pull/248))

## Building on a Linux Machine
1. Clone this repository
2. Run the following from root of the repository to set up the build environment: 
```console
user@server$ source layers/poky/oe-init-build-env build
```
3. To build an image, run the following command:
```console
user@server$ bitbake -k core-basic-image
```
4. Once it completes successfully, the image will be located in ```build/tmp/deploy/images/raspberrypi4-64/``` with the name ```rpi-basic-image-raspberrypi4-64.rpi-sdimg```
5. Use ```dd``` on Linux or a tool like [Balena Etcher](https://www.balena.io/etcher/) for Windows and Linux to flash the image to an SD Card

## Sources
- https://github.com/madisongh/meta-tegra
- https://medium.com/@shantanoodesai/run-docker-on-a-raspberry-pi-4-with-yocto-project-551d6b615c0b
