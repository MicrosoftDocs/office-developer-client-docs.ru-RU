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
localization_priority: Normal
ms.openlocfilehash: cec7890385e5730831cea9241278511d88b6f3a1
ms.sourcegitcommit: 8ead5b5501f59c108cf02969070be21f7fc52467
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/21/2019
ms.locfileid: "30135749"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="564df-102">Инициализация драйвера Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="564df-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="564df-103">Область **применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="564df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="564df-104">При установке драйвера Excel программа установки записывает набор значений по умолчанию в реестр Windows в подразделах Engines и ISAM formats.</span><span class="sxs-lookup"><span data-stu-id="564df-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="564df-105">Эти параметры не следует изменять напрямую; Используйте программу установки приложения, чтобы добавлять, удалять или изменять эти параметры.</span><span class="sxs-lookup"><span data-stu-id="564df-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="564df-106">В следующих разделах описываются параметры инициализации и ISAM Format для драйвера базы данных Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="564df-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="564df-107">Параметры инициализации Excel</span><span class="sxs-lookup"><span data-stu-id="564df-107">Excel initialization settings</span></span>

<span data-ttu-id="564df-108">Папка **\\Excel Engines\\Engine** включает параметры инициализации для драйвера ацеекскл. dll, который используется для внешнего доступа к листам Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="564df-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="564df-109">Типичные параметры записей в этой папке показаны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="564df-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="564df-110">Ядро СУБД Microsoft Access использует записи папки Excel, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="564df-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="564df-111">Запись</span><span class="sxs-lookup"><span data-stu-id="564df-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="564df-112">Описание</span><span class="sxs-lookup"><span data-stu-id="564df-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="564df-113">оригиналь</span><span class="sxs-lookup"><span data-stu-id="564df-113">win32</span></span></p></td>
<td><p><span data-ttu-id="564df-114">Расположение файла msexcl40. dll.</span><span class="sxs-lookup"><span data-stu-id="564df-114">The location of msexcl40.dll.</span></span> <span data-ttu-id="564df-115">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="564df-115">The full path is determined at the time of installation.</span></span> <span data-ttu-id="564df-116">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="564df-116">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="564df-117">Типегуессровс</span><span class="sxs-lookup"><span data-stu-id="564df-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="564df-118">Количество строк, проверяемых для типа данных.</span><span class="sxs-lookup"><span data-stu-id="564df-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="564df-119">Тип данных определяется с учетом максимального числа найденных типов данных.</span><span class="sxs-lookup"><span data-stu-id="564df-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="564df-120">Если задано значение, тип данных определяется в следующем порядке: Number, Currency, Date, Text, Boolean.</span><span class="sxs-lookup"><span data-stu-id="564df-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="564df-121">Если обнаружены данные, которые не совпадают с типом данных, предполагаемым для столбца, то возвращается значение <strong>null</strong> .</span><span class="sxs-lookup"><span data-stu-id="564df-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="564df-122">При импорте, если столбец содержит смешанные типы данных, весь столбец будет приведен в соответствии с параметром Импортмикседтипес.</span><span class="sxs-lookup"><span data-stu-id="564df-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="564df-123">По умолчанию число проверяемых строк равно 8.</span><span class="sxs-lookup"><span data-stu-id="564df-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="564df-124">Значения имеют тип REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="564df-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="564df-125">Импортмикседтипес</span><span class="sxs-lookup"><span data-stu-id="564df-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="564df-126">Может быть задано значение Мажорититипе или Text.</span><span class="sxs-lookup"><span data-stu-id="564df-126">Can be set to MajorityType or Text.</span></span> <span data-ttu-id="564df-127">Если задано значение Мажорититипе, столбцы смешанных типов данных будут приведены к типу данных предоминате при импорте.</span><span class="sxs-lookup"><span data-stu-id="564df-127">If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import.</span></span> <span data-ttu-id="564df-128">Если для параметра задано значение Text, при импорте столбцы смешанных типов данных будут приведены к типу text (текст).</span><span class="sxs-lookup"><span data-stu-id="564df-128">If set to Text, columns of mixed data types will be cast to Text on import.</span></span> <span data-ttu-id="564df-129">Значение по умолчанию — Text.</span><span class="sxs-lookup"><span data-stu-id="564df-129">The default is Text.</span></span> <span data-ttu-id="564df-130">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="564df-130">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="564df-131">Аппендбланкровс</span><span class="sxs-lookup"><span data-stu-id="564df-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="564df-132">Число пустых строк, добавляемых в конец листа версии 3,5 или версии 4,0 перед добавлением новых данных.</span><span class="sxs-lookup"><span data-stu-id="564df-132">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added.</span></span> <span data-ttu-id="564df-133">Например, если для Аппендбланкровс задано значение 4, Microsoft Jet добавит 4 пустые строки в конец листа перед добавлением строк, содержащих данные.</span><span class="sxs-lookup"><span data-stu-id="564df-133">For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data.</span></span> <span data-ttu-id="564df-134">Целочисленные значения этого параметра могут изменяться в диапазоне от 0 до 16; значение по умолчанию — 01 (добавляется одна дополнительная строка).</span><span class="sxs-lookup"><span data-stu-id="564df-134">Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended).</span></span> <span data-ttu-id="564df-135">Значения имеют тип REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="564df-135">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="564df-136">Фирстровхаснамес</span><span class="sxs-lookup"><span data-stu-id="564df-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="564df-137">Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="564df-137">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="564df-138">Значение 01 указывает, что во время импорта имена столбцов берутся из первой строки.</span><span class="sxs-lookup"><span data-stu-id="564df-138">A value of 01 indicates that, during import, column names are taken from the first row.</span></span> <span data-ttu-id="564df-139">Значение 00 указывает, что в первой строке нет имен столбцов; имена столбцов отображаются в виде F1, F2, F3 и т. д.</span><span class="sxs-lookup"><span data-stu-id="564df-139">A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on.</span></span> <span data-ttu-id="564df-140">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="564df-140">The default is 01.</span></span> <span data-ttu-id="564df-141">Значения имеют тип REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="564df-141">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="564df-142">Папка **\\Excel 8,0 Engine\\Engines Engine** содержит следующие записи, которые относятся к Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="564df-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="564df-143">Имя записи</span><span class="sxs-lookup"><span data-stu-id="564df-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="564df-144">Тип</span><span class="sxs-lookup"><span data-stu-id="564df-144">Type</span></span></p></th>
<th><p><span data-ttu-id="564df-145">Значение</span><span class="sxs-lookup"><span data-stu-id="564df-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="564df-146">Модул</span><span class="sxs-lookup"><span data-stu-id="564df-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="564df-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="564df-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="564df-148">Excel</span><span class="sxs-lookup"><span data-stu-id="564df-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="564df-149">Експортфилтер</span><span class="sxs-lookup"><span data-stu-id="564df-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="564df-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="564df-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="564df-151">Microsoft Excel 97-2000 (\*. xls)</span><span class="sxs-lookup"><span data-stu-id="564df-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="564df-152">Канлинк</span><span class="sxs-lookup"><span data-stu-id="564df-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="564df-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="564df-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="564df-154">01</span><span class="sxs-lookup"><span data-stu-id="564df-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="564df-155">Онетаблеперфиле</span><span class="sxs-lookup"><span data-stu-id="564df-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="564df-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="564df-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="564df-157">00</span><span class="sxs-lookup"><span data-stu-id="564df-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="564df-158">Исамтипе</span><span class="sxs-lookup"><span data-stu-id="564df-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="564df-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="564df-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="564df-160">1,1</span><span class="sxs-lookup"><span data-stu-id="564df-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="564df-161">Индексдиалог</span><span class="sxs-lookup"><span data-stu-id="564df-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="564df-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="564df-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="564df-163">00</span><span class="sxs-lookup"><span data-stu-id="564df-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="564df-164">Креатедбонекспорт</span><span class="sxs-lookup"><span data-stu-id="564df-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="564df-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="564df-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="564df-166">01</span><span class="sxs-lookup"><span data-stu-id="564df-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="564df-167">Ресулттекстекспорт</span><span class="sxs-lookup"><span data-stu-id="564df-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="564df-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="564df-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="564df-169">Экспорт данных из текущей базы данных в файл Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="564df-169">Export data from the current database into a Microsoft Excel 97 file.</span></span> <span data-ttu-id="564df-170">При этом данные будут перезаписаны при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="564df-170">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="564df-171">Суппортслонгнамес</span><span class="sxs-lookup"><span data-stu-id="564df-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="564df-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="564df-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="564df-173">01</span><span class="sxs-lookup"><span data-stu-id="564df-173">01</span></span></p></td>
</tr>
</tbody>
</table>

