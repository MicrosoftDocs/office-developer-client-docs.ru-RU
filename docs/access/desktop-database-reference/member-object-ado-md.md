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

Представляет элемент уровня в Кубе, дочерние элементы элемента уровня или элемента положения на оси в наборе ячеек.

## <a name="remarks"></a>Примечания

Свойства **элемента** различаются в зависимости от контекста, в котором он используется. **Элемент** [уровня](level-object-ado-md.md) в [CubeDef](cubedef-object-ado-md.md) имеет свойство [Children](children-property-ado-md.md) , возвращающее **элементы** следующего нижнего уровня в иерархии от текущего **элемента**. Для **элемента** [position](position-object-ado-md.md)коллекция **Children** всегда пуста. Кроме того, свойство [Type](type-property-ado-md.md) применяется только к **членам** **уровня**.

Элемент **position** имеет два свойства — [DrilledDown](drilleddown-property-ado-md.md) и [ParentSameAsPrev](parentsameasprev-property-ado-md.md) , которые удобно использовать при отображении **набора** [ячеек](cellset-object-ado-md.md). Если к этим свойствам обращаются по **элементу** **уровня**, произойдет ошибка.

С помощью коллекций и свойств объекта **member** **уровня**можно выполнить следующие действия:

  - Идентифицируйте **члена** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .

  - Возвращает строку, используемую при отображении **элемента** со свойством [Caption](caption-property-ado-md.md) .

  - Возвращает осмысленную строку, описывающую меру или **элемент** формулы, с помощью свойства [Description](description-property-ado-md.md) .

  - Определите природу **элемента** с помощью свойства [Type](type-property-ado-md.md) .

  - Получение сведений о **уровне** **элемента** с помощью свойств [LevelDepth](leveldepth-property-ado-md.md) и [LevelName](levelname-property-ado-md.md) .

  - Получение связанных **членов** в [иерархии](hierarchy-object-ado-md.md) с [родительскими](parent-property-ado-md.md) свойствами и свойствами [дочерних элементов](children-property-ado-md.md) .

  - Подсчитайте дочерние элементы **элемента** с помощью свойства [ChildCount](childcount-property-ado-md.md) .

  - Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об объекте **Level** .

С помощью коллекций и свойств **члена** **позиции** вдоль [оси](axis-object-ado-md.md)можно выполнить следующие действия:

  - Идентифицируйте **члена** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .

  - Возвращает строку, используемую при отображении **элемента** со свойством [Caption](caption-property-ado-md.md) .

  - Возвращает осмысленную строку, описывающую меру или **элемент** формулы, с помощью свойства [Description](description-property-ado-md.md) .

  - Получение сведений о **уровне** **элемента** с помощью свойств [LevelDepth](leveldepth-property-ado-md.md) и [LevelName](levelname-property-ado-md.md) .

  - Подсчитайте дочерние элементы **элемента** с помощью свойства [ChildCount](childcount-property-ado-md.md) .

  - Используйте свойство [DrilledDown](drilleddown-property-ado-md.md) , чтобы определить, есть ли по крайней мере один дочерний элемент на **оси** , которая сразу после этого **элемента**.

  - Используйте свойство [ParentSameAsPrev](parentsameasprev-property-ado-md.md) , чтобы определить, совпадает ли родительский **элемент этого члена** со родителем непосредственно предыдущего **члена**.

  - Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об объекте **Level** .

Коллекция **Properties** содержит свойства, предоставляемые поставщиком. В следующей таблице перечислены свойства, которые могут быть доступны. Фактический список свойств может различаться в зависимости от реализации поставщика. Просмотрите документацию для своего поставщика, чтобы получить полный список доступных свойств.

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
<td><p>каталогнаме</p></td>
<td><p>Имя каталога, к которому принадлежит куб.</p></td>
</tr>
<tr class="even">
<td><p>чилдренкардиналити</p></td>
<td><p>Количество дочерних элементов.</p></td>
</tr>
<tr class="odd">
<td><p>кубенаме</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="even">
<td><p>Описание</p></td>
<td><p>Понятное описание члена.</p></td>
</tr>
<tr class="odd">
<td><p>дименсионуникуенаме</p></td>
<td><p>Неоднозначное имя <a href="dimension-object-ado-md.md">измерения</a>.</p></td>
</tr>
<tr class="even">
<td><p>хиерарчюникуенаме</p></td>
<td><p>Неоднозначное имя иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>левелнумбер</p></td>
<td><p>Расстояние между уровнем и корнем иерархии.</p></td>
</tr>
<tr class="even">
<td><p>левелуникуенаме</p></td>
<td><p>Неоднозначное имя уровня.</p></td>
</tr>
<tr class="odd">
<td><p>мемберкаптион</p></td>
<td><p>Метка или заголовок, связанные с элементом.</p></td>
</tr>
<tr class="even">
<td><p>мембергуид</p></td>
<td><p>GUID члена.</p></td>
</tr>
<tr class="odd">
<td><p>MemberName</p></td>
<td><p>Имя элемента.</p></td>
</tr>
<tr class="even">
<td><p>мемберординал</p></td>
<td><p>Порядковый номер элемента.</p></td>
</tr>
<tr class="odd">
<td><p>мембертипе</p></td>
<td><p>Тип элемента.</p></td>
</tr>
<tr class="even">
<td><p>мемберуникуенаме</p></td>
<td><p>Неоднозначное имя элемента.</p></td>
</tr>
<tr class="odd">
<td><p>паренткаунт</p></td>
<td><p>Количество родительских элементов.</p></td>
</tr>
<tr class="even">
<td><p>парентлевел</p></td>
<td><p>Номер уровня родительского элемента.</p></td>
</tr>
<tr class="odd">
<td><p>парентуникуенаме</p></td>
<td><p>Неоднозначное имя родительского элемента.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит куб.</p></td>
</tr>
</tbody>
</table>

