# Kubernetes-Administration

## 1. Prefix

- 授课时长：
    - 上午：9:30 至 12:00
    - 下午：13:30 至 16:00
- Prerequisite
    - vim 基础操作 -- 编辑、修改、保存文件
    - 网络基础知识 -- 网段 cidr、vlan、vxlan、配置 linux 网卡等等
    - 基础的 linux 知识 -- 权限、文件系统、服务
    - systemd 的基础操作 -- 重启、关闭、启动、重载、查看 systemd 的服务

## 2. Catalog

| Date | Time | Title | Content |
| ---- | ---- | ----- | ------- |
| 第 1 天 | 上午 | [1. Linux 容器和 Docker](#lesson-01lxc--docker) | [1.1 什么是 Linux 容器？](#11-什么是-linux-容器) |
| | | | [1.2 容器和虚拟机有何区别？](#12-容器和虚拟机有何区别) |
| | | | [1.3 Docker 和容器技术有什么关系？](#13-docker-和容器技术有什么关系) |
| | | | [1.4 Docker 的架构和概念空间是怎样的？](#14-docker-的架构和概念空间是怎样的) |
| | | | [1.5 什么是所谓的安全容器技术？](#15-什么是所谓的安全容器技术) |
| | | | [1.6 实验：Docker Quick Start](#16-实验docker-quick-start) |
| | 下午 | | [1.7 Docker 的网络模型](#17-docker-的网络模型) |
| | | | [1.8 Docker 的存储模型](#18-docker-的存储模型) |
| | | [2. Kubernetes 的快速入门](#lesson-02kubernetes-concepts) | [2.1 什么是 K8S？](#21-什么是-k8s) |
| | | | [2.2 K8S 是为了解决什么问题？](#22-k8s-是为了解决什么问题) |
| | | | [2.3 K8S 不解决什么问题？](#23-k8s-不解决什么问题) |
| | | | [2.4 K8S 的模块架构是怎样的？](#24-k8s-的模块架构是怎样的) |
| | | | [2.5 K8S 有哪些竞争产品？](#25-k8s-有哪些竞争产品) |
| | | | [2.6 怎么部署出一个 K8S 群集？](#26-怎么部署出一个-k8s-群集) |
| | | | [2.7 实验：K8S 的部署](#27-实验k8s-的部署) |
| | | | [2.8 什么是 Pod？](#28-什么是-pod) |
| | | | [2.9 实验：启动一个 pod ](#29-启动一个-pod) |
| 第 2 天 | 上午 | [3. K8S 的概念空间](#lesson-03k8s-concepts) | [3.1 什么是 YAML？](#31-什么是-yaml) |
| | | | [3.2 什么是 Namespace & Quota？](#32-什么是-namespace--quota) |
| | | | [3.3 什么是 Deployment & ReplicaSet？](#33-什么是-deployment--replicaset) |
| | | | [3.4 什么是 Services？](#34-什么是-services) |
| | | | [3.5 实验：K8S Dashboard](#35-实验k8s-dashboard) |
| | | | [3.6 实验：K8S 怎么发布服务和扩缩容？](#36-实验k8s-怎么发布服务和扩缩容) |
| | | | [3.7 DeamonSet & SetfulSet](#37-deamonset--statefulset) |
| | 下午 | | [3.8 实验：ETCD 操作](#38-实验etcd-操作) |
| | | | [3.9 什么是静态 Pod？](#39-什么是静态-pod) |
| | | [4. K8S 的认证和安全](#lesson-04k8s-auth--security) | [4.1 什么是 K8S 的 3A？](#41-什么是-k8s-的-3a) |
| | | | [4.2 怎么配置 kubectl？](#42-怎么配置-kubectl) |
| | | | [4.3 K8S 怎么保证网络安全？](#43-k8s-怎么保证网络安全) |
| | | | [4.4 什么是用户和角色？](#44-什么是用户和角色) |
| | | | [4.5 实验：添加用户 & 绑定角色](#45-实验添加用户--绑定角色) |
| 第 3 天 | 上午 | [5. K8S 的调度](#lesson-05-k8s-schedule) | [5.1 怎么部署一个多节点的 K8S 群集？](#51-怎么部署多节点的-k8s-集群) |
| | | | [5.2 怎么把应用部署到指定的 Node？](#52-怎么把应用部署到指定的-node) |
| | | | [5.3 什么是 Taints & Toleration？](#53-什么是-taints--toleration) |
| | | | [5.4 什么是 Node Affinity？](#54-什么是-node-affinity) |
| | | | [5.5 什么是 Pod Affinity？](#55-什么是-pod-affinity) |
| | | | [5.6 实验：Pod 调度](#56-实验pod-调度) |
| | 下午 | [6. K8S 的数据持久化](#lesson-06-k8s-storage) | [6.1 什么是 ConfigMap & Secret？](#61-什么是-configmap--secret) |
| | | | [6.2 什么是 PV / PVC？](#62-什么是-pv--pvc) |
| | | | [6.3 什么是 Storage Class？](#63-什么是-storage-class) |
| | | | [6.4 实验：ConfigMap / Secret / PV & PVC / StorageClass](#64-实验configmap--secret--pv--pvc--storageclass) |
| | | [7. 服务发布](#lesson-07-service) | [7.1 Service 在底层是怎么实现的？](#71-service-在底层是怎么实现的) |
| | | | [7.2 实验：发布服务](#72-实验发布服务) |
| | | | [7.3 什么是 Ingress？](#73-什么是-ingress) |
| | | | [7.4 实验：对集群外发布服务](#74-实验对集群外发布服务) |
| | | [8. 其它](#lesson-08advance) | [8.1 监控、日志、排错](#81-监控日志排错) |
| | | | [8.2 什么是 HPA / CA / VA？](#82-什么是-hpa--ca--va) |
| | | | [8.3 什么是 Federation？](#83-什么是-federation) |
| | | | [8.4 K8S 怎么处理有状态服务？](#84-k8s-怎么处理有状态服务) |
| | | | [8.5 其它参考](#85-其它参考) |
| 第 4 天 | 上午 | [9. CKA 考试讲解](#lesson-09cka) | [9.1 考试注意事项](#91-考试注意事项) |
| | | | [9.2 模拟题讲解](#92-模拟题讲解) |
| | 下午 | | [9.3 实验：做模拟题](#93-实验做模拟题) |

## Lesson 01：LXC & Docker

### 1.1 什么是 Linux 容器？

- 虚拟化技术的演进

    ![](../images/container-evolution.png)

- 虚拟化是为了解决什么问题？资源隔离 & 资源限制
- 什么是 Linux 容器？namespace & cgroup
- 什么是 lxc namespace？

    ![](../images/kernel-user-mode.png)

- 什么是 CGroup？
- Mac 和 Win 上 有容器技术么？

### 1.2 容器和虚拟机有何区别？

- 原理
- 应用场景

### 1.3 Docker 和容器技术有什么关系？

- 什么是 [Docker](https://docs.docker.com/engine/docker-overview/#namespaces)（ [QuickStart](https://docs.docker.com/get-started/) ）？

    ![](../images/docker-undertech.png)

- Docker 和容器有什么关系（ why Linus don't care docker ）？
- Docker 有哪些竞争产品？[CRI-O ？](https://zhuanlan.zhihu.com/p/30667806)

### 1.4 Docker 的架构和概念空间是怎样的？

- 概念空间

    ![](../images/docker-arch.png)

- 模块架构

### 1.5 什么是所谓的安全容器技术？

- 容器的天然不安全与天然安全
- [Kata Container](https://katacontainers.io/learn/)，[PDF](https://katacontainers.io/collateral/kata-containers-1pager.pdf)

    ![](../images/katacontainers_traditionalvskata_diagram.jpg)

- 竞争者：gVisor / firecracker / rustVM

### 1.6 实验：Docker Quick Start

- 在 Ubuntu 18.04 上配置 Docker

    ```bash
    # 更新依赖仓库
    apt-get update -y

    # 安装 Docker
    apt-get install docker.io -y
    systemctl enable docker
    systemctl start docker

    ## 检查 docker 服务状态
    systemctl status docker

    ## run hello-world
    docker run hello-world
    ```

- [如何创建一个镜像？如何启动和调试容器？](https://github.com/99cloud/lab-openstack/tree/master/src/docker-quickstart)

    ```console
    $ python app.py
     * Running on http://0.0.0.0:80/ (Press CTRL+C to quit)

    $ docker run -p 4000:80 maodouzi/get-started:part2
     * Running on http://0.0.0.0:80/ (Press CTRL+C to quit)

    # 进入容器调试
    $ docker exec -it 4224b69e7ee3 /bin/bash
    root@4224b69e7ee3:/app# env
    HOSTNAME=4224b69e7ee3
    PWD=/app
    HOME=/root
    NAME=World
    ...

    # 查看容器日志
    $ docker logs -f 4224b69e7ee3

    # 结束容器
    $ docker stop 4224b69e7ee3

    # 删除容器
    $ docker rm 4224b69e7ee3

    #  删除镜像
    $ docker rmi maodouzi/get-started:part2
    ```

- [Docker 官方入门参考资料](https://docs.docker.com/get-started/)

### 1.7 Docker 的网络模型

- Bridge 模式
- Host 模式
- CNM

### 1.8 Docker 的存储模型

- Mount 模式
- Volumn 模式

## Lesson 02：Kubernetes Concepts

### 2.1 什么是 K8S？

- 什么是 Kubernetes？容器编排工具。为什么叫 K8S？
- K8S 和 Docker 有什么关系？参考：[Container runtimes](https://kubernetes.io/docs/setup/production-environment/container-runtimes/)
    - Orchestration API -> Container API (cri-runtime) -> Kernel API(oci-runtime)
    - OCI：runC / Kata（ 及其前身 runV 和 Clear Containers ），gVisor，Rust railcar
        - 容器镜像的制作标准，即 ImageSpec。大致规定：容器镜像这个压缩了的文件夹里以 xxx 结构放 xxx 文件
        - 容器要需要能接收哪些指令，以及这些指令的行为，即 RuntimeSpec。这里面的大致内容就是“容器”要能够执行 “create”，“start”，“stop”，“delete” 这些命令，并且行为要规范。
        - Docker 则把 libcontainer 封装了一下，变成 runC 捐献出来作为 OCI 的参考实现。
    - CRI：Docker（ 借助 dockershim ），containerd（ 借助 CRI-containerd ），CRI-O，Frakti。是一组 gRPC 接口，[cri-api/pkg/apis/services.go](https://github.com/kubernetes/cri-api/blob/master/pkg/apis/services.go)：
        - 一套针对容器操作的接口，包括创建，启停容器等等
        - 一套针对镜像操作的接口，包括拉取镜像删除镜像等
        - 一套针对 PodSandbox（容器沙箱环境）的操作接口
    - 正常的 K8S 调用 Docker 流程

        ![](../images/k8s-CRI-OCI-docker.png)

    - containerd-1.0，对 CRI 的适配通过一个单独的进程 CRI-containerd 来完成

        ![](../images/k8s-containerd-1-0.png)

    - containerd-1.1，把适配逻辑作为插件放进了 containerd 主进程中

        ![](../images/k8s-containerd-1-1.png)

    - CRI-O，更为专注的 cri-runtime，非常纯粹，兼容 CRI 和 OCI，做一个 Kubernetes 专用的运行时

        ![](../images/k8s-cri-o-flow.png)

- [CRI-O](https://cri-o.io/) 的架构：

    ![](../images/k8s-cri-o-arch-1.png)

    ![](../images/k8s-cri-o-arch-2.jpg)

- K8S 和 Borg 有何关系？Start from Borg, however completely different!

    ![](../images/borg-arch.png)

### 2.2 K8S 是为了解决什么问题？

- K8S 有什么优势？适用于哪些场景？自动化编排：自愈，快速缩放，一键部署和升降级，备份恢复
- 如何查文档？[K8S](https://kubernetes.io/)，[OpenShift Origin](https://www.okd.io/)
- 其它资料：slack、cncf、quay.io

### 2.3 K8S 不解决什么问题？

- 用户管理
- 限流熔断：istio
- 监控审计：prometheus / grafana / alertmanager / elasticsearch / fluent / kibana
- 用户界面
- 中间件
- 底层云平台支持

### 2.4 K8S 的模块架构是怎样的？

- [K8S 有哪些组件](https://kubernetes.io/zh/docs/concepts/architecture/#)？api-server、kube-scheduler、kube-controller、etcd、coredns、kubelete、kubeproxy

- 整体结构图

    ![](../images/k8s-architecture.png)

### 2.5 K8S 有哪些竞争产品？

- [OpenShift](https://www.openshift.com/learn/what-is-openshift-x)
    - 和 K8S 相比，OpenShift（ 红帽最有价值的产品 ）有哪些优势？

        ![](../images/openshift-k8s.svg)

- VMware
- KubeSphere
- Ranchel

### 2.6 怎么部署出一个 K8S 群集？

- kubeadm
- Ansible

### 2.7 实验：K8S 的部署

1. [安装 kubeadm](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/install-kubeadm/)

    ```bash
    # iptables 看到 bridged 流量
    cat <<EOF | sudo tee /etc/sysctl.d/k8s.conf
    net.bridge.bridge-nf-call-ip6tables = 1
    net.bridge.bridge-nf-call-iptables = 1
    EOF
    sudo sysctl --system

    # Install kubeadm
    apt-get update && apt-get install -y apt-transport-https curl
    curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
    cat <<EOF | sudo tee /etc/apt/sources.list.d/kubernetes.list
    deb https://apt.kubernetes.io/ kubernetes-xenial main
    EOF
    apt-get update -y && apt-get install -y kubelet kubeadm kubectl

    # 重启 kubelet
    systemctl daemon-reload
    systemctl restart kubelet

    # 检查 kubelet 状态
    systemctl status kubelet
    ```
1. [用 kubeadm 创建一个 k8s 群集](https://kubernetes.io/zh/docs/setup/independent/create-cluster-kubeadm/)

    ```bash
    # 拉起 k8s 群集
    kubeadm init --pod-network-cidr 192.168.1.90/16

    # 配置 kubectl 客户端
    mkdir -p $HOME/.kube
    sudo cp -i /etc/kubernetes/admin.conf $HOME/.kube/config
    sudo chown $(id -u):$(id -g) $HOME/.kube/config
    ```

1. 此时可以观察到 node 并未 ready，导致 coredns 无法调度。接下来需要：[安装网络插件](https://kubernetes.io/zh/docs/setup/independent/create-cluster-kubeadm/#Pod-network)，[插件列表](https://kubernetes.io/docs/concepts/cluster-administration/addons/)，这里我们用 [Calico](https://docs.projectcalico.org/getting-started/kubernetes/quickstart)。

    ```bash
    # 添加网络插件
    # Install the Tigera Calico operator and custom resource definitions
    kubectl create -f https://docs.projectcalico.org/manifests/tigera-operator.yaml
    # Install Calico by creating the necessary custom resource
    kubectl create -f https://docs.projectcalico.org/manifests/custom-resources.yaml

    # 查看 pods 和 nodes 状态
    kubectl get pods --all-namespaces
    kubectl get nodes
    ```

### 2.8 什么是 Pod？

- Pod 和容器的关系是什么？
- 为什么调度的基本单位是 pod 不是容器？

### 2.9 启动一个 pod

- [Pod YAML](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/)

    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: nginx
      labels:
        env: test
    spec:
      containers:
      - name: nginx
        image: nginx
    ```

- 启动一个 Pod

    ```
     起 nginx pod
    kubectl apply -f nginx.yaml

    # 可以看到 pod 无法被调度，进行诊断
    kubectl describe pod nginx

    # 去污点、允许调度到 master
    kubectl taint nodes cka003 node-role.kubernetes.io/master:NoSchedule-

    # 查看 pods
    kubectl get pods

    # 查看容器
    docker ps | grep nginx
    ```

- 在容器平台上发布 Python 应用
    - 我们将要做什么？
        - 下载应用代码，并且在本地跑起来
        - 为应用构建一个 Docker 镜像，然后启动一个 Docker 容器来运行此应用
        - 创建一个 Deployment 对象，将应用运行在 K8S 平台上
        - 参考：[https://kubernetes.io/blog/2019/07/23/get-started-with-kubernetes-using-python/](https://kubernetes.io/blog/2019/07/23/get-started-with-kubernetes-using-python/)
    - 预置条件有哪些？
        - 本地具备 Python 3.6+ 的运行环境
        - 安装了 Git（非必须）
        - 安装了 Docker
        - 一个 Kubernetes 平台
    - 获取代码：`git clone https://github.com/JasonHaley/hello-python.git`，在 hello-python/app 目录下有两个文件：
        - 其中 `requirements.txt` 里只有一行：Flask，是依赖包列表文件
        - 另一个文件是 `main.py`，是应用的逻辑代码

            ```python
            from flask import Flask
            import os
            import socket

            app = Flask(__name__)

            @app.route("/")
            def hello():
                html = "<h3>Hello {name}!</h3>" \
                       "<b>Hostname:</b> {hostname}<br/>"
                return html.format(name=os.getenv("NAME", "world"), hostname=socket.gethostname())

            if __name__ == "__main__":
                app.run(host='0.0.0.0')
            ```

    - 本地运行：
        - 安装依赖：`pip install -r requirements.txt`（pip 如果没有，改成 pip3）
        - 本地运行：`python main.py`（python 如果没有，改成 python3），会在本地启动一个用于开发的 web 服务器。
        - 你可以打开浏览器，访问 `http://localhost:5000` 端口
    - Docker 镜像构建文件，在 hello-python/docker 目录下有一个 Dockerfile 文件

        ```dockerfile
        FROM python:3.7

        RUN mkdir /app
        WORKDIR /app
        ADD . /app/
        RUN pip install -r requirements.txt

        EXPOSE 5000
        CMD ["python", "/app/main.py"]
        ```

    - 构建 Docker 镜像并运行
        - 将 Dockerfile 文件复制到 hello-python/app 目录中
        - 运行命令构建镜像：`docker build -f Dockerfile -t hello-python:latest .`
        - 构建完成后，可以通过 `docker image ls` 看到刚才构建的镜像
        - 然后运行此镜像：`docker run -p 5001:5000 hello-python`
        - 然后访问 `http://localhost:5001`，同样可以看到 `Hello form Python!` 字符串
    - 确定 Kubernetes 和 kubectl 运行正常
        - 运行命令：`kubectl version`，如果该命令不报错，就说明 kubectl 安装完成。
        - 运行命令：`kubectl get nodes`，如果返回节点信息，说明 K8S 运行正常，kubectl 配置正常。
    - K8S deployment YAML 文件：[https://github.com/JasonHaley/hello-python/blob/master/kubernetes/deployment.yaml
](https://github.com/JasonHaley/hello-python/blob/master/kubernetes/deployment.yaml)

        ```yaml
        apiVersion: v1
        kind: Service
        metadata:
          name: hello-python-service
        spec:
          type: NodePort
          selector:
            app: hello-python
          ports:
          - protocol: "TCP"
            port: 6000
            targetPort: 5000
            nodePort: 31000

        ---
        apiVersion: apps/v1
        kind: Deployment
        metadata:
          name: hello-python
        spec:
          selector:
            matchLabels:
              app: hello-python
          replicas: 4
          template:
            metadata:
              labels:
                app: hello-python
            spec:
              containers:
              - name: hello-python
                image: hello-python:latest
                imagePullPolicy: Never
                ports:
                - containerPort: 5000
        ```

    - 将 Deployment 部署到 K8S 平台
        - 运行命令：`kubectl apply -f deployment.yaml`
        - 运行命令：`kubectl get pods，检查 pods`
        - 然后可以打开浏览器，在 `http://localhost:31000` 看到 `Hello form Python!` 信息

## Lesson 03：K8S concepts

### 3.1 什么是 YAML？

- 怎么理解 YAML？列表 / 字典 / 数字 / 字符串 / Bool

### 3.2 什么是 Namespace & Quota？

- Namespace & 租户隔离
- [实验：namespace & quota](https://kubernetes.io/docs/tasks/administer-cluster/manage-resources/quota-memory-cpu-namespace/)

    ```bash
    # 创建一个 namespace
    kubectl create namespace quota-mem-cpu-example

    # 为这个 namespace 限定配额
    kubectl apply -f https://k8s.io/examples/admin/resource/quota-mem-cpu.yaml --namespace=quota-mem-cpu-example

    # 查看配额的详细信息
    kubectl get resourcequota mem-cpu-demo --namespace=quota-mem-cpu-example --output=yaml

    # 创建一个 pod，并限制它的资源使用
    kubectl apply -f https://k8s.io/examples/admin/resource/quota-mem-cpu-pod.yaml --namespace=quota-mem-cpu-example

    # 确认 pod 已经启动
    kubectl get pod quota-mem-cpu-demo --namespace=quota-mem-cpu-example

    # 再次查看配额信息，检查已用部分
    kubectl get resourcequota mem-cpu-demo --namespace=quota-mem-cpu-example --output=yaml

    # 尝试启动第二个 pod，因为配额原因，失败
    kubectl apply -f https://k8s.io/examples/admin/resource/quota-mem-cpu-pod-2.yaml --namespace=quota-mem-cpu-example

    # Error from server (Forbidden): error when creating "examples/admin/resource/quota-mem-cpu-pod-2.yaml":pods "quota-mem-cpu-demo-2" is forbidden: exceeded quota: mem-cpu-demo, requested: requests.memory=700Mi,used: requests.memory=600Mi, limited: requests.memory=1Gi

    # 删除命名空间
    kubectl delete namespace quota-mem-cpu-example
    ```

### 3.3 什么是 Deployment & ReplicaSet？

- 实验：Pod Label 和 Replica Controller
- [实验：Deployment 相关](https://kubernetes.io/docs/concepts/workloads/controllers/deployment/)

### 3.4 什么是 Services？

- 基本概念：Service
- 实验：Service

### 3.5 实验：K8S Dashboard

### 3.6 实验：K8S 怎么发布服务和扩缩容？

- [实验：通过 Service 发布服务](https://kubernetes.io/docs/concepts/services-networking/connect-applications-service/)
- 实验：通过 Deployment 扩缩容

### 3.7 DeamonSet & StatefulSet

- [DeamonSet](https://kubernetes.io/docs/concepts/workloads/controllers/daemonset/)
- [StatefulSet](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/)

### 3.8 实验：ETCD 操作

 - Set & Get

    ```console
    root@ckalab001:~# apt install etcd-client

    root@ckalab001:~# ps -ef | grep api | grep -i etcd
    root       24761   24743  3 10:17 ?        00:06:53 kube-apiserver --advertise-address=172.31.43.206 --allow-privileged=true --authorization-mode=Node,RBAC --client-ca-file=/etc/kubernetes/pki/ca.crt --enable-admission-plugins=NodeRestriction --enable-bootstrap-token-auth=true --etcd-cafile=/etc/kubernetes/pki/etcd/ca.crt --etcd-certfile=/etc/kubernetes/pki/apiserver-etcd-client.crt --etcd-keyfile=/etc/kubernetes/pki/apiserver-etcd-client.key --etcd-servers=https://127.0.0.1:2379 --insecure-port=0 --kubelet-client-certificate=/etc/kubernetes/pki/apiserver-kubelet-client.crt --kubelet-client-key=/etc/kubernetes/pki/apiserver-kubelet-client.key --kubelet-preferred-address-types=InternalIP,ExternalIP,Hostname --proxy-client-cert-file=/etc/kubernetes/pki/front-proxy-client.crt --proxy-client-key-file=/etc/kubernetes/pki/front-proxy-client.key --requestheader-allowed-names=front-proxy-client --requestheader-client-ca-file=/etc/kubernetes/pki/front-proxy-ca.crt --requestheader-extra-headers-prefix=X-Remote-Extra- --requestheader-group-headers=X-Remote-Group --requestheader-username-headers=X-Remote-User --secure-port=6443 --service-account-issuer=https://kubernetes.default.svc.cluster.local --service-account-key-file=/etc/kubernetes/pki/sa.pub --service-account-signing-key-file=/etc/kubernetes/pki/sa.key --service-cluster-ip-range=10.96.0.0/12 --tls-cert-file=/etc/kubernetes/pki/apiserver.crt --tls-private-key-file=/etc/kubernetes/pki/apiserver.key

    # 设置环境变量，ETCDCTL_API=3
    root@ckalab001:~# export ETCDCTL_API=3

    root@ckalab001:~# etcdctl --cert="/etc/kubernetes/pki/apiserver-etcd-client.crt" --key="/etc/kubernetes/pki/apiserver-etcd-client.key" --cacert="/etc/kubernetes/pki/etcd/ca.crt" --endpoints=https://127.0.0.1:2379 put /firstkey trystack
    OK

    root@ckalab001:~# etcdctl --cert="/etc/kubernetes/pki/apiserver-etcd-client.crt" --key="/etc/kubernetes/pki/apiserver-etcd-client.key" --cacert="/etc/kubernetes/pki/etcd/ca.crt" --endpoints=https://127.0.0.1:2379 get /firstkey
    /firstkey
    trystack
    ```

    ```bash
    # list 所有的 key
    etcdctl --cert="/etc/kubernetes/pki/apiserver-etcd-client.crt" --key="/etc/kubernetes/pki/apiserver-etcd-client.key" --cacert="/etc/kubernetes/pki/etcd/ca.crt" --endpoints=https://127.0.0.1:2379 get --prefix --keys-only ""

    # list 所有的 key & value
    etcdctl --cert="/etc/kubernetes/pki/apiserver-etcd-client.crt" --key="/etc/kubernetes/pki/apiserver-etcd-client.key" --cacert="/etc/kubernetes/pki/etcd/ca.crt" --endpoints=https://127.0.0.1:2379 get --prefix ""

    # backup & restore
    etcdctl --cert="/etc/kubernetes/pki/apiserver-etcd-client.crt" --key="/etc/kubernetes/pki/apiserver-etcd-client.key" --cacert="/etc/kubernetes/pki/etcd/ca.crt" --endpoints=https://127.0.0.1:2379 snapshot restore a.txt 
    # etcdctl --cert="/etc/kubernetes/pki/apiserver-etcd-client.crt" --key="/etc/kubernetes/pki/apiserver-etcd-client.key" --cacert="/etc/kubernetes/pki/etcd/ca.crt" --endpoints=https://127.0.0.1:2379 snapshot save a.txt
    ```

### 3.9 什么是静态 Pod？

- [Static Pod](https://kubernetes.io/docs/tasks/configure-pod-container/static-pod/)
- /etc/kubernetes/manifests

    ```console
    root@CKA003:~# ps -ef | grep kubelet
    root     10572     1  2 09:37 ?        00:07:41 /usr/bin/kubelet --bootstrap-kubeconfig=/etc/kubernetes/bootstrap-kubelet.conf --kubeconfig=/etc/kubernetes/kubelet.conf --config=/var/lib/kubelet/config.yaml --cgroup-driver=cgroupfs --network-plugin=cni --pod-infra-container-image=k8s.gcr.io/pause:3.2 --resolv-conf=/run/systemd/resolve/resolv.conf

    root@CKA003:~# grep mani /var/lib/kubelet/config.yaml
    staticPodPath: /etc/kubernetes/manifests

    root@CKA003:~# cd /etc/kubernetes/manifests
    root@CKA003:/etc/kubernetes/manifests# ls
    etcd.yaml  kube-apiserver.yaml  kube-controller-manager.yaml  kube-scheduler.yaml  static-web.yaml

    root@CKA003:/etc/kubernetes/manifests# cat static-web.yaml
    apiVersion: v1
    kind: Pod
    metadata:
    name: static-web
    labels:
        role: myrole
    spec:
    containers:
        - name: web
          image: nginx
          ports:
            - name: web
            containerPort: 80
            protocol: TCP

    root@CKA003:/etc/kubernetes/manifests# kubectl get pods
    NAME                READY   STATUS    RESTARTS   AGE
    dnsutils            1/1     Running   4          4h17m
    static-web          1/1     Running   0          98m
    static-web-cka003   1/1     Running   0          98m
    web-0               0/1     Pending   0          116m

    root@CKA003:/etc/kubernetes/manifests# kubectl delete pod static-web
    pod "static-web" deleted
    root@CKA003:/etc/kubernetes/manifests# kubectl get pods
    NAME                READY   STATUS    RESTARTS   AGE
    dnsutils            1/1     Running   4          4h17m
    static-web-cka003   1/1     Running   0          99m
    web-0               0/1     Pending   0          117m

    root@CKA003:/etc/kubernetes/manifests# kubectl delete pod static-web-cka003
    pod "static-web-cka003" deleted
    root@CKA003:/etc/kubernetes/manifests# kubectl get pods
    NAME                READY   STATUS    RESTARTS   AGE
    dnsutils            1/1     Running   4          4h18m
    static-web-cka003   1/1     Running   0          10s
    web-0               0/1     Pending   0          117m

    root@CKA003:/etc/kubernetes/manifests# ls
    etcd.yaml  kube-apiserver.yaml  kube-controller-manager.yaml  kube-scheduler.yaml  static-web.yaml
    root@CKA003:/etc/kubernetes/manifests# rm -rf static-web.yaml
    root@CKA003:/etc/kubernetes/manifests# kubectl get pods
    NAME       READY   STATUS    RESTARTS   AGE
    dnsutils   1/1     Running   4          4h18m
    web-0      0/1     Pending   0          117m
    ```

## Lesson 04：K8S Auth & Security

### 4.1 什么是 K8S 的 3A？

- Authentication / Authorization / Admission
- K8S 的认证过程？Authentication、Authorization（ RBRA / ABAC / WebHook ）、Admission Controller

### 4.2 怎么配置 kubectl？

###	4.3 K8S 怎么保证网络安全？

- Kubernetes 的网络选型？flannel、calico、ovs、ovn

### 4.4 什么是用户和角色？

### 4.5 实验：添加用户 & 绑定角色

- 实验：创建 Normal 用户使用 kubectl 工具

    ```console
    root@CKA003:~# kubectl config get-contexts
    CURRENT   NAME                          CLUSTER      AUTHINFO           NAMESPACE
    *         kubernetes-admin@kubernetes   kubernetes   kubernetes-admin

    root@CKA003:~# kubectl create namespace ns1
    namespace/ns1 created
    root@CKA003:~# kubectl create namespace ns2
    namespace/ns2 created

    root@CKA003:~# useradd -m -d /home/poweruser -s /bin/bash poweruser
    root@CKA003:~# passwd poweruser
    Enter new UNIX password:
    Retype new UNIX password:
    passwd: password updated successfully
    root@CKA003:~# cd /home/poweruser

    root@CKA003:/home/poweruser# openssl genrsa -out poweruser.key 2048
    Generating RSA private key, 2048 bit long modulus (2 primes)
    ......................+++++
    ..........................................................+++++
    e is 65537 (0x010001)

    root@CKA003:/home/poweruser# openssl req -new -key poweruser.key -out poweruser.csr -subj "/CN=poweruser/O=ns1"
    Can't load /root/.rnd into RNG
    139904427348416:error:2406F079:random number generator:RAND_load_file:Cannot open file:../crypto/rand/randfile.c:88:Filename=/root/.rnd

    root@CKA003:/home/poweruser# cat poweruser.key
    -----BEGIN RSA PRIVATE KEY-----
    MIIEowIBAAKCAQEAt07RnBpZFkux9vEmSUDiHsVFtAu1FmJQjia0ls2A/fbMBt2T
    ...
    njzqykeT5cLiixwUf6x35nF2r5VydsZMHypk6dgPgC6LikTbfsL0
    -----END RSA PRIVATE KEY-----

    root@CKA003:/home/poweruser# cat poweruser.csr
    -----BEGIN CERTIFICATE REQUEST-----
    MIICZzCCAU8CAQAwIjESMBAGA1UEAwwJcG93ZXJ1c2VyMQwwCgYDVQQKDANuczEw
    ...
    O5+ia4aC6Hn/lMsRNYzeSK/ovjMuzH7gjnYEogG8QdpIVLFF1a1D2/S1kQ==
    -----END CERTIFICATE REQUEST-----

    root@CKA003:/home/poweruser# openssl x509 -req -in poweruser.csr -CA /etc/kubernetes/pki/ca.crt -CAkey /etc/kubernetes/pki/ca.key -CAcreateserial -out poweruser.crt -days 60
    Signature ok
    subject=CN = poweruser, O = ns1
    Getting CA Private Key

    root@CKA003:/home/poweruser# chmod 777 poweruser.*
    root@CKA003:/home/poweruser# cd

    root@CKA003:~# kubectl config set-credentials poweruser --client-certificate=/home/poweruser/poweruser.crt --client-key=/home/poweruser/poweruser.key
    User "poweruser" set.
    root@CKA003:~# mkdir /home/poweruser/.kube
    root@CKA003:~# cp .kube/config /home/poweruser/.kube
    root@CKA003:~# chown -R poweruser:poweruser /home/poweruser/.kube
    root@CKA003:~# su poweruser

    poweruser@CKA003:/root$ cd
    poweruser@CKA003:~$ cd .kube/
    poweruser@CKA003:~/.kube$ vi config

    root@CKA003:~# diff /root/.kube/config /home/poweruser/.kube/config
    10,12c10,12
    <     user: kubernetes-admin
    <   name: kubernetes-admin@kubernetes
    < current-context: kubernetes-admin@kubernetes
    ---
    >     user: poweruser
    >   name: poweruser@kubernetes
    > current-context: poweruser@kubernetes

    poweruser@CKA003:~/.kube$ kubectl get pods
    Error from server (Forbidden): pods is forbidden: User "poweruser" cannot list resource "pods" in API group "" in the namespace "default"
    ```

    为 poweruser 用户绑定权限

    ```console
    root@CKA003:~# vi pod-read.yaml
    root@CKA003:~# cat pod-read.yaml
    apiVersion: rbac.authorization.k8s.io/v1
    kind: Role
    metadata:
      namespace: default
      name: pod-reader
    rules:
    - apiGroups: [""] # "" indicates the core API group
      resources: ["pods"]
      verbs: ["get", "watch", "list"]

    root@CKA003:~# kubectl apply -f pod-read.yaml
    role.rbac.authorization.k8s.io/pod-reader created

    root@CKA003:~# vi role-binding.yaml
    root@CKA003:~# cat role-binding.yaml
    apiVersion: rbac.authorization.k8s.io/v1
    # This role binding allows "jane" to read pods in the "default" namespace.
    # You need to already have a Role named "pod-reader" in that namespace.
    kind: RoleBinding
    metadata:
      name: read-pods
      namespace: default
    subjects:
    # You can specify more than one "subject"
    - kind: User
      name: poweruser # "name" is case sensitive
      apiGroup: rbac.authorization.k8s.io
    roleRef:
    # "roleRef" specifies the binding to a Role / ClusterRole
      kind: Role #this must be Role or ClusterRole
      name: pod-reader # this must match the name of the Role or ClusterRole you wish to bind to
      apiGroup: rbac.authorization.k8s.io

    root@CKA003:~# kubectl apply -f role-binding.yaml
    rolebinding.rbac.authorization.k8s.io/read-pods created
    ```

    现在 poweruser 用户有 list pod 的权限了

    ```console
    poweruser@CKA003:~/.kube$ kubectl get pods
    NAME       READY   STATUS    RESTARTS   AGE
    dnsutils   1/1     Running   4          4h22m
    web-0      0/1     Pending   0          122m
    poweruser@CKA003:~/.kube$
    ```

- 实验：创建 Normal 用户并给予超级管理员组

    ```console
    root@CKA003:~# openssl genrsa -out superuser.key 2048
    Generating RSA private key, 2048 bit long modulus (2 primes)
    ..........................+++++
    ........................................................................................+++++
    e is 65537 (0x010001)

    root@CKA003:~# openssl req -new -key superuser.key -out superuser.csr -subj "/CN=superuser /O=system:masters"
    Can't load /root/.rnd into RNG
    139767359660480:error:2406F079:random number generator:RAND_load_file:Cannot open file:../crypto/rand/randfile.c:88:Filename=/root/.rnd

    root@CKA003:~# openssl x509 -req -in superuser.csr -CA /etc/kubernetes/pki/ca.crt -CAkey /etc/kubernetes/pki/ca.key -CAcreateserial -out superuser.crt -days 60
    Signature ok
    subject=CN = "superuser ", O = system:masters
    Getting CA Private Key
    ```

    system:masters 是默认的 [cluster-rolebinding group](https://kubernetes.io/docs/reference/access-authn-authz/rbac/#user-facing-roles)，参考：[How to view members of subject with Group kind](https://stackoverflow.com/questions/51612976/how-to-view-members-of-subject-with-group-kind)

    ```console
    root@CKA003:~# kubectl get clusterrolebindings -o go-template='{{range .items}}{{range .subjects}}{{.kind}}-{{.name}} {{end}} {{" - "}} {{.metadata.name}} {{"\n"}}{{end}}' | grep "^Group-system:masters"
    Group-system:masters   -  cluster-admin
    ```

    设置 kubectl config

    ```console
    root@CKA003:~# kubectl config set-credentials superuser --client-certificate=superuser.crt --client-key=superuser.key
    User "superuser" set.
    root@CKA003:~# tail -f .kube/config
    ...
    - name: poweruser
    user:
        client-certificate: /home/poweruser/poweruser.crt
        client-key: /home/poweruser/poweruser.key
    - name: superuser
    user:
        client-certificate: /root/superuser.crt
        client-key: /root/superuser.key

    root@CKA003:~# kubectl config set-context superuser-context --cluster=kubernetes --user=superuser
    Context "superuser-context" created.

    root@CKA003:~# kubectl config get-contexts
    CURRENT   NAME                          CLUSTER      AUTHINFO           NAMESPACE
    *         kubernetes-admin@kubernetes   kubernetes   kubernetes-admin
            superuser-context             kubernetes   superuser

    root@CKA003:~# kubectl config use-context superuser-context
    Switched to context "superuser-context".

    root@CKA003:~# kubectl config get-contexts
    CURRENT   NAME                          CLUSTER      AUTHINFO           NAMESPACE
            kubernetes-admin@kubernetes   kubernetes   kubernetes-admin
    *         superuser-context             kubernetes   superuser

    root@CKA003:~# kubectl get pods
    NAME       READY   STATUS    RESTARTS   AGE
    dnsutils   1/1     Running   4          4h49m
    web-0      0/1     Pending   0          149m
    ```

- 实验：创建 Service Account 并绑定角色

    ```console
    root@CKA003:~# kubectl create serviceaccount sa-cluster-admin --namespace=kube-system
    serviceaccount/sa-cluster-admin created

    root@CKA003:~# kubectl get secret --all-namespaces | grep sa-cluster-admin
    kube-system             sa-cluster-admin-token-k9xfp                     kubernetes.io/service-account-token   3      53s

    root@CKA003:~# kubectl describe secret -n kube-system sa-cluster-admin-token-k9xfp
    Name:         sa-cluster-admin-token-k9xfp
    Namespace:    kube-system
    Labels:       <none>
    Annotations:  kubernetes.io/service-account.name: sa-cluster-admin
                kubernetes.io/service-account.uid: 11deb8dd-5625-4d75-ad44-3beef1bcd995
    Type:  kubernetes.io/service-account-token
    Data
    ====
    ca.crt:     1025 bytes
    namespace:  11 bytes
    token:      eyJhbGciOiJSUzI1NiIsImtpZCI6InRBUkJ6bkxQMHNHSi1MejR4T2ZtYk43b1Y0S2M3MXZOMTMtQmtOaHpsbXMifQ.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlLXN5c3RlbSIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJzYS1jbHVzdGVyLWFkbWluLXRva2VuLWs5eGZwIiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQubmFtZSI6InNhLWNsdXN0ZXItYWRtaW4iLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlcnZpY2UtYWNjb3VudC51aWQiOiIxMWRlYjhkZC01NjI1LTRkNzUtYWQ0NC0zYmVlZjFiY2Q5OTUiLCJzdWIiOiJzeXN0ZW06c2VydmljZWFjY291bnQ6a3ViZS1zeXN0ZW06c2EtY2x1c3Rlci1hZG1pbiJ9.Dr1aOVdwAXO_BPXlJAohKBjoxRhMmTWyfVy2AP3-D0V-2jzdzWKoEP_17wnAS3FP-hxuOtTr3XWN0zM4oAI8-CeXtP7AdB0sqZ9P7Wnp2s88DqDUNK0JUuYGke3js9xd44Bt5vhtRovNEMYEnLXj_NLOunW33f4g46ep4NvQpNGTd48BcgzFhiiWuXLKKGGoOZGrWlkXqyofE4li83B3D08oW-hjP4S0JBBXqmzpa0_PYi-hkPbirmn9J7F-oQd0So05uAzZROHSd7n8INlYwbJx2zRF8PKipscxu47ddEumr6R9b8qDDVolP5iawqFPeDTt9lOY7OdgEaVcL651UQ

    root@CKA003:~# vi sa-cluster-admin-rolebinding.yaml

    root@CKA003:~# cat sa-cluster-admin-rolebinding.yaml
    apiVersion: rbac.authorization.k8s.io/v1
    # This cluster role binding allows anyone in the "manager" group to read secrets in any namespace.
    kind: ClusterRoleBinding
    metadata:
      name: read-secrets-global
    subjects:
    - kind: User
      name: sa-cluster-admin
      apiGroup: rbac.authorization.k8s.io
    roleRef:
      kind: ClusterRole
      name: cluster-admin
      apiGroup: rbac.authorization.k8s.io

    root@CKA003:~# kubectl create -f sa-cluster-admin-rolebinding.yaml
    clusterrolebinding.rbac.authorization.k8s.io/read-secrets-global created

    root@CKA003:~# kubectl apply -f nginx-deployment.yaml --token=eyJhbGciOiJSUzI1NiIsImtpZCI6InRBUkJ6bkxQMHNHSi1MejR4T2ZtYk43b1Y0S2M3MXZOMTMtQmtOaHpsbXMifQ.eyJpc3MiOiJrdWJlcm5ldGVzL3NlcnZpY2VhY2NvdW50Iiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9uYW1lc3BhY2UiOiJrdWJlLXN5c3RlbSIsImt1YmVybmV0ZXMuaW8vc2VydmljZWFjY291bnQvc2VjcmV0Lm5hbWUiOiJzYS1jbHVzdGVyLWFkbWluLXRva2VuLWs5eGZwIiwia3ViZXJuZXRlcy5pby9zZXJ2aWNlYWNjb3VudC9zZXJ2aWNlLWFjY291bnQubmFtZSI6InNhLWNsdXN0ZXItYWRtaW4iLCJrdWJlcm5ldGVzLmlvL3NlcnZpY2VhY2NvdW50L3NlcnZpY2UtYWNjb3VudC51aWQiOiIxMWRlYjhkZC01NjI1LTRkNzUtYWQ0NC0zYmVlZjFiY2Q5OTUiLCJzdWIiOiJzeXN0ZW06c2VydmljZWFjY291bnQ6a3ViZS1zeXN0ZW06c2EtY2x1c3Rlci1hZG1pbiJ9.Dr1aOVdwAXO_BPXlJAohKBjoxRhMmTWyfVy2AP3-D0V-2jzdzWKoEP_17wnAS3FP-hxuOtTr3XWN0zM4oAI8-CeXtP7AdB0sqZ9P7Wnp2s88DqDUNK0JUuYGke3js9xd44Bt5vhtRovNEMYEnLXj_NLOunW33f4g46ep4NvQpNGTd48BcgzFhiiWuXLKKGGoOZGrWlkXqyofE4li83B3D08oW-hjP4S0JBBXqmzpa0_PYi-hkPbirmn9J7F-oQd0So05uAzZROHSd7n8INlYwbJx2zRF8PKipscxu47ddEumr6R9b8qDDVolP5iawqFPeDTt9lOY7OdgEaVcL651UQ
    deployment.apps/nginx-deployment created
    ```

## Lesson 05: K8S Schedule

### 5.1 怎么部署多节点的 k8s 集群？ 

- 参考资料
    - [怎么部署一个 Multi-Node 的 K8S 环境？](deploy-k8s-manual.md)
    - [怎么部署一个 Dual Stack HA 的 K8S 环境？](basic.md)
    - [基于 AWS 部署高可用 Kubernetes 集群](deploy-aws-ha-k8s-cluster.md)
    - [openshift-container-platform-reference-architecture-implementation-guides](https://blog.openshift.com/openshift-container-platform-reference-architecture-implementation-guides/)

        ![](../images/openshift-ha-deployment.png)

        ![](../images/openshift-network-arch-azure.png)

    - 网络多平面

        ![](../images/k8s-deploy-ha-multus.png)

- 步骤

    1. 在 master 节点上取得 token 和 ca_hash

        ```console
        root@ckamaster003:~# kubeadm token create
        b6k3qj.avofghaucefqe0a8

        root@ckamaster003:~# kubeadm token list | grep -v TOKEN | awk '{print $1}' | head -n -1
        b6k3qj.avofghaucefqe0a8

        root@ckamaster003:~# openssl x509 -pubkey -in /etc/kubernetes/pki/ca.crt | openssl rsa -pubin -outform der 2>/dev/null | openssl dgst -sha256 -hex | sed 's/^.* //'
        d7d0906ebe29f607587e404ef6c393169a51e5f6c81e22a2a48f30ef8702e12a

        root@ckamaster003:~# ifconfig | grep eth0 -A 1
        eth0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
                inet 172.31.43.105  netmask 255.255.240.0  broadcast 172.31.47.255
        ```

    2. 在新节点上允许 kubeadm 命令，将新节点加入 k8s cluster

        ```bash
        kubeadm token create
        master_ip=$(ifconfig | grep eth0 -A 1 | grep inet | awk '{print $2}')
        token=$(kubeadm token list | grep -v TOKEN | awk '{print $1}' | head -n 1)
        ca_hash=$(openssl x509 -pubkey -in /etc/kubernetes/pki/ca.crt | openssl rsa -pubin -outform der 2>/dev/null | openssl dgst -sha256 -hex | sed 's/^.* //')

        echo kubeadm join $master_ip:6443 --token $token --discovery-token-ca-cert-hash sha256:$ca_hash
        kubeadm join $master_ip:6443 --token $token --discovery-token-ca-cert-hash sha256:$ca_hash
        ```

    3. 在新节点上配置 kubectl

        ```bash
        mkdir -p $HOME/.kube
        scp root@$master_ip:/etc/kubernetes/admin.conf $HOME/.kube/config
        chown $(id -u):$(id -g) $HOME/.kube/config
        ```

    4. 然后在新节点上用 kubectl 命令可以看到 node 已经 ready

        ```console
        root@ckaslave003:~# kubectl get nodes
        NAME           STATUS   ROLES    AGE   VERSION
        ckamaster003   Ready    master   20m   v1.18.3
        ckaslave003    Ready    <none>   33s   v1.18.3
        ```

### 5.2 怎么把应用部署到指定的 Node？

- 参考：[Labels and Selectors](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/)

    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: label-demo
      labels:
        environment: production
        app: nginx
    spec:
      containers:
      - name: nginx
        image: nginx:1.14.2
        ports:
        - containerPort: 80
    ```

    ```bash
    # 创建一个带 label 的 pod 对象 label-pod.yaml，内容如上

    kubectl apply -f label-pod.yaml
    ```

    ```console
    root@ckatest:~# kubectl get pods -l environment=production
    NAME         READY   STATUS    RESTARTS   AGE
    label-demo   1/1     Running   0          4m16s
    root@ckatest:~# kubectl get pods -l environment=production,tier=frontend
    No resources found in default namespace.

    root@ckatest:~# kubectl get pods -l 'environment in (production),tier in (frontend)'
    No resources found in default namespace.
    root@ckatest:~# kubectl get pods -l 'environment in (production, qa)'
    NAME         READY   STATUS    RESTARTS   AGE
    label-demo   1/1     Running   0          4m42s
    root@ckatest:~# kubectl get pods -l 'environment,environment notin (frontend)'
    NAME         READY   STATUS    RESTARTS   AGE
    label-demo   1/1     Running   0          4m50s
    ```

- 参考：[Assigning Pods to Nodes](https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes/)

### 5.3 什么是 Taints & Toleration？

- 参考: [Taints and Tolerations](https://kubernetes.io/docs/concepts/scheduling-eviction/taint-and-toleration/)
- 实验

    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: nginx5
    spec:
      containers:
      - name: nginx
        image: nginx
        imagePullPolicy: IfNotPresent
      nodeSelector:
        node-role.kubernetes.io/master: ""
      tolerations:
      - key: "key"
        operator: "Equal"
        value: "value"
        effect: "NoSchedule"
    ```

- 如果不用 node selector，而是直接用 nodeName，可以无视 NoSchedule Taint，可以被调度。但调度上去之后，会被 NoExcute Taint 驱逐。

    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: nginx
    spec:
      nodeName: ckamaster003
      containers:
      - name: nginx
        image: nginx
        imagePullPolicy: IfNotPresent
    ```

### 5.4 什么是 Node Affinity？

- 参考：[Assign Pods to Nodes using Node Affinity](https://kubernetes.io/docs/tasks/configure-pod-container/assign-pods-nodes-using-node-affinity/)

### 5.5 什么是 Pod Affinity？

- [Inter-pod affinity and anti-affinity](https://kubernetes.io/docs/concepts/scheduling-eviction/assign-pod-node/#inter-pod-affinity-and-anti-affinity)

### 5.6 实验：Pod 调度

## Lesson 06: K8S Storage

### 6.1 什么是 ConfigMap & Secret？

- [ConfigMap](https://kubernetes.io/docs/concepts/configuration/configmap/)
    - 参考：[Configure a Pod to Use a ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)
    - 参考：[Configuring Redis using a ConfigMap](https://kubernetes.io/docs/tutorials/configuration/configure-redis-using-configmap/)

    ```yaml
    apiVersion: v1
    kind: ConfigMap
    metadata:
      name: example
    data:
      example.property.1: hello
      example.property.2: world
      example.property.file: |-
        property.1=value-1
        property.2=value-2
        property.3=value-3
    ```

    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: configmap-demo-pod
    spec:
      containers:
        - name: nginx
          image: nginx
          env:
            - name: TEST1
              valueFrom:
                configMapKeyRef:
                  name: example
                  key: example.property.2
          volumeMounts:
          - name: config
            mountPath: "/config"
            readOnly: true
      volumes:
        - name: config
          configMap:
            name: example
    ```

    ```console
    root@ckamaster003:~# kubectl exec -it configmap-demo-pod /bin/sh

    # env | grep TEST
    TEST1=world

    # ls /config
    example.property.1  example.property.2	example.property.file
    ```

- [Secret](https://kubernetes.io/docs/concepts/configuration/secret/)

### 6.2 什么是 PV / PVC？

- [Types of Volumes](https://kubernetes.io/docs/concepts/storage/volumes/#types-of-volumes)
- [Persistent Volumes](https://kubernetes.io/docs/concepts/storage/persistent-volumes/)
- [Configure a Pod to Use a Volume for Storage](https://kubernetes.io/docs/tasks/configure-pod-container/configure-volume-storage/)
- [Configure a Pod to Use a PersistentVolume for Storage](https://kubernetes.io/docs/tasks/configure-pod-container/configure-persistent-volume-storage/)，注意 hostpath 对应到 node 上的路径，要看好 pod 跑在哪个 node 上，最好事先 taint slave node，或者 node select 指定 pod 跑在 master 上，这样就没问题了。

### 6.3 什么是 Storage Class？

- [Storage Classes](https://kubernetes.io/docs/concepts/storage/storage-classes/)
- [Dynamic Volume Provisioning](https://kubernetes.io/docs/concepts/storage/dynamic-provisioning/)

### 6.4 实验：ConfigMap / Secret / PV & PVC / StorageClass

## Lesson 07: Service

### 7.1 Service 在底层是怎么实现的？

- [Service](https://kubernetes.io/docs/concepts/services-networking/service/)
- [Connecting Applications with Services](https://kubernetes.io/docs/concepts/services-networking/connect-applications-service/)
- [A Guide to the Kubernetes Networking Model](https://sookocheff.com/post/kubernetes/understanding-kubernetes-networking-model/)

### 7.2 实验：发布服务

- Cluster IP
- Service FQDN
- Nodeport
- LB Type Service

```bash
# Taint slave 节点，因为在有些环境中没有放开隧道防火墙，我们强制让 pod 都跑在 master 上
kubectl taint node ckaslave001 key=value:NoExecute

# 创建 Deployment
kubectl apply -f https://raw.githubusercontent.com/kubernetes/website/master/content/en/examples/service/networking/run-my-nginx.yaml

# 创建 Service
kubectl apply -f https://raw.githubusercontent.com/kubernetes/website/master/content/en/examples/service/networking/nginx-svc.yamlservice/my-nginx unchanged
```

```console
root@ckamaster001:~# kubectl get svc --all-namespaces -o wide
NAMESPACE     NAME         TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)                  AGE   SELECTOR
default       kubernetes   ClusterIP   10.96.0.1      <none>        443/TCP                  8h    <none>
default       my-nginx     ClusterIP   10.98.172.84   <none>        80/TCP                   36m   run=my-nginx
kube-system   kube-dns     ClusterIP   10.96.0.10     <none>        53/UDP,53/TCP,9153/TCP   8h    k8s-app=kube-dns

root@ckamaster001:~# dig @10.96.0.10 my-nginx.default.svc.cluster.local

; <<>> DiG 9.11.3-1ubuntu1.12-Ubuntu <<>> @10.96.0.10 my-nginx.default.svc.cluster.local
; (1 server found)
;; global options: +cmd
;; Got answer:
;; WARNING: .local is reserved for Multicast DNS
;; You are currently testing what happens when an mDNS query is leaked to DNS
;; ->>HEADER<<- opcode: QUERY, status: NOERROR, id: 23475
;; flags: qr aa rd; QUERY: 1, ANSWER: 1, AUTHORITY: 0, ADDITIONAL: 1
;; WARNING: recursion requested but not available

;; OPT PSEUDOSECTION:
; EDNS: version: 0, flags:; udp: 4096
; COOKIE: 2661e0af4b0ce87e (echoed)
;; QUESTION SECTION:
;my-nginx.default.svc.cluster.local. IN	A

;; ANSWER SECTION:
my-nginx.default.svc.cluster.local. 30 IN A	10.98.172.84

;; Query time: 0 msec
;; SERVER: 10.96.0.10#53(10.96.0.10)
;; WHEN: Sat Jun 13 16:15:23 CST 2020
;; MSG SIZE  rcvd: 125
```

### 7.3 什么是 Ingress？

- [Ingress Controller](https://kubernetes.io/docs/concepts/services-networking/ingress-controllers/)
- [Ingress](https://kubernetes.io/docs/concepts/services-networking/ingress/)

## Lesson 08：Advance

### 8.1 监控、日志、排错

- 监控：Grafana / Prometheus / AlertManager
- 日志：ElasticSearch / Fluent ( Logstash ) / Kibana
- 排错：
    - 怎么对 pod 的网口抓包？

        ```bash
        # 查看指定 pod 运行在那个 node 上
        kubectl describe pod <pod> -n <namespace>

        # 获得容器的 pid
        docker inspect -f {{.State.Pid}} <container>

        # 进入该容器的 network namespace
        nsenter --target <PID> -n

        # 使用 tcpdump 抓包，指定 eth0 网卡
        tcpdump -i eth0 tcp and port 80 -vvv

        # 或者抓包并导出到文件
        tcpdump -i eth0 -w ./out.cap
        ```

    - Debug tools

        ```bash
        apiVersion: v1
        kind: Pod
        metadata:
          name: demo-pod
          labels:
            app: demo-pod
        spec:
          containers:
            - name: nginx
              image: nginx
              ports:
                - containerPort: 80
              env:
                - name: DEMO_GREETING
                  value: "Hello from the environment"
                - name: DEMO_FAREWELL
                  value: "Such a sweet sorrow"
            - name: busybox
              image: busybox
              args:
                - sleep
                - "1000000"
        ```

        ```console
        root@ckatest001:~# kubectl exec -it demo-pod -c busybox -- /bin/sh
        / # ping 192.168.209.193
        PING 192.168.209.193 (192.168.209.193): 56 data bytes
        64 bytes from 192.168.209.193: seq=0 ttl=63 time=0.099 ms
        64 bytes from 192.168.209.193: seq=1 ttl=63 time=0.093 ms
        64 bytes from 192.168.209.193: seq=2 ttl=63 time=0.089 ms
        ```

        ```console
        root@ckalab001:~# tcpdump -i eth0 udp
        12:34:10.972395 IP 45.77.183.254.vultr.com.42125 > 45.32.33.135.vultr.com.4789: VXLAN, flags [I] (0x08), vni 4096
        IP 192.168.208.4 > 192.168.209.193: ICMP echo request, id 3072, seq 0, length 64
        12:34:10.972753 IP 45.32.33.135.vultr.com.41062 > 45.77.183.254.vultr.com.4789: VXLAN, flags [I] (0x08), vni 4096
        IP 192.168.209.193 > 192.168.208.4: ICMP echo reply, id 3072, seq 0, length 64
        12:34:11.972537 IP 45.77.183.254.vultr.com.42125 > 45.32.33.135.vultr.com.4789: VXLAN, flags [I] (0x08), vni 4096
        IP 192.168.208.4 > 192.168.209.193: ICMP echo request, id 3072, seq 1, length 64
        ```

        在阿里云上比较特别，阿里云把 calico / flannel 的 vxlan 魔改成路由协议了，因此需要在 VPC 上加路由才行，每个节点一条路由协议。该节点的 pod 网段都发给该节点的 node ip。[这篇 KB](https://yq.aliyun.com/articles/704175) 非常含糊其辞，翻译一下就是不支持 vxlan，魔改 vxlan，底层用路由协议实现，所以需要在 VPC 上加路由。

        正常的 vxlan，
        ```console
        root@ckalab001:~# ip r
        default via 45.77.182.1 dev ens3 proto dhcp src 45.77.183.254 metric 100 
        192.168.208.1 dev cali65a032ad3e5 scope link 
        192.168.209.192/26 via 192.168.209.192 dev vxlan.calico onlink 

        root@ckalab001:~# ip a
        2: ens3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
            link/ether 56:00:02:d8:35:5a brd ff:ff:ff:ff:ff:ff
            inet 45.77.183.254/23 brd 45.77.183.255 scope global dynamic ens3
              valid_lft 73639sec preferred_lft 73639sec
            inet6 fe80::5400:2ff:fed8:355a/64 scope link 
              valid_lft forever preferred_lft forever
        4: cali65a032ad3e5@if3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1410 qdisc noqueue state UP group default 
            link/ether ee:ee:ee:ee:ee:ee brd ff:ff:ff:ff:ff:ff link-netnsid 0
            inet6 fe80::ecee:eeff:feee:eeee/64 scope link 
              valid_lft forever preferred_lft forever
        9: vxlan.calico: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1410 qdisc noqueue state UNKNOWN group default 
            link/ether 66:f1:80:3e:ea:c6 brd ff:ff:ff:ff:ff:ff
            inet 192.168.208.0/32 brd 192.168.208.0 scope global vxlan.calico
              valid_lft forever preferred_lft forever
            inet6 fe80::64f1:80ff:fe3e:eac6/64 scope link 
              valid_lft forever preferred_lft forever
        ```

        阿里云魔改的 vxlan：`192.168.209.192/26 via 172.31.43.146 dev eth0 proto 80 onlink`，80 是 IGRP 网关间路由协议。所以跨 node 的 pod 间发 ping 包时，tcpdump 抓 tcp 包抓不到，抓 icmp 包可以抓到。

        ```console
        root@ckalab001:~# ip r
        default via 172.31.47.253 dev eth0 proto dhcp src 172.31.43.145 metric 100
        192.168.208.1 dev cali77bffbebec8 scope link 
        192.168.209.192/26 via 172.31.43.146 dev eth0 proto 80 onlink

        root@ckalab001:~# ip a
        2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc mq state UP group default qlen 1000
            link/ether 00:16:3e:08:2e:5f brd ff:ff:ff:ff:ff:ff
            inet 172.31.43.145/20 brd 172.31.47.255 scope global dynamic eth0
              valid_lft 315356000sec preferred_lft 315356000sec
            inet6 fe80::216:3eff:fe08:2e5f/64 scope link 
              valid_lft forever preferred_lft forever
        4: cali77bffbebec8@if3: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1410 qdisc noqueue state UP group default 
            link/ether ee:ee:ee:ee:ee:ee brd ff:ff:ff:ff:ff:ff link-netnsid 0
            inet6 fe80::ecee:eeff:feee:eeee/64 scope link 
              valid_lft forever preferred_lft forever
        8: vxlan.calico: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1410 qdisc noqueue state UNKNOWN group default 
            link/ether 66:f1:80:3e:ea:c6 brd ff:ff:ff:ff:ff:ff
            inet 192.168.208.0/32 brd 192.168.208.0 scope global vxlan.calico
              valid_lft forever preferred_lft forever
            inet6 fe80::64f1:80ff:fe3e:eac6/64 scope link 
              valid_lft forever preferred_lft forever
        ```

### 8.2 什么是 HPA / CA / VA？

- 怎么理解 HPA / CA / VPA？

### 8.3 什么是 Federation？

- Kubenetes Federation vs ManageIQ

### 8.4 K8S 怎么处理有状态服务？

- [StatefulSet](https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/)
- [StatefulSet Examples](https://kubernetes.io/docs/tutorials/stateful-application/basic-stateful-set/)
- CRD & Operator

### 8.5 其它参考

- [K8S 测试](https://jimmysong.io/kubernetes-handbook/develop/testing.html)
- 搭建 OpenStack 测试环境
  - [vultr](https://www.vultr.com/) 开 Ubuntu 18.04 / 20.4 Bare Metal 服务器
  - [安装 DevStack](https://docs.openstack.org/devstack/latest/)
  - [下载云镜像](https://docs.openstack.org/image-guide/obtain-images.html)

      ```bash
      wget http://cloud.centos.org/centos/7/images/CentOS-7-x86_64-GenericCloud-2009.qcow2
      wget https://cloud-images.ubuntu.com/bionic/current/bionic-server-cloudimg-amd64.img
      wget https://cloud-images.ubuntu.com/focal/current/focal-server-cloudimg-amd64.img
      ```

  - [上传云镜像](https://docs.openstack.org/murano/pike/reference/appendix/articles/image_builders/upload.html)

      ```bash
      openstack image create --public --disk-format qcow2 --file focal-server-cloudimg-amd64.img ubuntu-20.04
      openstack image create --public --disk-format qcow2 --file bionic-server-cloudimg-amd64.img ubuntu-18.04
      openstack image create --public --disk-format qcow2 --file CentOS-7-x86_64-GenericCloud-2009.qcow2 centos-7.8
      ```

  - [启用 ipip](https://www.infoq.cn/article/mqluyhvsdw8xopdwp17v)
- [k3s 环境搭建](https://github.com/k3s-io/k3s#quick-start---install-script)
- [KubeEdge Demo](https://kubeedge.io/zh/blog/kubeedge-deployment-manual/)

##	Lesson 09：CKA

### 9.1 考试注意事项

### 9.2 模拟题讲解

### 9.3 实验：做模拟题
