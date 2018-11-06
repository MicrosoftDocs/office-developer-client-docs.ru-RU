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
ms.openlocfilehash: 4248adc507a93284a15725bbda0255a3518e90a9
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997471"
---
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="a9774-102">Инициализация драйвера источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="a9774-102">Initializing the Text Data Source driver</span></span>

<span data-ttu-id="a9774-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9774-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9774-104">Для обоих источников данных и источники данных HTML, используется один и тот же драйвер базы данных.</span><span class="sxs-lookup"><span data-stu-id="a9774-104">The same database driver is used for both Text Data sources and for HTML data sources.</span></span>

<span data-ttu-id="a9774-105">При установке драйвера базы данных источника данных текста программа установки записывает набор значений по умолчанию реестра Microsoft Windows в подразделы обработчики и ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="a9774-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="a9774-106">Не изменяйте эти параметры напрямую; для добавления, удаления или изменения этих параметров с помощью программы установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="a9774-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="a9774-107">В следующих разделах инициализации и параметров ISAM Format драйвера базы данных источника данных текста.</span><span class="sxs-lookup"><span data-stu-id="a9774-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="a9774-108">Параметры инициализации источника данных текста</span><span class="sxs-lookup"><span data-stu-id="a9774-108">Text data source initialization settings</span></span>

