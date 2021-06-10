---
title: Объект Level (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70fb359aa4faa0bcfc99f0b1700b0eb51f665bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290116"
---
# <a name="level-object-ado-md"></a>Объект Level (ADO MD)


**Область применения**: Access 2013, Office 2013

Содержит набор участников, каждый из которых имеет один и тот же ранг в иерархии.

## <a name="remarks"></a>Примечания

С помощью коллекций и свойств объекта **Level** можно сделать следующее:

  - Определите **уровень** с [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)

  - Возвращаем строку, используемую при отобратии **уровня** с [свойством caption.](caption-property-ado-md.md)

  - Верни значимую строку, описываемую **свойством Level** с [свойством Description.](description-property-ado-md.md)

  - Возвращаем [объекты Member,](member-object-ado-md.md) которые составляют **level** с коллекцией [Members.](members-collection-ado-md.md)

  - Возвращаем количество уровней из корневого уровня **с** [свойством Depth.](depth-property-ado-md.md)

  - Используйте стандартную коллекцию свойств ADO [для](properties-collection-ado.md) получения дополнительных сведений об **объекте Level.**

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
<td><p>CatalogName</p></td>
<td><p>Имя каталога, к которому принадлежит этот куб.</p></td>
</tr>
<tr class="even">
<td><p>CubeName</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>Содержательное описание уровня.</p></td>
</tr>
<tr class="even">
<td><p>DimensionUniqueName</p></td>
<td><p>Однозначное имя <a href="dimension-object-ado-md.md">измерения</a>.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyUniqueName</p></td>
<td><p>Однозначное имя иерархии.</p></td>
</tr>
<tr class="even">
<td><p>LevelCaption</p></td>
<td><p>Метка или подпись, связанные с уровнем.</p></td>
</tr>
<tr class="odd">
<td><p>LevelCardinality</p></td>
<td><p>Количество участников на уровне.</p></td>
</tr>
<tr class="even">
<td><p>LevelGUID</p></td>
<td><p>GUID уровня.</p></td>
</tr>
<tr class="odd">
<td><p>LevelName</p></td>
<td><p>Имя уровня.</p></td>
</tr>
<tr class="even">
<td><p>LevelNumber</p></td>
<td><p>Расстояние между уровнем и корнем иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>LevelType</p></td>
<td><p>Тип уровня.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>Однозначное имя уровня.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит этот куб.</p></td>
</tr>
</tbody>
</table>

