---
title: Объект Dimension (ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: afea442aa535660b5bb618297640db8fbd546dec
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293898"
---
# <a name="dimension-object-ado-md"></a>Объект Dimension (ADO MD)


**Область применения**: Access 2013, Office 2013

Представляет одно из измерений многомерного куба, содержащего одну или несколько иерархий участников.

## <a name="remarks"></a>Примечания

С помощью коллекций и свойств объекта **Dimension** можно сделать следующее:

  - Определите **измерение** с [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)

  - Возвращаем значимую строку, описываемую **измерение** с [свойством Description.](description-property-ado-md.md)

  - Возвращаем [объекты Иерархия,](hierarchy-object-ado-md.md) которые составляют **Измерение** с [коллекцией Иерархии.](hierarchies-collection-ado-md.md)

  - Используйте стандартную коллекцию свойств ADO [для](properties-collection-ado.md) получения дополнительных сведений об **объекте Dimension.**

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
<td><p>DefaultHierarchy</p></td>
<td><p>Уникальное имя иерархии по умолчанию.</p></td>
</tr>
<tr class="even">
<td><p>Description</p></td>
<td><p>Содержательное описание куба.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionCaption</p></td>
<td><p>Метка или подпись, связанные с измерением.</p></td>
</tr>
<tr class="even">
<td><p>DimensionCardinality</p></td>
<td><p>Количество участников в измерении.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionGUID</p></td>
<td><p>GUID измерения.</p></td>
</tr>
<tr class="even">
<td><p>DimensionName</p></td>
<td><p>Имя измерения.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionOrdinal</p></td>
<td><p>Ordinal number of the dimension among the group of dimensions that form the cube.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Тип измерения.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Однозначное имя измерения.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит этот куб.</p></td>
</tr>
</tbody>
</table>

