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

При установке драйвера источника данных Microsoft Exchange программа установки записывает набор значений по умолчанию в реестр Microsoft Windows в подразделах Engines и ISAM formats. Эти параметры не следует изменять напрямую; Используйте программу установки приложения, чтобы добавлять, удалять или изменять эти параметры. В следующих разделах описываются параметры инициализации и ISAM Format для драйвера источника данных Microsoft Exchange.

## <a name="microsoft-exchange-data-source-initialization-settings"></a>Параметры инициализации источника данных Microsoft Exchange

Папка **\\Exchange Engine Engines Engine\\** включает параметры инициализации для драйвера ацеексч. dll, используемого для внешнего доступа к папкам Microsoft Outlook и Microsoft Exchange. Единственной записью в этой папке является следующее:

`win32=<path>\ACEEXCH.DLL`

Этот параметр используется ядром СУБД Microsoft Access для указания расположения Ацеексч. dll. Полный путь определяется во время установки. Значения имеют тип REG\_СЗ.

Результаты использования формата ISAM Outlook и с использованием формата ISAM клиента Exchange похожи. Единственное отличие состоит в том, что два разных клиента используют разные имена для одних и тех же столбцов. Были созданы два формата ISAM, поэтому ядро СУБД Microsoft Access может возвращать имена столбцов в определенном стиле, который пользователь хочет.

## <a name="microsoft-outlook-client-isam-formats"></a>ISAM formats клиента Microsoft Outlook

**\\Подсистема подключения доступа ISAM\\formats Outlook 9,0** содержит следующие записи.

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
<td><p>Модул</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>импортфилтер</p></td>
<td><p>REG_SZ</p></td>
<td><p>Outlook ()</p></td>
</tr>
<tr class="odd">
<td><p>канлинк</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>онетаблеперфиле</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>исамтипе</p></td>
<td><p>REG_DWORD</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>индексдиалог</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>креатедбонекспорт</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>суппортслонгнамес</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> При изменении параметров реестра Windows необходимо выйти и перезапустить ядро СУБД, чтобы новые параметры вступили в силу.



## <a name="microsoft-exchange-client-isam-formats"></a>ISAM formats клиента Microsoft Exchange

**Модуль\\подключения к службе доступа ISAM\\formats Exchange 4,0** папка содержит следующие записи.

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
<td><p>Модул</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange</p></td>
</tr>
<tr class="even">
<td><p>импортфилтер</p></td>
<td><p>REG_SZ</p></td>
<td><p>Exchange ()</p></td>
</tr>
<tr class="odd">
<td><p>канлинк</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
<tr class="even">
<td><p>онетаблеперфиле</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>исамтипе</p></td>
<td><p>REG_DWORD</p></td>
<td><p>4</p></td>
</tr>
<tr class="even">
<td><p>индексдиалог</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="odd">
<td><p>креатедбонекспорт</p></td>
<td><p>REG_BINARY</p></td>
<td><p>00</p></td>
</tr>
<tr class="even">
<td><p>суппортслонгнамес</p></td>
<td><p>REG_BINARY</p></td>
<td><p>01</p></td>
</tr>
</tbody>
</table>



> [!NOTE]
> При изменении параметров реестра Windows необходимо выйти и перезапустить ядро СУБД, чтобы новые параметры вступили в силу.



## <a name="customizing-the-schemaini-file-for-outlook-and-exchange-data"></a>Настройка файла Schema. ini для данных Outlook и Exchange

Файл Schema. ini используется в Outlook и Exchange ISAM точно так же, как и при использовании текста ISAM. Schema. ini содержит особенности источника данных: способ форматирования данных и имена столбцов, к которым нужно получить доступ.

Нет необходимости изменять файл Schema. ini до того, как данные могут быть прочитаны, импортированы или экспортированы для Outlook и Exchange. Многие параметры в файле Schema. ini для Outlook и Exchange относятся к внутренним тегам, которые необходимы для MAPI. Не пытайтесь изменить значения этих тегов.

