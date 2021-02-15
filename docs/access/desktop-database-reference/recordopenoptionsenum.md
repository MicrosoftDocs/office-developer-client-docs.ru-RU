---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caaf755ebd63f1805d0c77ef79a0f5863a85050e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300688"
---
# <a name="recordopenoptionsenum"></a>RecordOpenOptionsEnum


**Область применения**: Access 2013, Office 2013

Указывает параметры открытия [записи.](record-object-ado.md) Эти значения могут быть объединены с помощью OR.

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
<td><p>Указывает поставщику, что поля, <strong></strong> связанные с записью, не требуется извлекать изначально, но их можно получить при первой попытке доступа к полю. Поведение по умолчанию, на которое указывает отсутствие этого флага, — это извлечение всех полей <strong>объекта Record.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adDelayFetchStream</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Указывает поставщику, что поток по <strong></strong> умолчанию, связанный с записью, не требуется извлекать изначально. Поведение по умолчанию, на которое указывает отсутствие этого флага, — это извлечение потока по умолчанию, связанного с <strong>объектом Record.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenAsync</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Указывает, что <strong>объект Record</strong> открыт в асинхронном режиме.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenExecuteCommand</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что строка Source содержит текст команды, который должен быть выполнен. Это значение эквивалентно параметру <strong>adCmdText</strong> в <strong>Recordset.Open.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenRecordUnspecified</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Указывает, что параметры не указаны.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenOutput</strong></p></td>
<td><p>0x800000</p></td>
<td><p>Указывает, что если источник указывает на узел, содержащий исполняемый сценарий (например, . AsP page), после чего открытая <strong>запись</strong> будет содержать результаты выполненного сценария. Это значение допустимо только для записей, не внося в коллекции.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

