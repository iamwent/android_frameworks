# android_frameworks

在 Android Studio 中阅读 frameworks 源码

# 使用说明

```shell
# 使用以下命令 clone 本仓库
git clone --recurse-submodules --shallow-submodules git@github.com:iamwent/android_frameworks.git
```

# 原理

1. 创建一个目录，我这里是 android_frameworks，下面的操作都在此目录下进行
2. clone frameworks 源码

```shell
git clone --depth 1 https://android.googlesource.com/platform/frameworks/base
```

3. 从网上[下载 `idegen.jar` 文件](https://github.com/iamwent/android_frameworks/blob/main/out/host/linux-x86/framework/idegen.jar)，放在 `out/host/linux-x86/framework` 目录下

```shell
# 生成目录
mkdir -p out/host/linux-x86/framework
```

4. 生成 `android.ipr` 文件

```shell
# 先下载 development 源码
git clone --depth 1 https://android.googlesource.com/platform/development
# 然后执行 idegen.sh
development/tools/idegen/idegen.sh
```
