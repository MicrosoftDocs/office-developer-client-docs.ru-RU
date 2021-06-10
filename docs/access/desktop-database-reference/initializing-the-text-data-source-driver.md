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
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="2d31e-102">Инициализация драйвера источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="2d31e-102">Initializing the Text Data Source driver</span></span>

<span data-ttu-id="2d31e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d31e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d31e-104">Один и тот же драйвер базы данных используется как для источников текстовых данных, так и для HTML-источников данных.</span><span class="sxs-lookup"><span data-stu-id="2d31e-104">The same database driver is used for both text data sources and for HTML data sources.</span></span>

<span data-ttu-id="2d31e-105">При установке драйвера базы данных Text Data Source программа установки записывает набор значений по умолчанию в реестр Microsoft Windows в подкайлах Engines и ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="2d31e-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="2d31e-106">Не следует изменять эти параметры напрямую; используйте программу установки для приложения, чтобы добавить, удалить или изменить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="2d31e-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="2d31e-107">В следующих разделах описываются параметры инициализации и формата ISAM для драйвера базы данных Text Data Source.</span><span class="sxs-lookup"><span data-stu-id="2d31e-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="2d31e-108">Параметры инициализации источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="2d31e-108">Text data source initialization settings</span></span>

<span data-ttu-id="2d31e-109">Текстовая папка **Access Connectivity Engine \\ ISAM \\ Formats** включает параметры инициализации драйвера Acetxt.dll, используемой для внешнего доступа к текстовым файлам данных.</span><span class="sxs-lookup"><span data-stu-id="2d31e-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="2d31e-110">Типичные параметры для записей в этой папке показаны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="2d31e-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

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

