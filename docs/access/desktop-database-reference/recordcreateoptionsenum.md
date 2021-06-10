---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300695"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**Область применения**: Access 2013, Office 2013

Указывает, следует ли  открывать существующую запись  или новую запись, созданную для метода Открыть объект [Record.](record-object-ado.md) [](open-method-ado-record.md) Эти значения можно комбинировать с оператором AND.

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
<td><p><strong>adCreateCollection</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Создает новую запись <strong>в</strong> узле, указанном параметром <em>Source,</em> вместо открытия существующей <strong>записи.</strong> Если источник указывает на существующий узел, то возникает ошибка времени запуска, если <strong>adCreateCollection</strong> не сочетается с <strong>adOpenIfExists</strong> или <strong>adCreateOverwrite</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateNonCollection</strong></p></td>
<td><p>0</p></td>
<td><p>Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">adSimpleRecord</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCreateOverwrite</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>Изменяет флаги создания <strong>adCreateCollection,</strong> <strong>adCreateNonCollection</strong>и <strong>adCreateStructDoc.</strong> Когда или используется с этим значением и одним из значений флага создания, если исходный URL-адрес указывает на существующий узел или <strong>запись,</strong>то существующая запись перезаписывается и создается на его месте новый. <strong></strong> Это значение нельзя использовать вместе с <strong>adOpenIfExists.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateStructDoc</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">adStructDoc</a>вместо открытия существующей <strong>записи.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adFailIfNotExists</strong></p></td>
<td><p>–1</p></td>
<td><p>Значение, используемое по умолчанию. Приводит к ошибке во время работы, если <em>Источник</em> указывает на несуществующий узел.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenIfExists</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>Изменяет флаги создания <strong>adCreateCollection,</strong> <strong>adCreateNonCollection</strong>и <strong>adCreateStructDoc.</strong> Если ИЛИ используется с этим значением и одним из значений флага создания, если исходный URL-адрес <strong></strong> указывает на существующий узел или объект <strong>Record,</strong> поставщик должен открыть существующую запись вместо создания нового. Это значение нельзя использовать вместе с <strong>adCreateOverwrite.</strong></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Эти константы не имеют эквивалентов ADO/WFC.