<span data-ttu-id="a9774-109">**Модуль подключения к Access\\ISAM Formats\\текст папка** содержит параметры инициализации драйвера Acetxt.dll, который используется для внешнего доступа к файлам текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="a9774-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="a9774-110">В следующем примере приведены типичные параметры записей в этой папке.</span><span class="sxs-lookup"><span data-stu-id="a9774-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<span data-ttu-id="a9774-111">Ядро базы данных Microsoft Access использует записи в папке Text следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a9774-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9774-112">Запись</span><span class="sxs-lookup"><span data-stu-id="a9774-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="a9774-113">Описание</span><span class="sxs-lookup"><span data-stu-id="a9774-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9774-114">Win32</span><span class="sxs-lookup"><span data-stu-id="a9774-114">win32</span></span></p></td>
<td><p><span data-ttu-id="a9774-115">Расположение Acetxt.dll.</span><span class="sxs-lookup"><span data-stu-id="a9774-115">The location of Acetxt.dll.</span></span> <span data-ttu-id="a9774-116">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="a9774-116">The full path is determined at the time of installation.</span></span> <span data-ttu-id="a9774-117">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="a9774-117">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="a9774-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="a9774-119">Количество строк, просматриваемых при распознавании типы столбцов.</span><span class="sxs-lookup"><span data-stu-id="a9774-119">The number of rows to be scanned when guessing the column types.</span></span> <span data-ttu-id="a9774-120">Если задано значение 0, весь файл будет осуществляться.</span><span class="sxs-lookup"><span data-stu-id="a9774-120">If set to 0, the entire file will be searched.</span></span> <span data-ttu-id="a9774-121">Значение по умолчанию равно 25.</span><span class="sxs-lookup"><span data-stu-id="a9774-121">The default is 25.</span></span> <span data-ttu-id="a9774-122">Значения — типа REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="a9774-122">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-123">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="a9774-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="a9774-124">Двоичное значение, указывающее, содержит ли имена столбцов первой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="a9774-124">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="a9774-125">Значение 01 показывает, что во время импорта, имена столбцов берутся из первой строки.</span><span class="sxs-lookup"><span data-stu-id="a9774-125">A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-126">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="a9774-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="a9774-127">Указывает, как хранятся страницы текста.</span><span class="sxs-lookup"><span data-stu-id="a9774-127">An indicator of how text pages are stored.</span></span> <span data-ttu-id="a9774-128">Имеются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="a9774-128">Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="a9774-129">ANSI — Кодовая страница ANSI компьютера.</span><span class="sxs-lookup"><span data-stu-id="a9774-129">ANSI — The ANSI code page of the machine.</span></span> <span data-ttu-id="a9774-130">AnsiToUnicode и UnicodeToAnsi преобразований.</span><span class="sxs-lookup"><span data-stu-id="a9774-130">AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="a9774-131">OEM — Кодовая страница OEM компьютера.</span><span class="sxs-lookup"><span data-stu-id="a9774-131">OEM — The OEM code page of the machine.</span></span> <span data-ttu-id="a9774-132">OemToUnicode и UnicodeToOem преобразований.</span><span class="sxs-lookup"><span data-stu-id="a9774-132">OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="a9774-133">Unicode — преобразования кодовой страницы не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a9774-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="a9774-134">&lt;Преобразование десятичного числа&gt; — номер кодовой страницы заданного набора знаков.</span><span class="sxs-lookup"><span data-stu-id="a9774-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="a9774-135">Будет выполнено преобразование в Юникод и обратно.</span><span class="sxs-lookup"><span data-stu-id="a9774-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="a9774-136">Значение по умолчанию — ANSI.</span><span class="sxs-lookup"><span data-stu-id="a9774-136">The default is ANSI.</span></span> <span data-ttu-id="a9774-137">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="a9774-137">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-138">Format</span><span class="sxs-lookup"><span data-stu-id="a9774-138">Format</span></span></p></td>
<td><p><span data-ttu-id="a9774-139">Может быть любым из следующих значений: TabDelimited, CSVDelimited, с разделителями (&lt;отдельный знак&gt;).</span><span class="sxs-lookup"><span data-stu-id="a9774-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="a9774-140">Знаком разделителя в формате с разделителями может быть любой отдельный знак, за исключением двойные кавычки (&quot;).</span><span class="sxs-lookup"><span data-stu-id="a9774-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="a9774-141">Значение по умолчанию — CSVDelimited.</span><span class="sxs-lookup"><span data-stu-id="a9774-141">The default is CSVDelimited.</span></span> <span data-ttu-id="a9774-142">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="a9774-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-143">Расширения</span><span class="sxs-lookup"><span data-stu-id="a9774-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="a9774-144">Расширения файлов, для просмотра при поиске текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="a9774-144">The extension of any files to be browsed when looking for text-based data.</span></span> <span data-ttu-id="a9774-145">Значение по умолчанию — txt, csv, вкладка, asc.</span><span class="sxs-lookup"><span data-stu-id="a9774-145">The default is txt, csv, tab, asc.</span></span> <span data-ttu-id="a9774-146">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="a9774-146">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="a9774-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="a9774-148">Двоичное значение, указывающее, является ли символ валюты соответствующие при экспорте поля валюты.</span><span class="sxs-lookup"><span data-stu-id="a9774-148">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported.</span></span> <span data-ttu-id="a9774-149">Значение 01 указывает, что включен символ.</span><span class="sxs-lookup"><span data-stu-id="a9774-149">A value of 01 indicates that the symbol is included.</span></span> <span data-ttu-id="a9774-150">Значение 00 указывает, что только числовые данные экспортировать.</span><span class="sxs-lookup"><span data-stu-id="a9774-150">A value of 00 indicates that only the numeric data is exported.</span></span> <span data-ttu-id="a9774-151">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="a9774-151">The default is 01.</span></span> <span data-ttu-id="a9774-152">Значения — типа REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="a9774-152">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="a9774-153">Текстовые форматы ISAM источника данных</span><span class="sxs-lookup"><span data-stu-id="a9774-153">Text data source ISAM formats</span></span>

