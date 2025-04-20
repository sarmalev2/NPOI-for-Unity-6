[中文](./README.md) | [EN](./README.en.md)

<div align="center">
<h1>🍦 NPOI for Unity 6</h1>
</div>

**[`NPOI`](https://github.com/nissl-lab/npoi)** 是 Apache POI 项目的 .NET 版本，可用于便捷地读写 Office 2003/2007 文件格式。在 Unity 中使用 NPOI 时，需要将相关的 DLL 文件导入至 `Assets/Plugins/` 目录。早期版本 NPOI仅需导入 `NPOI.dll` `NPOI.OOXML.dll` `NPOI.OpenXml4Net.dll` `NPOI.OpenXmlFormats.dll`四个文件，较新版本的 NPOI 导入 Unity 后，会提示缺少多个依赖项，完整导入所有依赖会比较耗时。考虑到目前互联网上尚未提供开箱即用的完整 NPOI for Unity 资源，故分享一个已配置好依赖项的**NPOI for Unity**最新版 (截止到2025/04/19)，方便开发者快速集成 NPOI 至 Unity 项目中。


## 📌 主要文件版本及测试平台信息

- **NPOI** 2.7.3  
- **SharpZipLib** 1.4.2  
- **Unity** 6.0 LTS (.NET Standard 2.1)

> 其他 Unity 版本请自行测试兼容性。


## 💡 使用方法

- 下载以后将`NPOI`文件夹导入Unity项目`Assets/Plugins/`目录即可。
