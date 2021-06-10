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
ms.openlocfilehash: c3424fd4b85108120ea4accc2dfa65d55394f0d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291437"
---
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="36ca0-102">Инициализация драйвера Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="36ca0-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="36ca0-103">**Применяется к**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office для бизнеса Access 2013 | Excel 2010 | Access 2010</span><span class="sxs-lookup"><span data-stu-id="36ca0-103">**Applies to**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office for business Access 2013 | Excel 2010 | Access 2010</span></span>

<span data-ttu-id="36ca0-104">При установке Excel драйвера программа установки записывает набор значений по умолчанию в реестр Windows в подкайлах Engines и ISAM Formats.</span><span class="sxs-lookup"><span data-stu-id="36ca0-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="36ca0-105">Не следует изменять эти параметры напрямую; используйте программу установки для приложения, чтобы добавить, удалить или изменить эти параметры.</span><span class="sxs-lookup"><span data-stu-id="36ca0-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="36ca0-106">В следующих разделах описываются параметры инициализации и формата ISAM для драйвера Microsoft Excel базы данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="36ca0-107">Excel параметров инициализации</span><span class="sxs-lookup"><span data-stu-id="36ca0-107">Excel initialization settings</span></span>

<span data-ttu-id="36ca0-108">Папка **\\ Engines \\ Excel access Connectivity Engines** включает параметры инициализации драйвера Aceexcl.dll, используемой для внешнего доступа к Microsoft Excel таблицам.</span><span class="sxs-lookup"><span data-stu-id="36ca0-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="36ca0-109">Типичные параметры для записей в этой папке показаны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="36ca0-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="36ca0-110">В движке базы данных Microsoft Access Excel записи папок следующим образом.</span><span class="sxs-lookup"><span data-stu-id="36ca0-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36ca0-111">Запись</span><span class="sxs-lookup"><span data-stu-id="36ca0-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="36ca0-112">Description</span><span class="sxs-lookup"><span data-stu-id="36ca0-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36ca0-113">win32</span><span class="sxs-lookup"><span data-stu-id="36ca0-113">win32</span></span></p></td>
<td><p><span data-ttu-id="36ca0-114">Расположение msexcl40.dll.</span><span class="sxs-lookup"><span data-stu-id="36ca0-114">The location of msexcl40.dll.</span></span> <span data-ttu-id="36ca0-115">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="36ca0-115">The full path is determined at the time of installation.</span></span> <span data-ttu-id="36ca0-116">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="36ca0-116">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ca0-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="36ca0-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="36ca0-118">Количество строк, которые необходимо проверить для типа данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="36ca0-119">Тип данных определяется с учетом максимального количества найденных данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="36ca0-120">Если есть связь, тип данных определяется в следующем порядке: Номер, Валюта, Дата, Текст, Boolean.</span><span class="sxs-lookup"><span data-stu-id="36ca0-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="36ca0-121">Если встречаются данные, которые не соответствуют типу данных, угадал для столбца, он возвращается в качестве <strong>значения Null.</strong></span><span class="sxs-lookup"><span data-stu-id="36ca0-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="36ca0-122">При импорте, если столбец имеет смешанные типы данных, весь столбец будет отлит в соответствии с параметром ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="36ca0-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="36ca0-123">По умолчанию число строк, которые необходимо проверить, — 8.</span><span class="sxs-lookup"><span data-stu-id="36ca0-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="36ca0-124">Значения имеют тип REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="36ca0-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ca0-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="36ca0-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="36ca0-126">Можно установить для MajorityType или Text.</span><span class="sxs-lookup"><span data-stu-id="36ca0-126">Can be set to MajorityType or Text.</span></span> <span data-ttu-id="36ca0-127">Если задатки для MajorityType, столбцы смешанных типов данных будут отбрасываться к основному типу данных при импорте.</span><span class="sxs-lookup"><span data-stu-id="36ca0-127">If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import.</span></span> <span data-ttu-id="36ca0-128">Если заостряется на тексте, столбцы смешанных типов данных будут отбрасаны в Текст по импорту.</span><span class="sxs-lookup"><span data-stu-id="36ca0-128">If set to Text, columns of mixed data types will be cast to Text on import.</span></span> <span data-ttu-id="36ca0-129">По умолчанию — Текст.</span><span class="sxs-lookup"><span data-stu-id="36ca0-129">The default is Text.</span></span> <span data-ttu-id="36ca0-130">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="36ca0-130">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ca0-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="36ca0-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="36ca0-132">Количество пустых строк, которые должны быть добавлены до конца листа версии 3.5 или Версии 4.0 перед добавлением новых данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-132">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added.</span></span> <span data-ttu-id="36ca0-133">Например, если в AppendBlankRows установлено 4 строки, Microsoft Jet пристроит 4 пустых строки к концу листа перед тем, как примкнуть к строкам с данными.</span><span class="sxs-lookup"><span data-stu-id="36ca0-133">For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data.</span></span> <span data-ttu-id="36ca0-134">Значения для этого параметра могут варьироваться от 0 до 16; по умолчанию — 01 (одна дополнительная строка.</span><span class="sxs-lookup"><span data-stu-id="36ca0-134">Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended).</span></span> <span data-ttu-id="36ca0-135">Значения имеют тип REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="36ca0-135">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ca0-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="36ca0-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="36ca0-137">Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="36ca0-137">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="36ca0-138">Значение 01 указывает, что во время импорта из первой строки будут взяты имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="36ca0-138">A value of 01 indicates that, during import, column names are taken from the first row.</span></span> <span data-ttu-id="36ca0-139">Значение 00 не указывает имен столбцов в первом ряду; Имена столбцов отображаются как F1, F2, F3 и так далее.</span><span class="sxs-lookup"><span data-stu-id="36ca0-139">A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on.</span></span> <span data-ttu-id="36ca0-140">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="36ca0-140">The default is 01.</span></span> <span data-ttu-id="36ca0-141">Значения имеют тип REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="36ca0-141">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="36ca0-142">Папка **\\ Engines \\ Excel 8.0** содержит следующие записи, применимые к Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="36ca0-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36ca0-143">Имя входа</span><span class="sxs-lookup"><span data-stu-id="36ca0-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="36ca0-144">Тип</span><span class="sxs-lookup"><span data-stu-id="36ca0-144">Type</span></span></p></th>
<th><p><span data-ttu-id="36ca0-145">Значение</span><span class="sxs-lookup"><span data-stu-id="36ca0-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36ca0-146">Двигатель</span><span class="sxs-lookup"><span data-stu-id="36ca0-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="36ca0-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="36ca0-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="36ca0-148">Excel</span><span class="sxs-lookup"><span data-stu-id="36ca0-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ca0-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="36ca0-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="36ca0-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="36ca0-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="36ca0-151">Microsoft Excel 97-2000 (\*.xls)</span><span class="sxs-lookup"><span data-stu-id="36ca0-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ca0-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="36ca0-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="36ca0-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="36ca0-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="36ca0-154">01</span><span class="sxs-lookup"><span data-stu-id="36ca0-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ca0-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="36ca0-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="36ca0-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="36ca0-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="36ca0-157">00</span><span class="sxs-lookup"><span data-stu-id="36ca0-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ca0-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="36ca0-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="36ca0-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="36ca0-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="36ca0-160">1</span><span class="sxs-lookup"><span data-stu-id="36ca0-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ca0-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="36ca0-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="36ca0-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="36ca0-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="36ca0-163">00</span><span class="sxs-lookup"><span data-stu-id="36ca0-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ca0-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="36ca0-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="36ca0-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="36ca0-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="36ca0-166">01</span><span class="sxs-lookup"><span data-stu-id="36ca0-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36ca0-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="36ca0-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="36ca0-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="36ca0-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="36ca0-169">Экспорт данных из текущей базы данных в файл Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="36ca0-169">Export data from the current database into a Microsoft Excel 97 file.</span></span> <span data-ttu-id="36ca0-170">Этот процесс переопишет данные, если они будут экспортироваться в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="36ca0-170">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36ca0-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="36ca0-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="36ca0-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="36ca0-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="36ca0-173">01</span><span class="sxs-lookup"><span data-stu-id="36ca0-173">01</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a><span data-ttu-id="36ca0-174">Использование параметра TypeGuessRows для Excel драйвера</span><span class="sxs-lookup"><span data-stu-id="36ca0-174">Using the TypeGuessRows setting for Excel Driver</span></span>
<span data-ttu-id="36ca0-175">При использовании Microsoft Excel драйвера можно использовать значение **реестра TypeGuessRows,** чтобы настроить количество строк для проверки типа данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-175">When you use Microsoft Excel Driver, you can use the **TypeGuessRows** registry value to configure how many rows are to be checked for the data type.</span></span> <span data-ttu-id="36ca0-176">Значение **TypeGuessRows** расположено в следующем подкайке реестра:</span><span class="sxs-lookup"><span data-stu-id="36ca0-176">The **TypeGuessRows** value is located under the following registry subkey:</span></span>

