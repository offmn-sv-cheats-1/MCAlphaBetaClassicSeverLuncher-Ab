
# Minecraft Alpha/Beta/Classic 服务器启动器
## 项目概述
本启动器专为运行Minecraft上古版本（Alpha/Beta/Classic）服务器设计，提供快速部署、配置管理和环境搭建功能。遵循 **OFFMN开发哲学**：在功能实现优先的前提下，用户体验优化属于未来版本的可选项。
## 核心功能
| 功能                | 状态   | 说明 |
|---------------------|--------|------|
| **服务器核心下载**  | ✅ 稳定 | 通过wget从GitHub仓库获取36个历史版本服务器文件 |
| **内存分配管理**    | ✅ 稳定 | 支持自定义Xmx/Xms内存参数（单位MB） |
| **服务器配置编辑**  | ✅ 基础 | 提供server.properties的12项关键参数修改 |
| **Java环境安装**    | ⚠️ 测试 | Windows自动安装JDK8/Linux调用apt |
| **跨平台支持**      | ✅ 稳定 | 兼容Windows 10+/主流Linux发行版 |
| **内网穿透集成**    | ⌛ 规划 | 功能开发中（优先级：低） |
## 使用指南
### 基础操作
```bash
1. 运行主程序: python main.py
2. 选择版本类型: 
   1- Alpha 
   2- Beta 
   3- Classic 
   4- Release
3. 选择具体版本号 (1-15)
4. 设置内存分配 (示例: 最大1024M/最小512M)
5. 选择GUI模式 (Y/N)
```
### 高级功能
- **配置编辑器** (选项12):
  - 实时编辑server.properties
  - 支持13项参数自定义
- **Java安装** (选项7):
  - Windows: 自动安装JDK8
  - Linux: 调用apt安装openjdk-8-jre
## 兼容性说明
| 系统               | 状态     | 备注 |
|--------------------|----------|------|
| Windows 10/11      | ✅ 支持 | 推荐平台 |
| Linux (Ubuntu/Debian) | ✅ 支持 | 需手动配置Java |
| Windows 7          | ⚠️ 测试中 | 虚拟机适配进行中（或自己编译） |
| macOS              | ❌ 不支持 | 无开发计划 |
## 注意事项
### 内存分配建议
| 版本类型   | 推荐内存 | 最大支持 |
|------------|----------|----------|
| Classic    | 128-256M | 512M     |
| Alpha      | 256-512M | 1024M    |
| Beta       | 512-1024M| 2048M    |
### 常见问题处理
1. **杀毒软件误报**  
   因PyInstaller打包机制导致，可通过[VirusTotal检测](https://www.virustotal.com/)后添加白名单
2. **文件下载失败**  
   检查系统根证书有效性（更新教程见[此处](https://docs.microsoft.com/en-us/skype-sdk/sdn/articles/installing-the-trusted-root-certificate)）
3. **Java安装异常**  
   备用方案：手动安装[JDK 1.6](https://www.oracle.com/java/technologies/javase-java-archive-javase6-downloads.html)
