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
# <a name="initializing-the-text-data-source-driver"></a><span data-ttu-id="bd15c-102">Инициализация драйвера источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="bd15c-102">Initializing the Text Data Source driver</span></span>

<span data-ttu-id="bd15c-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bd15c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bd15c-104">Один и тот же драйвер базы данных используется как для текстовых источников данных, так и для источников данных HTML.</span><span class="sxs-lookup"><span data-stu-id="bd15c-104">The same database driver is used for both text data sources and for HTML data sources.</span></span>

<span data-ttu-id="bd15c-105">При установке драйвера базы данных для источника текстовых данных программа установки записывает набор значений по умолчанию в реестр Microsoft Windows в подразделах Engines и ISAM formats.</span><span class="sxs-lookup"><span data-stu-id="bd15c-105">When you install the Text Data Source database driver, the Setup program writes a set of default values to the Microsoft Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="bd15c-106">Эти параметры не следует изменять напрямую; Используйте программу установки приложения, чтобы добавлять, удалять или изменять эти параметры.</span><span class="sxs-lookup"><span data-stu-id="bd15c-106">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="bd15c-107">В следующих разделах описываются параметры инициализации и ISAM Format драйвера базы данных для источника текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="bd15c-107">The following sections describe initialization and ISAM Format settings for the Text Data Source database driver.</span></span>

## <a name="text-data-source-initialization-settings"></a><span data-ttu-id="bd15c-108">Параметры инициализации источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="bd15c-108">Text data source initialization settings</span></span>

<span data-ttu-id="bd15c-109">В **папке ISAM formats\\\\подсистемы подключения Access** содержатся параметры инициализации драйвера ацеткст. dll, используемого для внешнего доступа к файлам текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="bd15c-109">The **Access Connectivity Engine\\ISAM Formats\\Text folder** includes initialization settings for the Acetxt.dll driver, used for external access to text data files.</span></span> <span data-ttu-id="bd15c-110">Типичные параметры записей в этой папке показаны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="bd15c-110">Typical settings for the entries in this folder are shown in the following example.</span></span>

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

