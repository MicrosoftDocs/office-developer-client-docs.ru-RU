---
title: Initializing the Microsoft Excel Driver
TOCTitle: Initializing the Microsoft Excel Driver
ms:assetid: 06c7f823-8e74-0811-cc00-e6b32075ef11
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844939(v=office.15)
ms:contentKeyID: 48543054
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032159
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 7c9a3282f3bb508a4c68ecbd3f2c0465cfee9bac
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603100"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="27daa-102">Initializing the Microsoft Excel Driver</span><span class="sxs-lookup"><span data-stu-id="27daa-102">Initializing the Microsoft Excel Driver</span></span>


<span data-ttu-id="27daa-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="27daa-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="27daa-104"><<<<<<< HEAD при установке драйвера Microsoft® Excel, программа установки записывает набор значений по умолчанию в реестр Microsoft Windows® в подразделах обработчики и ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="27daa-104"><<<<<<< HEAD When you install the Microsoft® Excel driver, the Setup program writes a set of default values to the Microsoft Windows® Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="27daa-105">Не изменяйте эти параметры напрямую; для добавления, удаления или изменения этих параметров с помощью программы установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="27daa-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="27daa-106">В следующих разделах инициализации и параметров ISAM Format драйвера базы данных Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="27daa-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="microsoft-excel-initialization-settings"></a><span data-ttu-id="27daa-107">Параметры инициализации Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="27daa-107">Microsoft Excel Initialization Settings</span></span>
<span data-ttu-id="27daa-108">=== При установке драйвера Excel, программа установки записывает набор значений по умолчанию в реестре Windows в подразделах обработчики и ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="27daa-108">======= When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="27daa-109">Не изменяйте эти параметры напрямую; для добавления, удаления или изменения этих параметров с помощью программы установки для приложения.</span><span class="sxs-lookup"><span data-stu-id="27daa-109">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="27daa-110">В следующих разделах инициализации и параметров ISAM Format драйвера базы данных Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="27daa-110">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="27daa-111">Параметры инициализации Excel</span><span class="sxs-lookup"><span data-stu-id="27daa-111">Excel Initialization Settings</span></span>
>>>>>>> <span data-ttu-id="27daa-112">master</span><span class="sxs-lookup"><span data-stu-id="27daa-112">master</span></span>

