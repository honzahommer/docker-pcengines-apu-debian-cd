# Docker image for building Debian installer CD for PC Engines APU board with mSATA drive

## How to use this image

#### Dockerfile

```
FROM honzahommer/pcengines-apu-debian-cd
...
```

#### Docker run

Debian installer CD image file will be builded into `$PWD/images` directory.

```
docker run --rm -v $PWD/images:/opt/pcengines/images honzahommer/pcengines-apu-debian-cd [profile]
```

#### Clone repository and build custom image

```
git clone https://github.com/honzahommer/docker-pcengines-apu-debian-cd.git
cd docker-pcengines-apu-debian-cd
...
docker build --tag pcengines-apu-debian-cd .
docker run --rm -v $PWD/images:/opt/pcengines/images pcengines-apu-debian-cd [profile]
```