<span data-ttu-id="bd15c-111">Ядро СУБД Microsoft Access использует записи в папке Text, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="bd15c-111">The Microsoft Access database engine uses the Text folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd15c-112">Введен</span><span class="sxs-lookup"><span data-stu-id="bd15c-112">Entry</span></span></p></th>
<th><p><span data-ttu-id="bd15c-113">Описание</span><span class="sxs-lookup"><span data-stu-id="bd15c-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-114">оригиналь</span><span class="sxs-lookup"><span data-stu-id="bd15c-114">win32</span></span></p></td>
<td><p><span data-ttu-id="bd15c-115">Расположение файла Ацеткст. dll.</span><span class="sxs-lookup"><span data-stu-id="bd15c-115">The location of Acetxt.dll.</span></span> <span data-ttu-id="bd15c-116">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="bd15c-116">The full path is determined at the time of installation.</span></span> <span data-ttu-id="bd15c-117">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bd15c-117">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-118">макссканровс</span><span class="sxs-lookup"><span data-stu-id="bd15c-118">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="bd15c-119">Количество строк, проверяемых при подборе типов столбцов.</span><span class="sxs-lookup"><span data-stu-id="bd15c-119">The number of rows to be scanned when guessing the column types.</span></span> <span data-ttu-id="bd15c-120">Если задано значение 0, поиск выполняется во всем файле.</span><span class="sxs-lookup"><span data-stu-id="bd15c-120">If set to 0, the entire file will be searched.</span></span> <span data-ttu-id="bd15c-121">Значение по умолчанию — 25.</span><span class="sxs-lookup"><span data-stu-id="bd15c-121">The default is 25.</span></span> <span data-ttu-id="bd15c-122">Значения имеют тип REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="bd15c-122">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-123">фирстровхаснамес</span><span class="sxs-lookup"><span data-stu-id="bd15c-123">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="bd15c-124">Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="bd15c-124">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="bd15c-125">Значение 01 указывает, что во время импорта имена столбцов берутся из первой строки.</span><span class="sxs-lookup"><span data-stu-id="bd15c-125">A value of 01 indicates that, during import, column names are taken from the first row.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-126">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="bd15c-126">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="bd15c-127">Индикатор того, как хранятся страницы текста.</span><span class="sxs-lookup"><span data-stu-id="bd15c-127">An indicator of how text pages are stored.</span></span> <span data-ttu-id="bd15c-128">Возможные параметры:</span><span class="sxs-lookup"><span data-stu-id="bd15c-128">Possible settings are:</span></span></p>
<p></p>
<ul>
<li><p><span data-ttu-id="bd15c-129">ANSI — кодовая страница ANSI компьютера.</span><span class="sxs-lookup"><span data-stu-id="bd15c-129">ANSI — The ANSI code page of the machine.</span></span> <span data-ttu-id="bd15c-130">Преобразования Анситауникоде и Уникодетоанси выполнены.</span><span class="sxs-lookup"><span data-stu-id="bd15c-130">AnsiToUnicode and UnicodeToAnsi conversions done.</span></span></p></li>
<li><p><span data-ttu-id="bd15c-131">OEM — кодовая страница OEM компьютера.</span><span class="sxs-lookup"><span data-stu-id="bd15c-131">OEM — The OEM code page of the machine.</span></span> <span data-ttu-id="bd15c-132">Преобразования Оемтауникоде и Уникодетуем выполнены.</span><span class="sxs-lookup"><span data-stu-id="bd15c-132">OemToUnicode and UnicodeToOem conversions done.</span></span></p></li>
<li><p><span data-ttu-id="bd15c-133">Юникод — преобразования кодовой страницы не выполнены.</span><span class="sxs-lookup"><span data-stu-id="bd15c-133">Unicode — codepage conversions not done.</span></span></p></li>
<li><p><span data-ttu-id="bd15c-134">&lt;десятичное&gt; число — номер кодовой страницы определенного набора символов.</span><span class="sxs-lookup"><span data-stu-id="bd15c-134">&lt;decimal number&gt; — The code page number of a specific character set.</span></span> <span data-ttu-id="bd15c-135">Выполняется преобразование в Юникод и из Юникода.</span><span class="sxs-lookup"><span data-stu-id="bd15c-135">Conversions to and from Unicode will be done.</span></span></p></li>
</ul>
<p></p>
<p><span data-ttu-id="bd15c-136">Значение по умолчанию — ANSI.</span><span class="sxs-lookup"><span data-stu-id="bd15c-136">The default is ANSI.</span></span> <span data-ttu-id="bd15c-137">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bd15c-137">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-138">Format</span><span class="sxs-lookup"><span data-stu-id="bd15c-138">Format</span></span></p></td>
<td><p><span data-ttu-id="bd15c-139">Может быть любым из следующих элементов: Табделимитед, Ксвделимитед, с разделителями&lt;(один&gt;символ).</span><span class="sxs-lookup"><span data-stu-id="bd15c-139">Can be any of the following: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;).</span></span> <span data-ttu-id="bd15c-140">Разделитель из одного символа в формате с разделителями может быть любым одиночным символом, кроме двойных кавычек (&quot;).</span><span class="sxs-lookup"><span data-stu-id="bd15c-140">The single-character delimiter in the Delimited format can be any single character except a double quotation mark (&quot;).</span></span> <span data-ttu-id="bd15c-141">Значение по умолчанию — Ксвделимитед.</span><span class="sxs-lookup"><span data-stu-id="bd15c-141">The default is CSVDelimited.</span></span> <span data-ttu-id="bd15c-142">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bd15c-142">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-143">Расширения</span><span class="sxs-lookup"><span data-stu-id="bd15c-143">Extensions</span></span></p></td>
<td><p><span data-ttu-id="bd15c-144">Расширение файлов, просматриваемых при поиске текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="bd15c-144">The extension of any files to be browsed when looking for text-based data.</span></span> <span data-ttu-id="bd15c-145">Значение по умолчанию — TXT, CSV, TAB, ASC.</span><span class="sxs-lookup"><span data-stu-id="bd15c-145">The default is txt, csv, tab, asc.</span></span> <span data-ttu-id="bd15c-146">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="bd15c-146">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-147">експорткурренцисимболс</span><span class="sxs-lookup"><span data-stu-id="bd15c-147">ExportCurrencySymbols</span></span></p></td>
<td><p><span data-ttu-id="bd15c-148">Двоичное значение, указывающее, включается ли соответствующий символ валюты при экспорте полей валюты.</span><span class="sxs-lookup"><span data-stu-id="bd15c-148">A binary value that indicates whether the appropriate currency symbol is included when currency fields are exported.</span></span> <span data-ttu-id="bd15c-149">Значение 01 указывает, что символ включен.</span><span class="sxs-lookup"><span data-stu-id="bd15c-149">A value of 01 indicates that the symbol is included.</span></span> <span data-ttu-id="bd15c-150">Значение 00 указывает на то, что экспортируются только числовые данные.</span><span class="sxs-lookup"><span data-stu-id="bd15c-150">A value of 00 indicates that only the numeric data is exported.</span></span> <span data-ttu-id="bd15c-151">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="bd15c-151">The default is 01.</span></span> <span data-ttu-id="bd15c-152">Значения имеют тип REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="bd15c-152">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="text-data-source-isam-formats"></a><span data-ttu-id="bd15c-153">Форматы ISAM для источника текстовых данных</span><span class="sxs-lookup"><span data-stu-id="bd15c-153">Text data source ISAM formats</span></span>

