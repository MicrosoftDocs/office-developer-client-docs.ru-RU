---
title: Customization File Logs Section
TOCTitle: Customization File Logs Section
ms:assetid: de331a97-c9cd-5f02-692b-d7afd9e9342a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250124(v=office.15)
ms:contentKeyID: 48548178
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 479bac0c61718f12af8fcb1b176b91d3fc57841b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482552"
---
# <a name="customization-file-logs-section"></a>Customization File Logs Section

**Применимо к**: Access 2013 | Office 2013

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
<td><p><strong>err</strong></p></td>
<td><p>Строковый литерал, которое указывает, это — это записи файла журнала.</p></td>
</tr>
<tr class="even">
<td><p><em>Имя файла</em></p></td>
<td><p>Полный путь и имя файла. Имя файла типичные — <strong>c:\msdfmap.log</strong>.</p></td>
</tr>
</tbody>
</table>


Файл журнала будет содержать имя пользователя, HRESULT, Дата и время каждой ошибки.

