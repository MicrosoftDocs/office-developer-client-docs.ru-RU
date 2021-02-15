---
title: Инициализация драйвера источника текстовых данных
TOCTitle: Initializing the Text Data Source driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 2e76cc7d6b5254f2347e2264b0588ee1df643d05
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291423"
---
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="bbbbd-102">Инициализация драйвера источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="bbbbd-102">Initializing the Text Data Source driver</span></span>

<span data-ttu-id="bbbbd-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bbbbd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bbbbd-104">Один и тот же драйвер базы данных используется как для текстовых источников данных, так и для источников данных HTML.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-104">The same database driver is used for both text data sources and for HTML data sources.</span></span>

<span data-ttu-id="bbbbd-105">При установке драйвера базы данных источника текстовых данных программа установки записывает набор значений по умолчанию в реестр Microsoft Windows в подмайсах "Подпрограммы" и "Форматы ISAM".</span><span class="sxs-lookup"><span data-stu-id="bbbbd-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="bbbbd-106">Не следует изменять эти параметры напрямую; используйте программу установки приложения для добавления, удаления или изменения этих параметров.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="bbbbd-107">В следующих разделах описаны параметры инициализации и формата ISAM для драйвера базы данных источника текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="bbbbd-108">Параметры инициализации источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="bbbbd-108">Text data source initialization settings</span></span>

<span data-ttu-id="bbbbd-109">Текстовая папка **\\ ISAM \\** для средства подключения к Access включает параметры инициализации драйвера Acetxt.dll, используемой для внешнего доступа к текстовым файлам данных.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="bbbbd-110">Типичные параметры для записей в этой папке показаны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<br/>

<span data-ttu-id="bbbbd-111">Ядер баз данных Microsoft Access использует записи текстовых папок следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbbbd-112">Запись</span><span class="sxs-lookup"><span data-stu-id="bbbbd-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="bbbbd-113">Описание</span><span class="sxs-lookup"><span data-stu-id="bbbbd-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-114">win32</span><span class="sxs-lookup"><span data-stu-id="bbbbd-114">win32</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-115">Расположение Acetxt.dll.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-115">The location of Acetxt.dll.</span></span> <span data-ttu-id="bbbbd-116">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-116">The full path is determined at the time of installation.</span></span> <span data-ttu-id="bbbbd-117">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-117">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="bbbbd-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-119">Количество строк, сканированных при угадать типы столбцов.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-119">The number of rows to be scanned when guessing the column types.</span></span> <span data-ttu-id="bbbbd-120">Если установлено 0, будет искаться весь файл.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-120">If set to 0, the entire file will be searched.</span></span> <span data-ttu-id="bbbbd-121">Значение по умолчанию — 25.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-121">The default is 25.</span></span> <span data-ttu-id="bbbbd-122">Значения имеют тип REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-122">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-123">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="bbbbd-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-124">Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-124">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="bbbbd-125">Значение 01 указывает, что во время импорта имена столбцов принимаются из первой строки.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-125">A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-126">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="bbbbd-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-127">Индикатор хранения текстовых страниц.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-127">An indicator of how text pages are stored.</span></span> <span data-ttu-id="bbbbd-128">Возможные параметры:</span><span class="sxs-lookup"><span data-stu-id="bbbbd-128">Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="bbbbd-129">ANSI — кодовая страница ANSI компьютера.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-129">ANSI — The ANSI code page of the machine.</span></span> <span data-ttu-id="bbbbd-130">Преобразования AnsiToUnicode и UnicodeToAnsi были сделаны.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-130">AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="bbbbd-131">OEM — кодовая страница OEM компьютера.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-131">OEM — The OEM code page of the machine.</span></span> <span data-ttu-id="bbbbd-132">Преобразования OemToUnicode и UnicodeToOem были сделаны.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-132">OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="bbbbd-133">Юникод — преобразования на странице кода не были сделаны.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="bbbbd-134">&lt;десятичной номер &gt; — кодовая страница определенного набора символов.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="bbbbd-135">Преобразования в Юникод и из него будут сделаны.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="bbbbd-136">Значение по умолчанию — ANSI.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-136">The default is ANSI.</span></span> <span data-ttu-id="bbbbd-137">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-137">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-138">Format</span><span class="sxs-lookup"><span data-stu-id="bbbbd-138">Format</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-139">Может иметь одно из следующих символов: TabDelimited, CSVDelimited, Delimited ( &lt; single &gt; character).</span><span class="sxs-lookup"><span data-stu-id="bbbbd-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="bbbbd-140">Односиматором в формате с делегированием может быть любой отдельный символ, кроме двойных кавычках ( &quot; ).</span><span class="sxs-lookup"><span data-stu-id="bbbbd-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="bbbbd-141">Значение по умолчанию — CSVDelimited.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-141">The default is CSVDelimited.</span></span> <span data-ttu-id="bbbbd-142">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-143">Расширения</span><span class="sxs-lookup"><span data-stu-id="bbbbd-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-144">Расширение любых файлов, которые необходимо просмотреть при поиске текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-144">The extension of any files to be browsed when looking for text-based data.</span></span> <span data-ttu-id="bbbbd-145">Значение по умолчанию: txt, csv, tab, asc.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-145">The default is txt, csv, tab, asc.</span></span> <span data-ttu-id="bbbbd-146">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-146">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="bbbbd-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-148">Двоичное значение, которое указывает, включается ли соответствующий символ валюты при экспорте полей валюты.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-148">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported.</span></span> <span data-ttu-id="bbbbd-149">Значение 01 указывает, что символ включен.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-149">A value of 01 indicates that the symbol is included.</span></span> <span data-ttu-id="bbbbd-150">Значение 00 указывает, что экспортируются только числовая информация.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-150">A value of 00 indicates that only the numeric data is exported.</span></span> <span data-ttu-id="bbbbd-151">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-151">The default is 01.</span></span> <span data-ttu-id="bbbbd-152">Значения имеют тип REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-152">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="bbbbd-153">Форматы ISAM источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="bbbbd-153">Text data source ISAM formats</span></span>

