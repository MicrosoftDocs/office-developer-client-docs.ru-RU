---
title: Объект Иерархия (ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c6668dfd40f7d0d26bcfa2ca4149acdc713e14c6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291931"
---
# <a name="hierarchy-object-ado-md"></a>Объект Иерархия (ADO MD)


**Область применения**: Access 2013, Office 2013

Представляет один из способов агрегировать или "свернуть" участников измерения. [](dimension-object-ado-md.md) Измерение можно агрегировать по одной или несколько иерархий.

## <a name="remarks"></a>Примечания

С помощью коллекций и свойств объекта **Иерархия** можно сделать следующее:

  - Определите **иерархию** с [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)

  - Верни значимую строку, **описываемую иерархией** с [свойством Description.](description-property-ado-md.md)

  - Возвращаем [объекты Level,](level-object-ado-md.md) которые составляют **Иерархию** с коллекцией [Уровней.](levels-collection-ado-md.md)

  - Используйте стандартную коллекцию свойств ADO [для](properties-collection-ado.md) получения дополнительных сведений об объекте **Иерархия.**

Коллекция **свойств** содержит свойства, предоставленные поставщиком. В следующей таблице перечислены свойства, которые могут быть доступны. Фактический список свойств может отличаться в зависимости от реализации поставщика. Дополнительный список доступных свойств см. в документации для поставщика.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AllMember</p></td>
<td><p>Участник на самом высоком уровне отката в иерархии.</p></td>
</tr>
<tr class="even">
<td><p>CatalogName</p></td>
<td><p>Имя каталога, к которому принадлежит этот куб.</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="even">
<td><p>DefaultMember</p></td>
<td><p>Уникальное имя члена по умолчанию для этой иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>Содержательное описание иерархии.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Тип измерения, которому принадлежит эта иерархия.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Однозначное имя измерения.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyCaption</p></td>
<td><p>Метка или подпись, связанные с иерархией.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyCardinality</p></td>
<td><p>Количество участников в иерархии.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyGUID</p></td>
<td><p>GUID иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyName</p></td>
<td><p>Имя иерархии.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Однозначное имя иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит этот куб.</p></td>
</tr>
</tbody>
</table>

