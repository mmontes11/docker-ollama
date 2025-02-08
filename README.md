# docker-ollama

Docker compose setup for Ollama and Open WebUI

## CPU installation

```bash
docker compose up -d
```

## NVIDIA GPU installation in Ubuntu

First of all, make sure you have the nVidia drivers install. You may [follow this guide](https://github.com/oddmario/NVIDIA-Ubuntu-Driver-Guide?tab=readme-ov-file#-installing-through-the-graphics-drivers-ppa-repository-recommended).


Then, install the [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/latest/install-guide.html#installation) package:
```bash
sudo bash scripts/nvidia.sh
```

Finally, run the docker compose:
```bash
docker compose -f docker-compose.yml -f docker-compose.gpu.yml up -d
```