<span data-ttu-id="bd15c-154">В **текстовой папке\\ISAM formats\\модуля подключения к Access** содержатся следующие записи.</span><span class="sxs-lookup"><span data-stu-id="bd15c-154">The **Access Connectivity Engine\\ISAM Formats\\Text** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd15c-155">Имя записи</span><span class="sxs-lookup"><span data-stu-id="bd15c-155">Entry name</span></span></p></th>
<th><p><span data-ttu-id="bd15c-156">Тип</span><span class="sxs-lookup"><span data-stu-id="bd15c-156">Type</span></span></p></th>
<th><p><span data-ttu-id="bd15c-157">Значение</span><span class="sxs-lookup"><span data-stu-id="bd15c-157">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-158">Модул</span><span class="sxs-lookup"><span data-stu-id="bd15c-158">Engine</span></span></p></td>
<td><p><span data-ttu-id="bd15c-159">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-159">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-160">Текст</span><span class="sxs-lookup"><span data-stu-id="bd15c-160">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-161">експортфилтер</span><span class="sxs-lookup"><span data-stu-id="bd15c-161">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="bd15c-162">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-162">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-163">Текстовые файлы (\*. txt; \*. csv; \*. Tab; \*. ASC)</span><span class="sxs-lookup"><span data-stu-id="bd15c-163">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-164">импортфилтер</span><span class="sxs-lookup"><span data-stu-id="bd15c-164">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="bd15c-165">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-165">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-166">Текстовые файлы (\*. txt; \*. csv; \*. Tab; \*. ASC)</span><span class="sxs-lookup"><span data-stu-id="bd15c-166">Text Files (\*.txt; \*.csv; \*.tab; \*.asc)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-167">канлинк</span><span class="sxs-lookup"><span data-stu-id="bd15c-167">CanLink</span></span></p></td>
<td><p><span data-ttu-id="bd15c-168">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-168">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-169">01</span><span class="sxs-lookup"><span data-stu-id="bd15c-169">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-170">онетаблеперфиле</span><span class="sxs-lookup"><span data-stu-id="bd15c-170">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="bd15c-171">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-171">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-172">01</span><span class="sxs-lookup"><span data-stu-id="bd15c-172">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-173">исамтипе</span><span class="sxs-lookup"><span data-stu-id="bd15c-173">IsamType</span></span></p></td>
<td><p><span data-ttu-id="bd15c-174">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bd15c-174">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="bd15c-175">2</span><span class="sxs-lookup"><span data-stu-id="bd15c-175">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-176">индексдиалог</span><span class="sxs-lookup"><span data-stu-id="bd15c-176">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="bd15c-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-178">00</span><span class="sxs-lookup"><span data-stu-id="bd15c-178">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-179">креатедбонекспорт</span><span class="sxs-lookup"><span data-stu-id="bd15c-179">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="bd15c-180">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-180">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-181">00</span><span class="sxs-lookup"><span data-stu-id="bd15c-181">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-182">ресулттекстимпорт</span><span class="sxs-lookup"><span data-stu-id="bd15c-182">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="bd15c-183">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-183">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-184">Импорт данных из внешнего файла в текущую базу данных.</span><span class="sxs-lookup"><span data-stu-id="bd15c-184">Import data from the external file into the current database.</span></span> <span data-ttu-id="bd15c-185">Изменение данных в текущей базе данных не приведет к изменению данных во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="bd15c-185">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-186">ресулттекстлинк</span><span class="sxs-lookup"><span data-stu-id="bd15c-186">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="bd15c-187">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-187">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-188">Создайте в текущей базе данных таблицу, связанную с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="bd15c-188">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="bd15c-189">Изменение данных в текущей базе данных приведет к изменению данных во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="bd15c-189">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-190">ресулттекстекспорт</span><span class="sxs-lookup"><span data-stu-id="bd15c-190">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="bd15c-191">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-191">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-192">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="bd15c-192">Export data from the current database into a text file.</span></span> <span data-ttu-id="bd15c-193">При этом данные будут перезаписаны при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="bd15c-193">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-194">суппортслонгнамес</span><span class="sxs-lookup"><span data-stu-id="bd15c-194">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="bd15c-195">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-195">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-196">01</span><span class="sxs-lookup"><span data-stu-id="bd15c-196">01</span></span></p></td>
</tr>
</tbody>
</table>


> [!NOTE]
> <span data-ttu-id="bd15c-197">При изменении параметров реестра Windows необходимо выйти и перезапустить ядро СУБД, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bd15c-197">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-import-isam-formats"></a><span data-ttu-id="bd15c-198">Форматы ISAM для импорта HTML-кода</span><span class="sxs-lookup"><span data-stu-id="bd15c-198">HTML import ISAM formats</span></span>