<span data-ttu-id="27daa-113">**Модуль подключения к Access\\обработчики\\Excel** папка содержит параметры инициализации драйвера Aceexcl.dll, который используется для внешнего доступа к лист Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="27daa-113">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="27daa-114">В следующем примере приведены типичные параметры записей в этой папке.</span><span class="sxs-lookup"><span data-stu-id="27daa-114">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="27daa-115">Ядро базы данных Microsoft Access записи папки Excel используются следующим образом.</span><span class="sxs-lookup"><span data-stu-id="27daa-115">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27daa-116">Запись</span><span class="sxs-lookup"><span data-stu-id="27daa-116">Entry</span></span></p></th>
<th><p><span data-ttu-id="27daa-117">Описание</span><span class="sxs-lookup"><span data-stu-id="27daa-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27daa-118">Win32</span><span class="sxs-lookup"><span data-stu-id="27daa-118">win32</span></span></p></td>
<td><p><span data-ttu-id="27daa-119">Расположение msexcl40.dll.</span><span class="sxs-lookup"><span data-stu-id="27daa-119">The location of msexcl40.dll.</span></span> <span data-ttu-id="27daa-120">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="27daa-120">The full path is determined at the time of installation.</span></span> <span data-ttu-id="27daa-121">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="27daa-121">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27daa-122">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="27daa-122">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="27daa-123">Количество строк для проверки типа данных.</span><span class="sxs-lookup"><span data-stu-id="27daa-123">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="27daa-124">Тип данных определяется максимальное количество типов данных.</span><span class="sxs-lookup"><span data-stu-id="27daa-124">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="27daa-125">Если имеется набор функций, тип данных определяется в следующем порядке: номер, валюта, дата, текст, логическое значение.</span><span class="sxs-lookup"><span data-stu-id="27daa-125">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="27daa-126">Если обнаружены данные, которые не соответствует типу данных, указанному для столбца, он возвращается как значение <strong>Null</strong> .</span><span class="sxs-lookup"><span data-stu-id="27daa-126">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="27daa-127">При импорте Если столбец имеет смешанный тип данных, столбец целиком приводится в соответствии с параметром ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="27daa-127">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="27daa-128">По умолчанию число строк для проверки — 8.</span><span class="sxs-lookup"><span data-stu-id="27daa-128">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="27daa-129">Значения — типа REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="27daa-129">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27daa-130">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="27daa-130">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="27daa-131">Может иметь значение MajorityType или текст.</span><span class="sxs-lookup"><span data-stu-id="27daa-131">Can be set to MajorityType or Text.</span></span> <span data-ttu-id="27daa-132">Если параметр имеет значение MajorityType, столбцы смешанный типы данных приводится к типу данных основной при импорте.</span><span class="sxs-lookup"><span data-stu-id="27daa-132">If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import.</span></span> <span data-ttu-id="27daa-133">Если установлено значение Text, столбцы mixed типы данных приводится в текст при импорте.</span><span class="sxs-lookup"><span data-stu-id="27daa-133">If set to Text, columns of mixed data types will be cast to Text on import.</span></span> <span data-ttu-id="27daa-134">Значение по умолчанию — текст.</span><span class="sxs-lookup"><span data-stu-id="27daa-134">The default is Text.</span></span> <span data-ttu-id="27daa-135">Значения — типа REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="27daa-135">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27daa-136">Значение параметра AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="27daa-136">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="27daa-137">Добавлен номер пустые строки для добавления в конец версии 3.5 или листа версии 4.0 перед новыми данными.</span><span class="sxs-lookup"><span data-stu-id="27daa-137">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added.</span></span> <span data-ttu-id="27daa-138">Например, если значение параметра AppendBlankRows равно 4, Microsoft Jet добавляет 4 пустые строки в конец рабочего листа перед добавлением строки, содержащие данные.</span><span class="sxs-lookup"><span data-stu-id="27daa-138">For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data.</span></span> <span data-ttu-id="27daa-139">Целые значения для этого параметра можно в диапазоне от 0 до 16; значение по умолчанию — 01 (добавляется один дополнительный ряд).</span><span class="sxs-lookup"><span data-stu-id="27daa-139">Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended).</span></span> <span data-ttu-id="27daa-140">Значения — типа REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="27daa-140">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27daa-141">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="27daa-141">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="27daa-142">Двоичное значение, указывающее, содержит ли имена столбцов первой строки в таблице.</span><span class="sxs-lookup"><span data-stu-id="27daa-142">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="27daa-143">Значение 01 показывает, что во время импорта, имена столбцов берутся из первой строки.</span><span class="sxs-lookup"><span data-stu-id="27daa-143">A value of 01 indicates that, during import, column names are taken from the first row.</span></span> <span data-ttu-id="27daa-144">Значение 00 указывает не имена столбцов в первой строке; имена столбцов отображаются в виде F1, F2, F3 и т. д.</span><span class="sxs-lookup"><span data-stu-id="27daa-144">A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on.</span></span> <span data-ttu-id="27daa-145">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="27daa-145">The default is 01.</span></span> <span data-ttu-id="27daa-146">Значения — типа REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="27daa-146">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="27daa-147">**Модуль подключения к Access\\обработчики\\Excel 8.0** папка содержит следующие записи, которые применяются к Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="27daa-147">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27daa-148">Имя записи</span><span class="sxs-lookup"><span data-stu-id="27daa-148">Entry name</span></span></p></th>
<th><p><span data-ttu-id="27daa-149">Тип</span><span class="sxs-lookup"><span data-stu-id="27daa-149">Type</span></span></p></th>
<th><p><span data-ttu-id="27daa-150">Значение</span><span class="sxs-lookup"><span data-stu-id="27daa-150">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27daa-151">Модуль</span><span class="sxs-lookup"><span data-stu-id="27daa-151">Engine</span></span></p></td>
<td><p><span data-ttu-id="27daa-152">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="27daa-152">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="27daa-153">Excel</span><span class="sxs-lookup"><span data-stu-id="27daa-153">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27daa-154">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="27daa-154">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="27daa-155">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="27daa-155">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="27daa-156">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="27daa-156">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27daa-157">CanLink</span><span class="sxs-lookup"><span data-stu-id="27daa-157">CanLink</span></span></p></td>
<td><p><span data-ttu-id="27daa-158">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27daa-158">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27daa-159">01</span><span class="sxs-lookup"><span data-stu-id="27daa-159">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27daa-160">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="27daa-160">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="27daa-161">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27daa-161">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27daa-162">00</span><span class="sxs-lookup"><span data-stu-id="27daa-162">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27daa-163">IsamType</span><span class="sxs-lookup"><span data-stu-id="27daa-163">IsamType</span></span></p></td>
<td><p><span data-ttu-id="27daa-164">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="27daa-164">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="27daa-165">1</span><span class="sxs-lookup"><span data-stu-id="27daa-165">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27daa-166">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="27daa-166">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="27daa-167">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27daa-167">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27daa-168">00</span><span class="sxs-lookup"><span data-stu-id="27daa-168">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27daa-169">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="27daa-169">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="27daa-170">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27daa-170">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27daa-171">01</span><span class="sxs-lookup"><span data-stu-id="27daa-171">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27daa-172">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="27daa-172">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="27daa-173">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="27daa-173">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="27daa-174">Экспорт данных из текущей базы данных в файл Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="27daa-174">Export data from the current database into a Microsoft Excel 97 file.</span></span> <span data-ttu-id="27daa-175">В этом будут перезаписаны данные при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="27daa-175">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27daa-176">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="27daa-176">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="27daa-177">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27daa-177">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27daa-178">01</span><span class="sxs-lookup"><span data-stu-id="27daa-178">01</span></span></p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> <span data-ttu-id="27daa-179">При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="27daa-179">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

<span data-ttu-id="27daa-180"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="27daa-180"><<<<<<< HEAD</span></span>

=======
## <a name="see-also"></a><span data-ttu-id="27daa-181">См. также</span><span class="sxs-lookup"><span data-stu-id="27daa-181">See also</span></span>

[<span data-ttu-id="27daa-182">С помощью параметра TypeGuessRows драйвера Excel</span><span class="sxs-lookup"><span data-stu-id="27daa-182">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
>>>>>>> <span data-ttu-id="27daa-183">master</span><span class="sxs-lookup"><span data-stu-id="27daa-183">master</span></span>