# <a name="office-2016"></a>[<span data-ttu-id="36ca0-177">Office 2016</span><span class="sxs-lookup"><span data-stu-id="36ca0-177">Office 2016</span></span>](#tab/office-2016)

<span data-ttu-id="36ca0-178">Для установки MSI Office</span><span class="sxs-lookup"><span data-stu-id="36ca0-178">For an MSI installation of Office</span></span>

- <span data-ttu-id="36ca0-179">Для 32-битных Office 32-Windows или 64-Office 64-битных Windows:</span><span class="sxs-lookup"><span data-stu-id="36ca0-179">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="36ca0-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="36ca0-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="36ca0-181">Для 32-Office 64-битных Windows:</span><span class="sxs-lookup"><span data-stu-id="36ca0-181">For 32-bit Office on 64-bit Windows:</span></span>

  <span data-ttu-id="36ca0-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="36ca0-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>
    
<span data-ttu-id="36ca0-183">Для установки нажатие кнопки на запуск Office</span><span class="sxs-lookup"><span data-stu-id="36ca0-183">For a Click-to-Run installation of Office</span></span>

- <span data-ttu-id="36ca0-184">Для 32-битных Office 32-Windows или 64-Office 64-битных Windows:</span><span class="sxs-lookup"><span data-stu-id="36ca0-184">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="36ca0-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="36ca0-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="36ca0-186">Для 32-Office 64-битных Windows:</span><span class="sxs-lookup"><span data-stu-id="36ca0-186">For 32-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="36ca0-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="36ca0-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="36ca0-188">По умолчанию количество строк, которые необходимо проверить, **— 8** (восемь).</span><span class="sxs-lookup"><span data-stu-id="36ca0-188">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="36ca0-189">Если значение **TypeGuessRows** установлено до **0** (ноль), Excel драйвер проверяет первые 16 384 строк для типа данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-189">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="36ca0-190">Если требуется проверить более 16 384 строк, установите **TypeGuessRows** значение, основанное на желаемом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="36ca0-190">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="36ca0-191">Чтобы проверить все строки, установите **TypeGuessRows** до 1 048 576 (максимальное количество строк, разрешенных в Excel).</span><span class="sxs-lookup"><span data-stu-id="36ca0-191">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="36ca0-192">Тип данных определяется максимальным количеством найденных данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-192">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="36ca0-193">Если имеется связь, тип данных определяется в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="36ca0-193">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="36ca0-194">Номер</span><span class="sxs-lookup"><span data-stu-id="36ca0-194">Number</span></span>
- <span data-ttu-id="36ca0-195">Денежный</span><span class="sxs-lookup"><span data-stu-id="36ca0-195">Currency</span></span>
- <span data-ttu-id="36ca0-196">Date</span><span class="sxs-lookup"><span data-stu-id="36ca0-196">Date</span></span>
- <span data-ttu-id="36ca0-197">Текст</span><span class="sxs-lookup"><span data-stu-id="36ca0-197">Text</span></span>
- <span data-ttu-id="36ca0-198">Boolean</span><span class="sxs-lookup"><span data-stu-id="36ca0-198">Boolean</span></span>

