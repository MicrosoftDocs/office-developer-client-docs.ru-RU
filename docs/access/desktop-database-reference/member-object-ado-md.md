---
title: Объект Member (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289424"
---
# <a name="member-object-ado-md"></a>Объект Member (ADO MD)


**Область применения**: Access 2013, Office 2013

Представляет элемент уровня в кубе, его детей или позицию вдоль оси ячеек.

## <a name="remarks"></a>Заметки

Свойства члена отличаются **в** зависимости от контекста, в котором он используется. У **члена** [уровня](level-object-ado-md.md) в [CubeDef](cubedef-object-ado-md.md) есть свойство [Children,](children-property-ado-md.md) которое возвращает члены на следующем нижнем уровне иерархии от текущего **члена.**  Для  члена позиции [коллекция](position-object-ado-md.md) **Children** всегда пуста. Кроме того, свойство [Type](type-property-ado-md.md) применяется только к **членам** **уровня.**

Элемент **Позиции** **имеет** два свойства ( [DrilledDown](drilleddown-property-ado-md.md) и [ParentSameAsPrev),](parentsameasprev-property-ado-md.md) которые полезны при отобралении [cellset](cellset-object-ado-md.md). При доступе к этим свойствам на  члене уровня произойдет **ошибка.**

С помощью коллекций и свойств объекта  **Member** уровня можно сделать следующее:

  - Определите **участника** со [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)

  - Возвращает строку, которая будет применяться при отобраке **объекта Member** со [свойством Caption.](caption-property-ado-md.md)

  - Возвращает осмысленные строки, описывая меру или **формулу Member со** [свойством Description.](description-property-ado-md.md)

  - Определите природу члена **с** помощью свойства [Type.](type-property-ado-md.md)

  - Получите сведения об **уровне участника** **со** свойствами [LevelDepth](leveldepth-property-ado-md.md) и [LevelName.](levelname-property-ado-md.md)

  - Получение **связанных членов** в [иерархии со](hierarchy-object-ado-md.md) свойствами [Parent](parent-property-ado-md.md) и [Children.](children-property-ado-md.md)

  - Посчитайте количество детей **члена с** помощью свойства [ChildCount.](childcount-property-ado-md.md)

  - Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об **объекте Level.**

С помощью коллекций и  свойств члена  позиции вдоль оси [можно](axis-object-ado-md.md)сделать следующее:

  - Определите **участника** со [свойствами Name](name-property-ado-md.md) и [UniqueName.](uniquename-property-ado-md.md)

  - Возвращает строку, которая будет применяться при отобраке **объекта Member** со [свойством Caption.](caption-property-ado-md.md)

  - Возвращает осмысленные строки, описывая меру или **формулу Member со** [свойством Description.](description-property-ado-md.md)

  - Получите сведения об **уровне участника** **со** свойствами [LevelDepth](leveldepth-property-ado-md.md) и [LevelName.](levelname-property-ado-md.md)

  - Посчитайте количество детей **члена с** помощью свойства [ChildCount.](childcount-property-ado-md.md)

  - Используйте свойство [DrilledDown,](drilleddown-property-ado-md.md) чтобы определить, есть ли по крайней мере один child на оси **сразу** после этого **члена**.

  - Используйте свойство [ParentSameAsPrev,](parentsameasprev-property-ado-md.md) чтобы определить,  является ли родительский объект этого члена тем же, что и родительский объект предшествующего **члена.**

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
<td><p>ChildrenCardinality</p></td>
<td><p>Количество детей, которые есть у участника.</p></td>
</tr>
<tr class="odd">
<td><p>CubeName</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="even">
<td><p>Описание</p></td>
<td><p>Осмысленное описание участника.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Однозначное имя <a href="dimension-object-ado-md.md">измерения.</a></p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Однозначное имя иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>LevelNumber</p></td>
<td><p>Расстояние между уровнем и корнем иерархии.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>Однозначное имя уровня.</p></td>
</tr>
<tr class="odd">
<td><p>MemberCaption</p></td>
<td><p>Метка или подпись, связанная с участником.</p></td>
</tr>
<tr class="even">
<td><p>MemberGUID</p></td>
<td><p>GUID участника.</p></td>
</tr>
<tr class="odd">
<td><p>MemberName</p></td>
<td><p>Имя участника.</p></td>
</tr>
<tr class="even">
<td><p>MemberOrdinal</p></td>
<td><p>Порядковая номер участника.</p></td>
</tr>
<tr class="odd">
<td><p>MemberType</p></td>
<td><p>Тип члена.</p></td>
</tr>
<tr class="even">
<td><p>MemberUniqueName</p></td>
<td><p>Однозначное имя члена.</p></td>
</tr>
<tr class="odd">
<td><p>ParentCount</p></td>
<td><p>Количество родителей, которые есть у этого участника.</p></td>
</tr>
<tr class="even">
<td><p>ParentLevel</p></td>
<td><p>Номер уровня родительского члена.</p></td>
</tr>
<tr class="odd">
<td><p>ParentUniqueName</p></td>
<td><p>Однозначное имя родительского члена.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит этот куб.</p></td>
</tr>
</tbody>
</table>