## <a name="using-the-typeguessrows-setting-for-excel-driver"></a><span data-ttu-id="564df-174">Использование параметра Типегуессровс для драйвера Excel</span><span class="sxs-lookup"><span data-stu-id="564df-174">Using the TypeGuessRows setting for Excel Driver</span></span>
<span data-ttu-id="564df-175">При использовании драйвера Microsoft Excel можно указать количество строк, проверяемых для типа данных, с помощью значения реестра **типегуессровс** .</span><span class="sxs-lookup"><span data-stu-id="564df-175">When you use Microsoft Excel Driver, you can use the **TypeGuessRows** registry value to configure how many rows are to be checked for the data type.</span></span> <span data-ttu-id="564df-176">Значение **типегуессровс** находится в следующем подразделе реестра:</span><span class="sxs-lookup"><span data-stu-id="564df-176">The **TypeGuessRows** value is located under the following registry subkey:</span></span>

# <a name="office-2016taboffice-2016"></a>[<span data-ttu-id="564df-177">Office 2016</span><span class="sxs-lookup"><span data-stu-id="564df-177">Office 2016</span></span>](#tab/office-2016)

<span data-ttu-id="564df-178">Для установки пакета Office для MSI</span><span class="sxs-lookup"><span data-stu-id="564df-178">For an MSI installation of Office</span></span>

