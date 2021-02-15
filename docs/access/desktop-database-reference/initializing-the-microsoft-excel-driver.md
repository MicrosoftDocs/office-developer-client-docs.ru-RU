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
# <a name="initializing-the-microsoft-excel-driver"></a>Инициализация драйвера Microsoft Excel

**Применимо к**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office для бизнеса Access 2013 | Excel 2010 | Access 2010

При установке драйвера Excel программа установки записывает набор значений по умолчанию в реестр Windows в подмайсах "Подпрограммы" и "Форматы ISAM". Не следует изменять эти параметры напрямую; используйте программу установки приложения для добавления, удаления или изменения этих параметров. В следующих разделах описаны параметры инициализации и формата ISAM для драйвера базы данных Microsoft Excel.

## <a name="excel-initialization-settings"></a>Параметры инициализации Excel

Папка "Под управлением ядер подключения **\\ \\ Access" Excel** включает параметры инициализации драйвера Aceexcl.dll, используемой для внешнего доступа к листам Microsoft Excel. Типичные параметры для записей в этой папке показаны в следующем примере.

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

Ядер баз данных Microsoft Access использует записи папки Excel следующим образом.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Запись</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>win32</p></td>
<td><p>Расположение msexcl40.dll. Полный путь определяется во время установки. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>TypeGuessRows</p></td>
<td><p>Количество строк, проверяемого на наличие типа данных. Тип данных определяется с учетом максимального количества найденных видов данных. Если имеется связь, тип данных определяется в следующем порядке: Number, Currency, Date, Text, Boolean. Если встречаются данные, которые не соответствуют типу данных, угадать для столбца, он возвращается в виде <strong>значения NULL.</strong> При импорте, если столбец имеет смешанные типы данных, весь столбец будет приводиться в соответствии с параметром ImportMixedTypes. По умолчанию проверяемая строка имеет значение 8. Значения имеют тип REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>ImportMixedTypes</p></td>
<td><p>Может иметь тип MajorityType или Text. Если этот тип имеет тип MajorityType, столбцы смешанных типов данных будут преобразовываться к предопределему типу данных при импорте. Если за установлено "Текст", столбцы смешанных типов данных будут при импорте привнося в текст. Значение по умолчанию — Text. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>AppendBlankRows</p></td>
<td><p>Количество пустых строк, добавляемого в конец листа версии 3.5 или версии 4.0 перед добавлением новых данных. Например, если для AppendBlankRows задано 4, Microsoft Jet применет 4 пустых строки в конец листа, а не строки, содержащие данные. Значения этого параметра могут быть в диапазоне от 0 до 16; значение по умолчанию — 01 (одна дополнительная строка. Значения имеют тип REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов. Значение 01 указывает, что во время импорта имена столбцов принимаются из первой строки. Значение 00 означает отсутствие имен столбцов в первой строке; имена столбцов отображаются как F1, F2, F3 и так далее. Значение по умолчанию — 01. Значения имеют тип REG_BINARY.</p></td>
</tr>
</tbody>
</table>

<br/>

Папка **Подмагивщика \\ подключений Access Excel \\ 8.0** содержит следующие записи, применимые к Microsoft Excel 97.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя записи</p></th>
<th><p>Тип</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Engine</p></td>
<td><p>REG_SZ</p></td>
<td><p>Excel</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (XLS)</p></td>
</tr>
<tr class="odd">
<td><p>CanLink</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>OneTablePerFile</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>IsamType</p></td>
<td><p>REG_DWORD</p></td>
<td><p>1 </p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>ResultTextExport</p></td>
<td><p>REG_SZ</p></td>
<td><p>Экспорт данных из текущей базы данных в файл Microsoft Excel 97. Этот процесс переопишет данные при экспорте в существующий файл.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a>Использование параметра TypeGuessRows для драйвера Excel
При использовании драйвера Microsoft Excel можно использовать значение реестра **TypeGuessRows,** чтобы настроить количество строк, проверяемых для типа данных. Значение **TypeGuessRows** находится в следующем поднайме реестра:

# <a name="office-2016"></a>[Office 2016](#tab/office-2016)

Для установки Office с MSI

- Для 32-битной версии Office в 32-битной версии Windows или 64-битной версии Office в 64-битной версии Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- Для 32-битной версии Office в 64-битной версии Windows:

  **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**
    
Для установки Office "нажми и нажми и нажми и

- Для 32-битной версии Office в 32-битной версии Windows или 64-битной версии Office в 64-битной версии Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- Для 32-битной версии Office в 64-битной версии Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

По умолчанию проверяемая строка имеет **значение 8** (восемь). Если для **TypeGuessRows установлено** значение **0** (ноль), драйвер Excel проверяет первые 16 384 строк на наличие типа данных. Если вы хотите проверить более 16 384 строк, задайте **для TypeGuessRows** значение, основанное на нужном диапазоне. Чтобы проверить все строки, установите **для TypeGuessRows** значение 1 048 576 (максимальное число строк, разрешенных в Excel).
 
Тип данных определяется максимальным количеством найденных видов данных. Если имеется связь, тип данных определяется в следующем порядке:

- Числовой
- Денежный
- Date
- Текст
- Boolean

Если встречаются данные, которые не соответствуют угадать тип данных для столбца, эти данные возвращаются в виде **значения NULL.** При импорте, если столбец имеет смешанные типы данных, весь столбец привоцируется к типу данных, установленного параметром **ImportMixedTypes.**

# <a name="office-2013"></a>[Office 2013](#tab/office-2013)

Для 32-битной версии Office в 32-битной версии Windows или 64-битной версии Office в 64-битной версии Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Для 32-битной версии Office в 64-битной версии Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

По умолчанию проверяемая строка имеет **значение 8** (восемь). Если для **TypeGuessRows установлено** значение **0** (ноль), драйвер Excel проверяет первые 16 384 строк на наличие типа данных. Если вы хотите проверить более 16 384 строк, задайте **для TypeGuessRows** значение, основанное на нужном диапазоне. Чтобы проверить все строки, установите **для TypeGuessRows** значение 1 048 576 (максимальное число строк, разрешенных в Excel).
 
Тип данных определяется максимальным числом найденных видов данных. Если имеется связь, тип данных определяется в следующем порядке:

- Числовой
- Денежный
- Date
- Текст
- Boolean

Если встречаются данные, которые не соответствуют угадать тип данных для столбца, эти данные возвращаются в виде **значения NULL.** При импорте, если столбец имеет смешанные типы данных, весь столбец привоцируется к типу данных, установленного параметром **ImportMixedTypes.**

# <a name="office-2010"></a>[Office 2010](#tab/office-2010)

Для 32-битной версии Office в 32-битной версии Windows или 64-битной версии Office в 64-битной версии Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Для 32-битной версии Office в 64-битной версии Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

По умолчанию проверяемая строка имеет **значение 8** (восемь). Если для **TypeGuessRows установлено** значение **0** (ноль), драйвер Excel проверяет первые 16 384 строк на наличие типа данных. Если вы хотите проверить более 16 384 строк, задайте **для TypeGuessRows** значение, основанное на нужном диапазоне. Чтобы проверить все строки, установите **для TypeGuessRows** значение 1 048 576 (максимальное число строк, разрешенных в Excel).
 
Тип данных определяется максимальным количеством найденных видов данных. Если имеется связь, тип данных определяется в следующем порядке:

- Числовой
- Денежный
- Date
- Текст
- Boolean

Если встречаются данные, которые не соответствуют угадать тип данных для столбца, эти данные возвращаются в виде **значения NULL.** При импорте, если столбец имеет смешанные типы данных, весь столбец привоцируется к типу данных, установленного параметром **ImportMixedTypes.**

---
> [!NOTE]
> При изменении параметров реестра Windows необходимо выйти из системы, а затем перезапустить механизм баз данных, чтобы новые параметры вступили в силу.

## <a name="see-also"></a>См. также

- [Использование параметра TypeGuessRows для драйвера Excel](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

