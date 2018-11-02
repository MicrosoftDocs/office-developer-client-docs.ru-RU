---
title: Объект Member (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 341f6711044a577fdb82c47b1a782c17c6884bf0
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924206"
---
# <a name="member-object-ado-md"></a>Объект Member (ADO MD)


**Применимо к**: Access 2013, Office 2013

Представляет элемент уровень в кубе, дочерние элементы элемента уровня или членом положение оси набора ячеек.

## <a name="remarks"></a>Примечания

Свойства **члена** отличаются в зависимости от контекста, в котором она используется. **Член** [уровень](level-object-ado-md.md) [CubeDef](cubedef-object-ado-md.md) имеет свойство [дочерних элементов](children-property-ado-md.md) , которое возвращает **члены** на уровень ниже в иерархии из текущего **элемента**. Для **члена** [позицию](position-object-ado-md.md) **дочерней** коллекции всегда будет пустым. Кроме того свойство [Type](type-property-ado-md.md) применяется только к **члены** **уровня**.

**Член** **положение** имеет два свойства — [DrilledDown](drilleddown-property-ado-md.md) и [ParentSameAsPrev](parentsameasprev-property-ado-md.md) —, могут быть полезны при отображении [ячеек](cellset-object-ado-md.md). Если эти свойства доступны на **уровень** **член** , произойдет ошибка.

Со свойствами объекта **члена** **уровень**и семейств сайтов выполните следующее:

  - Определите с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) **члена** .

  - Возвращает строку, используемую при отображении **элемента** с помощью свойства [Caption](caption-property-ado-md.md) .

  - Возвращает удобной для восприятия строка, описывающая измерения или формулу **элемента** с помощью свойства [Description](description-property-ado-md.md) .

  - Определите характер **член** со свойством [типа](type-property-ado-md.md) .

  - Получите информацию о **уровень** **член** с помощью свойства [LevelDepth](leveldepth-property-ado-md.md) и [LevelName](levelname-property-ado-md.md) .

  - Получение связанных **элементов** в [иерархии](hierarchy-object-ado-md.md) с помощью свойства [родительских](parent-property-ado-md.md) и [дочерних элементов](children-property-ado-md.md) .

  - Счетчик потомков **члена** со свойством [ChildCount](childcount-property-ado-md.md) .

  - Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **уровень** .

Со свойствами **члена** **положение** по [оси](axis-object-ado-md.md)и семейств сайтов выполните следующее:

  - Определите с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) **члена** .

  - Возвращает строку, используемую при отображении **элемента** с помощью свойства [Caption](caption-property-ado-md.md) .

  - Возвращает удобной для восприятия строка, описывающая измерения или формулу **элемента** с помощью свойства [Description](description-property-ado-md.md) .

  - Получите информацию о **уровень** **член** с помощью свойства [LevelDepth](leveldepth-property-ado-md.md) и [LevelName](levelname-property-ado-md.md) .

  - Счетчик потомков **члена** со свойством [ChildCount](childcount-property-ado-md.md) .

  - Свойство [DrilledDown](drilleddown-property-ado-md.md) используется для определения, является ли на **оси** сразу после этот **член**по крайней мере один дочерний элемент.

  - Свойство [ParentSameAsPrev](parentsameasprev-property-ado-md.md) используется для определения, совпадает ли родительский этот **член** родительской предыдущего **элемента**.

  - Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **уровень** .

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
<td><p>ИмяКаталога</p></td>
<td><p>Имя каталога, к которому принадлежит этот куб.</p></td>
</tr>
<tr class="even">
<td><p>ChildrenCardinality</p></td>
<td><p>Число дочерних элементов элемента.</p></td>
</tr>
<tr class="odd">
<td><p>Имя куба</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="even">
<td><p>Описание</p></td>
<td><p>Понятное описание элемента.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionUniqueName</p></td>
<td><p>Однозначное имя <a href="dimension-object-ado-md.md">измерения</a>.</p></td>
</tr>
<tr class="even">
<td><p>HierarchyUniqueName</p></td>
<td><p>Однозначное имя иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>LevelNumber</p></td>
<td><p>Расстояние между на уровне и корень иерархии.</p></td>
</tr>
<tr class="even">
<td><p>LevelUniqueName</p></td>
<td><p>Однозначное имя уровня.</p></td>
</tr>
<tr class="odd">
<td><p>MemberCaption</p></td>
<td><p>Метка или заголовок, связанный с элементом.</p></td>
</tr>
<tr class="even">
<td><p>MemberGUID</p></td>
<td><p>Идентификатор GUID члена.</p></td>
</tr>
<tr class="odd">
<td><p>Имя пользователя</p></td>
<td><p>Имя участника.</p></td>
</tr>
<tr class="even">
<td><p>MemberOrdinal</p></td>
<td><p>Порядковый номер элемента.</p></td>
</tr>
<tr class="odd">
<td><p>MemberType</p></td>
<td><p>Тип элемента.</p></td>
</tr>
<tr class="even">
<td><p>MemberUniqueName</p></td>
<td><p>Однозначное имя участника.</p></td>
</tr>
<tr class="odd">
<td><p>ParentCount</p></td>
<td><p>Счетчик количество родительских элементов данного элемента.</p></td>
</tr>
<tr class="even">
<td><p>ParentLevel</p></td>
<td><p>Номер уровня родительского элемента.</p></td>
</tr>
<tr class="odd">
<td><p>ParentUniqueName</p></td>
<td><p>Однозначное имя родительского элемента.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит этот куб.</p></td>
</tr>
</tbody>
</table>

