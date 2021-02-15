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
# <a name="initializing-the-microsoft-excel-driver"></a><span data-ttu-id="27b82-102">Инициализация драйвера Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="27b82-102">Initializing the Microsoft Excel driver</span></span>

<span data-ttu-id="27b82-103">**Применимо к**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office для бизнеса Access 2013 | Excel 2010 | Access 2010</span><span class="sxs-lookup"><span data-stu-id="27b82-103">**Applies to**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office for business Access 2013 | Excel 2010 | Access 2010</span></span>

<span data-ttu-id="27b82-104">При установке драйвера Excel программа установки записывает набор значений по умолчанию в реестр Windows в подмайсах "Подпрограммы" и "Форматы ISAM".</span><span class="sxs-lookup"><span data-stu-id="27b82-104">When you install the Excel driver, the Setup program writes a set of default values to the Windows Registry in the Engines and ISAM Formats subkeys.</span></span> <span data-ttu-id="27b82-105">Не следует изменять эти параметры напрямую; используйте программу установки приложения для добавления, удаления или изменения этих параметров.</span><span class="sxs-lookup"><span data-stu-id="27b82-105">You should not modify these settings directly; use the setup program for your application to add, remove, or change these settings.</span></span> <span data-ttu-id="27b82-106">В следующих разделах описаны параметры инициализации и формата ISAM для драйвера базы данных Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="27b82-106">The following sections describe initialization and ISAM Format settings for the Microsoft Excel database driver.</span></span>

## <a name="excel-initialization-settings"></a><span data-ttu-id="27b82-107">Параметры инициализации Excel</span><span class="sxs-lookup"><span data-stu-id="27b82-107">Excel initialization settings</span></span>

<span data-ttu-id="27b82-108">Папка "Под управлением ядер подключения **\\ \\ Access" Excel** включает параметры инициализации драйвера Aceexcl.dll, используемой для внешнего доступа к листам Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="27b82-108">The **Access Connectivity Engine\\Engines\\Excel** folder includes initialization settings for the Aceexcl.dll driver, used for external access to Microsoft Excel worksheets.</span></span> <span data-ttu-id="27b82-109">Типичные параметры для записей в этой папке показаны в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="27b82-109">Typical settings for the entries in this folder are shown in the following example.</span></span>

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