<span data-ttu-id="bd15c-199">Папка **импорта HTML-\\кода для\\модуля подключения к службе доступа ISAM formats** содержит следующие записи.</span><span class="sxs-lookup"><span data-stu-id="bd15c-199">The **Access Connectivity Engine\\ISAM Formats\\HTML Import** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd15c-200">Имя записи</span><span class="sxs-lookup"><span data-stu-id="bd15c-200">Entry name</span></span></p></th>
<th><p><span data-ttu-id="bd15c-201">Тип</span><span class="sxs-lookup"><span data-stu-id="bd15c-201">Type</span></span></p></th>
<th><p><span data-ttu-id="bd15c-202">Значение</span><span class="sxs-lookup"><span data-stu-id="bd15c-202">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-203">Модул</span><span class="sxs-lookup"><span data-stu-id="bd15c-203">Engine</span></span></p></td>
<td><p><span data-ttu-id="bd15c-204">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-204">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-205">Текст</span><span class="sxs-lookup"><span data-stu-id="bd15c-205">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-206">импортфилтер</span><span class="sxs-lookup"><span data-stu-id="bd15c-206">ImportFilter</span></span></p></td>
<td><p><span data-ttu-id="bd15c-207">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-207">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-208">HTML-файлы (*. HT*)</span><span class="sxs-lookup"><span data-stu-id="bd15c-208">HTML Files (*.ht*)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-209">канлинк</span><span class="sxs-lookup"><span data-stu-id="bd15c-209">CanLink</span></span></p></td>
<td><p><span data-ttu-id="bd15c-210">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-210">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-211">01</span><span class="sxs-lookup"><span data-stu-id="bd15c-211">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-212">онетаблеперфиле</span><span class="sxs-lookup"><span data-stu-id="bd15c-212">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="bd15c-213">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-213">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-214">00</span><span class="sxs-lookup"><span data-stu-id="bd15c-214">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-215">исамтипе</span><span class="sxs-lookup"><span data-stu-id="bd15c-215">IsamType</span></span></p></td>
<td><p><span data-ttu-id="bd15c-216">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bd15c-216">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="bd15c-217">2</span><span class="sxs-lookup"><span data-stu-id="bd15c-217">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-218">индексдиалог</span><span class="sxs-lookup"><span data-stu-id="bd15c-218">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="bd15c-219">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-219">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-220">00</span><span class="sxs-lookup"><span data-stu-id="bd15c-220">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-221">креатедбонекспорт</span><span class="sxs-lookup"><span data-stu-id="bd15c-221">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="bd15c-222">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-222">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-223">00</span><span class="sxs-lookup"><span data-stu-id="bd15c-223">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-224">ресулттекстимпорт</span><span class="sxs-lookup"><span data-stu-id="bd15c-224">ResultTextImport</span></span></p></td>
<td><p><span data-ttu-id="bd15c-225">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-225">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-226">Импорт данных из внешнего файла в текущую базу данных.</span><span class="sxs-lookup"><span data-stu-id="bd15c-226">Import data from the external file into the current database.</span></span> <span data-ttu-id="bd15c-227">Изменение данных в текущей базе данных не приведет к изменению данных во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="bd15c-227">Changing data in the current database will not change data in the external file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-228">ресулттекстлинк</span><span class="sxs-lookup"><span data-stu-id="bd15c-228">ResultTextLink</span></span></p></td>
<td><p><span data-ttu-id="bd15c-229">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-229">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-230">Создайте в текущей базе данных таблицу, связанную с внешним файлом.</span><span class="sxs-lookup"><span data-stu-id="bd15c-230">Create a table in the current database that is linked to the external file.</span></span> <span data-ttu-id="bd15c-231">Изменение данных в текущей базе данных приведет к изменению данных во внешнем файле.</span><span class="sxs-lookup"><span data-stu-id="bd15c-231">Changing data in the current database will change data in the external file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-232">суппортслонгнамес</span><span class="sxs-lookup"><span data-stu-id="bd15c-232">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="bd15c-233">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-233">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-234">01</span><span class="sxs-lookup"><span data-stu-id="bd15c-234">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bd15c-235">При изменении параметров реестра Windows необходимо выйти и перезапустить ядро СУБД, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bd15c-235">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="html-export-isam-formats"></a><span data-ttu-id="bd15c-236">Форматы ISAM для экспорта HTML</span><span class="sxs-lookup"><span data-stu-id="bd15c-236">HTML export ISAM formats</span></span>

