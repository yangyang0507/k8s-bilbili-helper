# k8s-bilbili-helper

本项目仅对 bilibli-helper 以及 docker 化的 docker-bilibili-helper 进行了简单的 Kubernetes 容器编排脚本编写，没有什么技术含量，仅方便大家能够快速的在 Kubernetes 中启动一个 bilibili-helper。如有需要后续可考虑提供 helm 版本。

感谢原本作者及其项目：[JunzhouLiu/BILIBILI-HELPER](https://github.com/JunzhouLiu/BILIBILI-HELPER)

感谢 Docker 化作者及其项目：[SuperNG6/docker-bilbili-helper](https://github.com/SuperNG6/docker-bilbili-helper)

## 使用方法

> 使用前提：你已经有了一个 Kubernetes 容器环境，且已经配置好 kubectl 命令行工具以及集群访问的密钥

克隆或者下载本项目，然后编辑 bilibili-helper.yaml 中对应的配置（具体参考 [docker-bilbili-helper](https://github.com/SuperNG6/docker-bilbili-helper)），修改好之后使用 `kubectl apply -f bilibili-helper.yaml` 即可向集群中部署 bilibili-helper。

## 备注

Deployment 中的 spec.template.spec.containers.env 中的配置请参考 [docker-bilibili-helpoer 的参数说明](https://github.com/SuperNG6/docker-bilbili-helper#%E5%8F%82%E6%95%B0%E8%AF%B4%E6%98%8E)。
ConfigMap 中的 config.json 配置请参考 [docker-bilibili-helpoer 的配置自定义功能说明](https://github.com/SuperNG6/docker-bilbili-helper#%E9%85%8D%E7%BD%AE%E8%87%AA%E5%AE%9A%E4%B9%89%E5%8A%9F%E8%83%BD)
