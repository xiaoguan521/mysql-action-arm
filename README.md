# MySQL 5.7.33 ARM64 RPM 构建项目

这个项目提供了一个 GitHub Actions 工作流，用于自动构建适用于 ARM64 架构的 MySQL 5.7.33 RPM 安装包。

## 功能特点

- 使用 GitHub Actions 自动构建
- 通过 QEMU 模拟在 ARM64 架构上编译
- 生成标准的 RPM 安装包
- 完整的构建配置选项

## 工作流程说明

工作流程包含以下步骤：

1. 环境准备：安装所需的编译工具和依赖库
2. 下载源码：获取 MySQL 5.7.33 官方源代码
3. 配置编译：设置适合 ARM64 的编译参数
4. 编译安装：编译源码并安装到临时目录
5. RPM 打包：创建 RPM 规范文件并生成 RPM 包

## 使用方法

1. 克隆此仓库到您的 GitHub 账户
2. GitHub Actions 将自动在推送和 PR 时触发构建
3. 构建完成后，可以在工作流的构件中下载生成的 RPM 包

## 自定义配置

如需修改编译配置，可编辑 `.github/workflows/build-mysql-arm64.yml` 文件中的 CMake 参数。

## 注意事项

- 编译过程可能需要较长时间，因为使用 QEMU 模拟 ARM64 架构
- 请确保您的 GitHub Actions 配额足够支持长时间运行的工作流

## 许可证

本项目遵循 MIT 许可证。 