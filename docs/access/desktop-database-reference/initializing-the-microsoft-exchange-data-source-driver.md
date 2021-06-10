---
title: Инициализация драйвера microsoft Exchange источника данных
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
localization_priority: Normal
ms.openlocfilehash: b3460786785ae7b21184b6d96384ecc59e89d287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291409"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Инициализация драйвера microsoft Exchange источника данных

**Область применения**: Access 2013, Office 2013

При установке драйвера Microsoft Exchange источника данных программа установки записывает набор значений по умолчанию в реестр microsoft Windows в подкайлах Engines и ISAM Formats. Не следует изменять эти параметры напрямую; используйте программу установки для приложения, чтобы добавить, удалить или изменить эти параметры. В следующих разделах описываются параметры инициализации и формата ISAM для драйвера Microsoft Exchange данных.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Параметры Exchange исходных данных Microsoft

Папка **\\ Engines \\ Exchange access Connectivity Engines** включает параметры инициализации драйвера Aceexch.dll, используемых для внешнего доступа к папкам Microsoft Outlook и Microsoft Exchange. В этой папке только одна запись:

`win32=<path>\ACEEXCH.DLL`

Движок базы данных Microsoft Access использует этот параметр, чтобы указать расположение Aceexch.dll. Полный путь определяется во время установки. Значения имеют тип REG \_ SZ.

Результаты использования формата Outlook ISAM и использования Exchange клиентского формата ISAM похожи. Единственное отличие состоит в том, что два разных клиента используют разные имена для одинаковых столбцов. Два формата ISAM созданы таким образом, чтобы двигатель базы данных Microsoft Access мог возвращать имена столбцов в определенном стиле, который желает пользователь.

## <a name="microsoft-outlook-client-isam-formats"></a>Microsoft Outlook клиентских форматов ISAM

В **папке IsAM Engine ISAM Outlook \\ \\ 9.0** содержатся следующие записи.

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
> При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.



## <a name="microsoft-exchange-client-isam-formats"></a>Microsoft Exchange клиентских форматов ISAM

В **папке IsAM Engine ISAM Exchange \\ \\ 4.0** содержатся следующие записи.

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
> При изменении параметров Windows реестра необходимо выйти и перезапустить двигатель базы данных, чтобы новые параметры вступили в силу.



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Настройка файла Schema.ini для Outlook и Exchange данных

Файл Schema.ini используется Outlook и Exchange ISAM таким же образом, как и текстовый ISAM. Schema.ini содержит особенности источника данных: форматирование данных и имена столбцов, к которых необходимо получить доступ.

Нет необходимости изменять файл Schema.ini перед чтением, импортом или экспортом для Outlook и Exchange. Многие параметры внутри файла Schema.ini для Outlook и Exchange для внутренних тегов, необходимых MAPI. Не следует пытаться изменить эти значения тегов.

