---
title: FieldEnum (Ссылка на настольные базы данных)
TOCTitle: FieldEnum
ms:assetid: fbd415c0-d6b4-278f-318b-98432c013634
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250289(v=office.15)
ms:contentKeyID: 48548876
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e42dcfe63194364986e5b235c59b011231307a7c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292596"
---
# <a name="fieldenum"></a>FieldEnum

**Область применения**: Access 2013, Office 2013

Указывает специальные поля, на которые ссылается коллекция [Полей](record-object-ado.md) объекта [Record.](fields-collection-ado.md)

## <a name="remarks"></a>Примечания

Эти константы обеспечивают "ярлык" для доступа к специальным полям, связанным с **записью.** Извлекать [объект Field](field-object-ado.md) из коллекции **Fields,** а затем получать его содержимое с помощью свойства **Value** [объекта Field.](value-property-ado.md)

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
<td><p>–1</p></td>
<td><p>Ссылается на поле, содержащее объект <a href="stream-object-ado.md">Stream по</a> умолчанию, связанный с <strong>записью.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adRecordURL</strong></p></td>
<td><p>–2</p></td>
<td><p>Ссылки на поле, содержащее абсолютную строку URL-адреса для текущей <strong>записи.</strong></p></td>
</tr>
</tbody>
</table>

