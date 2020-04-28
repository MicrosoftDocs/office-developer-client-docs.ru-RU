---
title: Раздел Logs в файле настройки
TOCTitle: Customization File Logs section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3a9af5d09a7a7a7a7ec97d757d502efbf2402900
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295151"
---
# <a name="customization-file-logs-section"></a>Раздел Logs в файле настройки

**Область применения**: Access 2013, Office 2013

Раздел **logs** содержит запись файла журнала, в которой задается имя файла, записывающего ошибки во время выполнения **операции.**

## <a name="syntax"></a>Синтаксис

Запись файла журнала имеет следующий вид:

`err=FileName`

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Часть</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>err</strong></p></td>
<td><p>Строка литерала, указывающая на запись в файле журнала.</p></td>
</tr>
<tr class="even">
<td><p><em>FileName</em></p></td>
<td><p>Полный путь и имя файла. Обычное имя файла — <strong>к:\мсдфмап.лог</strong>.</p></td>
</tr>
</tbody>
</table>


Файл журнала будет содержать имя пользователя, HRESULT, дату и время каждой ошибки.

