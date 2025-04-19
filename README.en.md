

<div align="center">
<h1>🍦 NPOI-For-Unity-6</h1>
</div>

**[`NPOI`](https://github.com/nissl-lab/npoi)** is the .NET version of Apache POI project, which enables convenient reading and writing of Office 2003/2007 file formats.  
To use NPOI in Unity, the required DLL files need to be placed under the `Assets/Plugins/` directory.  
Older versions of NPOI only require importing the following four files:  
`NPOI.dll`, `NPOI.OOXML.dll`, `NPOI.OpenXml4Net.dll`, and `NPOI.OpenXmlFormats.dll`.

However, newer versions of NPOI may prompt for many additional dependencies when imported into Unity. Importing all of them manually can be time-consuming.  
Since there are currently no ready-to-use full NPOI packages available online for Unity, this repository provides a pre-configured **NPOI for Unity** package (as of 2025/04/19), making it easier for developers to integrate NPOI into Unity projects.

## 📌 Version & Platform Info

- **NPOI** 2.7.3  
- **SharpZipLib** 1.4.2  
- **Unity** 6.0 LTS (.NET Standard 2.1)

> Please test compatibility if you are using a different version of Unity.

## 💡 How to Use

- After downloading, simply import the `NPOI` folder into your Unity project's `Assets/Plugins/` directory.
