---
title: FieldEnum (Справочник по для настольных баз данных Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5efcdbd9da4214d7f2b78ffbcfb81fb13265087e
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479944"
---
# <a name="fieldenum"></a>FieldEnum


**Применимо к**: Access 2013 | Office 2013

Задает особых полей, указанных в коллекции [полей](fields-collection-ado.md) объект [записи](record-object-ado.md) .

**Замечания**

Эти константы предоставляют «ярлык» для доступа к особых полей, сопоставленных с **записи**. Получение объекта [поля](field-object-ado.md) из коллекции **полей** и получение его содержимое с помощью свойства [Value](value-property-ado.md) объекта **поля** .

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
<td><p><strong>adDefaultStream</strong></p></td>
<td><p>-1</p></td>
<td><p>Ссылается на поле, содержащее объект <a href="stream-object-ado.md">потока</a> по умолчанию, связанный с <strong>записи</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>adRecordURL</strong></p></td>
<td><p>-2</p></td>
<td><p>Ссылается на поле, содержащее строку абсолютный URL-адрес для текущей <strong>записи</strong>.</p></td>
</tr>
</tbody>
</table>