<span data-ttu-id="27b82-110">Ядер баз данных Microsoft Access использует записи папки Excel следующим образом.</span><span class="sxs-lookup"><span data-stu-id="27b82-110">The Microsoft Access database engine uses the Excel folder entries as follows.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27b82-111">Запись</span><span class="sxs-lookup"><span data-stu-id="27b82-111">Entry</span></span></p></th>
<th><p><span data-ttu-id="27b82-112">Описание</span><span class="sxs-lookup"><span data-stu-id="27b82-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27b82-113">win32</span><span class="sxs-lookup"><span data-stu-id="27b82-113">win32</span></span></p></td>
<td><p><span data-ttu-id="27b82-114">Расположение msexcl40.dll.</span><span class="sxs-lookup"><span data-stu-id="27b82-114">The location of msexcl40.dll.</span></span> <span data-ttu-id="27b82-115">Полный путь определяется во время установки.</span><span class="sxs-lookup"><span data-stu-id="27b82-115">The full path is determined at the time of installation.</span></span> <span data-ttu-id="27b82-116">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="27b82-116">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27b82-117">TypeGuessRows</span><span class="sxs-lookup"><span data-stu-id="27b82-117">TypeGuessRows</span></span></p></td>
<td><p><span data-ttu-id="27b82-118">Количество строк, проверяемого на наличие типа данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-118">The number of rows to be checked for the data type.</span></span> <span data-ttu-id="27b82-119">Тип данных определяется с учетом максимального количества найденных видов данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-119">The data type is determined given the maximum number of kinds of data found.</span></span> <span data-ttu-id="27b82-120">Если имеется связь, тип данных определяется в следующем порядке: Number, Currency, Date, Text, Boolean.</span><span class="sxs-lookup"><span data-stu-id="27b82-120">If there is a tie, the data type is determined in the following order: Number, Currency, Date, Text, Boolean.</span></span> <span data-ttu-id="27b82-121">Если встречаются данные, которые не соответствуют типу данных, угадать для столбца, он возвращается в виде <strong>значения NULL.</strong></span><span class="sxs-lookup"><span data-stu-id="27b82-121">If data is encountered that does not match the data type guessed for the column, it is returned as a <strong>Null</strong> value.</span></span> <span data-ttu-id="27b82-122">При импорте, если столбец имеет смешанные типы данных, весь столбец будет приводиться в соответствии с параметром ImportMixedTypes.</span><span class="sxs-lookup"><span data-stu-id="27b82-122">On import, if a column has mixed data types, the entire column will be cast according to the ImportMixedTypes setting.</span></span> <span data-ttu-id="27b82-123">По умолчанию проверяемая строка имеет значение 8.</span><span class="sxs-lookup"><span data-stu-id="27b82-123">The default number of rows to be checked is 8.</span></span> <span data-ttu-id="27b82-124">Значения имеют тип REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="27b82-124">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27b82-125">ImportMixedTypes</span><span class="sxs-lookup"><span data-stu-id="27b82-125">ImportMixedTypes</span></span></p></td>
<td><p><span data-ttu-id="27b82-126">Может иметь тип MajorityType или Text.</span><span class="sxs-lookup"><span data-stu-id="27b82-126">Can be set to MajorityType or Text.</span></span> <span data-ttu-id="27b82-127">Если этот тип имеет тип MajorityType, столбцы смешанных типов данных будут преобразовываться к предопределему типу данных при импорте.</span><span class="sxs-lookup"><span data-stu-id="27b82-127">If set to MajorityType, columns of mixed data types will be cast to the predominate data type on import.</span></span> <span data-ttu-id="27b82-128">Если за установлено "Текст", столбцы смешанных типов данных будут при импорте привнося в текст.</span><span class="sxs-lookup"><span data-stu-id="27b82-128">If set to Text, columns of mixed data types will be cast to Text on import.</span></span> <span data-ttu-id="27b82-129">Значение по умолчанию — Text.</span><span class="sxs-lookup"><span data-stu-id="27b82-129">The default is Text.</span></span> <span data-ttu-id="27b82-130">Значения имеют тип REG_SZ.</span><span class="sxs-lookup"><span data-stu-id="27b82-130">Values are of type REG_SZ.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27b82-131">AppendBlankRows</span><span class="sxs-lookup"><span data-stu-id="27b82-131">AppendBlankRows</span></span></p></td>
<td><p><span data-ttu-id="27b82-132">Количество пустых строк, добавляемого в конец листа версии 3.5 или версии 4.0 перед добавлением новых данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-132">The number of blank rows to be appended to the end of a Version 3.5 or Version 4.0 worksheet before new data is added.</span></span> <span data-ttu-id="27b82-133">Например, если для AppendBlankRows задано 4, Microsoft Jet применет 4 пустых строки в конец листа, а не строки, содержащие данные.</span><span class="sxs-lookup"><span data-stu-id="27b82-133">For example, if AppendBlankRows is set to 4, Microsoft Jet will append 4 blank rows to the end of the worksheet before appending rows that contain data.</span></span> <span data-ttu-id="27b82-134">Значения этого параметра могут быть в диапазоне от 0 до 16; значение по умолчанию — 01 (одна дополнительная строка.</span><span class="sxs-lookup"><span data-stu-id="27b82-134">Integer values for this setting can range from 0 to 16; the default is 01 (one additional row appended).</span></span> <span data-ttu-id="27b82-135">Значения имеют тип REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="27b82-135">Values are of type REG_DWORD.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27b82-136">FirstRowHasNames</span><span class="sxs-lookup"><span data-stu-id="27b82-136">FirstRowHasNames</span></span></p></td>
<td><p><span data-ttu-id="27b82-137">Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов.</span><span class="sxs-lookup"><span data-stu-id="27b82-137">A binary value that indicates whether the first row of the table contains column names.</span></span> <span data-ttu-id="27b82-138">Значение 01 указывает, что во время импорта имена столбцов принимаются из первой строки.</span><span class="sxs-lookup"><span data-stu-id="27b82-138">A value of 01 indicates that, during import, column names are taken from the first row.</span></span> <span data-ttu-id="27b82-139">Значение 00 означает отсутствие имен столбцов в первой строке; имена столбцов отображаются как F1, F2, F3 и так далее.</span><span class="sxs-lookup"><span data-stu-id="27b82-139">A value of 00 indicates no column names in the first row; column names appear as F1, F2, F3, and so on.</span></span> <span data-ttu-id="27b82-140">Значение по умолчанию — 01.</span><span class="sxs-lookup"><span data-stu-id="27b82-140">The default is 01.</span></span> <span data-ttu-id="27b82-141">Значения имеют тип REG_BINARY.</span><span class="sxs-lookup"><span data-stu-id="27b82-141">Values are of type REG_BINARY.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>