<span data-ttu-id="a9774-154">**Модуль подключения к Access\\ISAM Formats\\текст** папка содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="a9774-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9774-155">Имя записи</span><span class="sxs-lookup"><span data-stu-id="a9774-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="a9774-156">Тип</span><span class="sxs-lookup"><span data-stu-id="a9774-156">Type</span></span></p></th>
<th><p><span data-ttu-id="a9774-157">Значение</span><span class="sxs-lookup"><span data-stu-id="a9774-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9774-158">Модуль</span><span class="sxs-lookup"><span data-stu-id="a9774-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="a9774-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-160">Текст</span><span class="sxs-lookup"><span data-stu-id="a9774-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="a9774-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="a9774-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-163">Текстовые файлы (\*.txt; \*.csv; \* .tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="a9774-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="a9774-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="a9774-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-166">Текстовые файлы (\*.txt; \*.csv; \* .tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="a9774-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="a9774-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="a9774-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-169">01</span><span class="sxs-lookup"><span data-stu-id="a9774-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="a9774-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="a9774-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-172">01</span><span class="sxs-lookup"><span data-stu-id="a9774-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="a9774-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="a9774-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a9774-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="a9774-175">2</span><span class="sxs-lookup"><span data-stu-id="a9774-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="a9774-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="a9774-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-178">00</span><span class="sxs-lookup"><span data-stu-id="a9774-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="a9774-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="a9774-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-181">00</span><span class="sxs-lookup"><span data-stu-id="a9774-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="a9774-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="a9774-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-184">Импорт данных из внешнего файла в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="a9774-184">Import data from the external file into the current database.</span></span> <span data-ttu-id="a9774-185">Изменение данных в текущей базе данных остаются без изменений данных во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="a9774-185">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="a9774-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="a9774-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-188">Создайте таблицу в текущей базе данных, которая связана с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="a9774-188">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="a9774-189">Изменение данных в текущей базе данных будет изменять данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="a9774-189">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="a9774-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="a9774-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-192">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="a9774-192">Export data from the current database into a text file.</span></span> <span data-ttu-id="a9774-193">В этом будут перезаписаны данные при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="a9774-193">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="a9774-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="a9774-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-196">01</span><span class="sxs-lookup"><span data-stu-id="a9774-196">01</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="a9774-197">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="a9774-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-import-isam-formats"></a><span data-ttu-id="a9774-198">Форматы ISAM импорта HTML</span><span class="sxs-lookup"><span data-stu-id="a9774-198">HTML import ISAM formats</span></span>

<span data-ttu-id="a9774-199">**Модуль подключения к Access\\ISAM Formats\\импорта HTML** папка содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="a9774-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9774-200">Имя записи</span><span class="sxs-lookup"><span data-stu-id="a9774-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="a9774-201">Тип</span><span class="sxs-lookup"><span data-stu-id="a9774-201">Type</span></span></p></th>
<th><p><span data-ttu-id="a9774-202">Значение</span><span class="sxs-lookup"><span data-stu-id="a9774-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9774-203">Модуль</span><span class="sxs-lookup"><span data-stu-id="a9774-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="a9774-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-205">Текст</span><span class="sxs-lookup"><span data-stu-id="a9774-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="a9774-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="a9774-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-208">HTML-файлы (*.ht*)</span><span class="sxs-lookup"><span data-stu-id="a9774-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="a9774-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="a9774-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-211">01</span><span class="sxs-lookup"><span data-stu-id="a9774-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="a9774-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="a9774-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-214">00</span><span class="sxs-lookup"><span data-stu-id="a9774-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="a9774-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="a9774-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a9774-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="a9774-217">2</span><span class="sxs-lookup"><span data-stu-id="a9774-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="a9774-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="a9774-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-220">00</span><span class="sxs-lookup"><span data-stu-id="a9774-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="a9774-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="a9774-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-223">00</span><span class="sxs-lookup"><span data-stu-id="a9774-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="a9774-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="a9774-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-226">Импорт данных из внешнего файла в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="a9774-226">Import data from the external file into the current database.</span></span> <span data-ttu-id="a9774-227">Изменение данных в текущей базе данных остаются без изменений данных во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="a9774-227">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="a9774-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="a9774-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-230">Создайте таблицу в текущей базе данных, которая связана с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="a9774-230">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="a9774-231">Изменение данных в текущей базе данных будет изменять данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="a9774-231">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="a9774-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="a9774-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-234">01</span><span class="sxs-lookup"><span data-stu-id="a9774-234">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a9774-235">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="a9774-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-export-isam-formats"></a><span data-ttu-id="a9774-236">Форматы ISAM экспорта HTML</span><span class="sxs-lookup"><span data-stu-id="a9774-236">HTML export ISAM formats</span></span>

