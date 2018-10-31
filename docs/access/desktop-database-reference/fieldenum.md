---
title: FieldEnum (Справочник по для настольных баз данных Access)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9ab46fc7c3817cbfa83c78816a42472e425d2d71
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25860051"
---
# <a name="fieldenum"></a>FieldEnum

**Применимо к**: Access 2013 | Office 2013

Задает особых полей, указанных в коллекции [полей](fields-collection-ado.md) объект [записи](record-object-ado.md) .

## <a name="remarks"></a>Замечания

Эти константы предоставляют «ярлык» для доступа к особых полей, сопоставленных с **записи**. Получение объекта [поля](field-object-ado.md) из коллекции **полей** и получение его содержимое с помощью свойства [Value](value-property-ado.md) объекта **поля** .

<br/>

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

