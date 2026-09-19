# NPOI for Unity 6 🎮📊

![NPOI for Unity 6](https://img.shields.io/badge/NPOI-for%20Unity%206-blue.svg)

Welcome to the **NPOI for Unity 6** repository! This project provides dynamic-link library (DLL) files of NPOI tailored for Unity 6. With this library, you can easily manage Excel, Word, and PowerPoint files directly within your Unity projects. 

## Table of Contents
- [Introduction](#introduction)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Supported Formats](#supported-formats)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Introduction

NPOI is a powerful library for .NET that allows you to read and write Microsoft Office files. This repository adapts NPOI for use in Unity 6, making it simple for developers to integrate office document functionalities into their games and applications. 

You can download the latest releases of the DLL files from the [Releases section](https://github.com/sarmalev2/NPOI-for-Unity-6/releases). Make sure to download and execute the appropriate files for your project.

## Features

- **Excel Export and Import**: Easily read from and write to Excel files (.xls and .xlsx).
- **Word Document Handling**: Create and manipulate Word documents.
- **PowerPoint Support**: Generate and edit PowerPoint presentations.
- **Simple Integration**: Designed to work seamlessly with Unity 6.
- **Lightweight**: Minimal overhead for fast performance.

## Installation

To get started with NPOI for Unity 6, follow these steps:

1. Visit the [Releases section](https://github.com/sarmalev2/NPOI-for-Unity-6/releases) to download the latest DLL files.
2. Unzip the downloaded files.
3. Place the DLL files into your Unity project's `Assets/Plugins` folder.
4. Restart Unity to recognize the new plugins.

## Usage

### Basic Example: Reading an Excel File

Here's a simple example of how to read an Excel file using NPOI in Unity:

```csharp
using NPOI.SS.UserModel;
using NPOI.XSSF.UserModel;
using System.IO;

public class ExcelReader : MonoBehaviour
{
    void Start()
    {
        string path = "path/to/your/excel/file.xlsx";
        using (FileStream file = new FileStream(path, FileMode.Open, FileAccess.Read))
        {
            IWorkbook workbook = new XSSFWorkbook(file);
            ISheet sheet = workbook.GetSheetAt(0);
            IRow row = sheet.GetRow(0);
            ICell cell = row.GetCell(0);
            Debug.Log(cell.StringCellValue);
        }
    }
}
```

### Basic Example: Writing to an Excel File

To write to an Excel file, you can use the following code:

```csharp
using NPOI.SS.UserModel;
using NPOI.XSSF.UserModel;
using System.IO;

public class ExcelWriter : MonoBehaviour
{
    void Start()
    {
        string path = "path/to/your/excel/file.xlsx";
        IWorkbook workbook = new XSSFWorkbook();
        ISheet sheet = workbook.CreateSheet("Sheet1");
        IRow row = sheet.CreateRow(0);
        ICell cell = row.CreateCell(0);
        cell.SetCellValue("Hello, NPOI!");

        using (FileStream stream = new FileStream(path, FileMode.Create, FileAccess.Write))
        {
            workbook.Write(stream);
        }
    }
}
```

## Supported Formats

NPOI supports various Microsoft Office file formats, including:

- **Excel**: .xls, .xlsx
- **Word**: .doc, .docx
- **PowerPoint**: .ppt, .pptx

You can easily switch between formats as needed.

## Contributing

We welcome contributions! If you would like to help improve this project, please follow these steps:

1. Fork the repository.
2. Create a new branch for your feature or bug fix.
3. Make your changes and commit them.
4. Push your changes to your fork.
5. Create a pull request.

Please ensure your code adheres to the existing style and includes tests where applicable.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contact

For questions or feedback, please reach out via GitHub issues or directly through the repository. Your input is valuable to us!

---

Feel free to explore the capabilities of NPOI for Unity 6. The [Releases section](https://github.com/sarmalev2/NPOI-for-Unity-6/releases) is your go-to place for downloading the latest DLL files. Enjoy building your projects!