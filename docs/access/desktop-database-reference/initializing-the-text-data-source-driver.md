---
title: Инициализация драйвера источника текстовых данных
TOCTitle: Initializing the Text Data Source Driver
ms:assetid: cba0864e-5f94-bf43-4708-b1981e3acaff
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834391(v=office.15)
ms:contentKeyID: 48547718
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032166
f1_categories:
- Office.Version=v15
ms.openlocfilehash: d52020deecce9235db12f749b9d6913653157034
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937773"
---
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="97202-102">Инициализация драйвера источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="97202-102">Initializing the Text Data Source Driver</span></span>


<span data-ttu-id="97202-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="97202-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="97202-104">Для обоих источников данных и источники данных HTML, используется один и тот же драйвер базы данных.</span><span class="sxs-lookup"><span data-stu-id="97202-104">The same database driver is used for both Text Data sources and for HTML data sources.</span></span>

<span data-ttu-id="97202-105">При установке драйвера базы данных источника данных текста программа установки записывает набор значений по умолчанию реестра Microsoft Windows в подразделы обработчики и ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="97202-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="97202-106">Не изменяйте эти параметры напрямую; для добавления, удаления или изменения этих параметров с помощью программы установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="97202-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="97202-107">В следующих разделах инициализации и параметров ISAM Format драйвера базы данных источника данных текста.</span><span class="sxs-lookup"><span data-stu-id="97202-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="97202-108">Параметры инициализации источника данных текста</span><span class="sxs-lookup"><span data-stu-id="97202-108">Text Data Source Initialization Settings</span></span>

<span data-ttu-id="97202-109">**Модуль подключения к Access\\ISAM Formats\\текст папка** содержит параметры инициализации драйвера Acetxt.dll, который используется для внешнего доступа к файлам текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="97202-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="97202-110">В следующем примере приведены типичные параметры записей в этой папке.</span><span class="sxs-lookup"><span data-stu-id="97202-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ ACETXT.DLL 
    
    MaxScanRows=25 
    
    FirstRowHasNames=True 
    
    CharacterSet= ANSI 
    
    Format=CSVDelimited 
    
    Extensions= txt,csv,tab,asc 
    
    ExportCurrencySymbols=Yes