<span data-ttu-id="27b82-142">Папка **Подмагивщика \\ подключений Access Excel \\ 8.0** содержит следующие записи, применимые к Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="27b82-142">The **Access Connectivity Engine\\Engines\\Excel 8.0** folder contains the following entries, which apply to Microsoft Excel 97.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27b82-143">Имя записи</span><span class="sxs-lookup"><span data-stu-id="27b82-143">Entry name</span></span></p></th>
<th><p><span data-ttu-id="27b82-144">Тип</span><span class="sxs-lookup"><span data-stu-id="27b82-144">Type</span></span></p></th>
<th><p><span data-ttu-id="27b82-145">Значение</span><span class="sxs-lookup"><span data-stu-id="27b82-145">Value</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27b82-146">Engine</span><span class="sxs-lookup"><span data-stu-id="27b82-146">Engine</span></span></p></td>
<td><p><span data-ttu-id="27b82-147">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="27b82-147">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="27b82-148">Excel</span><span class="sxs-lookup"><span data-stu-id="27b82-148">Excel</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27b82-149">ExportFilter</span><span class="sxs-lookup"><span data-stu-id="27b82-149">ExportFilter</span></span></p></td>
<td><p><span data-ttu-id="27b82-150">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="27b82-150">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="27b82-151">Microsoft Excel 97-2000 (XLS)</span><span class="sxs-lookup"><span data-stu-id="27b82-151">Microsoft Excel 97-2000 (\*.xls)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27b82-152">CanLink</span><span class="sxs-lookup"><span data-stu-id="27b82-152">CanLink</span></span></p></td>
<td><p><span data-ttu-id="27b82-153">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27b82-153">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27b82-154">01</span><span class="sxs-lookup"><span data-stu-id="27b82-154">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27b82-155">OneTablePerFile</span><span class="sxs-lookup"><span data-stu-id="27b82-155">OneTablePerFile</span></span></p></td>
<td><p><span data-ttu-id="27b82-156">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27b82-156">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27b82-157">00</span><span class="sxs-lookup"><span data-stu-id="27b82-157">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27b82-158">IsamType</span><span class="sxs-lookup"><span data-stu-id="27b82-158">IsamType</span></span></p></td>
<td><p><span data-ttu-id="27b82-159">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="27b82-159">REG_DWORD</span></span></p></td>
<td><p><span data-ttu-id="27b82-160">1 </span><span class="sxs-lookup"><span data-stu-id="27b82-160">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27b82-161">IndexDialog</span><span class="sxs-lookup"><span data-stu-id="27b82-161">IndexDialog</span></span></p></td>
<td><p><span data-ttu-id="27b82-162">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27b82-162">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27b82-163">00</span><span class="sxs-lookup"><span data-stu-id="27b82-163">00</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27b82-164">CreateDBOnExport</span><span class="sxs-lookup"><span data-stu-id="27b82-164">CreateDBOnExport</span></span></p></td>
<td><p><span data-ttu-id="27b82-165">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27b82-165">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27b82-166">01</span><span class="sxs-lookup"><span data-stu-id="27b82-166">01</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27b82-167">ResultTextExport</span><span class="sxs-lookup"><span data-stu-id="27b82-167">ResultTextExport</span></span></p></td>
<td><p><span data-ttu-id="27b82-168">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="27b82-168">REG_SZ</span></span></p></td>
<td><p><span data-ttu-id="27b82-169">Экспорт данных из текущей базы данных в файл Microsoft Excel 97.</span><span class="sxs-lookup"><span data-stu-id="27b82-169">Export data from the current database into a Microsoft Excel 97 file.</span></span> <span data-ttu-id="27b82-170">Этот процесс переопишет данные при экспорте в существующий файл.</span><span class="sxs-lookup"><span data-stu-id="27b82-170">This process will overwrite the data if exported to an existing file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27b82-171">SupportsLongNames</span><span class="sxs-lookup"><span data-stu-id="27b82-171">SupportsLongNames</span></span></p></td>
<td><p><span data-ttu-id="27b82-172">REG_BINARY</span><span class="sxs-lookup"><span data-stu-id="27b82-172">REG_BINARY</span></span></p></td>
<td><p><span data-ttu-id="27b82-173">01</span><span class="sxs-lookup"><span data-stu-id="27b82-173">01</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a><span data-ttu-id="27b82-174">Использование параметра TypeGuessRows для драйвера Excel</span><span class="sxs-lookup"><span data-stu-id="27b82-174">Using the TypeGuessRows setting for Excel Driver</span></span>
<span data-ttu-id="27b82-175">При использовании драйвера Microsoft Excel можно использовать значение реестра **TypeGuessRows,** чтобы настроить количество строк, проверяемых для типа данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-175">When you use Microsoft Excel Driver, you can use the **TypeGuessRows** registry value to configure how many rows are to be checked for the data type.</span></span> <span data-ttu-id="27b82-176">Значение **TypeGuessRows** находится в следующем поднайме реестра:</span><span class="sxs-lookup"><span data-stu-id="27b82-176">The **TypeGuessRows** value is located under the following registry subkey:</span></span>