- <span data-ttu-id="564df-179">Для 32 — разрядная версия Office в 32 — разрядная версия Windows или 64 — разрядная версия для Windows:</span><span class="sxs-lookup"><span data-stu-id="564df-179">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="564df-180">**Подключение к HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Енгине\енгинес\ексцел**</span><span class="sxs-lookup"><span data-stu-id="564df-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="564df-181">Для 32 — разрядная версия Office в 64 — разрядная версия Windows:</span><span class="sxs-lookup"><span data-stu-id="564df-181">For 32-bit Office on 64-bit Windows:</span></span>

  <span data-ttu-id="564df-182">**Подключение к HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Енгине\енгинес\ексцел**</span><span class="sxs-lookup"><span data-stu-id="564df-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>
    
<span data-ttu-id="564df-183">Установка Office "нажми и работай"</span><span class="sxs-lookup"><span data-stu-id="564df-183">For a Click-to-Run installation of Office</span></span>

- <span data-ttu-id="564df-184">Для 32 — разрядная версия Office в 32 — разрядная версия Windows или 64 — разрядная версия для Windows:</span><span class="sxs-lookup"><span data-stu-id="564df-184">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="564df-185">**Подключение к HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Енгине\енгинес\ексцел**</span><span class="sxs-lookup"><span data-stu-id="564df-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="564df-186">Для 32 — разрядная версия Office в 64 — разрядная версия Windows:</span><span class="sxs-lookup"><span data-stu-id="564df-186">For 32-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="564df-187">**Подключение к HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Енгине\енгинес\ексцел**</span><span class="sxs-lookup"><span data-stu-id="564df-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="564df-188">Значение по умолчанию для проверяемых строк равно **8** (8).</span><span class="sxs-lookup"><span data-stu-id="564df-188">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="564df-189">Если для параметра **типегуессровс** задано значение **0** (ноль), драйвер Excel проверяет первые 16 384 строк для типа данных.</span><span class="sxs-lookup"><span data-stu-id="564df-189">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="564df-190">Если требуется проверить более 16 384 строк, задайте для параметра **типегуессровс** значение в соответствии с требуемым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="564df-190">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="564df-191">Чтобы проверить все строки, задайте для параметра **типегуессровс** значение 1 048 576 (максимально допустимое число строк в Excel).</span><span class="sxs-lookup"><span data-stu-id="564df-191">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="564df-192">Тип данных определяется максимальным количеством найденных типов данных.</span><span class="sxs-lookup"><span data-stu-id="564df-192">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="564df-193">Если задано значение, тип данных определяется в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="564df-193">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="564df-194">Число.</span><span class="sxs-lookup"><span data-stu-id="564df-194">Number</span></span>
- <span data-ttu-id="564df-195">Денежные единицы.</span><span class="sxs-lookup"><span data-stu-id="564df-195">Currency</span></span>
- <span data-ttu-id="564df-196">Дата</span><span class="sxs-lookup"><span data-stu-id="564df-196">Date</span></span>
- <span data-ttu-id="564df-197">Текст</span><span class="sxs-lookup"><span data-stu-id="564df-197">Text</span></span>
- <span data-ttu-id="564df-198">Логический</span><span class="sxs-lookup"><span data-stu-id="564df-198">Boolean</span></span>

