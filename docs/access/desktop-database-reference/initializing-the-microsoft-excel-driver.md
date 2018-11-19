---
title: Инициализация драйвера Microsoft Excel
TOCTitle: Initializing the Microsoft Excel driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 87f2b5667c1406caec3e750c1ee256606851fe96
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026339"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="38105-102">Инициализация драйвера Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="38105-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="38105-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="38105-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="38105-104">При установке драйвера Excel, программа установки записывает набор значений по умолчанию в реестре Windows в подразделах обработчики и ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="38105-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="38105-105">Не изменяйте эти параметры напрямую; для добавления, удаления или изменения этих параметров с помощью программы установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="38105-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="38105-106">В следующих разделах инициализации и параметров ISAM Format драйвера базы данных Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="38105-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="38105-107">Параметры инициализации Excel</span><span class="sxs-lookup"><span data-stu-id="38105-107">Excel initialization settings</span></span>

<span data-ttu-id="38105-108">**Модуль подключения к Access\\обработчики\\Excel** папка содержит параметры инициализации драйвера Aceexcl.dll, который используется для внешнего доступа к лист Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="38105-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="38105-109">В следующем примере приведены типичные параметры записей в этой папке.</span><span class="sxs-lookup"><span data-stu-id="38105-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="38105-110">Ядро базы данных Microsoft Access записи папки Excel используются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="38105-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38105-111">Запись</span><span class="sxs-lookup"><span data-stu-id="38105-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="38105-112">Описание</span><span class="sxs-lookup"><span data-stu-id="38105-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38105-113">Win32</span><span class="sxs-lookup"><span data-stu-id="38105-113">win32</span></span></p></td>
<td><p><span data-ttu-id="38105-114">Расположение msexcl40.dll.</span><span class="sxs-lookup"><span data-stu-id="38105-114">The location of msexcl40.dll.</span></span> <span data-ttu-id="38105-115">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="38105-115">The full path is determined at the time of installation.</span></span> <span data-ttu-id="38105-116">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="38105-116">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38105-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="38105-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="38105-118">Количество строк для проверки типа данных.</span><span class="sxs-lookup"><span data-stu-id="38105-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="38105-119">Тип данных определяется максимальное количество типов данных.</span><span class="sxs-lookup"><span data-stu-id="38105-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="38105-120">Если имеется набор функций, тип данных определяется в следующем порядке: номер, валюта, дата, текст, логическое значение.</span><span class="sxs-lookup"><span data-stu-id="38105-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="38105-121">Если обнаружены данные, которые не соответствует типу данных, указанному для столбца, он возвращается как значение <strong>Null</strong> .</span><span class="sxs-lookup"><span data-stu-id="38105-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="38105-122">При импорте Если столбец имеет смешанный тип данных, столбец целиком приводится в соответствии с параметром ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="38105-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="38105-123">По умолчанию число строк для проверки — 8.</span><span class="sxs-lookup"><span data-stu-id="38105-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="38105-124">Значения — типа REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="38105-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38105-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="38105-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="38105-126">Может иметь значение MajorityType или текст.</span><span class="sxs-lookup"><span data-stu-id="38105-126">Can be set to MajorityType or Text.</span></span> <span data-ttu-id="38105-127">Если параметр имеет значение MajorityType, столбцы смешанный типы данных приводится к типу данных основной при импорте.</span><span class="sxs-lookup"><span data-stu-id="38105-127">If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import.</span></span> <span data-ttu-id="38105-128">Если установлено значение Text, столбцы mixed типы данных приводится в текст при импорте.</span><span class="sxs-lookup"><span data-stu-id="38105-128">If set to Text, columns of mixed data types will be cast to Text on import.</span></span> <span data-ttu-id="38105-129">Значение по умолчанию — текст.</span><span class="sxs-lookup"><span data-stu-id="38105-129">The default is Text.</span></span> <span data-ttu-id="38105-130">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="38105-130">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38105-131">Значение параметра AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="38105-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="38105-132">Добавлен номер пустые строки для добавления в конец версии 3.5 или листа версии 4.0 перед новыми данными.</span><span class="sxs-lookup"><span data-stu-id="38105-132">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added.</span></span> <span data-ttu-id="38105-133">Например, если значение параметра AppendBlankRows равно 4, Microsoft Jet добавляет 4 пустые строки в конец рабочего листа перед добавлением строки, содержащие данные.</span><span class="sxs-lookup"><span data-stu-id="38105-133">For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data.</span></span> <span data-ttu-id="38105-134">Целые значения для этого параметра можно в диапазоне от 0 до 16; значение по умолчанию — 01 (добавляется один дополнительный ряд).</span><span class="sxs-lookup"><span data-stu-id="38105-134">Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended).</span></span> <span data-ttu-id="38105-135">Значения — типа REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="38105-135">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38105-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="38105-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="38105-137">Двоичное значение, указывающее, содержит ли имена столбцов первой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="38105-137">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="38105-138">Значение 01 показывает, что во время импорта, имена столбцов берутся из первой строки.</span><span class="sxs-lookup"><span data-stu-id="38105-138">A value of 01 indicates that, during import, column names are taken from the first row.</span></span> <span data-ttu-id="38105-139">Значение 00 указывает не имена столбцов в первой строке; имена столбцов отображаются в виде F1, F2, F3 и т. д.</span><span class="sxs-lookup"><span data-stu-id="38105-139">A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on.</span></span> <span data-ttu-id="38105-140">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="38105-140">The default is 01.</span></span> <span data-ttu-id="38105-141">Значения — типа REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="38105-141">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="38105-142">**Модуль подключения к Access\\обработчики\\Excel 8.0** папка содержит следующие записи, которые применяются к Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="38105-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="38105-143">Имя записи</span><span class="sxs-lookup"><span data-stu-id="38105-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="38105-144">Тип</span><span class="sxs-lookup"><span data-stu-id="38105-144">Type</span></span></p></th>
<th><p><span data-ttu-id="38105-145">Значение</span><span class="sxs-lookup"><span data-stu-id="38105-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="38105-146">Модуль</span><span class="sxs-lookup"><span data-stu-id="38105-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="38105-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="38105-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="38105-148">Excel</span><span class="sxs-lookup"><span data-stu-id="38105-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38105-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="38105-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="38105-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="38105-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="38105-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="38105-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38105-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="38105-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="38105-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="38105-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="38105-154">01</span><span class="sxs-lookup"><span data-stu-id="38105-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38105-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="38105-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="38105-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="38105-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="38105-157">00</span><span class="sxs-lookup"><span data-stu-id="38105-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38105-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="38105-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="38105-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="38105-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="38105-160">1</span><span class="sxs-lookup"><span data-stu-id="38105-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38105-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="38105-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="38105-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="38105-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="38105-163">00</span><span class="sxs-lookup"><span data-stu-id="38105-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38105-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="38105-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="38105-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="38105-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="38105-166">01</span><span class="sxs-lookup"><span data-stu-id="38105-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="38105-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="38105-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="38105-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="38105-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="38105-169">Экспорт данных из текущей базы данных в файл Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="38105-169">Export data from the current database into a Microsoft Excel 97 file.</span></span> <span data-ttu-id="38105-170">В этом будут перезаписаны данные при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="38105-170">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="38105-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="38105-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="38105-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="38105-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="38105-173">01</span><span class="sxs-lookup"><span data-stu-id="38105-173">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="38105-174">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="38105-174">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="38105-175">См. также</span><span class="sxs-lookup"><span data-stu-id="38105-175">See also</span></span>

- [<span data-ttu-id="38105-176">С помощью параметра TypeGuessRows драйвера Excel</span><span class="sxs-lookup"><span data-stu-id="38105-176">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)