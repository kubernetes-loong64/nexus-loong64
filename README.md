# Nexus for LoongArch64

<p align="center"><a href="README.md">English</a> | <a href="README-zh.md">中文</a></p>

<p align="center"><img src="https://img.shields.io/badge/Nexus%20LoongArch64%20%E9%BE%99%E8%8A%AF%E6%9E%B6%E6%9E%84%E5%8F%91%E8%A1%8C%E7%89%88-blue?logo=sonatype&logoColor=white" alt="Nexus LoongArch64 龙芯架构发行版"></p>

Prebuilt [Sonatype Nexus Repository Manager](https://www.sonatype.com/products/sonatype-nexus-repository) Docker images for the **LoongArch64 (loong64)** architecture.

## Docker Images

Images are published to Docker Hub under [`kubernetesloong64/nexus3-loong64`](https://hub.docker.com/r/kubernetesloong64/nexus3-loong64).

- [![kubernetesloong64/nexus3-loong64](https://img.shields.io/docker/v/kubernetesloong64/nexus3-loong64?arch=loong64&logo=docker&label=kubernetesloong64%2Fnexus3-loong64&sort=semver)](https://hub.docker.com/r/kubernetesloong64/nexus3-loong64/tags)

### Pull Images

```shell
docker pull kubernetesloong64/nexus3-loong64:3.93.1
```

### Usage

```shell
docker run -d --name nexus \
  -p 8081:8081 \
  -v nexus-data:/nexus-data \
  kubernetesloong64/nexus3-loong64:3.93.1
```

After starting, get the initial admin password:

```shell
docker exec nexus cat /nexus-data/admin.password
```

## Branch Naming

Push a branch named `loong64-<nexus-version>` (e.g. `loong64-3.93.1`) to trigger a build.

## License

[Apache License 2.0](LICENSE)
