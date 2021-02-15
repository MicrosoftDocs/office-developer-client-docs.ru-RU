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
localization_priority: Normal
ms.openlocfilehash: b3460786785ae7b21184b6d96384ecc59e89d287
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291409"
---
# <a name="initializing-the-microsoft-exchange-data-source-driver"></a>Инициализация драйвера источника данных Microsoft Exchange

**Область применения**: Access 2013, Office 2013

При установке драйвера источника данных Microsoft Exchange программа установки записывает набор значений по умолчанию в реестр Microsoft Windows в подкайтах "Подпрограммы" и "Форматы ISAM". Не следует изменять эти параметры напрямую; используйте программу установки приложения для добавления, удаления или изменения этих параметров. В следующих разделах описаны параметры инициализации и формата ISAM для драйвера источника данных Microsoft Exchange.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Параметры инициализации источника данных Microsoft Exchange

Папка Exchange обдвижки подключения **\\ \\ Access** включает параметры инициализации драйвера Aceexch.dll, используемой для внешнего доступа к папок Microsoft Outlook и Microsoft Exchange. В этой папке есть только следующая запись:

`win32=<path>\ACEEXCH.DLL`

Яд баз данных Microsoft Access использует этот параметр, чтобы указать расположение Aceexch.dll. Полный путь определяется во время установки. Значения имеют тип REG \_ SZ.

Результаты использования формата ISAM Outlook и формата ISAM клиента Exchange аналогичны. Единственное отличие состоит в том, что два разных клиента используют разные имена для одинаковых столбцов. Созданы два формата ISAM, чтобы яд баз данных Microsoft Access мог возвращать имена столбцов в определенном стиле, который хочет пользователь.

## <a name="microsoft-outlook-client-isam-formats"></a>Форматы ISAM клиента Microsoft Outlook

Папка ISAM для средства подключения **\\ Access Форматы Outlook \\ 9.0** содержит следующие записи.

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
<td><p>3 </p></td>
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
> При изменении параметров реестра Windows необходимо выйти из системы, а затем перезапустить механизм баз данных, чтобы новые параметры вступили в силу.



## <a name="microsoft-exchange-client-isam-formats"></a>Форматы ISAM клиента Microsoft Exchange

Папка ISAM в формате ISAM для средства подключения **\\ Access \\ 4.0** содержит следующие записи.

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
<td><p>3 </p></td>
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
> При изменении параметров реестра Windows необходимо выйти из системы, а затем перезапустить механизм баз данных, чтобы новые параметры вступили в силу.



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Настройка Schema.ini для данных Outlook и Exchange

The Schema.ini file is used by the Outlook and Exchange ISAM in much the same way that it is used by the Text ISAM. Schema.ini содержит особенности источника данных: форматирование данных и имена столбцов, к которые необходимо получить доступ.

Нет необходимости изменять файл Schema.ini перед чтением, импортом или экспортом данных для Outlook и Exchange. Многие параметры в файле Schema.ini Для Outlook и Exchange специфически для внутренних тегов, необходимых mapI. Не следует пытаться изменить эти значения тегов.