<span data-ttu-id="bd15c-237">В папке **экспорта\\\\HTML в HTML-папке экспорта подсистемы подключения Access** содержатся следующие записи.</span><span class="sxs-lookup"><span data-stu-id="bd15c-237">The **Access Connectivity Engine\\ISAM Formats\\HTML Export** folder contains the following entries.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd15c-238">Имя записи</span><span class="sxs-lookup"><span data-stu-id="bd15c-238">Entry name</span></span></p></th>
<th><p><span data-ttu-id="bd15c-239">Тип</span><span class="sxs-lookup"><span data-stu-id="bd15c-239">Type</span></span></p></th>
<th><p><span data-ttu-id="bd15c-240">Значение</span><span class="sxs-lookup"><span data-stu-id="bd15c-240">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-241">Модул</span><span class="sxs-lookup"><span data-stu-id="bd15c-241">Engine</span></span></p></td>
<td><p><span data-ttu-id="bd15c-242">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-242">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-243">Текст</span><span class="sxs-lookup"><span data-stu-id="bd15c-243">Text</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-244">експортфилтер</span><span class="sxs-lookup"><span data-stu-id="bd15c-244">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="bd15c-245">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-245">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-246">HTML-файлы (\*. htm)</span><span class="sxs-lookup"><span data-stu-id="bd15c-246">HTML Files (\*.htm)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-247">канлинк</span><span class="sxs-lookup"><span data-stu-id="bd15c-247">CanLink</span></span></p></td>
<td><p><span data-ttu-id="bd15c-248">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-248">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-249">00</span><span class="sxs-lookup"><span data-stu-id="bd15c-249">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-250">онетаблеперфиле</span><span class="sxs-lookup"><span data-stu-id="bd15c-250">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="bd15c-251">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-251">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-252">01</span><span class="sxs-lookup"><span data-stu-id="bd15c-252">01</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-253">исамтипе</span><span class="sxs-lookup"><span data-stu-id="bd15c-253">IsamType</span></span></p></td>
<td><p><span data-ttu-id="bd15c-254">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="bd15c-254">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="bd15c-255">2</span><span class="sxs-lookup"><span data-stu-id="bd15c-255">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-256">индексдиалог</span><span class="sxs-lookup"><span data-stu-id="bd15c-256">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="bd15c-257">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-257">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-258">00</span><span class="sxs-lookup"><span data-stu-id="bd15c-258">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-259">креатедбонекспорт</span><span class="sxs-lookup"><span data-stu-id="bd15c-259">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="bd15c-260">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-260">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-261">00</span><span class="sxs-lookup"><span data-stu-id="bd15c-261">00</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-262">ресулттекстекспорт</span><span class="sxs-lookup"><span data-stu-id="bd15c-262">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="bd15c-263">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="bd15c-263">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="bd15c-264">Экспорт данных из текущей базы данных в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="bd15c-264">Export data from the current database into a text file.</span></span> <span data-ttu-id="bd15c-265">При этом данные будут перезаписаны при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="bd15c-265">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-266">суппортслонгнамес</span><span class="sxs-lookup"><span data-stu-id="bd15c-266">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="bd15c-267">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="bd15c-267">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="bd15c-268">01</span><span class="sxs-lookup"><span data-stu-id="bd15c-268">01</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bd15c-269">При изменении параметров реестра Windows необходимо выйти и перезапустить ядро СУБД, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bd15c-269">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="customizing-the-schemaini-file-for-text-and-html-data"></a><span data-ttu-id="bd15c-270">Настройка файла Schema. ini для текстовых и HTML-данных</span><span class="sxs-lookup"><span data-stu-id="bd15c-270">Customizing the Schema.ini file for text and HTML data</span></span>

<span data-ttu-id="bd15c-271">Для чтения, импорта и экспорта текста и HTML-данных необходимо создать файл Schema. ini, который включает в себя сведения о тексте ISAM в ini-файле.</span><span class="sxs-lookup"><span data-stu-id="bd15c-271">To read, import, or export text and HTML data, you need to create a Schema.ini file in addition to including the Text ISAM information in the .ini file.</span></span> <span data-ttu-id="bd15c-272">Schema. ini содержит особенности источника данных: способ форматирования текстового файла, его чтение во время импорта, а также используемый по умолчанию формат экспорта для файлов.</span><span class="sxs-lookup"><span data-stu-id="bd15c-272">Schema.ini contains the specifics of a data source: how the text file is formatted, how it is read at import time, and what the default export format is for files.</span></span> <span data-ttu-id="bd15c-273">В приведенных ниже примерах показана структура для файла фиксированной ширины filename. txt:</span><span class="sxs-lookup"><span data-stu-id="bd15c-273">The following examples show the layout for a fixed-width file, Filename.txt:</span></span>

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

<span data-ttu-id="bd15c-274">Аналогично, формат для файла с разделителями задается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="bd15c-274">Similarly, the format for a delimited file is specified as follows:</span></span>

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

<span data-ttu-id="bd15c-275">При экспорте данных в текстовый файл с разделителями необходимо также указать формат этого файла:</span><span class="sxs-lookup"><span data-stu-id="bd15c-275">If you are exporting data into a delimited text file, specify the format for that file as well:</span></span>

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

Пример "Мой экспорт" относится к конкретному параметру экспорта; во время подключения можно указать любой вариант экспортируемых параметров. <span data-ttu-id="bd15c-277">Последний пример также соответствует имени источника данных (DSN), которое может быть дополнительно передано во время подключения.</span><span class="sxs-lookup"><span data-stu-id="bd15c-277">This last example also corresponds to a data source name (DSN) that can be optionally passed at connect time.</span></span> <span data-ttu-id="bd15c-278">Все три раздела форматирования могут быть включены в один и тот же ini-файл.</span><span class="sxs-lookup"><span data-stu-id="bd15c-278">All three format sections can be included in the same .ini file.</span></span>