# <a name="office-2016"></a>[<span data-ttu-id="27b82-177">Office 2016</span><span class="sxs-lookup"><span data-stu-id="27b82-177">Office 2016</span></span>](#tab/office-2016)

<span data-ttu-id="27b82-178">Для установки Office с MSI</span><span class="sxs-lookup"><span data-stu-id="27b82-178">For an MSI installation of Office</span></span>

- <span data-ttu-id="27b82-179">Для 32-битной версии Office в 32-битной версии Windows или 64-битной версии Office в 64-битной версии Windows:</span><span class="sxs-lookup"><span data-stu-id="27b82-179">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="27b82-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="27b82-180">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="27b82-181">Для 32-битной версии Office в 64-битной версии Windows:</span><span class="sxs-lookup"><span data-stu-id="27b82-181">For 32-bit Office on 64-bit Windows:</span></span>

  <span data-ttu-id="27b82-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="27b82-182">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>
    
<span data-ttu-id="27b82-183">Для установки Office "нажми и нажми и нажми и</span><span class="sxs-lookup"><span data-stu-id="27b82-183">For a Click-to-Run installation of Office</span></span>

- <span data-ttu-id="27b82-184">Для 32-битной версии Office в 32-битной версии Windows или 64-битной версии Office в 64-битной версии Windows:</span><span class="sxs-lookup"><span data-stu-id="27b82-184">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="27b82-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="27b82-185">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

- <span data-ttu-id="27b82-186">Для 32-битной версии Office в 64-битной версии Windows:</span><span class="sxs-lookup"><span data-stu-id="27b82-186">For 32-bit Office on 64-bit Windows:</span></span>
    
  <span data-ttu-id="27b82-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="27b82-187">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="27b82-188">По умолчанию проверяемая строка имеет **значение 8** (восемь).</span><span class="sxs-lookup"><span data-stu-id="27b82-188">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="27b82-189">Если для **TypeGuessRows установлено** значение **0** (ноль), драйвер Excel проверяет первые 16 384 строк на наличие типа данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-189">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="27b82-190">Если вы хотите проверить более 16 384 строк, задайте **для TypeGuessRows** значение, основанное на нужном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="27b82-190">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="27b82-191">Чтобы проверить все строки, установите **для TypeGuessRows** значение 1 048 576 (максимальное число строк, разрешенных в Excel).</span><span class="sxs-lookup"><span data-stu-id="27b82-191">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="27b82-192">Тип данных определяется максимальным количеством найденных видов данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-192">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="27b82-193">Если имеется связь, тип данных определяется в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="27b82-193">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="27b82-194">Числовой</span><span class="sxs-lookup"><span data-stu-id="27b82-194">Number</span></span>
