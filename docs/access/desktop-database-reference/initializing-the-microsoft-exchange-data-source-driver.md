---
title: Инициализация драйвера источника данных Microsoft Exchange
TOCTitle: Initializing the Microsoft Exchange Data Source driver
ms:assetid: cf87a746-f846-1a01-f4ec-20a25e335193
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834677(v=office.15)
ms:contentKeyID: 48547810
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- acmain11.chm1032667
f1_categories:
- Office.Version=v15
ms.openlocfilehash: c64f28769d88c2684485ba537bdbdf22afd30ac5
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26026052"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Инициализация драйвера источника данных Microsoft Exchange

**Применимо к**: Access 2013, Office 2013

При установке драйвера источника данных Microsoft Exchange, программа установки записывает набор значений по умолчанию реестра Microsoft Windows в подразделы обработчики и ISAM Formats. Не изменяйте эти параметры напрямую; для добавления, удаления или изменения этих параметров с помощью программы установки для приложения. В следующих разделах инициализации и параметров ISAM Format драйвера источника данных Microsoft Exchange.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Параметры инициализации источника данных Microsoft Exchange

**Модуль подключения к Access\\обработчики\\Exchange** папка содержит параметры инициализации для драйвера Aceexch.dll, который используется для внешнего доступа к папкам Microsoft Outlook и Microsoft Exchange. Единственная запись в этой папке выглядит следующим образом:

`win32=<path>\ACEEXCH.DLL`

Ядро базы данных Microsoft Access использует этот параметр для указания расположения Aceexch.dll. Полный путь определяется во время установки. Тип Реестра значений —\_SZ.

Результаты использования формата Outlook ISAM и использования формата ISAM клиента Exchange похожи. Единственное отличие заключается в том, что два разных клиента используют разные имена для одного столбца. Два формата ISAM были созданы, чтобы ядро базы данных Microsoft Access может вернуть имена столбцов в виде, который определит пользователь.

## <a name="microsoft-outlook-client-isam-formats"></a>Клиент Microsoft Outlook ISAM formats

**Модуль подключения к Access\\ISAM Formats\\Outlook 9.0** папка содержит следующие записи.

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
<td><p>Модуль</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Outlook()</p></td>
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
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.



## <a name="microsoft-exchange-client-isam-formats"></a>Форматы ISAM клиента Microsoft Exchange

**Модуль подключения к Access\\ISAM Formats\\Exchange 4.0** папка содержит следующие записи.

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
<td><p>Модуль</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>ImportFilter</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange()</p></td>
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
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>IndexDialog</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>CreateDBOnExport</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>SupportsLongNames</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> При изменении параметров реестра Windows, необходимо выйти из и перезапустить ядро базы данных для новых параметров вступили в силу.



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Настройка Schema.ini файла данных Outlook и Exchange

Файл Schema.ini используется Outlook и Exchange ISAM точно так же, как он используется в ISAM текста. Этот файл содержит особенности источника данных: формат данных и имена столбцов, которые должны быть доступны.

Измените файл Schema.ini перед данных можно прочитать, импортируемые или экспортируемые для Outlook и Exchange необязательно. Многие из параметров в файле Schema.ini для Outlook и Exchange специфичны для внутренних тегов, которые требуется MAPI. Не следует пытаться изменить значения этих тегов.