<span data-ttu-id="a9774-237">**Модуль подключения к Access\\ISAM Formats\\экспорта HTML** папка содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="a9774-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9774-238">Имя записи</span><span class="sxs-lookup"><span data-stu-id="a9774-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="a9774-239">Тип</span><span class="sxs-lookup"><span data-stu-id="a9774-239">Type</span></span></p></th>
<th><p><span data-ttu-id="a9774-240">Значение</span><span class="sxs-lookup"><span data-stu-id="a9774-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9774-241">Модуль</span><span class="sxs-lookup"><span data-stu-id="a9774-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="a9774-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-243">Текст</span><span class="sxs-lookup"><span data-stu-id="a9774-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="a9774-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="a9774-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-246">HTML-файлы (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="a9774-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="a9774-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="a9774-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-249">00</span><span class="sxs-lookup"><span data-stu-id="a9774-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="a9774-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="a9774-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-252">01</span><span class="sxs-lookup"><span data-stu-id="a9774-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="a9774-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="a9774-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="a9774-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="a9774-255">2</span><span class="sxs-lookup"><span data-stu-id="a9774-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="a9774-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="a9774-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-258">00</span><span class="sxs-lookup"><span data-stu-id="a9774-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="a9774-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="a9774-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-261">00</span><span class="sxs-lookup"><span data-stu-id="a9774-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="a9774-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="a9774-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="a9774-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="a9774-264">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="a9774-264">Export data from the current database into a text file.</span></span> <span data-ttu-id="a9774-265">В этом будут перезаписаны данные при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="a9774-265">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="a9774-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="a9774-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="a9774-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="a9774-268">01</span><span class="sxs-lookup"><span data-stu-id="a9774-268">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a9774-269">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="a9774-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="a9774-270">Настройка файла Schema.ini текста и данных HTML</span><span class="sxs-lookup"><span data-stu-id="a9774-270">Customizing the Schema.ini file for text and HTML data</span></span>

<span data-ttu-id="a9774-271">Для чтения, импорта, или экспорта текстовых данных и данных HTML, необходимо создать файл Schema.ini Кроме включения сведений Text ISAM в INI-файле.</span><span class="sxs-lookup"><span data-stu-id="a9774-271">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file.</span></span> <span data-ttu-id="a9774-272">Этот файл содержит особенности источника данных: формат текстового файла, как она считывается во время импорта и экспорта формат по умолчанию — для файлов.</span><span class="sxs-lookup"><span data-stu-id="a9774-272">Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files.</span></span> <span data-ttu-id="a9774-273">В следующих примерах показано макета для файла фиксированной ширины Filename.txt:</span><span class="sxs-lookup"><span data-stu-id="a9774-273">The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

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

<span data-ttu-id="a9774-274">Аналогично формат для файла с разделителями задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a9774-274">Similarly, the format for a delimited file is specified as follows:</span></span>

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

<span data-ttu-id="a9774-275">Если данные экспортируются в файл с разделителями, укажите формат для этого файла:</span><span class="sxs-lookup"><span data-stu-id="a9774-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

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