```

<span data-ttu-id="97202-111">Ядро базы данных Microsoft Access использует записи в папке Text следующим образом.</span><span class="sxs-lookup"><span data-stu-id="97202-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97202-112">Запись</span><span class="sxs-lookup"><span data-stu-id="97202-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="97202-113">Описание</span><span class="sxs-lookup"><span data-stu-id="97202-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97202-114">Win32</span><span class="sxs-lookup"><span data-stu-id="97202-114">win32</span></span></p></td>
<td><p><span data-ttu-id="97202-115">Расположение Acetxt.dll.</span><span class="sxs-lookup"><span data-stu-id="97202-115">The location of Acetxt.dll.</span></span> <span data-ttu-id="97202-116">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="97202-116">The full path is determined at the time of installation.</span></span> <span data-ttu-id="97202-117">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="97202-117">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="97202-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="97202-119">Количество строк, просматриваемых при распознавании типы столбцов.</span><span class="sxs-lookup"><span data-stu-id="97202-119">The number of rows to be scanned when guessing the column types.</span></span> <span data-ttu-id="97202-120">Если задано значение 0, весь файл будет осуществляться.</span><span class="sxs-lookup"><span data-stu-id="97202-120">If set to 0, the entire file will be searched.</span></span> <span data-ttu-id="97202-121">Значение по умолчанию равно 25.</span><span class="sxs-lookup"><span data-stu-id="97202-121">The default is 25.</span></span> <span data-ttu-id="97202-122">Значения — типа REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="97202-122">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-123">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="97202-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="97202-124">Двоичное значение, указывающее, содержит ли имена столбцов первой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="97202-124">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="97202-125">Значение 01 показывает, что во время импорта, имена столбцов берутся из первой строки.</span><span class="sxs-lookup"><span data-stu-id="97202-125">A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-126">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="97202-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="97202-127">Указывает, как хранятся страницы текста.</span><span class="sxs-lookup"><span data-stu-id="97202-127">An indicator of how text pages are stored.</span></span> <span data-ttu-id="97202-128">Имеются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="97202-128">Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="97202-129">ANSI — Кодовая страница ANSI компьютера.</span><span class="sxs-lookup"><span data-stu-id="97202-129">ANSI — The ANSI code page of the machine.</span></span> <span data-ttu-id="97202-130">AnsiToUnicode и UnicodeToAnsi преобразований.</span><span class="sxs-lookup"><span data-stu-id="97202-130">AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="97202-131">OEM — Кодовая страница OEM компьютера.</span><span class="sxs-lookup"><span data-stu-id="97202-131">OEM — The OEM code page of the machine.</span></span> <span data-ttu-id="97202-132">OemToUnicode и UnicodeToOem преобразований.</span><span class="sxs-lookup"><span data-stu-id="97202-132">OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="97202-133">Unicode — преобразования кодовой страницы не выполняется.</span><span class="sxs-lookup"><span data-stu-id="97202-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="97202-134">&lt;Преобразование десятичного числа&gt; — номер кодовой страницы заданного набора знаков.</span><span class="sxs-lookup"><span data-stu-id="97202-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="97202-135">Будет выполнено преобразование в Юникод и обратно.</span><span class="sxs-lookup"><span data-stu-id="97202-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="97202-136">Значение по умолчанию — ANSI.</span><span class="sxs-lookup"><span data-stu-id="97202-136">The default is ANSI.</span></span> <span data-ttu-id="97202-137">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="97202-137">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-138">Format</span><span class="sxs-lookup"><span data-stu-id="97202-138">Format</span></span></p></td>
<td><p><span data-ttu-id="97202-139">Может быть любым из следующих значений: TabDelimited, CSVDelimited, с разделителями (&lt;отдельный знак&gt;).</span><span class="sxs-lookup"><span data-stu-id="97202-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="97202-140">Знаком разделителя в формате с разделителями может быть любой отдельный знак, за исключением двойные кавычки (&quot;).</span><span class="sxs-lookup"><span data-stu-id="97202-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="97202-141">Значение по умолчанию — CSVDelimited.</span><span class="sxs-lookup"><span data-stu-id="97202-141">The default is CSVDelimited.</span></span> <span data-ttu-id="97202-142">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="97202-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-143">Расширения</span><span class="sxs-lookup"><span data-stu-id="97202-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="97202-144">Расширения файлов, для просмотра при поиске текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="97202-144">The extension of any files to be browsed when looking for text-based data.</span></span> <span data-ttu-id="97202-145">Значение по умолчанию — txt, csv, вкладка, asc.</span><span class="sxs-lookup"><span data-stu-id="97202-145">The default is txt, csv, tab, asc.</span></span> <span data-ttu-id="97202-146">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="97202-146">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="97202-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="97202-148">Двоичное значение, указывающее, является ли символ валюты соответствующие при экспорте поля валюты.</span><span class="sxs-lookup"><span data-stu-id="97202-148">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported.</span></span> <span data-ttu-id="97202-149">Значение 01 указывает, что включен символ.</span><span class="sxs-lookup"><span data-stu-id="97202-149">A value of 01 indicates that the symbol is included.</span></span> <span data-ttu-id="97202-150">Значение 00 указывает, что только числовые данные экспортировать.</span><span class="sxs-lookup"><span data-stu-id="97202-150">A value of 00 indicates that only the numeric data is exported.</span></span> <span data-ttu-id="97202-151">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="97202-151">The default is 01.</span></span> <span data-ttu-id="97202-152">Значения — типа REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="97202-152">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="97202-153">Текстовые форматы ISAM источника данных</span><span class="sxs-lookup"><span data-stu-id="97202-153">Text Data Source ISAM Formats</span></span>

<span data-ttu-id="97202-154">**Модуль подключения к Access\\ISAM Formats\\текст** папка содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="97202-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97202-155">Имя записи</span><span class="sxs-lookup"><span data-stu-id="97202-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="97202-156">Тип</span><span class="sxs-lookup"><span data-stu-id="97202-156">Type</span></span></p></th>
<th><p><span data-ttu-id="97202-157">Значение</span><span class="sxs-lookup"><span data-stu-id="97202-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97202-158">Модуль</span><span class="sxs-lookup"><span data-stu-id="97202-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="97202-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-160">Текст</span><span class="sxs-lookup"><span data-stu-id="97202-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="97202-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="97202-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-163">Текстовые файлы (\*.txt; \*.csv; \* .tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="97202-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="97202-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="97202-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-166">Текстовые файлы (\*.txt; \*.csv; \* .tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="97202-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="97202-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="97202-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-169">01</span><span class="sxs-lookup"><span data-stu-id="97202-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="97202-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="97202-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-172">01</span><span class="sxs-lookup"><span data-stu-id="97202-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="97202-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="97202-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="97202-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="97202-175">2</span><span class="sxs-lookup"><span data-stu-id="97202-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="97202-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="97202-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-178">00</span><span class="sxs-lookup"><span data-stu-id="97202-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="97202-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="97202-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-181">00</span><span class="sxs-lookup"><span data-stu-id="97202-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="97202-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="97202-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-184">Импорт данных из внешнего файла в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="97202-184">Import data from the external file into the current database.</span></span> <span data-ttu-id="97202-185">Изменение данных в текущей базе данных остаются без изменений данных во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="97202-185">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="97202-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="97202-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-188">Создайте таблицу в текущей базе данных, которая связана с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="97202-188">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="97202-189">Изменение данных в текущей базе данных будет изменять данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="97202-189">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="97202-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="97202-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-192">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="97202-192">Export data from the current database into a text file.</span></span> <span data-ttu-id="97202-193">В этом будут перезаписаны данные при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="97202-193">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="97202-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="97202-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-196">01</span><span class="sxs-lookup"><span data-stu-id="97202-196">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="97202-197">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="97202-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span></P>



## <a name="html-import-isam-formats"></a><span data-ttu-id="97202-198">Форматы ISAM импорта HTML</span><span class="sxs-lookup"><span data-stu-id="97202-198">HTML Import ISAM Formats</span></span>

<span data-ttu-id="97202-199">**Модуль подключения к Access\\ISAM Formats\\импорта HTML** папка содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="97202-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97202-200">Имя записи</span><span class="sxs-lookup"><span data-stu-id="97202-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="97202-201">Тип</span><span class="sxs-lookup"><span data-stu-id="97202-201">Type</span></span></p></th>
<th><p><span data-ttu-id="97202-202">Значение</span><span class="sxs-lookup"><span data-stu-id="97202-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97202-203">Модуль</span><span class="sxs-lookup"><span data-stu-id="97202-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="97202-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-205">Текст</span><span class="sxs-lookup"><span data-stu-id="97202-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="97202-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="97202-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-208">HTML-файлы (*.ht*)</span><span class="sxs-lookup"><span data-stu-id="97202-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="97202-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="97202-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-211">01</span><span class="sxs-lookup"><span data-stu-id="97202-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="97202-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="97202-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-214">00</span><span class="sxs-lookup"><span data-stu-id="97202-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="97202-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="97202-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="97202-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="97202-217">2</span><span class="sxs-lookup"><span data-stu-id="97202-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="97202-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="97202-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-220">00</span><span class="sxs-lookup"><span data-stu-id="97202-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="97202-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="97202-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-223">00</span><span class="sxs-lookup"><span data-stu-id="97202-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="97202-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="97202-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-226">Импорт данных из внешнего файла в текущей базе данных.</span><span class="sxs-lookup"><span data-stu-id="97202-226">Import data from the external file into the current database.</span></span> <span data-ttu-id="97202-227">Изменение данных в текущей базе данных остаются без изменений данных во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="97202-227">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="97202-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="97202-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-230">Создайте таблицу в текущей базе данных, которая связана с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="97202-230">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="97202-231">Изменение данных в текущей базе данных будет изменять данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="97202-231">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="97202-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="97202-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-234">01</span><span class="sxs-lookup"><span data-stu-id="97202-234">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="97202-235">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="97202-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span></P>



## <a name="html-export-isam-formats"></a><span data-ttu-id="97202-236">Форматы ISAM экспорта HTML</span><span class="sxs-lookup"><span data-stu-id="97202-236">HTML Export ISAM Formats</span></span>

<span data-ttu-id="97202-237">**Модуль подключения к Access\\ISAM Formats\\экспорта HTML** папка содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="97202-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97202-238">Имя записи</span><span class="sxs-lookup"><span data-stu-id="97202-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="97202-239">Тип</span><span class="sxs-lookup"><span data-stu-id="97202-239">Type</span></span></p></th>
<th><p><span data-ttu-id="97202-240">Значение</span><span class="sxs-lookup"><span data-stu-id="97202-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97202-241">Модуль</span><span class="sxs-lookup"><span data-stu-id="97202-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="97202-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-243">Текст</span><span class="sxs-lookup"><span data-stu-id="97202-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="97202-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="97202-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-246">HTML-файлы (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="97202-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="97202-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="97202-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-249">00</span><span class="sxs-lookup"><span data-stu-id="97202-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="97202-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="97202-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-252">01</span><span class="sxs-lookup"><span data-stu-id="97202-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="97202-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="97202-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="97202-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="97202-255">2</span><span class="sxs-lookup"><span data-stu-id="97202-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="97202-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="97202-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-258">00</span><span class="sxs-lookup"><span data-stu-id="97202-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="97202-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="97202-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-261">00</span><span class="sxs-lookup"><span data-stu-id="97202-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="97202-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="97202-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="97202-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="97202-264">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="97202-264">Export data from the current database into a text file.</span></span> <span data-ttu-id="97202-265">В этом будут перезаписаны данные при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="97202-265">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="97202-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="97202-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="97202-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="97202-268">01</span><span class="sxs-lookup"><span data-stu-id="97202-268">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <P><span data-ttu-id="97202-269">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="97202-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span></P>



## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="97202-270">Настройка файла Schema.ini для текста и данных HTML</span><span class="sxs-lookup"><span data-stu-id="97202-270">Customizing the Schema.ini File for Text and HTML Data</span></span>

<span data-ttu-id="97202-271">Для чтения, импорта, или экспорта текстовых данных и данных HTML, необходимо создать файл Schema.ini Кроме включения сведений Text ISAM в INI-файле.</span><span class="sxs-lookup"><span data-stu-id="97202-271">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file.</span></span> <span data-ttu-id="97202-272">Этот файл содержит особенности источника данных: формат текстового файла, как она считывается во время импорта и экспорта формат по умолчанию — для файлов.</span><span class="sxs-lookup"><span data-stu-id="97202-272">Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files.</span></span> <span data-ttu-id="97202-273">В следующих примерах показано макета для файла фиксированной ширины Filename.txt:</span><span class="sxs-lookup"><span data-stu-id="97202-273">The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

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

<span data-ttu-id="97202-274">Аналогично формат для файла с разделителями задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="97202-274">Similarly, the format for a delimited file is specified as follows:</span></span>

```text
    [Delimit.txt] 
    
    ColNameHeader=True 
    
    Format=Delimited() 
    
    MaxScanRows=0 
    
    CharacterSet=OEM 
    
    Col1=username char width 50 
    
    Col2=dateofbirth Date width 9
