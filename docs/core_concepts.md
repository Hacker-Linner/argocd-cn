# 核心概念

假设您熟悉核心的 Git，Docker，Kubernetes，持续交付和 GitOps 概念。

* **Application** 清单定义的一组 Kubernetes 资源。这是一个自定义资源定义（CRD）。
* **Application source type** 使用哪个**工具**来构建应用程序。
* **Target state** 应用程序的期望状态，由 Git 存储库中的文件表示。
* **Live state** 该应用程序的实时状态。部署了哪些Pod等。
* **Sync status** 实时状态是否与目标状态匹配。部署的应用程序应该与 Git 所说的一样吗？
* **Sync** 使应用程序移至其目标状态的过程。 例如：通过将更改应用于 Kubernetes 集群。
* **Sync operation status** 同步是否成功。
* **Refresh** 将 Git 中的最新代码与实时状态进行比较。找出有什么不同。
* **Health** 应用程序的运行状况是否正常运行？它可以满足请求吗？
* **Tool** 从文件目录创建清单的工具。例如：Kustomize 或 Ksonnet。请参阅 **Application Source Type**。
* **Configuration management tool** 参阅 **Tool**。
* **Configuration management plugin** 一个自定义工具。