- <span data-ttu-id="27b82-195">Денежный</span><span class="sxs-lookup"><span data-stu-id="27b82-195">Currency</span></span>
- <span data-ttu-id="27b82-196">Date</span><span class="sxs-lookup"><span data-stu-id="27b82-196">Date</span></span>
- <span data-ttu-id="27b82-197">Текст</span><span class="sxs-lookup"><span data-stu-id="27b82-197">Text</span></span>
- <span data-ttu-id="27b82-198">Boolean</span><span class="sxs-lookup"><span data-stu-id="27b82-198">Boolean</span></span>

<span data-ttu-id="27b82-199">Если встречаются данные, которые не соответствуют угадать тип данных для столбца, эти данные возвращаются в виде **значения NULL.**</span><span class="sxs-lookup"><span data-stu-id="27b82-199">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="27b82-200">При импорте, если столбец имеет смешанные типы данных, весь столбец привоцируется к типу данных, установленного параметром **ImportMixedTypes.**</span><span class="sxs-lookup"><span data-stu-id="27b82-200">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2013"></a>[<span data-ttu-id="27b82-201">Office 2013</span><span class="sxs-lookup"><span data-stu-id="27b82-201">Office 2013</span></span>](#tab/office-2013)

<span data-ttu-id="27b82-202">Для 32-битной версии Office в 32-битной версии Windows или 64-битной версии Office в 64-битной версии Windows:</span><span class="sxs-lookup"><span data-stu-id="27b82-202">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="27b82-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="27b82-203">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="27b82-204">Для 32-битной версии Office в 64-битной версии Windows:</span><span class="sxs-lookup"><span data-stu-id="27b82-204">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="27b82-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="27b82-205">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="27b82-206">По умолчанию проверяемая строка имеет **значение 8** (восемь).</span><span class="sxs-lookup"><span data-stu-id="27b82-206">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="27b82-207">Если для **TypeGuessRows установлено** значение **0** (ноль), драйвер Excel проверяет первые 16 384 строк на наличие типа данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-207">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="27b82-208">Если вы хотите проверить более 16 384 строк, задайте **для TypeGuessRows** значение, основанное на нужном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="27b82-208">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="27b82-209">Чтобы проверить все строки, установите **для TypeGuessRows** значение 1 048 576 (максимальное число строк, разрешенных в Excel).</span><span class="sxs-lookup"><span data-stu-id="27b82-209">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="27b82-210">Тип данных определяется максимальным числом найденных видов данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-210">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="27b82-211">Если имеется связь, тип данных определяется в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="27b82-211">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="27b82-212">Числовой</span><span class="sxs-lookup"><span data-stu-id="27b82-212">Number</span></span>
- <span data-ttu-id="27b82-213">Денежный</span><span class="sxs-lookup"><span data-stu-id="27b82-213">Currency</span></span>
- <span data-ttu-id="27b82-214">Date</span><span class="sxs-lookup"><span data-stu-id="27b82-214">Date</span></span>
- <span data-ttu-id="27b82-215">Текст</span><span class="sxs-lookup"><span data-stu-id="27b82-215">Text</span></span>
- <span data-ttu-id="27b82-216">Boolean</span><span class="sxs-lookup"><span data-stu-id="27b82-216">Boolean</span></span>

<span data-ttu-id="27b82-217">Если встречаются данные, которые не соответствуют угадать тип данных для столбца, эти данные возвращаются в виде **значения NULL.**</span><span class="sxs-lookup"><span data-stu-id="27b82-217">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="27b82-218">При импорте, если столбец имеет смешанные типы данных, весь столбец привоцируется к типу данных, установленного параметром **ImportMixedTypes.**</span><span class="sxs-lookup"><span data-stu-id="27b82-218">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

# <a name="office-2010"></a>[<span data-ttu-id="27b82-219">Office 2010</span><span class="sxs-lookup"><span data-stu-id="27b82-219">Office 2010</span></span>](#tab/office-2010)

<span data-ttu-id="27b82-220">Для 32-битной версии Office в 32-битной версии Windows или 64-битной версии Office в 64-битной версии Windows:</span><span class="sxs-lookup"><span data-stu-id="27b82-220">For 32-bit Office on 32-bit Windows or 64-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="27b82-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="27b82-221">**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="27b82-222">Для 32-битной версии Office в 64-битной версии Windows:</span><span class="sxs-lookup"><span data-stu-id="27b82-222">For 32-bit Office on 64-bit Windows:</span></span>

