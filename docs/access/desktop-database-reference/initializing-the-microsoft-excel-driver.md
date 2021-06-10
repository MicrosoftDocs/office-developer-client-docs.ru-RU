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

**Применяется к**: Excel 2016 | Access 2016 | Access 2013 | Office 2013 | Excel 2013 | Office для бизнеса Access 2013 | Excel 2010 | Access 2010

При установке Excel драйвера программа установки записывает набор значений по умолчанию в реестр Windows в подкайлах Engines и ISAM Formats. Не следует изменять эти параметры напрямую; используйте программу установки для приложения, чтобы добавить, удалить или изменить эти параметры. В следующих разделах описываются параметры инициализации и формата ISAM для драйвера Microsoft Excel базы данных.

## <a name="excel-initialization-settings"></a>Excel параметров инициализации

Папка **\\ Engines \\ Excel access Connectivity Engines** включает параметры инициализации драйвера Aceexcl.dll, используемой для внешнего доступа к Microsoft Excel таблицам. Типичные параметры для записей в этой папке показаны в следующем примере.

```vb
    win32=<path>\ Aceexcl.dll  
    
    TypeGuessRows=8 
    
    ImportMixedTypes=Text 
    
    AppendBlankRows=1 
    
    FirstRowHasNames=Yes
```