<span data-ttu-id="2d31e-111">В движке базы данных Microsoft Access используются записи текстовых папок следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2d31e-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d31e-112">Запись</span><span class="sxs-lookup"><span data-stu-id="2d31e-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="2d31e-113">Description</span><span class="sxs-lookup"><span data-stu-id="2d31e-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-114">win32</span><span class="sxs-lookup"><span data-stu-id="2d31e-114">win32</span></span></p></td>
<td><p><span data-ttu-id="2d31e-115">Расположение Acetxt.dll.</span><span class="sxs-lookup"><span data-stu-id="2d31e-115">The location of Acetxt.dll.</span></span> <span data-ttu-id="2d31e-116">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="2d31e-116">The full path is determined at the time of installation.</span></span> <span data-ttu-id="2d31e-117">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="2d31e-117">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-118">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="2d31e-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="2d31e-119">Количество строк, которые необходимо отсканировать при угадывке типов столбцов.</span><span class="sxs-lookup"><span data-stu-id="2d31e-119">The number of rows to be scanned when guessing the column types.</span></span> <span data-ttu-id="2d31e-120">Если установлено 0, весь файл будет искаться.</span><span class="sxs-lookup"><span data-stu-id="2d31e-120">If set to 0, the entire file will be searched.</span></span> <span data-ttu-id="2d31e-121">По умолчанию — 25.</span><span class="sxs-lookup"><span data-stu-id="2d31e-121">The default is 25.</span></span> <span data-ttu-id="2d31e-122">Значения имеют тип REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="2d31e-122">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-123">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="2d31e-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="2d31e-124">Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="2d31e-124">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="2d31e-125">Значение 01 указывает, что во время импорта из первой строки будут взяты имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="2d31e-125">A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-126">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="2d31e-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="2d31e-127">Индикатор хранения текстовых страниц.</span><span class="sxs-lookup"><span data-stu-id="2d31e-127">An indicator of how text pages are stored.</span></span> <span data-ttu-id="2d31e-128">Возможные параметры:</span><span class="sxs-lookup"><span data-stu-id="2d31e-128">Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="2d31e-129">ANSI — страница кода ANSI компьютера.</span><span class="sxs-lookup"><span data-stu-id="2d31e-129">ANSI — The ANSI code page of the machine.</span></span> <span data-ttu-id="2d31e-130">Преобразования AnsiToUnicode и UnicodeToAnsi сделаны.</span><span class="sxs-lookup"><span data-stu-id="2d31e-130">AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="2d31e-131">OEM — страница кода OEM машины.</span><span class="sxs-lookup"><span data-stu-id="2d31e-131">OEM — The OEM code page of the machine.</span></span> <span data-ttu-id="2d31e-132">Преобразования OemToUnicode и UnicodeToOem сделаны.</span><span class="sxs-lookup"><span data-stu-id="2d31e-132">OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="2d31e-133">Unicode — преобразования кода не были сделаны.</span><span class="sxs-lookup"><span data-stu-id="2d31e-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="2d31e-134">&lt;десятичной номер &gt; — номер страницы кода определенного набора символов.</span><span class="sxs-lookup"><span data-stu-id="2d31e-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="2d31e-135">Преобразования в Юникод и из него будут сделаны.</span><span class="sxs-lookup"><span data-stu-id="2d31e-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="2d31e-136">По умолчанию — ANSI.</span><span class="sxs-lookup"><span data-stu-id="2d31e-136">The default is ANSI.</span></span> <span data-ttu-id="2d31e-137">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="2d31e-137">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-138">Формат</span><span class="sxs-lookup"><span data-stu-id="2d31e-138">Format</span></span></p></td>
<td><p><span data-ttu-id="2d31e-139">Может быть любой из следующих: TabDelimited, CSVDelimited, Delimited &lt; (один &gt; символ).</span><span class="sxs-lookup"><span data-stu-id="2d31e-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="2d31e-140">Делимитер с одним персонажем в формате Delimited может быть любым одним персонажем, за исключением двойной кавычка ( &quot; ).</span><span class="sxs-lookup"><span data-stu-id="2d31e-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="2d31e-141">По умолчанию CSVDelimited.</span><span class="sxs-lookup"><span data-stu-id="2d31e-141">The default is CSVDelimited.</span></span> <span data-ttu-id="2d31e-142">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="2d31e-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-143">Расширения</span><span class="sxs-lookup"><span data-stu-id="2d31e-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="2d31e-144">Расширение любых файлов, которые необходимо просмотреть при поиске текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="2d31e-144">The extension of any files to be browsed when looking for text-based data.</span></span> <span data-ttu-id="2d31e-145">По умолчанию это txt, csv, tab, asc.</span><span class="sxs-lookup"><span data-stu-id="2d31e-145">The default is txt, csv, tab, asc.</span></span> <span data-ttu-id="2d31e-146">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="2d31e-146">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-147">ExportCurrencySymbols</span><span class="sxs-lookup"><span data-stu-id="2d31e-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="2d31e-148">Двоичное значение, которое указывает, включен ли соответствующий символ валюты при экспорте валютных полей.</span><span class="sxs-lookup"><span data-stu-id="2d31e-148">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported.</span></span> <span data-ttu-id="2d31e-149">Значение 01 указывает, что символ включен.</span><span class="sxs-lookup"><span data-stu-id="2d31e-149">A value of 01 indicates that the symbol is included.</span></span> <span data-ttu-id="2d31e-150">Значение 00 указывает, что экспортируются только числовая информация.</span><span class="sxs-lookup"><span data-stu-id="2d31e-150">A value of 00 indicates that only the numeric data is exported.</span></span> <span data-ttu-id="2d31e-151">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="2d31e-151">The default is 01.</span></span> <span data-ttu-id="2d31e-152">Значения имеют тип REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="2d31e-152">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="2d31e-153">Форматы ISAM источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="2d31e-153">Text data source ISAM formats</span></span>

