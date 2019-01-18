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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715636"
---
# <a name="customization-file-logs-section"></a>Раздел Logs в файле настройки

**Применимо к**: Access 2013, Office 2013

В разделе **Журналы** содержит записи файла журнала, который определяет имя файла, ошибки во время операции **DataFactory**.

## <a name="syntax"></a>Синтаксис

Запись файла журнала имеет форму:

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
<td><p><strong>Ошибка</strong></p></td>
<td><p>Строковый литерал, которое указывает, это — это записи файла журнала.</p></td>
</tr>
<tr class="even">
<td><p><em>FileName</em></p></td>
<td><p>Полный путь и имя файла. Имя файла типичные — <strong>c:\msdfmap.log</strong>.</p></td>
</tr>
</tbody>
</table>


Файл журнала будет содержать имя пользователя, HRESULT, Дата и время каждой ошибки.