В движке базы данных Microsoft Access Excel записи папок следующим образом.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Запись</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>win32</p></td>
<td><p>Расположение msexcl40.dll. Полный путь определяется во время установки. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>TypeGuessRows</p></td>
<td><p>Количество строк, которые необходимо проверить для типа данных. Тип данных определяется с учетом максимального количества найденных данных. Если есть связь, тип данных определяется в следующем порядке: Номер, Валюта, Дата, Текст, Boolean. Если встречаются данные, которые не соответствуют типу данных, угадал для столбца, он возвращается в качестве <strong>значения Null.</strong> При импорте, если столбец имеет смешанные типы данных, весь столбец будет отлит в соответствии с параметром ImportMixedTypes. По умолчанию число строк, которые необходимо проверить, — 8. Значения имеют тип REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>ImportMixedTypes</p></td>
<td><p>Можно установить для MajorityType или Text. Если задатки для MajorityType, столбцы смешанных типов данных будут отбрасываться к основному типу данных при импорте. Если заостряется на тексте, столбцы смешанных типов данных будут отбрасаны в Текст по импорту. По умолчанию — Текст. Значения имеют тип REG_SZ.</p></td>
</tr>
<tr class="even">
<td><p>AppendBlankRows</p></td>
<td><p>Количество пустых строк, которые должны быть добавлены до конца листа версии 3.5 или Версии 4.0 перед добавлением новых данных. Например, если в AppendBlankRows установлено 4 строки, Microsoft Jet пристроит 4 пустых строки к концу листа перед тем, как примкнуть к строкам с данными. Значения для этого параметра могут варьироваться от 0 до 16; по умолчанию — 01 (одна дополнительная строка. Значения имеют тип REG_DWORD.</p></td>
</tr>
<tr class="odd">
<td><p>FirstRowHasNames</p></td>
<td><p>Двоичное значение, которое указывает, содержит ли первая строка таблицы имена столбцов. Значение 01 указывает, что во время импорта из первой строки будут взяты имена столбцов. Значение 00 не указывает имен столбцов в первом ряду; Имена столбцов отображаются как F1, F2, F3 и так далее. Значение по умолчанию — 01. Значения имеют тип REG_BINARY.</p></td>
</tr>
</tbody>
</table>

<br/>

Папка **\\ Engines \\ Excel 8.0** содержит следующие записи, применимые к Microsoft Excel 97.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя входа</p></th>
<th><p>Тип</p></th>
<th><p>Значение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Двигатель</p></td>
<td><p>REG_SZ</p></td>
<td><p>Excel</p></td>
</tr>
<tr class="even">
<td><p>ExportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Microsoft Excel 97-2000 (*.xls)</p></td>
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
<td><p>1</p></td>
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
<td><p>Экспорт данных из текущей базы данных в файл Microsoft Excel 97. Этот процесс переопишет данные, если они будут экспортироваться в существующий файл.</p></td>
</tr>
<tr class="odd">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>


## <a name="using-the-typeguessrows-setting-for-excel-driver"></a>Использование параметра TypeGuessRows для Excel драйвера
При использовании Microsoft Excel драйвера можно использовать значение **реестра TypeGuessRows,** чтобы настроить количество строк для проверки типа данных. Значение **TypeGuessRows** расположено в следующем подкайке реестра:

# <a name="office-2016"></a>[Office 2016](#tab/office-2016)

Для установки MSI Office

- Для 32-битных Office 32-Windows или 64-Office 64-битных Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- Для 32-Office 64-битных Windows:

  **HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**
    
Для установки нажатие кнопки на запуск Office

- Для 32-битных Office 32-Windows или 64-Office 64-битных Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

- Для 32-Office 64-битных Windows:
    
  **HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\ClickToRun\REGISTRY\MACHINE\Software\Wow6432Node\Microsoft\Office\16.0\Access Connectivity Engine\Engines\Excel**

По умолчанию количество строк, которые необходимо проверить, **— 8** (восемь). Если значение **TypeGuessRows** установлено до **0** (ноль), Excel драйвер проверяет первые 16 384 строк для типа данных. Если требуется проверить более 16 384 строк, установите **TypeGuessRows** значение, основанное на желаемом диапазоне. Чтобы проверить все строки, установите **TypeGuessRows** до 1 048 576 (максимальное количество строк, разрешенных в Excel).
 
Тип данных определяется максимальным количеством найденных данных. Если имеется связь, тип данных определяется в следующем порядке:

- Номер
- Денежный
- Date
- Текст
- Boolean

Если встречаются данные, которые не совпадают с угадалным типом данных для столбца, эти данные возвращаются в виде **значения Null.** При импорте, если столбец имеет смешанные типы данных, весь столбец отбрасируется к типу данных, за набору **параметра ImportMixedTypes.**

# <a name="office-2013"></a>[Office 2013](#tab/office-2013)

Для 32-битных Office 32-Windows или 64-Office 64-битных Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Для 32-Office 64-битных Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

По умолчанию количество строк, которые необходимо проверить, **— 8** (восемь). Если значение **TypeGuessRows** установлено до **0** (ноль), Excel драйвер проверяет первые 16 384 строк для типа данных. Если требуется проверить более 16 384 строк, установите **TypeGuessRows** значение, основанное на желаемом диапазоне. Чтобы проверить все строки, установите **TypeGuessRows** до 1 048 576 (максимальное количество строк, разрешенных в Excel).
 
Тип данных определяется максимальным количеством найденных данных. Если имеется связь, тип данных определяется в следующем порядке:

- Номер
- Денежный
- Date
- Текст
- Boolean

Если встречаются данные, которые не совпадают с угадалным типом данных для столбца, эти данные возвращаются в виде **значения Null.** При импорте, если столбец имеет смешанные типы данных, весь столбец отбрасируется к типу данных, за набору **параметра ImportMixedTypes.**

# <a name="office-2010"></a>[Office 2010](#tab/office-2010)

Для 32-битных Office 32-Windows или 64-Office 64-битных Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

Для 32-Office 64-битных Windows:

**HKEY_LOCAL_MACHINE\SOFTWARE\Wow6432Node\Microsoft\Office\15.0\Access Connectivity Engine\Engines\Excel**

По умолчанию количество строк, которые необходимо проверить, **— 8** (восемь). Если значение **TypeGuessRows** установлено до **0** (ноль), Excel драйвер проверяет первые 16 384 строк для типа данных. Если требуется проверить более 16 384 строк, установите **TypeGuessRows** значение, основанное на желаемом диапазоне. Чтобы проверить все строки, установите **TypeGuessRows** до 1 048 576 (максимальное количество строк, разрешенных в Excel).
 
Тип данных определяется максимальным количеством найденных данных. Если имеется связь, тип данных определяется в следующем порядке:

- Номер
- Денежный
- Date
- Текст
- Boolean

Если встречаются данные, которые не совпадают с угадалным типом данных для столбца, эти данные возвращаются в виде **значения Null.** При импорте, если столбец имеет смешанные типы данных, весь столбец отбрасируется к типу данных, за набору **параметра ImportMixedTypes.**

---
> [!NOTE]
> При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.

## <a name="see-also"></a>См. также

- [Использование параметра TypeGuessRows для Excel драйвера](https://support.office.com/en-us/article/using-the-typeguessrows-setting-for-excel-driver-6aa3e101-2a90-47ac-bf0f-7d4109a5708b?ui=en-US&rs=en-US&ad=US)

