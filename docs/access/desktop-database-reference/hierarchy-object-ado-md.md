---
title: Объект Hierarchy (ADO MD)
TOCTitle: Hierarchy object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 5005ffec000c8fecc1188f37fad75227385f9ee2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928189"
---
# <a name="hierarchy-object-ado-md"></a>Объект Hierarchy (ADO MD)


**Применимо к**: Access 2013, Office 2013

Представляет один из способов в котором элементов [измерения](dimension-object-ado-md.md) можно сгруппировать или «сведение.» Измерения можно объединить вместе один или несколько иерархий.

## <a name="remarks"></a>Примечания

Со свойствами объекта **иерархии** и семейств сайтов выполните следующее:

  - Определение **иерархии** с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) .

  - Возвращает удобной для восприятия строку, которая описывает **иерархии** с помощью свойства [Description](description-property-ado-md.md) .

  - Возвращает объекты [уровня](level-object-ado-md.md) , которые будут включены в **иерархии** с коллекцией [уровней](levels-collection-ado-md.md) .

  - Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **иерархии** .

Коллекции **свойств** содержит свойства, предоставленных поставщиком. В следующей таблице перечислены свойства, которые могут быть недоступны. Список свойств фактический может различаться в зависимости от реализации поставщика. Обратитесь к документации вашего поставщика для получения более полного списка доступных свойств.

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
<td><p>Член на верхнем уровне накопительный пакет обновления в иерархии.</p></td>
</tr>
<tr class="even">
<td><p>ИмяКаталога</p></td>
<td><p>Имя каталога, к которому принадлежит этот куб.</p></td>
</tr>
<tr class="odd">
<td><p>Имя куба</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="even">
<td><p>DefaultMember</p></td>
<td><p>Уникальное имя элемента по умолчанию для этой иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>Описание</p></td>
<td><p>Подробное описание иерархии.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Тип измерения, к которой принадлежит этой иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Однозначное имя измерения.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyCaption</p></td>
<td><p>Метка или заголовок, связанный с иерархией.</p></td>
</tr>
<tr class="odd">
<td><p>HierarchyCardinality</p></td>
<td><p>Число элементов в иерархии.</p></td>
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