<span data-ttu-id="27b82-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span><span class="sxs-lookup"><span data-stu-id="27b82-223">**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**</span></span>

<span data-ttu-id="27b82-224">По умолчанию проверяемая строка имеет **значение 8** (восемь).</span><span class="sxs-lookup"><span data-stu-id="27b82-224">The default number of rows to be checked is **8** (eight).</span></span> <span data-ttu-id="27b82-225">Если для **TypeGuessRows установлено** значение **0** (ноль), драйвер Excel проверяет первые 16 384 строк на наличие типа данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-225">When you set the **TypeGuessRows** value to **0** (zero), Excel Driver checks the first 16,384 rows for the data type.</span></span> <span data-ttu-id="27b82-226">Если вы хотите проверить более 16 384 строк, задайте **для TypeGuessRows** значение, основанное на нужном диапазоне.</span><span class="sxs-lookup"><span data-stu-id="27b82-226">If you want to check more than 16,384 rows, set **TypeGuessRows** to a value that is based on your desired range.</span></span> <span data-ttu-id="27b82-227">Чтобы проверить все строки, установите **для TypeGuessRows** значение 1 048 576 (максимальное число строк, разрешенных в Excel).</span><span class="sxs-lookup"><span data-stu-id="27b82-227">To check all rows, set **TypeGuessRows** to 1,048,576 (the maximum number of rows that are allowed in Excel).</span></span>
 
<span data-ttu-id="27b82-228">Тип данных определяется максимальным количеством найденных видов данных.</span><span class="sxs-lookup"><span data-stu-id="27b82-228">The data type is determined by the maximum number of kinds of data that is found.</span></span> <span data-ttu-id="27b82-229">Если имеется связь, тип данных определяется в следующем порядке:</span><span class="sxs-lookup"><span data-stu-id="27b82-229">If there is a tie, the data type is determined in the following order:</span></span>

- <span data-ttu-id="27b82-230">Числовой</span><span class="sxs-lookup"><span data-stu-id="27b82-230">Number</span></span>
- <span data-ttu-id="27b82-231">Денежный</span><span class="sxs-lookup"><span data-stu-id="27b82-231">Currency</span></span>
- <span data-ttu-id="27b82-232">Date</span><span class="sxs-lookup"><span data-stu-id="27b82-232">Date</span></span>
- <span data-ttu-id="27b82-233">Текст</span><span class="sxs-lookup"><span data-stu-id="27b82-233">Text</span></span>
- <span data-ttu-id="27b82-234">Boolean</span><span class="sxs-lookup"><span data-stu-id="27b82-234">Boolean</span></span>

<span data-ttu-id="27b82-235">Если встречаются данные, которые не соответствуют угадать тип данных для столбца, эти данные возвращаются в виде **значения NULL.**</span><span class="sxs-lookup"><span data-stu-id="27b82-235">If data is encountered that doesn’t match the guessed data type for the column, that data is returned as a **Null** value.</span></span> <span data-ttu-id="27b82-236">При импорте, если столбец имеет смешанные типы данных, весь столбец привоцируется к типу данных, установленного параметром **ImportMixedTypes.**</span><span class="sxs-lookup"><span data-stu-id="27b82-236">During an import, if a column has mixed data types, the whole column is cast to the data type that’s set by the **ImportMixedTypes** setting.</span></span>

---
> [!NOTE]
> <span data-ttu-id="27b82-237">При изменении параметров реестра Windows необходимо выйти из системы, а затем перезапустить механизм баз данных, чтобы новые параметры вступили в силу.</span><span class="sxs-lookup"><span data-stu-id="27b82-237">When you change Windows Registry settings, you must exit and then restart the database engine for the new settings to take effect.</span></span>

## <a name="see-also"></a><span data-ttu-id="27b82-238">См. также</span><span class="sxs-lookup"><span data-stu-id="27b82-238">See also</span></span>

- [<span data-ttu-id="27b82-239">Использование параметра TypeGuessRows для драйвера Excel</span><span class="sxs-lookup"><span data-stu-id="27b82-239">Using the TypeGuessRows setting for Excel Driver</span></span>](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