<span data-ttu-id="2d31e-154">**Текстовая папка \\ IsAM \\ Formats IsAM Engine Access Connectivity Engine** содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="2d31e-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d31e-155">Имя входа</span><span class="sxs-lookup"><span data-stu-id="2d31e-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="2d31e-156">Тип</span><span class="sxs-lookup"><span data-stu-id="2d31e-156">Type</span></span></p></th>
<th><p><span data-ttu-id="2d31e-157">Значение</span><span class="sxs-lookup"><span data-stu-id="2d31e-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-158">Двигатель</span><span class="sxs-lookup"><span data-stu-id="2d31e-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="2d31e-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-160">Текст</span><span class="sxs-lookup"><span data-stu-id="2d31e-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-161">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="2d31e-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="2d31e-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-163">Текстовые файлы (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="2d31e-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-164">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="2d31e-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="2d31e-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-166">Текстовые файлы (\*.txt; \*.csv; \*.tab; \*.asc)</span><span class="sxs-lookup"><span data-stu-id="2d31e-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-167">CanLink</span><span class="sxs-lookup"><span data-stu-id="2d31e-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="2d31e-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-169">01</span><span class="sxs-lookup"><span data-stu-id="2d31e-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-170">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="2d31e-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="2d31e-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-172">01</span><span class="sxs-lookup"><span data-stu-id="2d31e-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-173">IsamType</span><span class="sxs-lookup"><span data-stu-id="2d31e-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="2d31e-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2d31e-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="2d31e-175">2</span><span class="sxs-lookup"><span data-stu-id="2d31e-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-176">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="2d31e-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="2d31e-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-178">00</span><span class="sxs-lookup"><span data-stu-id="2d31e-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-179">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="2d31e-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="2d31e-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-181">00</span><span class="sxs-lookup"><span data-stu-id="2d31e-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-182">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="2d31e-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="2d31e-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-184">Импорт данных из внешнего файла в текущую базу данных.</span><span class="sxs-lookup"><span data-stu-id="2d31e-184">Import data from the external file into the current database.</span></span> <span data-ttu-id="2d31e-185">Изменение данных в текущей базе данных не изменит данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="2d31e-185">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-186">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="2d31e-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="2d31e-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-188">Создание таблицы в текущей базе данных, связанной с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="2d31e-188">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="2d31e-189">Изменение данных в текущей базе данных изменит данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="2d31e-189">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-190">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="2d31e-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="2d31e-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-192">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="2d31e-192">Export data from the current database into a text file.</span></span> <span data-ttu-id="2d31e-193">Этот процесс переопишет данные, если они будут экспортироваться в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="2d31e-193">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-194">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="2d31e-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="2d31e-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-196">01</span><span class="sxs-lookup"><span data-stu-id="2d31e-196">01</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="2d31e-197">При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="2d31e-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-import-isam-formats"></a><span data-ttu-id="2d31e-198">Форматы HTML-импорта ISAM</span><span class="sxs-lookup"><span data-stu-id="2d31e-198">HTML import ISAM formats</span></span>

<span data-ttu-id="2d31e-199">Папка **\\ \\ HTML Import в** движке ISAM Для подключения к системе подключения к доступу содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="2d31e-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d31e-200">Имя входа</span><span class="sxs-lookup"><span data-stu-id="2d31e-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="2d31e-201">Тип</span><span class="sxs-lookup"><span data-stu-id="2d31e-201">Type</span></span></p></th>
<th><p><span data-ttu-id="2d31e-202">Значение</span><span class="sxs-lookup"><span data-stu-id="2d31e-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-203">Двигатель</span><span class="sxs-lookup"><span data-stu-id="2d31e-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="2d31e-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-205">Текст</span><span class="sxs-lookup"><span data-stu-id="2d31e-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-206">ImportFilter</span><span class="sxs-lookup"><span data-stu-id="2d31e-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="2d31e-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-208">HTML Files *(.ht)*</span><span class="sxs-lookup"><span data-stu-id="2d31e-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-209">CanLink</span><span class="sxs-lookup"><span data-stu-id="2d31e-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="2d31e-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-211">01</span><span class="sxs-lookup"><span data-stu-id="2d31e-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-212">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="2d31e-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="2d31e-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-214">00</span><span class="sxs-lookup"><span data-stu-id="2d31e-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-215">IsamType</span><span class="sxs-lookup"><span data-stu-id="2d31e-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="2d31e-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2d31e-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="2d31e-217">2</span><span class="sxs-lookup"><span data-stu-id="2d31e-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-218">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="2d31e-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="2d31e-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-220">00</span><span class="sxs-lookup"><span data-stu-id="2d31e-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-221">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="2d31e-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="2d31e-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-223">00</span><span class="sxs-lookup"><span data-stu-id="2d31e-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-224">ResultTextImport</span><span class="sxs-lookup"><span data-stu-id="2d31e-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="2d31e-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-226">Импорт данных из внешнего файла в текущую базу данных.</span><span class="sxs-lookup"><span data-stu-id="2d31e-226">Import data from the external file into the current database.</span></span> <span data-ttu-id="2d31e-227">Изменение данных в текущей базе данных не изменит данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="2d31e-227">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-228">ResultTextLink</span><span class="sxs-lookup"><span data-stu-id="2d31e-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="2d31e-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-230">Создание таблицы в текущей базе данных, связанной с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="2d31e-230">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="2d31e-231">Изменение данных в текущей базе данных изменит данные во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="2d31e-231">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-232">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="2d31e-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="2d31e-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-234">01</span><span class="sxs-lookup"><span data-stu-id="2d31e-234">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2d31e-235">При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="2d31e-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-export-isam-formats"></a><span data-ttu-id="2d31e-236">Форматы HTML-экспорта ISAM</span><span class="sxs-lookup"><span data-stu-id="2d31e-236">HTML export ISAM formats</span></span>

<span data-ttu-id="2d31e-237">Папка **\\ \\ HTML Export в** движке ISAM Engine ISAM Для подключения к доступу содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="2d31e-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d31e-238">Имя входа</span><span class="sxs-lookup"><span data-stu-id="2d31e-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="2d31e-239">Тип</span><span class="sxs-lookup"><span data-stu-id="2d31e-239">Type</span></span></p></th>
<th><p><span data-ttu-id="2d31e-240">Значение</span><span class="sxs-lookup"><span data-stu-id="2d31e-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-241">Двигатель</span><span class="sxs-lookup"><span data-stu-id="2d31e-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="2d31e-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-243">Текст</span><span class="sxs-lookup"><span data-stu-id="2d31e-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-244">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="2d31e-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="2d31e-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-246">HTML-файлы (\*.htm)</span><span class="sxs-lookup"><span data-stu-id="2d31e-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-247">CanLink</span><span class="sxs-lookup"><span data-stu-id="2d31e-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="2d31e-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-249">00</span><span class="sxs-lookup"><span data-stu-id="2d31e-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-250">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="2d31e-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="2d31e-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-252">01</span><span class="sxs-lookup"><span data-stu-id="2d31e-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-253">IsamType</span><span class="sxs-lookup"><span data-stu-id="2d31e-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="2d31e-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="2d31e-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="2d31e-255">2</span><span class="sxs-lookup"><span data-stu-id="2d31e-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-256">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="2d31e-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="2d31e-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-258">00</span><span class="sxs-lookup"><span data-stu-id="2d31e-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-259">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="2d31e-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="2d31e-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-261">00</span><span class="sxs-lookup"><span data-stu-id="2d31e-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-262">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="2d31e-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="2d31e-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="2d31e-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="2d31e-264">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="2d31e-264">Export data from the current database into a text file.</span></span> <span data-ttu-id="2d31e-265">Этот процесс переопишет данные, если они будут экспортироваться в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="2d31e-265">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-266">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="2d31e-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="2d31e-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="2d31e-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="2d31e-268">01</span><span class="sxs-lookup"><span data-stu-id="2d31e-268">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2d31e-269">При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="2d31e-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="2d31e-270">Настройка файла Schema.ini для текстовых и HTML-данных</span><span class="sxs-lookup"><span data-stu-id="2d31e-270">Customizing the Schema.ini file for text and HTML data</span></span>

<span data-ttu-id="2d31e-271">Чтобы читать, импортировать или экспортировать текстовые и HTML-данные, необходимо создать файл Schema.ini, а также включив в него сведения об ISAM text .ini файле.</span><span class="sxs-lookup"><span data-stu-id="2d31e-271">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file.</span></span> <span data-ttu-id="2d31e-272">Schema.ini содержит особенности источника данных: форматирование текстового файла, его чтение во время импорта и формат экспорта по умолчанию для файлов.</span><span class="sxs-lookup"><span data-stu-id="2d31e-272">Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files.</span></span> <span data-ttu-id="2d31e-273">В следующих примерах покажите макет файла с фиксированной шириной, Filename.txt:</span><span class="sxs-lookup"><span data-stu-id="2d31e-273">The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

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

<span data-ttu-id="2d31e-274">Кроме того, формат делимитного файла указывается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2d31e-274">Similarly, the format for a delimited file is specified as follows:</span></span>

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

<span data-ttu-id="2d31e-275">Если вы экспортируете данные в делимитированный текстовый файл, укажите формат этого файла:</span><span class="sxs-lookup"><span data-stu-id="2d31e-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

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

Пример "Мой специальный экспорт" относится к определенному варианту экспорта; вы можете указать любые варианты экспорта во время подключения. <span data-ttu-id="2d31e-277">Этот последний пример также соответствует имени источника данных (DSN), которое может быть дополнительно передано во время подключения.</span><span class="sxs-lookup"><span data-stu-id="2d31e-277">This last example also corresponds to a data source name (DSN) that can be optionally passed at connect time.</span></span> <span data-ttu-id="2d31e-278">Все три раздела формата могут быть включены в один .ini файл.</span><span class="sxs-lookup"><span data-stu-id="2d31e-278">All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="2d31e-279">Движок базы данных Microsoft Access использует Schema.ini записей следующим образом.</span><span class="sxs-lookup"><span data-stu-id="2d31e-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d31e-280">Запись</span><span class="sxs-lookup"><span data-stu-id="2d31e-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="2d31e-281">Description</span><span class="sxs-lookup"><span data-stu-id="2d31e-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-282">ColNameHeader</span><span class="sxs-lookup"><span data-stu-id="2d31e-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="2d31e-283">Можно установить как <strong>True</strong> (указывая, что первая запись данных указывает имена столбцов), так и <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="2d31e-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-284">Формат</span><span class="sxs-lookup"><span data-stu-id="2d31e-284">Format</span></span></p></td>
<td><p><span data-ttu-id="2d31e-285">Можно установить одно из следующих значений: TabDelimited, CSVDelimited, Delimited &lt; (один символ) или &gt; FixedLength.</span><span class="sxs-lookup"><span data-stu-id="2d31e-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="2d31e-286">Делимитер, указанный для формата делимитированный файл, может быть любым одним персонажем, за исключением двойной кавычка ( &quot; ).</span><span class="sxs-lookup"><span data-stu-id="2d31e-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-287">FixedFormat</span><span class="sxs-lookup"><span data-stu-id="2d31e-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="2d31e-288">Только если формат fixedLength, его можно установить к одному из следующих значений: RaggedEdGe или TrueFixedLength.</span><span class="sxs-lookup"><span data-stu-id="2d31e-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="2d31e-289">RaggedEdge позволяет прекращать строки с помощью символа Carriage Return.</span><span class="sxs-lookup"><span data-stu-id="2d31e-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="2d31e-290">TrueFixedLength требует, чтобы каждая строка была точным числом символов, и предполагается, что любые символы возвращения кареты, не на границе строки, будут встроены в поле.</span><span class="sxs-lookup"><span data-stu-id="2d31e-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="2d31e-291">Если этого параметра нет, по умолчанию значение RaggedEdge.</span><span class="sxs-lookup"><span data-stu-id="2d31e-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-292">MaxScanRows</span><span class="sxs-lookup"><span data-stu-id="2d31e-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="2d31e-293">Указывает количество строк, которые необходимо отсканировать при угадывке типов данных столбцов.</span><span class="sxs-lookup"><span data-stu-id="2d31e-293">Indicates the number of rows to be scanned when guessing the column data types.</span></span> <span data-ttu-id="2d31e-294">Если это установлено до 0, весь файл будет искаться.</span><span class="sxs-lookup"><span data-stu-id="2d31e-294">If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-295">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="2d31e-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="2d31e-296">Можно установить OEM, ANSI, UNICODE или десятичной номер допустимой страницы кода и указать набор символов исходных файлов.</span><span class="sxs-lookup"><span data-stu-id="2d31e-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-297">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="2d31e-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="2d31e-298">Можно установить строку формата, указывающее даты и время.</span><span class="sxs-lookup"><span data-stu-id="2d31e-298">Can be set to a format string indicating dates and times.</span></span> <span data-ttu-id="2d31e-299">Эта запись должна быть указана, если все поля даты и времени в импорте/экспорте обрабатываются в одном формате.</span><span class="sxs-lookup"><span data-stu-id="2d31e-299">This entry should be specified if all date/time fields in the import/export are handled with the same format.</span></span> <span data-ttu-id="2d31e-300">Поддерживаются все форматы двигателей базы данных Microsoft Jet, кроме AM и PM.</span><span class="sxs-lookup"><span data-stu-id="2d31e-300">All of the Microsoft Jet database engine formats except AM and PM are supported.</span></span> <span data-ttu-id="2d31e-301">При отсутствии строки формата используется Windows панели управления краткое изображение даты и параметры времени.</span><span class="sxs-lookup"><span data-stu-id="2d31e-301">In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="2d31e-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="2d31e-303">Указывает символ валюты, который будет использоваться для значений валюты в текстовом файле.</span><span class="sxs-lookup"><span data-stu-id="2d31e-303">Indicates the currency symbol to be used for currency values in the text file.</span></span> <span data-ttu-id="2d31e-304">Примеры включают знак доллара ($) и dm.</span><span class="sxs-lookup"><span data-stu-id="2d31e-304">Examples include the dollar sign ($) and Dm.</span></span> <span data-ttu-id="2d31e-305">Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</span><span class="sxs-lookup"><span data-stu-id="2d31e-305">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-306">CurrencyPosFormat</span><span class="sxs-lookup"><span data-stu-id="2d31e-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="2d31e-307">Можно установить любое из следующих значений: префикс символа валюты без разделения ($1) Суффикс символа валюты без префикса символа разделения (1$) с суффиксом символа разделения символа ($ 1) с разделением одного символа (1 $) Если эта запись отсутствует, используется значение по умолчанию в панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="2d31e-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="2d31e-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="2d31e-309">Указывает количество цифр, используемых для дробной части суммы валюты.</span><span class="sxs-lookup"><span data-stu-id="2d31e-309">Specifies the number of digits used for the fractional part of a currency amount.</span></span> <span data-ttu-id="2d31e-310">Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</span><span class="sxs-lookup"><span data-stu-id="2d31e-310">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-311">CurrencyNegFormat</span><span class="sxs-lookup"><span data-stu-id="2d31e-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="2d31e-312">Может быть одним из следующих значений: ($1) -$1 $-1 $1 - (1$) -1$1-$ 1$- -1 $-1 $- $1 - $1 - $1 - $1 ($1) Знак доллара показан для целей этого примера, но его следует заменить соответствующим значением CurrencySymbol в фактической программе.</span><span class="sxs-lookup"><span data-stu-id="2d31e-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="2d31e-313">Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</span><span class="sxs-lookup"><span data-stu-id="2d31e-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-314">CurrencyThousandSymbol</span><span class="sxs-lookup"><span data-stu-id="2d31e-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="2d31e-315">Указывает символ одного символа, который используется для разделения значений валюты на тысячи в текстовом файле.</span><span class="sxs-lookup"><span data-stu-id="2d31e-315">Indicates the single-character symbol to be used for separating currency values by thousands in the text file.</span></span> <span data-ttu-id="2d31e-316">Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</span><span class="sxs-lookup"><span data-stu-id="2d31e-316">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-317">CurrencyDecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="2d31e-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="2d31e-318">Можно установить для любого отдельного символа, который используется для отделить целое от дробной части суммы валюты.</span><span class="sxs-lookup"><span data-stu-id="2d31e-318">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount.</span></span> <span data-ttu-id="2d31e-319">Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</span><span class="sxs-lookup"><span data-stu-id="2d31e-319">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-320">DecimalSymbol</span><span class="sxs-lookup"><span data-stu-id="2d31e-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="2d31e-321">Можно установить для любого отдельного символа, который используется для отделить целый ряд от дробной части номера.</span><span class="sxs-lookup"><span data-stu-id="2d31e-321">Can be set to any single character that is used to separate the integer from the fractional part of a number.</span></span> <span data-ttu-id="2d31e-322">Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</span><span class="sxs-lookup"><span data-stu-id="2d31e-322">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-323">NumberDigits</span><span class="sxs-lookup"><span data-stu-id="2d31e-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="2d31e-324">Указывает количество десятичных цифр в дробной части номера.</span><span class="sxs-lookup"><span data-stu-id="2d31e-324">Indicates the number of decimal digits in the fractional portion of a number.</span></span> <span data-ttu-id="2d31e-325">Если эта запись отсутствует, используется значение по умолчанию Windows панели управления.</span><span class="sxs-lookup"><span data-stu-id="2d31e-325">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-326">NumberLeadingZeros</span><span class="sxs-lookup"><span data-stu-id="2d31e-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="2d31e-327">Указывает, должно ли десятичная величина меньше 1 и больше -1 содержать ведущие нули; это значение может быть false (без ведущих нулей) или True.</span><span class="sxs-lookup"><span data-stu-id="2d31e-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d31e-328">Col1, Col2, ...</span><span class="sxs-lookup"><span data-stu-id="2d31e-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="2d31e-329">Списки столбцов в текстовом файле для чтения.</span><span class="sxs-lookup"><span data-stu-id="2d31e-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="2d31e-330">Формат этой записи должен быть: <em>тип coln</em> = columnName [Width ]<em>columnName:</em> Имена столбцов со встроенными пробелами должны быть заключены <em>#</em> в кавычках. <em></em></span><span class="sxs-lookup"><span data-stu-id="2d31e-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="2d31e-331"><em>тип:</em>Может быть Бит, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span><span class="sxs-lookup"><span data-stu-id="2d31e-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="2d31e-332">Двоичный, OLE, текст или памятка.</span><span class="sxs-lookup"><span data-stu-id="2d31e-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="2d31e-333">Кроме того, поддерживаются следующие типы текстовых драйверов ODBC: Для указания столбцов, которые должны быть активными URL-адресами в Microsoft Access, поддерживаются следующие типы текстовых драйверов ODBC: Char (такой же, как Text) Float (так же, как и Double) Формат даты LongChar (так же, как и формат Memo). Для указания столбцов, которые должны быть активными URL-адресами в Microsoft Access, можно использовать дополнительный маркер формата. <em></em></span><span class="sxs-lookup"><span data-stu-id="2d31e-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="2d31e-334">В случае десятичных типов необходимо использовать дополнительные маркеры формата [Scale #] Precision #]</span><span class="sxs-lookup"><span data-stu-id="2d31e-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d31e-335">TextDelimiter</span><span class="sxs-lookup"><span data-stu-id="2d31e-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="2d31e-336">Можно установить для любого отдельного символа, используемого для делимитации строк, содержащих любые другие специальные символы.</span><span class="sxs-lookup"><span data-stu-id="2d31e-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="2d31e-337">Например,</span><span class="sxs-lookup"><span data-stu-id="2d31e-337">E.g.</span></span> <span data-ttu-id="2d31e-338">&quot;ABC, &quot; &quot; xyz, pqr, hij Если эта запись не представлена, делимитер по умолчанию &quot; является двойной &quot; &quot; цитатой.</span><span class="sxs-lookup"><span data-stu-id="2d31e-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="2d31e-339">Если эта запись не является &quot; строкой, никакие символы не будут &quot; рассматриваться как делимитеры.</span><span class="sxs-lookup"><span data-stu-id="2d31e-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="2d31e-340">При изменении Schema.ini параметров файла необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="2d31e-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


