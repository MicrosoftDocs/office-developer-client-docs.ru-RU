---
title: Объект CubeDef (ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c82c95a430da76694fe26300e877e86f86a2eb4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295312"
---
# <a name="cubedef-object-ado-md"></a>Объект CubeDef (ADO MD)


**Область применения**: Access 2013, Office 2013

Представляет куб из многомерной схемы, содержащей набор связанных измерений.

## <a name="remarks"></a>Примечания

С коллекциями и свойствами объекта **CubeDef** можно сделать следующее:

  - Определите **CubeDef с** [свойством Name.](name-property-ado-md.md)

  - Верни строку, описываемую кубом с [свойством Description.](description-property-ado-md.md)

  - Возвращайте размеры, которые составляют куб в коллекции [Dimensions.](dimensions-collection-ado-md.md)

  - Получение дополнительных сведений **о CubeDef в** стандартной коллекции свойств [ADO.](properties-collection-ado.md)

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
<td><p>CreatedOn</p></td>
<td><p>Дата и время создания куба.</p></td>
</tr>
<tr class="odd">
<td><p>CubeGUID</p></td>
<td><p>GUID Cube.</p></td>
</tr>
<tr class="even">
<td><p>CubeName</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="odd">
<td><p>CubeType</p></td>
<td><p>Тип куба.</p></td>
</tr>
<tr class="even">
<td><p>DataUpdatedBy</p></td>
<td><p>Пользовательский ID пользователя, который делает последнее обновление данных.</p></td>
</tr>
<tr class="odd">
<td><p>Description</p></td>
<td><p>Содержательное описание куба.</p></td>
</tr>
<tr class="even">
<td><p>LastSchemaUpdate</p></td>
<td><p>Дата и время последнего обновления схемы.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит этот куб.</p></td>
</tr>
<tr class="even">
<td><p>SchemaUpdatedBy</p></td>
<td><p>Пользовательский ID пользователя, который делает последнее обновление схемы.</p></td>
</tr>
</tbody>
</table>

