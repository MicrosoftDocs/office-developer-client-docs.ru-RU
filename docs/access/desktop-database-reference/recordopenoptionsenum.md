---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c39d9ca7da2955343e38c67628c9c603a2c256b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869808"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum


**Применимо к**: Access 2013, Office 2013

Задает параметры открытия для [записи](record-object-ado.md). Эти значения можно объединять с помощью или.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adDelayFetchFields</strong></p></td>
<td><p>0x8000</p></td>
<td><p>Указывает поставщик, что поля, связанные с <strong>записи</strong> не требуется сначала получить, но могут быть получены во первая попытка получить доступ к полю. — Это поведение по умолчанию, указанный в параметре отсутствия этот флаг для извлечения всех полей объекта <strong>записи</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong>adDelayFetchStream</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Указывает поставщику на то, что поток по умолчанию, связанные с <strong>записи</strong> должны не удалось получить данные, изначально. — Это поведение по умолчанию, указанный в параметре отсутствия этот флаг для извлечения потока по умолчанию, связанного с объектом <strong>записи</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenAsync</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Указывает, что объект <strong>записи</strong> открыт в асинхронном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenExecuteCommand</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что исходная строка содержит текст команды, которая должна выполняться. Это значение эквивалентно параметру <strong>adCmdText</strong> на <strong>Recordset.Open</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenRecordUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что параметры не заданы.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenOutput</strong></p></td>
<td><p>0x800000</p></td>
<td><p>Указывает, что если источник указывает на узле, содержащем исполняемый файл сценария (например,. Страница ASP), а затем открытой <strong>записи</strong> будет содержать результаты выполненного сценария. Это значение допустимо только с записями без семейства сайтов.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы нет ADO/WFC эквивалентами.