В примере Мой Экспорт относится к определенным экспорте; можно указать любые изменения параметров экспорта во время подключения. Этот пример также соответствует имени источника данных (DSN), который может быть передан при необходимости во время подключения. <span data-ttu-id="a9774-278">Все три раздела может быть включен в одном INI-файла.</span><span class="sxs-lookup"><span data-stu-id="a9774-278">All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="a9774-279">Ядро базы данных Microsoft Access использует записи Schema.ini следующим образом.</span><span class="sxs-lookup"><span data-stu-id="a9774-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9774-280">Запись</span><span class="sxs-lookup"><span data-stu-id="a9774-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="a9774-281">Описание</span><span class="sxs-lookup"><span data-stu-id="a9774-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9774-282">ColNameHeader</span><span class="sxs-lookup"><span data-stu-id="a9774-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="a9774-283">Может быть присвоено значение <strong>True</strong> (это означает, что первая запись данных задает имена столбцов) или <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9774-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-284">Format</span><span class="sxs-lookup"><span data-stu-id="a9774-284">Format</span></span></p></td>
<td><p><span data-ttu-id="a9774-285">Может быть установлено одно из следующих значений: TabDelimited, CSVDelimited, с разделителями (&lt;отдельный знак&gt;), или FixedLength.</span><span class="sxs-lookup"><span data-stu-id="a9774-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="a9774-286">Разделитель, указанный для формата файла с разделителями может быть любой отдельный знак, за исключением двойные кавычки (&quot;).</span><span class="sxs-lookup"><span data-stu-id="a9774-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-287">FixedFormat</span><span class="sxs-lookup"><span data-stu-id="a9774-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="a9774-288">Только для использования при FixedLength имеет формат, это может быть установлено одно из следующих значений: значение RaggedEdge или TrueFixedLength.</span><span class="sxs-lookup"><span data-stu-id="a9774-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="a9774-289">Значение RaggedEdge позволяет прерывать символом возврата каретки строки.</span><span class="sxs-lookup"><span data-stu-id="a9774-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="a9774-290">Значение TrueFixedLength каждую строку, чтобы быть точное количество символов и знаков возврата каретки не в конце строки предполагается, что внедрены в поле.</span><span class="sxs-lookup"><span data-stu-id="a9774-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="a9774-291">Если этот параметр не указан, значением по умолчанию является значение RaggedEdge.</span><span class="sxs-lookup"><span data-stu-id="a9774-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="a9774-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="a9774-293">Указывает число строк, просматриваемых при распознавании в столбце типов данных.</span><span class="sxs-lookup"><span data-stu-id="a9774-293">Indicates the number of rows to be scanned when guessing the column data types.</span></span> <span data-ttu-id="a9774-294">Если это имеет значение 0, выполняется весь файл.</span><span class="sxs-lookup"><span data-stu-id="a9774-294">If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-295">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="a9774-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="a9774-296">Можно задать OEM, ANSI, UNICODE или десятичное число допустимый код страницы и указывает набор знаков исходного файла.</span><span class="sxs-lookup"><span data-stu-id="a9774-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="a9774-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="a9774-298">Можно задать строку формата даты и времени.</span><span class="sxs-lookup"><span data-stu-id="a9774-298">Can be set to a format string indicating dates and times.</span></span> <span data-ttu-id="a9774-299">Если все поля даты/времени в тот же формат обрабатываются импорта и экспорта должны быть указаны в этой записи.</span><span class="sxs-lookup"><span data-stu-id="a9774-299">This entry should be specified if all date/time fields in the import/export are handled with the same format.</span></span> <span data-ttu-id="a9774-300">Поддерживаются все форматы ядра базы данных Microsoft Jet за исключением AM и PM.</span><span class="sxs-lookup"><span data-stu-id="a9774-300">All of the Microsoft Jet database engine formats except AM and PM are supported.</span></span> <span data-ttu-id="a9774-301">В случае отсутствия строку формата используются параметры изображения и время краткий формат даты панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a9774-301">In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="a9774-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="a9774-303">Указывает символ валюты, которое будет использоваться для денежных значений в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="a9774-303">Indicates the currency symbol to be used for currency values in the text file.</span></span> <span data-ttu-id="a9774-304">Примеры включают доллара ($) и интеллектуальный анализ данных.</span><span class="sxs-lookup"><span data-stu-id="a9774-304">Examples include the dollar sign ($) and Dm.</span></span> <span data-ttu-id="a9774-305">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a9774-305">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="a9774-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="a9774-307">Может быть установлено любое из следующих значений: символ денежной единицы перед без пробела ($1) суффикс символ валюты без пробела (1$) символ денежной единицы перед суффикс символ валюты один символ пробела ($ 1) с одним пробелом (1 $) Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a9774-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="a9774-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="a9774-309">Указывает количество знаков, используемых для дробной части денежной суммы.</span><span class="sxs-lookup"><span data-stu-id="a9774-309">Specifies the number of digits used for the fractional part of a currency amount.</span></span> <span data-ttu-id="a9774-310">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a9774-310">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="a9774-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="a9774-312">Может иметь одно из следующих значений: (1) — $1 $– 1 $1 — (1$) -1$ $ 1 – $ 1 – – 1 $ – $ 1 1 – $ 1 – $ 1-1 – $ ($ 1) (1 $) знак доллара отображается для этого примера, но оно должно быть заменено соответствующим значением качестве в самой программы.</span><span class="sxs-lookup"><span data-stu-id="a9774-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="a9774-313">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a9774-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="a9774-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="a9774-315">Символ одного знака, используемый для разделения денежных значений тысячи людей в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="a9774-315">Indicates the single-character symbol to be used for separating currency values by thousands in the text file.</span></span> <span data-ttu-id="a9774-316">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a9774-316">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="a9774-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="a9774-318">Можно задать для любой отдельный знак, используемый для разделения целой дробная часть денежной суммы.</span><span class="sxs-lookup"><span data-stu-id="a9774-318">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount.</span></span> <span data-ttu-id="a9774-319">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a9774-319">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="a9774-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="a9774-321">Можно задать для любой отдельный знак, используемый для отделения целое число от дробная часть числа.</span><span class="sxs-lookup"><span data-stu-id="a9774-321">Can be set to any single character that is used to separate the integer from the fractional part of a number.</span></span> <span data-ttu-id="a9774-322">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a9774-322">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="a9774-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="a9774-324">Указывает число десятичных знаков в дробной части числа.</span><span class="sxs-lookup"><span data-stu-id="a9774-324">Indicates the number of decimal digits in the fractional portion of a number.</span></span> <span data-ttu-id="a9774-325">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="a9774-325">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="a9774-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="a9774-327">Определяет, содержат ли десятичное значение меньше 1 и больше -1 нулей; Это значение может быть False (отсутствие нуля) или True.</span><span class="sxs-lookup"><span data-stu-id="a9774-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9774-328">Столбец1 Col2...</span><span class="sxs-lookup"><span data-stu-id="a9774-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="a9774-329">Список столбцов в текстовый файл для чтения.</span><span class="sxs-lookup"><span data-stu-id="a9774-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="a9774-330">Формат этой записи должны быть: <em>Coln</em>=<em>columnName</em> тип [Width <em> #</em>] <em>columnName</em>: имена столбцов с внедренным пробелов должно заключаться в кавычки.</span><span class="sxs-lookup"><span data-stu-id="a9774-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="a9774-331"><em>Тип</em>: бит, Byte, Short, Long, знаков после запятой, Currency, Single, Double, даты и времени.</span><span class="sxs-lookup"><span data-stu-id="a9774-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="a9774-332">Двоичный OLE, текст или заметка.</span><span class="sxs-lookup"><span data-stu-id="a9774-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="a9774-333">Кроме того, поддерживаются следующие типы текстовых драйверов ODBC: символ (то же, как текст) с плавающей запятой (то же, что Double) Integer (то же, что Short) LongChar (то же, что Memo) даты <em>формата даты</em> в случае типа Memo может быть маркер дополнительные формат [атрибут гиперссылка] используется для указания столбцов, которые должны быть активные URL-адреса в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="a9774-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="a9774-334">В случае тип Decimal введите дополнительные формат маркеры [масштабировать #] точности #] следует использовать.</span><span class="sxs-lookup"><span data-stu-id="a9774-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9774-335">TextDelimiter</span><span class="sxs-lookup"><span data-stu-id="a9774-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="a9774-336">Можно задать для любой отдельный знак, используемый для выделения строки, содержащие любое из специальных символов.</span><span class="sxs-lookup"><span data-stu-id="a9774-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="a9774-337">Пример:</span><span class="sxs-lookup"><span data-stu-id="a9774-337">E.g.</span></span> <span data-ttu-id="a9774-338">&quot;ABC&quot;,&quot;xyz, компании pqr&quot;,&quot;hij&quot; при этом нет разделителем по умолчанию является двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="a9774-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="a9774-339">Если эта запись — это строка &quot;нет&quot; затем символы не будут рассматриваться в качестве разделителей.</span><span class="sxs-lookup"><span data-stu-id="a9774-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="a9774-340">При изменении параметров файла Schema.ini необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="a9774-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