```

<span data-ttu-id="97202-275">Если данные экспортируются в файл с разделителями, укажите формат для этого файла:</span><span class="sxs-lookup"><span data-stu-id="97202-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

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

В примере Мой Экспорт относится к определенным экспорте; можно указать любые изменения параметров экспорта во время подключения. Этот пример также соответствует имени источника данных (DSN), который может быть передан при необходимости во время подключения. <span data-ttu-id="97202-278">Все три раздела может быть включен в одном INI-файла.</span><span class="sxs-lookup"><span data-stu-id="97202-278">All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="97202-279">Ядро базы данных Microsoft Access использует записи Schema.ini следующим образом.</span><span class="sxs-lookup"><span data-stu-id="97202-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="97202-280">Запись</span><span class="sxs-lookup"><span data-stu-id="97202-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="97202-281">Описание</span><span class="sxs-lookup"><span data-stu-id="97202-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="97202-282">ColNameHeader</span><span class="sxs-lookup"><span data-stu-id="97202-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="97202-283">Может быть присвоено значение <strong>True</strong> (это означает, что первая запись данных задает имена столбцов) или <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="97202-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-284">Format</span><span class="sxs-lookup"><span data-stu-id="97202-284">Format</span></span></p></td>
<td><p><span data-ttu-id="97202-285">Может быть установлено одно из следующих значений: TabDelimited, CSVDelimited, с разделителями (&lt;отдельный знак&gt;), или FixedLength.</span><span class="sxs-lookup"><span data-stu-id="97202-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="97202-286">Разделитель, указанный для формата файла с разделителями может быть любой отдельный знак, за исключением двойные кавычки (&quot;).</span><span class="sxs-lookup"><span data-stu-id="97202-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-287">FixedFormat</span><span class="sxs-lookup"><span data-stu-id="97202-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="97202-288">Только для использования при FixedLength имеет формат, это может быть установлено одно из следующих значений: значение RaggedEdge или TrueFixedLength.</span><span class="sxs-lookup"><span data-stu-id="97202-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="97202-289">Значение RaggedEdge позволяет прерывать символом возврата каретки строки.</span><span class="sxs-lookup"><span data-stu-id="97202-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="97202-290">Значение TrueFixedLength каждую строку, чтобы быть точное количество символов и знаков возврата каретки не в конце строки предполагается, что внедрены в поле.</span><span class="sxs-lookup"><span data-stu-id="97202-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="97202-291">Если этот параметр не указан, значением по умолчанию является значение RaggedEdge.</span><span class="sxs-lookup"><span data-stu-id="97202-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="97202-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="97202-293">Указывает число строк, просматриваемых при распознавании в столбце типов данных.</span><span class="sxs-lookup"><span data-stu-id="97202-293">Indicates the number of rows to be scanned when guessing the column data types.</span></span> <span data-ttu-id="97202-294">Если это имеет значение 0, выполняется весь файл.</span><span class="sxs-lookup"><span data-stu-id="97202-294">If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-295">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="97202-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="97202-296">Можно задать OEM, ANSI, UNICODE или десятичное число допустимый код страницы и указывает набор знаков исходного файла.</span><span class="sxs-lookup"><span data-stu-id="97202-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="97202-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="97202-298">Можно задать строку формата даты и времени.</span><span class="sxs-lookup"><span data-stu-id="97202-298">Can be set to a format string indicating dates and times.</span></span> <span data-ttu-id="97202-299">Если все поля даты/времени в тот же формат обрабатываются импорта и экспорта должны быть указаны в этой записи.</span><span class="sxs-lookup"><span data-stu-id="97202-299">This entry should be specified if all date/time fields in the import/export are handled with the same format.</span></span> <span data-ttu-id="97202-300">Поддерживаются все форматы ядра базы данных Microsoft Jet за исключением AM и PM.</span><span class="sxs-lookup"><span data-stu-id="97202-300">All of the Microsoft Jet database engine formats except AM and PM are supported.</span></span> <span data-ttu-id="97202-301">В случае отсутствия строку формата используются параметры изображения и время краткий формат даты панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="97202-301">In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="97202-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="97202-303">Указывает символ валюты, которое будет использоваться для денежных значений в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="97202-303">Indicates the currency symbol to be used for currency values in the text file.</span></span> <span data-ttu-id="97202-304">Примеры включают доллара ($) и интеллектуальный анализ данных.</span><span class="sxs-lookup"><span data-stu-id="97202-304">Examples include the dollar sign ($) and Dm.</span></span> <span data-ttu-id="97202-305">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="97202-305">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="97202-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="97202-307">Может быть установлено любое из следующих значений: символ денежной единицы перед без пробела ($1) суффикс символ валюты без пробела (1$) символ денежной единицы перед суффикс символ валюты один символ пробела ($ 1) с одним пробелом (1 $) Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="97202-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="97202-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="97202-309">Указывает количество знаков, используемых для дробной части денежной суммы.</span><span class="sxs-lookup"><span data-stu-id="97202-309">Specifies the number of digits used for the fractional part of a currency amount.</span></span> <span data-ttu-id="97202-310">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="97202-310">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="97202-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="97202-312">Может иметь одно из следующих значений: (1) — $1 $– 1 $1 — (1$) -1$ $ 1 – $ 1 – – 1 $ – $ 1 1 – $ 1 – $ 1-1 – $ ($ 1) (1 $) знак доллара отображается для этого примера, но оно должно быть заменено соответствующим значением качестве в самой программы.</span><span class="sxs-lookup"><span data-stu-id="97202-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="97202-313">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="97202-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="97202-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="97202-315">Символ одного знака, используемый для разделения денежных значений тысячи людей в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="97202-315">Indicates the single-character symbol to be used for separating currency values by thousands in the text file.</span></span> <span data-ttu-id="97202-316">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="97202-316">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="97202-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="97202-318">Можно задать для любой отдельный знак, используемый для разделения целой дробная часть денежной суммы.</span><span class="sxs-lookup"><span data-stu-id="97202-318">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount.</span></span> <span data-ttu-id="97202-319">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="97202-319">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="97202-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="97202-321">Можно задать для любой отдельный знак, используемый для отделения целое число от дробная часть числа.</span><span class="sxs-lookup"><span data-stu-id="97202-321">Can be set to any single character that is used to separate the integer from the fractional part of a number.</span></span> <span data-ttu-id="97202-322">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="97202-322">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="97202-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="97202-324">Указывает число десятичных знаков в дробной части числа.</span><span class="sxs-lookup"><span data-stu-id="97202-324">Indicates the number of decimal digits in the fractional portion of a number.</span></span> <span data-ttu-id="97202-325">Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="97202-325">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="97202-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="97202-327">Определяет, содержат ли десятичное значение меньше 1 и больше -1 нулей; Это значение может быть False (отсутствие нуля) или True.</span><span class="sxs-lookup"><span data-stu-id="97202-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="97202-328">Столбец1 Col2...</span><span class="sxs-lookup"><span data-stu-id="97202-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="97202-329">Список столбцов в текстовый файл для чтения.</span><span class="sxs-lookup"><span data-stu-id="97202-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="97202-330">Формат этой записи должны быть: <em>Coln</em>=<em>columnName</em> тип [Width <em> #</em>] <em>columnName</em>: имена столбцов с внедренным пробелов должно заключаться в кавычки.</span><span class="sxs-lookup"><span data-stu-id="97202-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="97202-331"><em>Тип</em>: бит, Byte, Short, Long, знаков после запятой, Currency, Single, Double, даты и времени.</span><span class="sxs-lookup"><span data-stu-id="97202-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="97202-332">Двоичный OLE, текст или заметка.</span><span class="sxs-lookup"><span data-stu-id="97202-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="97202-333">Кроме того, поддерживаются следующие типы текстовых драйверов ODBC: символ (то же, как текст) с плавающей запятой (то же, что Double) Integer (то же, что Short) LongChar (то же, что Memo) даты <em>формата даты</em> в случае типа Memo может быть маркер дополнительные формат [атрибут гиперссылка] используется для указания столбцов, которые должны быть активные URL-адреса в Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="97202-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="97202-334">В случае тип Decimal введите дополнительные формат маркеры [масштабировать #] точности #] следует использовать.</span><span class="sxs-lookup"><span data-stu-id="97202-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="97202-335">TextDelimiter</span><span class="sxs-lookup"><span data-stu-id="97202-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="97202-336">Можно задать для любой отдельный знак, используемый для выделения строки, содержащие любое из специальных символов.</span><span class="sxs-lookup"><span data-stu-id="97202-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="97202-337">Пример:</span><span class="sxs-lookup"><span data-stu-id="97202-337">E.g.</span></span> <span data-ttu-id="97202-338">&quot;ABC&quot;,&quot;xyz, компании pqr&quot;,&quot;hij&quot; при этом нет разделителем по умолчанию является двойные кавычки.</span><span class="sxs-lookup"><span data-stu-id="97202-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="97202-339">Если эта запись — это строка &quot;нет&quot; затем символы не будут рассматриваться в качестве разделителей.</span><span class="sxs-lookup"><span data-stu-id="97202-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="97202-340">При изменении параметров файла Schema.ini необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="97202-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