<span data-ttu-id="36ca0-199">Если встречаются данные, которые не совпадают с угадалным типом данных для столбца, эти данные возвращаются в виде **значения Null.**</span><span class="sxs-lookup"><span data-stu-id="36ca0-199">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="36ca0-200">При импорте, если столбец имеет смешанные типы данных, весь столбец отбрасируется к типу данных, за набору **параметра ImportMixedTypes.**</span><span class="sxs-lookup"><span data-stu-id="36ca0-200">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2013"></a>[<span data-ttu-id="36ca0-201">Office 2013</span><span class="sxs-lookup"><span data-stu-id="36ca0-201">Office 2013</span></span>](#tab/office-2013)

<span data-ttu-id="36ca0-202">Для 32-битных Office 32-Windows или 64-Office 64-битных Windows:</span><span class="sxs-lookup"><span data-stu-id="36ca0-202">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="36ca0-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="36ca0-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="36ca0-204">Для 32-Office 64-битных Windows:</span><span class="sxs-lookup"><span data-stu-id="36ca0-204">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="36ca0-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="36ca0-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="36ca0-206">По умолчанию количество строк, которые необходимо проверить, **— 8** (восемь).</span><span class="sxs-lookup"><span data-stu-id="36ca0-206">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="36ca0-207">Если значение **TypeGuessRows** установлено до **0** (ноль), Excel драйвер проверяет первые 16 384 строк для типа данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-207">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="36ca0-208">Если требуется проверить более 16 384 строк, установите **TypeGuessRows** значение, основанное на желаемом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="36ca0-208">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="36ca0-209">Чтобы проверить все строки, установите **TypeGuessRows** до 1 048 576 (максимальное количество строк, разрешенных в Excel).</span><span class="sxs-lookup"><span data-stu-id="36ca0-209">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="36ca0-210">Тип данных определяется максимальным количеством найденных данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-210">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="36ca0-211">Если имеется связь, тип данных определяется в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="36ca0-211">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="36ca0-212">Номер</span><span class="sxs-lookup"><span data-stu-id="36ca0-212">Number</span></span>
- <span data-ttu-id="36ca0-213">Денежный</span><span class="sxs-lookup"><span data-stu-id="36ca0-213">Currency</span></span>
- <span data-ttu-id="36ca0-214">Date</span><span class="sxs-lookup"><span data-stu-id="36ca0-214">Date</span></span>
- <span data-ttu-id="36ca0-215">Текст</span><span class="sxs-lookup"><span data-stu-id="36ca0-215">Text</span></span>
- <span data-ttu-id="36ca0-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="36ca0-216">Boolean</span></span>