<span data-ttu-id="564df-199">Если обнаружены данные, которые не совпадают с предполагаемым типом данных для столбца, эти данные возвращаются в виде значения **null** .</span><span class="sxs-lookup"><span data-stu-id="564df-199">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="564df-200">При импорте, если столбец содержит смешанные типы данных, столбец целиком приводится к типу данных, заданному параметром **импортмикседтипес** .</span><span class="sxs-lookup"><span data-stu-id="564df-200">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2013taboffice-2013"></a>[<span data-ttu-id="564df-201">Office 2013</span><span class="sxs-lookup"><span data-stu-id="564df-201">Office 2013</span></span>](#tab/office-2013)

<span data-ttu-id="564df-202">Для 32 — разрядная версия Office в 32 — разрядная версия Windows или 64 — разрядная версия для Windows:</span><span class="sxs-lookup"><span data-stu-id="564df-202">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="564df-203">**Подключение к HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Енгине\енгинес\ексцел**</span><span class="sxs-lookup"><span data-stu-id="564df-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="564df-204">Для 32 — разрядная версия Office в 64 — разрядная версия Windows:</span><span class="sxs-lookup"><span data-stu-id="564df-204">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="564df-205">**Подключение к HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Енгине\енгинес\ексцел**</span><span class="sxs-lookup"><span data-stu-id="564df-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="564df-206">Значение по умолчанию для проверяемых строк равно **8** (8).</span><span class="sxs-lookup"><span data-stu-id="564df-206">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="564df-207">Если для параметра **типегуессровс** задано значение **0** (ноль), драйвер Excel проверяет первые 16 384 строк для типа данных.</span><span class="sxs-lookup"><span data-stu-id="564df-207">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="564df-208">Если требуется проверить более 16 384 строк, задайте для параметра **типегуессровс** значение в соответствии с требуемым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="564df-208">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="564df-209">Чтобы проверить все строки, задайте для параметра **типегуессровс** значение 1 048 576 (максимально допустимое число строк в Excel).</span><span class="sxs-lookup"><span data-stu-id="564df-209">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="564df-210">Тип данных определяется максимальным количеством найденных типов данных.</span><span class="sxs-lookup"><span data-stu-id="564df-210">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="564df-211">Если задано значение, тип данных определяется в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="564df-211">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="564df-212">Число.</span><span class="sxs-lookup"><span data-stu-id="564df-212">Number</span></span>
- <span data-ttu-id="564df-213">Денежные единицы.</span><span class="sxs-lookup"><span data-stu-id="564df-213">Currency</span></span>
- <span data-ttu-id="564df-214">Дата</span><span class="sxs-lookup"><span data-stu-id="564df-214">Date</span></span>
- <span data-ttu-id="564df-215">Текст</span><span class="sxs-lookup"><span data-stu-id="564df-215">Text</span></span>
- <span data-ttu-id="564df-216">Логический</span><span class="sxs-lookup"><span data-stu-id="564df-216">Boolean</span></span>