<span data-ttu-id="bd15c-279">Ядро СУБД Microsoft Access использует записи Schema. ini следующим образом.</span><span class="sxs-lookup"><span data-stu-id="bd15c-279">The Microsoft Access database engine uses the Schema.ini entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bd15c-280">Введен</span><span class="sxs-lookup"><span data-stu-id="bd15c-280">Entry</span></span></p></th>
<th><p><span data-ttu-id="bd15c-281">Описание</span><span class="sxs-lookup"><span data-stu-id="bd15c-281">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-282">колнамехеадер</span><span class="sxs-lookup"><span data-stu-id="bd15c-282">ColNameHeader</span></span></p></td>
<td><p><span data-ttu-id="bd15c-283">Может иметь значение <strong>true</strong> (что означает, что первая запись данных указывает имена столбцов) или <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="bd15c-283">Can be set to either <strong>True</strong> (indicating that the first record of data specifies the column names) or <strong>False</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-284">Format</span><span class="sxs-lookup"><span data-stu-id="bd15c-284">Format</span></span></p></td>
<td><p><span data-ttu-id="bd15c-285">Можно задать одно из следующих значений: Табделимитед, Ксвделимитед, с разделителями (&lt;один символ&gt;) или фикседленгс.</span><span class="sxs-lookup"><span data-stu-id="bd15c-285">Can be set to one of the following values: TabDelimited, CSVDelimited, Delimited (&lt;single character&gt;), or FixedLength.</span></span> <span data-ttu-id="bd15c-286">Разделитель, указанный для формата файла с разделителями, может быть любым одиночным символом, кроме двойных кавычек&quot;().</span><span class="sxs-lookup"><span data-stu-id="bd15c-286">The delimiter specified for the Delimited file format can be any single character except a double quotation mark (&quot;).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-287">фикседформат</span><span class="sxs-lookup"><span data-stu-id="bd15c-287">FixedFormat</span></span></p></td>
<td><p><span data-ttu-id="bd15c-288">Используется только в том случае, если используется формат Фикседленгс, для этого может быть задано одно из следующих значений: Рагжедедже или Труефикседленгс.</span><span class="sxs-lookup"><span data-stu-id="bd15c-288">Only used when the Format is FixedLength, this can be set to one of the following values: RaggedEdge or TrueFixedLength.</span></span> <span data-ttu-id="bd15c-289">Рагжедедже позволяет завершать строки символом возврата каретки.</span><span class="sxs-lookup"><span data-stu-id="bd15c-289">RaggedEdge allows rows to be terminated with a Carriage Return character.</span></span> <span data-ttu-id="bd15c-290">Для Труефикседленгс требуется, чтобы каждая строка была точным числом символов, а все символы возврата каретки, не равные границе строки, были внедрены в поле.</span><span class="sxs-lookup"><span data-stu-id="bd15c-290">TrueFixedLength requires each row to be an exact number of characters, and any Carriage Return characters not at a row boundary are assumed to be embedded in a field.</span></span> <span data-ttu-id="bd15c-291">Если этот параметр не указан, по умолчанию используется значение Рагжедедже.</span><span class="sxs-lookup"><span data-stu-id="bd15c-291">If this setting is not present, the default value is RaggedEdge.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-292">макссканровс</span><span class="sxs-lookup"><span data-stu-id="bd15c-292">MaxScanRows</span></span></p></td>
<td><p><span data-ttu-id="bd15c-293">Указывает количество строк, проверяемых при выгадке типов данных столбца.</span><span class="sxs-lookup"><span data-stu-id="bd15c-293">Indicates the number of rows to be scanned when guessing the column data types.</span></span> <span data-ttu-id="bd15c-294">Если для этого параметра задано значение 0, выполняется поиск по всему файлу.</span><span class="sxs-lookup"><span data-stu-id="bd15c-294">If this is set to 0, the entire file is searched.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-295">CharacterSet</span><span class="sxs-lookup"><span data-stu-id="bd15c-295">CharacterSet</span></span></p></td>
<td><p><span data-ttu-id="bd15c-296">Может иметь значение OEM, ANSI, UNICODE или десятичное число допустимой кодовой страницы, а также указывает кодировку исходного файла.</span><span class="sxs-lookup"><span data-stu-id="bd15c-296">Can be set to OEM, ANSI, UNICODE, or the decimal number of a valid code page, and indicates the character set of the source file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-297">датетимеформат</span><span class="sxs-lookup"><span data-stu-id="bd15c-297">DateTimeFormat</span></span></p></td>
<td><p><span data-ttu-id="bd15c-298">Может быть задано значение типа String, указывающее даты и время.</span><span class="sxs-lookup"><span data-stu-id="bd15c-298">Can be set to a format string indicating dates and times.</span></span> <span data-ttu-id="bd15c-299">Эта запись должна быть указана, если все поля даты и времени в импорте/экспорте обрабатываются в том же формате.</span><span class="sxs-lookup"><span data-stu-id="bd15c-299">This entry should be specified if all date/time fields in the import/export are handled with the same format.</span></span> <span data-ttu-id="bd15c-300">Поддерживаются все форматы ядра базы данных Microsoft Jet, кроме AM и PM.</span><span class="sxs-lookup"><span data-stu-id="bd15c-300">All of the Microsoft Jet database engine formats except AM and PM are supported.</span></span> <span data-ttu-id="bd15c-301">В случае отсутствия строки формата используются параметры времени и аватара на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bd15c-301">In the absence of a format string, the Windows Control Panel short date picture and time options are used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-302">CurrencySymbol</span><span class="sxs-lookup"><span data-stu-id="bd15c-302">CurrencySymbol</span></span></p></td>
<td><p><span data-ttu-id="bd15c-303">Указывает символ валюты, используемый для денежных значений в текстовом файле.</span><span class="sxs-lookup"><span data-stu-id="bd15c-303">Indicates the currency symbol to be used for currency values in the text file.</span></span> <span data-ttu-id="bd15c-304">Примеры включают знак доллара ($) и DM.</span><span class="sxs-lookup"><span data-stu-id="bd15c-304">Examples include the dollar sign ($) and Dm.</span></span> <span data-ttu-id="bd15c-305">Если эта запись отсутствует, используется значение по умолчанию на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bd15c-305">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-306">курренципосформат</span><span class="sxs-lookup"><span data-stu-id="bd15c-306">CurrencyPosFormat</span></span></p></td>
<td><p><span data-ttu-id="bd15c-307">Может быть задано любое из следующих значений: префикс символа валюты без цветоделения ($1) $1 суффикс символа валюты без цветоделения () префикс символа валюты с одним символом разделения ($1), с одним символом ($1), если эта запись отсутствует, используется значение по умолчанию на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bd15c-307">Can be set to any of the following values: Currency symbol prefix with no separation ($1) Currency symbol suffix with no separation (1$) Currency symbol prefix with one character separation ($ 1) Currency symbol suffix with one character separation (1 $) If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-308">CurrencyDigits</span><span class="sxs-lookup"><span data-stu-id="bd15c-308">CurrencyDigits</span></span></p></td>
<td><p><span data-ttu-id="bd15c-309">Указывает количество цифр, используемых для дробной части денежной суммы.</span><span class="sxs-lookup"><span data-stu-id="bd15c-309">Specifies the number of digits used for the fractional part of a currency amount.</span></span> <span data-ttu-id="bd15c-310">Если эта запись отсутствует, используется значение по умолчанию на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bd15c-310">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-311">курренцинегформат</span><span class="sxs-lookup"><span data-stu-id="bd15c-311">CurrencyNegFormat</span></span></p></td>
<td><p><span data-ttu-id="bd15c-312">Может принимать одно из следующих значений: ($1) – $1 $ – $1 1 – ($1) – $1 1 – $1 $ – $1 – $1 $1 – $1 – $ – 1 1 – $ ($1) ($1) знак доллара отображается для этого примера, но его следует заменить соответствующим значением Курренцисимбол в реальной программе.</span><span class="sxs-lookup"><span data-stu-id="bd15c-312">Can be one of the following values: ($1) –$1 $–1 $1– (1$) –1$ 1–$ 1$– –1 $ –$ 1 1 $– $ 1– $ –1 1– $ ($ 1) (1 $) The dollar sign is shown for purposes of this example, but it should be replaced with the appropriate CurrencySymbol value in the actual program.</span></span> <span data-ttu-id="bd15c-313">Если эта запись отсутствует, используется значение по умолчанию на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bd15c-313">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-314">курренцисаусандсимбол</span><span class="sxs-lookup"><span data-stu-id="bd15c-314">CurrencyThousandSymbol</span></span></p></td>
<td><p><span data-ttu-id="bd15c-315">Указывает символ, состоящего из одного символа, который используется для разделения значений денежных единиц на тысячах в текстовом файле.</span><span class="sxs-lookup"><span data-stu-id="bd15c-315">Indicates the single-character symbol to be used for separating currency values by thousands in the text file.</span></span> <span data-ttu-id="bd15c-316">Если эта запись отсутствует, используется значение по умолчанию на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bd15c-316">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-317">курренцидеЦималсимбол</span><span class="sxs-lookup"><span data-stu-id="bd15c-317">CurrencyDecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="bd15c-318">Можно задать любой символ, который используется для отделения целого от дробной части денежной суммы.</span><span class="sxs-lookup"><span data-stu-id="bd15c-318">Can be set to any single character that is used to separate the whole from the fractional part of a currency amount.</span></span> <span data-ttu-id="bd15c-319">Если эта запись отсутствует, используется значение по умолчанию на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bd15c-319">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-320">деЦималсимбол</span><span class="sxs-lookup"><span data-stu-id="bd15c-320">DecimalSymbol</span></span></p></td>
<td><p><span data-ttu-id="bd15c-321">Можно задать любой символ, который используется для отделения целого числа от дробной части числа.</span><span class="sxs-lookup"><span data-stu-id="bd15c-321">Can be set to any single character that is used to separate the integer from the fractional part of a number.</span></span> <span data-ttu-id="bd15c-322">Если эта запись отсутствует, используется значение по умолчанию на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bd15c-322">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-323">нумбердигитс</span><span class="sxs-lookup"><span data-stu-id="bd15c-323">NumberDigits</span></span></p></td>
<td><p><span data-ttu-id="bd15c-324">Указывает количество десятичных цифр в дробной части числа.</span><span class="sxs-lookup"><span data-stu-id="bd15c-324">Indicates the number of decimal digits in the fractional portion of a number.</span></span> <span data-ttu-id="bd15c-325">Если эта запись отсутствует, используется значение по умолчанию на панели управления Windows.</span><span class="sxs-lookup"><span data-stu-id="bd15c-325">If this entry is absent, the default value in the Windows Control Panel is used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-326">нумберлеадингзерос</span><span class="sxs-lookup"><span data-stu-id="bd15c-326">NumberLeadingZeros</span></span></p></td>
<td><p><span data-ttu-id="bd15c-327">Указывает, должны ли дробные значения меньше 1 и больше, чем – 1, должны содержать начальные нули; Это может быть значение false (без нулей в начале) или true.</span><span class="sxs-lookup"><span data-stu-id="bd15c-327">Specifies whether a decimal value less than 1 and greater than –1 should contain leading zeros; this value can either be False (no leading zeros) or True.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd15c-328">Столбец1, col2,...</span><span class="sxs-lookup"><span data-stu-id="bd15c-328">Col1, Col2, …</span></span></p></td>
<td><p><span data-ttu-id="bd15c-329">Перечисляет столбцы в текстовом файле, которые необходимо прочитать.</span><span class="sxs-lookup"><span data-stu-id="bd15c-329">Lists the columns in the text file to be read.</span></span> <span data-ttu-id="bd15c-330">Этот параметр должен иметь следующий формат: <em>Колн</em>=<em>ColumnName</em> Type [width <em> #</em>] <em>ColumnName</em>: имена столбцов со встроенными пробелами должны быть заключены в кавычки.</span><span class="sxs-lookup"><span data-stu-id="bd15c-330">The format of this entry should be: <em>Coln</em>=<em>columnName</em> type [Width <em>#</em>] <em>columnName</em>: Column names with embedded spaces should be enclosed in quotation marks.</span></span> <span data-ttu-id="bd15c-331"><em>тип</em>: может быть бит, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span><span class="sxs-lookup"><span data-stu-id="bd15c-331"><em>type</em>: Can be Bit, Byte, Short, Long, Decimal, Currency, Single, Double, DateTime.</span></span> <span data-ttu-id="bd15c-332">Двоичный, OLE, Text или MEMO.</span><span class="sxs-lookup"><span data-stu-id="bd15c-332">Binary, OLE, Text, or Memo.</span></span> <span data-ttu-id="bd15c-333">Кроме того, поддерживаются следующие типы текстовых драйверов ODBC: char (то же, как текст) с плавающей запятой (то же, что и в виде текста) (то же, что и Short) (то же, что и Short) Лонгчар (то же, что и Short) (то же, что и Short) Дата в <em>формате</em> даты в случае с типом "Примечание".</span><span class="sxs-lookup"><span data-stu-id="bd15c-333">In addition, the following ODBC Text Driver types are supported: Char (same as Text) Float (same as Double) Integer (same as Short) LongChar (same as Memo) Date <em>date format</em> In the case of a Memo type an additional format marker [Attribute Hyperlink] can be used to specify columns that should be active URLs in Microsoft Access.</span></span> <span data-ttu-id="bd15c-334">В случае десятичного типа следует использовать дополнительные маркеры формата [Scale #] Precision #].</span><span class="sxs-lookup"><span data-stu-id="bd15c-334">In the case of a Decimal type the additional format markers [Scale #] Precision #] should be used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd15c-335">текстделимитер</span><span class="sxs-lookup"><span data-stu-id="bd15c-335">TextDelimiter</span></span></p></td>
<td><p><span data-ttu-id="bd15c-336">Можно задать любой символ, используемый для разграничения строк, содержащих любой из других специальных символов.</span><span class="sxs-lookup"><span data-stu-id="bd15c-336">Can be set to any single character that is used to delimit strings that contain any of the other special characters.</span></span> <span data-ttu-id="bd15c-337">Например,</span><span class="sxs-lookup"><span data-stu-id="bd15c-337">E.g.</span></span> <span data-ttu-id="bd15c-338">&quot;ABC&quot;,&quot;XYZ, ПКР&quot;,&quot;хиж&quot; если этот параметр отсутствует, разделителем по умолчанию является двойная кавычка.</span><span class="sxs-lookup"><span data-stu-id="bd15c-338">&quot;abc&quot;,&quot;xyz,pqr&quot;,&quot;hij&quot; If this entry is not present the default delimiter is a double quote.</span></span> <span data-ttu-id="bd15c-339">Если эта запись является строкой &quot;None&quot; (нет), символы не будут рассматриваться как разделители.</span><span class="sxs-lookup"><span data-stu-id="bd15c-339">If this entry is the string &quot;none&quot; then no characters will be treated as delimiters.</span></span></p></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="bd15c-340">При изменении параметров файла Schema. ini необходимо выйти и перезапустить ядро СУБД, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="bd15c-340">When you change Schema.ini file settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>


