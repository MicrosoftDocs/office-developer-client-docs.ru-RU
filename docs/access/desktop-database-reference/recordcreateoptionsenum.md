---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3315fc0b6d72689e36530b7e7daf7b94732459f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481571"
---
# <a name="recordcreateoptionsenum"></a>RecordCreateOptionsEnum


**Применимо к**: Access 2013 | Office 2013

Указывает, должен быть открыт существующей **записи** или создана новая **запись** для объекта [записи](record-object-ado.md) метода [Open](open-method-ado-record.md) . Значения может использоваться совместно с оператора AND.

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
<td><p>Создает новую <strong>запись</strong> в узле, заданное параметром <em>источника</em> , не открывая существующей <strong>записи</strong>. Если источник указывает на существующий узел, во время выполнения возникает ошибка, если не <strong>adCreateCollection</strong> в сочетании с <strong>adOpenIfExists</strong> или <strong>adCreateOverwrite</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateNonCollection</strong></p></td>
<td><p>0</p></td>
<td><p>Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">adSimpleRecord</a>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adCreateOverwrite</strong></p></td>
<td><p>0x4000000</p></td>
<td><p>Изменяет флаги создания <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>и <strong>adCreateStructDoc</strong>. Когда или будет использоваться с этим значением и одно из значений флаг создания, если источник указывает URL-адрес существующего узла или <strong>записи</strong>, а затем перезаписать существующие <strong>записи</strong> и на его месте создается новый. Это значение не может использоваться вместе с <strong>adOpenIfExists</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adCreateStructDoc</strong></p></td>
<td><p>0x80000000</p></td>
<td><p>Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">adStructDoc</a>, не открывая существующей <strong>записи</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adFailIfNotExists</strong></p></td>
<td><p>-1</p></td>
<td><p>Значение, используемое по умолчанию. Приводит к ошибке времени выполнения, если <em>источник</em> указывает на несуществующий узел.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenIfExists</strong></p></td>
<td><p>0x2000000</p></td>
<td><p>Изменяет флаги создания <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>и <strong>adCreateStructDoc</strong>. Когда или будет использоваться с этим значением и одно из значений флаг создания, если источник указывает URL-адрес существующего узла или объект <strong>записи</strong> , а затем поставщика необходимо открыть существующей <strong>записи</strong> вместо создания нового. Это значение не может использоваться вместе с <strong>adCreateOverwrite</strong>.</p></td>
</tr>
</tbody>
</table>


**Эквивалент ADO/WFC**

Эти константы нет ADO/WFC эквивалентами.