<span data-ttu-id="564df-217">Если обнаружены данные, которые не совпадают с предполагаемым типом данных для столбца, эти данные возвращаются в виде значения **null** .</span><span class="sxs-lookup"><span data-stu-id="564df-217">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="564df-218">При импорте, если столбец содержит смешанные типы данных, столбец целиком приводится к типу данных, заданному параметром **импортмикседтипес** .</span><span class="sxs-lookup"><span data-stu-id="564df-218">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2010taboffice-2010"></a>[<span data-ttu-id="564df-219">Office 2010</span><span class="sxs-lookup"><span data-stu-id="564df-219">Office 2010</span></span>](#tab/office-2010)

<span data-ttu-id="564df-220">Для 32 — разрядная версия Office в 32 — разрядная версия Windows или 64 — разрядная версия для Windows:</span><span class="sxs-lookup"><span data-stu-id="564df-220">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="564df-221">**Подключение к HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Енгине\енгинес\ексцел**</span><span class="sxs-lookup"><span data-stu-id="564df-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="564df-222">Для 32 — разрядная версия Office в 64 — разрядная версия Windows:</span><span class="sxs-lookup"><span data-stu-id="564df-222">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="564df-223">**Подключение к HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Енгине\енгинес\ексцел**</span><span class="sxs-lookup"><span data-stu-id="564df-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="564df-224">Значение по умолчанию для проверяемых строк равно **8** (8).</span><span class="sxs-lookup"><span data-stu-id="564df-224">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="564df-225">Если для параметра **типегуессровс** задано значение **0** (ноль), драйвер Excel проверяет первые 16 384 строк для типа данных.</span><span class="sxs-lookup"><span data-stu-id="564df-225">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="564df-226">Если требуется проверить более 16 384 строк, задайте для параметра **типегуессровс** значение в соответствии с требуемым диапазоном.</span><span class="sxs-lookup"><span data-stu-id="564df-226">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="564df-227">Чтобы проверить все строки, задайте для параметра **типегуессровс** значение 1 048 576 (максимально допустимое число строк в Excel).</span><span class="sxs-lookup"><span data-stu-id="564df-227">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="564df-228">Тип данных определяется максимальным количеством найденных типов данных.</span><span class="sxs-lookup"><span data-stu-id="564df-228">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="564df-229">Если задано значение, тип данных определяется в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="564df-229">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="564df-230">Число.</span><span class="sxs-lookup"><span data-stu-id="564df-230">Number</span></span>
- <span data-ttu-id="564df-231">Денежные единицы.</span><span class="sxs-lookup"><span data-stu-id="564df-231">Currency</span></span>
- <span data-ttu-id="564df-232">Дата</span><span class="sxs-lookup"><span data-stu-id="564df-232">Date</span></span>
- <span data-ttu-id="564df-233">Текст</span><span class="sxs-lookup"><span data-stu-id="564df-233">Text</span></span>
- <span data-ttu-id="564df-234">Логический</span><span class="sxs-lookup"><span data-stu-id="564df-234">Boolean</span></span>

<span data-ttu-id="564df-235">Если обнаружены данные, которые не совпадают с предполагаемым типом данных для столбца, эти данные возвращаются в виде значения **null** .</span><span class="sxs-lookup"><span data-stu-id="564df-235">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="564df-236">При импорте, если столбец содержит смешанные типы данных, столбец целиком приводится к типу данных, заданному параметром **импортмикседтипес** .</span><span class="sxs-lookup"><span data-stu-id="564df-236">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

---
> [!NOTE]
> <span data-ttu-id="564df-237">При изменении параметров реестра Windows необходимо выйти и перезапустить ядро СУБД, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="564df-237">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="564df-238">См. также</span><span class="sxs-lookup"><span data-stu-id="564df-238">See also</span></span>

- [<span data-ttu-id="564df-239">Использование параметра Типегуессровс для драйвера Excel</span><span class="sxs-lookup"><span data-stu-id="564df-239">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)
