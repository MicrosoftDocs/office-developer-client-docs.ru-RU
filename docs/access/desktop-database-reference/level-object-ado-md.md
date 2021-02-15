---
title: Level object (ADO MD)
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
# <a name="level-object-ado-md"></a>Level object (ADO MD)


**Область применения**: Access 2013, Office 2013

Содержит набор членов, каждый из которых имеет одинаковый ранг в иерархии.

## <a name="remarks"></a>Заметки

С помощью коллекций и свойств объекта **Level** можно сделать следующее:

  - Определите **уровень** со [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)

  - Возвращает строку, которая будет применяться при отобраке **уровня** со [свойством Caption.](caption-property-ado-md.md)

  - Возвращает осмысленные строки, описывая **уровень** со [свойством Description.](description-property-ado-md.md)

  - Возвращает [объекты Member,](member-object-ado-md.md) которые составляют **уровень** с [коллекцией Members.](members-collection-ado-md.md)

  - Возвращает количество уровней из корневого объекта **Level** со [свойством Depth.](depth-property-ado-md.md)

  - Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об **объекте Level.**

Коллекция **Properties** содержит свойства, предоставленные поставщиком. В следующей таблице перечислены свойства, которые могут быть доступны. Фактический список свойств может отличаться в зависимости от реализации поставщика. Более полный список доступных свойств см. в документации к поставщику.

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
<td><p>Описание</p></td>
<td><p>Осмысленное описание уровня.</p></td>
</tr>
<tr class="even">
<td><p>DimensionUniqueName</p></td>
<td><p>Однозначное имя <a href="dimension-object-ado-md.md">измерения.</a></p></td>
</tr>
<tr class="odd">
<td><p>HierarchyUniqueName</p></td>
<td><p>Однозначное имя иерархии.</p></td>
</tr>
<tr class="even">
<td><p>LevelCaption</p></td>
<td><p>Метка или заголовок, связанный с уровнем.</p></td>
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