<span data-ttu-id="bbbbd-154">**Текстовая папка \\ "Форматы ISAM" \\** средства подключения Access содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbbbd-155">Имя записи</span><span class="sxs-lookup"><span data-stu-id="bbbbd-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="bbbbd-156">Тип</span><span class="sxs-lookup"><span data-stu-id="bbbbd-156">Type</span></span></p></th>
<th><p><span data-ttu-id="bbbbd-157">Значение</span><span class="sxs-lookup"><span data-stu-id="bbbbd-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-158">Engine</span><span class="sxs-lookup"><span data-stu-id="bbbbd-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-160">Текст</span><span class="sxs-lookup"><span data-stu-id="bbbbd-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="bbbbd-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-163">Текстовые файлы (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="bbbbd-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="bbbbd-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-166">Текстовые файлы (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="bbbbd-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="bbbbd-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-169">01</span><span class="sxs-lookup"><span data-stu-id="bbbbd-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="bbbbd-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-172">01</span><span class="sxs-lookup"><span data-stu-id="bbbbd-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="bbbbd-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bbbbd-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-175">2 </span><span class="sxs-lookup"><span data-stu-id="bbbbd-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="bbbbd-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-178">00</span><span class="sxs-lookup"><span data-stu-id="bbbbd-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="bbbbd-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-181">00</span><span class="sxs-lookup"><span data-stu-id="bbbbd-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="bbbbd-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-184">Импорт данных из внешнего файла в текущую базу данных.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-184">Import data from the external file into the current database.</span></span> <span data-ttu-id="bbbbd-185">Изменение данных в текущей базе данных не изменяет данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-185">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="bbbbd-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-188">Создайте таблицу в текущей базе данных, связанную с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-188">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="bbbbd-189">Изменение данных в текущей базе данных изменит данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-189">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="bbbbd-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-192">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-192">Export data from the current database into a text file.</span></span> <span data-ttu-id="bbbbd-193">Этот процесс переопишет данные при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-193">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="bbbbd-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-196">01</span><span class="sxs-lookup"><span data-stu-id="bbbbd-196">01</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="bbbbd-197">При изменении параметров реестра Windows необходимо выйти из системы и перезапустить механизм баз данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-import-isam-formats"></a><span data-ttu-id="bbbbd-198">Форматы ISAM для импорта HTML</span><span class="sxs-lookup"><span data-stu-id="bbbbd-198">HTML import ISAM formats</span></span>

<span data-ttu-id="bbbbd-199">HtmL-папка "Импорт" в формате **\\ \\ ISAM** средства подключения Access содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbbbd-200">Имя записи</span><span class="sxs-lookup"><span data-stu-id="bbbbd-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="bbbbd-201">Тип</span><span class="sxs-lookup"><span data-stu-id="bbbbd-201">Type</span></span></p></th>
<th><p><span data-ttu-id="bbbbd-202">Значение</span><span class="sxs-lookup"><span data-stu-id="bbbbd-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-203">Engine</span><span class="sxs-lookup"><span data-stu-id="bbbbd-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-205">Текст</span><span class="sxs-lookup"><span data-stu-id="bbbbd-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="bbbbd-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-208">HTML-файлы (*HT)*</span><span class="sxs-lookup"><span data-stu-id="bbbbd-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="bbbbd-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-211">01</span><span class="sxs-lookup"><span data-stu-id="bbbbd-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="bbbbd-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-214">00</span><span class="sxs-lookup"><span data-stu-id="bbbbd-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="bbbbd-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bbbbd-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-217">2 </span><span class="sxs-lookup"><span data-stu-id="bbbbd-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="bbbbd-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-220">00</span><span class="sxs-lookup"><span data-stu-id="bbbbd-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="bbbbd-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-223">00</span><span class="sxs-lookup"><span data-stu-id="bbbbd-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="bbbbd-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-226">Импорт данных из внешнего файла в текущую базу данных.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-226">Import data from the external file into the current database.</span></span> <span data-ttu-id="bbbbd-227">Изменение данных в текущей базе данных не изменяет данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-227">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="bbbbd-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-230">Создайте таблицу в текущей базе данных, связанную с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-230">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="bbbbd-231">Изменение данных в текущей базе данных изменит данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-231">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="bbbbd-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-234">01</span><span class="sxs-lookup"><span data-stu-id="bbbbd-234">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bbbbd-235">При изменении параметров реестра Windows необходимо выйти из системы и перезапустить механизм баз данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-export-isam-formats"></a><span data-ttu-id="bbbbd-236">Форматы ISAM экспорта HTML</span><span class="sxs-lookup"><span data-stu-id="bbbbd-236">HTML export ISAM formats</span></span>

<span data-ttu-id="bbbbd-237">Папка **\\ \\ HTML Export** в формате ISAM средства подключения Access содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbbbd-238">Имя записи</span><span class="sxs-lookup"><span data-stu-id="bbbbd-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="bbbbd-239">Тип</span><span class="sxs-lookup"><span data-stu-id="bbbbd-239">Type</span></span></p></th>
<th><p><span data-ttu-id="bbbbd-240">Значение</span><span class="sxs-lookup"><span data-stu-id="bbbbd-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-241">Engine</span><span class="sxs-lookup"><span data-stu-id="bbbbd-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-243">Текст</span><span class="sxs-lookup"><span data-stu-id="bbbbd-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="bbbbd-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-246">HTML-файлы (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="bbbbd-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="bbbbd-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-249">00</span><span class="sxs-lookup"><span data-stu-id="bbbbd-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="bbbbd-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-252">01</span><span class="sxs-lookup"><span data-stu-id="bbbbd-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="bbbbd-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bbbbd-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-255">2 </span><span class="sxs-lookup"><span data-stu-id="bbbbd-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="bbbbd-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-258">00</span><span class="sxs-lookup"><span data-stu-id="bbbbd-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="bbbbd-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-261">00</span><span class="sxs-lookup"><span data-stu-id="bbbbd-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="bbbbd-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bbbbd-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-264">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-264">Export data from the current database into a text file.</span></span> <span data-ttu-id="bbbbd-265">Этот процесс переопишет данные при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-265">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="bbbbd-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bbbbd-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-268">01</span><span class="sxs-lookup"><span data-stu-id="bbbbd-268">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bbbbd-269">При изменении параметров реестра Windows необходимо выйти из системы и перезапустить механизм баз данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="bbbbd-270">Настройка Schema.ini для текстовых и HTML-данных</span><span class="sxs-lookup"><span data-stu-id="bbbbd-270">Customizing the Schema.ini file for text and HTML data</span></span>

<span data-ttu-id="bbbbd-271">Чтобы читать, импортировать или экспортировать текст и HTML-данные, необходимо создать Schema.ini в дополнение к сведениям ISAM text в INI-файле.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-271">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file.</span></span> <span data-ttu-id="bbbbd-272">Schema.ini содержит особенности источника данных: форматирование текстового файла, его чтение во время импорта и формат экспорта по умолчанию для файлов.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-272">Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files.</span></span> <span data-ttu-id="bbbbd-273">В следующих примерах покажите макет для файла фиксированной ширины, Filename.txt:</span><span class="sxs-lookup"><span data-stu-id="bbbbd-273">The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

```text
    [Filename.txt] 
    
    ColNameHeader=False 
    
    Format=FixedLength 
    
    FixedFormat= RaggedEdge 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    Col1=columnname Char Width 24 
    
    Col2=columnname2 Date Width 9 
    
    Col3=columnname7 Float Width 10 
    
    Col4=columnname8 Integer Width 10 
    Col5=columnname9 LongChar Width 10
```

<br/>

<span data-ttu-id="bbbbd-274">Аналогичным образом, формат файла с делегированием задан следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bbbbd-274">Similarly, the format for a delimited file is specified as follows:</span></span>

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<br/>

<span data-ttu-id="bbbbd-275">Если вы экспортируете данные в текстовый файл с делениями, также укажите формат для этого файла:</span><span class="sxs-lookup"><span data-stu-id="bbbbd-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

```text
    [Export: My Special Export] 
    
    ColNameHeader=True 
    
    Format=TabDelimited 
    
    MaxScanRows=25 
    
    CharacterSet=OEM 
    
    DateTimeFormat=mm.dd.yy.hh.mm.ss 
    
    CurrencySymbol=Dm 
    
    CurrencyPosFormat=0 
    
    CurrencyDigits=2 
    
    CurrencyNegFormat=0 
    
    CurrencyThousandSymbol=, 
    
    CurrencyDecimalSymbol=. 
    
    DecimalSymbol=, 
    
    NumberDigits=2 
    
    NumberLeadingZeros=0 
    
    TextDelimeter="
```

<br/>

В примере "Мой специальный экспорт" указывается определенный параметр экспорта; Вы можете указать любой вариант параметров экспорта во время подключения. <span data-ttu-id="bbbbd-277">Этот последний пример также соответствует имени источника данных (DSN), которое можно передать при подключении.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-277">This last example also corresponds to a data source name (DSN) that can be optionally passed at connect time.</span></span> <span data-ttu-id="bbbbd-278">Все три раздела формата можно включить в один INI-файл.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-278">All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="bbbbd-279">Яд баз данных Microsoft Access использует Schema.ini записи следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bbbbd-280">Запись</span><span class="sxs-lookup"><span data-stu-id="bbbbd-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="bbbbd-281">Описание</span><span class="sxs-lookup"><span data-stu-id="bbbbd-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-282">ColNameHeader</span><span class="sxs-lookup"><span data-stu-id="bbbbd-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-283">Может иметь либо <strong>true</strong> (указывая, что первая запись данных указывает имена столбцов) или <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-284">Format</span><span class="sxs-lookup"><span data-stu-id="bbbbd-284">Format</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-285">Можно установить одно из следующих значений: TabDelimited, CSVDelimited, Delimited ( &lt; single &gt; character) или FixedLength.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="bbbbd-286">Для формата файлов с делегированием заданы отдельные знаки, кроме двойных кавычках ( &quot; ).</span><span class="sxs-lookup"><span data-stu-id="bbbbd-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-287">FixedFormat</span><span class="sxs-lookup"><span data-stu-id="bbbbd-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-288">Только если формат имеет значение FixedLength, можно установить одно из следующих значений: RaggedEdge или TrueFixedLength.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="bbbbd-289">RaggedEdge позволяет завершать строки символом возврата каретки.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="bbbbd-290">TrueFixedLength требует, чтобы каждая строка была точным количеством символов, а любые символы возврата каретки, не вложенные в границу строки, должны быть внедрены в поле.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="bbbbd-291">Если этого параметра нет, значение по умолчанию — RaggedEdge.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="bbbbd-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-293">Указывает количество строк, которые будут сканироваться при угадать типы данных столбцов.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-293">Indicates the number of rows to be scanned when guessing the column data types.</span></span> <span data-ttu-id="bbbbd-294">Если установлено 0, поиск будет искаться во всем файле.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-294">If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-295">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="bbbbd-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-296">Можно указать OEM, ANSI, UNICODE или десятичной кодировку допустимой кодировки, а также указать кодировку для исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="bbbbd-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-298">Можно установить строку формата, указывающее даты и время.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-298">Can be set to a format string indicating dates and times.</span></span> <span data-ttu-id="bbbbd-299">Эта запись должна быть указана, если все поля даты и времени в импорте/экспорте обрабатываются в одном формате.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-299">This entry should be specified if all date/time fields in the import/export are handled with the same format.</span></span> <span data-ttu-id="bbbbd-300">Поддерживаются все форматы ядер ядер баз данных Microsoft Jet, кроме AM и PM.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-300">All of the Microsoft Jet database engine formats except AM and PM are supported.</span></span> <span data-ttu-id="bbbbd-301">При отсутствии строки формата используются краткие параметры даты и времени панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-301">In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="bbbbd-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-303">Указывает символ валюты, используемый для значений валюты в текстовом файле.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-303">Indicates the currency symbol to be used for currency values in the text file.</span></span> <span data-ttu-id="bbbbd-304">Примеры: знак доллара ($) и dm.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-304">Examples include the dollar sign ($) and Dm.</span></span> <span data-ttu-id="bbbbd-305">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-305">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="bbbbd-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-307">Можно установить любое из следующих значений: префикс символа валюты без суффикса символа разделения ($1) без префикса символа разделения (1$) валюты с одним символом разделения символов ($ 1) с одним разделением символов (1 $). Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="bbbbd-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-309">Указывает количество цифр, используемых для дробной части валюты.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-309">Specifies the number of digits used for the fractional part of a currency amount.</span></span> <span data-ttu-id="bbbbd-310">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-310">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="bbbbd-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-312">Может иметь одно из следующих значений: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ 1 $– 1– $ –1– $ –1– $ ($ 1) ($ 1 $) Знак доллара отображается в этом примере, но его следует заменить соответствующим значением CurrencySymbol в фактической программе.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="bbbbd-313">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="bbbbd-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-315">Указывает символ, который будет использоваться для разделения значений валюты на тысячи в текстовом файле.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-315">Indicates the single-character symbol to be used for separating currency values by thousands in the text file.</span></span> <span data-ttu-id="bbbbd-316">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-316">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="bbbbd-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-318">Можно установить любой отдельный символ, используемый для отделения целого от дробной части валюты.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-318">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount.</span></span> <span data-ttu-id="bbbbd-319">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-319">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="bbbbd-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-321">Можно установить любой отдельный символ, используемый для отделять это число от дробной части числа.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-321">Can be set to any single character that is used to separate the integer from the fractional part of a number.</span></span> <span data-ttu-id="bbbbd-322">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-322">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="bbbbd-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-324">Указывает количество десятичных цифр в дробной части числа.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-324">Indicates the number of decimal digits in the fractional portion of a number.</span></span> <span data-ttu-id="bbbbd-325">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-325">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="bbbbd-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-327">Указывает, должно ли десятичной заданное значение меньше 1 и больше –1 содержать нулей в 1; это значение может иметь значение False (без нулей в окнах в окнах) или True.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bbbbd-328">Col1, Col2, ...</span><span class="sxs-lookup"><span data-stu-id="bbbbd-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-329">Перечисляет столбцы в текстовом файле для чтения.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="bbbbd-330">Формат этой записи: <em>Coln</em> = <em>columnName</em> type [Width <em>#</em> ] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="bbbbd-331"><em>тип:</em>может быть бит, byte, short, Long, Decimal, Currency, Single, Double, DateTime.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="bbbbd-332">Двоичный файл, OLE, текст или memo.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="bbbbd-333">Кроме того, поддерживаются следующие типы текстовых драйверов ODBC: Char (такой же, как Text) Float (то же, что и Double) Integer (то же, что и Short) LongChar (то же, что и Memo) <em>Формат</em> даты даты В случае с memo-типом можно использовать дополнительный маркер формата [гиперссылка атрибута] для указания столбцов, которые должны быть активными URL-адресами в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="bbbbd-334">В случае десятичных знаков следует использовать дополнительные маркеры формата [Scale #] Precision #] (Точность).</span><span class="sxs-lookup"><span data-stu-id="bbbbd-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bbbbd-335">TextDelimiter</span><span class="sxs-lookup"><span data-stu-id="bbbbd-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="bbbbd-336">Можно установить любой отдельный символ, используемый для разграничия строк, содержащих любые другие специальные символы.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="bbbbd-337">Например,</span><span class="sxs-lookup"><span data-stu-id="bbbbd-337">E.g.</span></span> <span data-ttu-id="bbbbd-338">&quot;abc &quot; , &quot; xyz,pqr &quot; , &quot; hij If this entry is not present &quot; the default delimiter is a double quote.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="bbbbd-339">Если эта запись не является строкой, никакие символы не будут рассматриваться &quot; &quot; как разлицы.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bbbbd-340">При изменении Schema.ini файлов необходимо выйти из системы и перезапустить механизм баз данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bbbbd-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