<span data-ttu-id="36ca0-217">Если встречаются данные, которые не совпадают с угадалным типом данных для столбца, эти данные возвращаются в виде **значения Null.**</span><span class="sxs-lookup"><span data-stu-id="36ca0-217">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="36ca0-218">При импорте, если столбец имеет смешанные типы данных, весь столбец отбрасируется к типу данных, за набору **параметра ImportMixedTypes.**</span><span class="sxs-lookup"><span data-stu-id="36ca0-218">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2010"></a>[<span data-ttu-id="36ca0-219">Office 2010</span><span class="sxs-lookup"><span data-stu-id="36ca0-219">Office 2010</span></span>](#tab/office-2010)

<span data-ttu-id="36ca0-220">Для 32-битных Office 32-Windows или 64-Office 64-битных Windows:</span><span class="sxs-lookup"><span data-stu-id="36ca0-220">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="36ca0-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="36ca0-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="36ca0-222">Для 32-Office 64-битных Windows:</span><span class="sxs-lookup"><span data-stu-id="36ca0-222">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="36ca0-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="36ca0-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="36ca0-224">По умолчанию количество строк, которые необходимо проверить, **— 8** (восемь).</span><span class="sxs-lookup"><span data-stu-id="36ca0-224">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="36ca0-225">Если значение **TypeGuessRows** установлено до **0** (ноль), Excel драйвер проверяет первые 16 384 строк для типа данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-225">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="36ca0-226">Если требуется проверить более 16 384 строк, установите **TypeGuessRows** значение, основанное на желаемом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="36ca0-226">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="36ca0-227">Чтобы проверить все строки, установите **TypeGuessRows** до 1 048 576 (максимальное количество строк, разрешенных в Excel).</span><span class="sxs-lookup"><span data-stu-id="36ca0-227">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="36ca0-228">Тип данных определяется максимальным количеством найденных данных.</span><span class="sxs-lookup"><span data-stu-id="36ca0-228">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="36ca0-229">Если имеется связь, тип данных определяется в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="36ca0-229">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="36ca0-230">Номер</span><span class="sxs-lookup"><span data-stu-id="36ca0-230">Number</span></span>
- <span data-ttu-id="36ca0-231">Денежный</span><span class="sxs-lookup"><span data-stu-id="36ca0-231">Currency</span></span>
- <span data-ttu-id="36ca0-232">Date</span><span class="sxs-lookup"><span data-stu-id="36ca0-232">Date</span></span>
- <span data-ttu-id="36ca0-233">Текст</span><span class="sxs-lookup"><span data-stu-id="36ca0-233">Text</span></span>
- <span data-ttu-id="36ca0-234">Boolean</span><span class="sxs-lookup"><span data-stu-id="36ca0-234">Boolean</span></span>

<span data-ttu-id="36ca0-235">Если встречаются данные, которые не совпадают с угадалным типом данных для столбца, эти данные возвращаются в виде **значения Null.**</span><span class="sxs-lookup"><span data-stu-id="36ca0-235">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="36ca0-236">При импорте, если столбец имеет смешанные типы данных, весь столбец отбрасируется к типу данных, за набору **параметра ImportMixedTypes.**</span><span class="sxs-lookup"><span data-stu-id="36ca0-236">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

---
> [!NOTE]
> <span data-ttu-id="36ca0-237">При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="36ca0-237">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="36ca0-238">См. также</span><span class="sxs-lookup"><span data-stu-id="36ca0-238">See also</span></span>

- [<span data-ttu-id="36ca0-239">Использование параметра TypeGuessRows для Excel драйвера</span><span class="sxs-lookup"><span data-stu-id="36ca0-239">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

