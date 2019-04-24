---
title: Объект Hierarchy (ADO MD)
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
# <a name="hierarchy-object-ado-md"></a>Объект Hierarchy (ADO MD)


**Область применения**: Access 2013, Office 2013

Представляет один из способов, с помощью которого можно выполнить статистическую настройку элементов [измерения](dimension-object-ado-md.md) или выполнить их сведение. Измерение можно объединить вдоль одной или нескольких иерархий.

## <a name="remarks"></a>Замечания

С помощью коллекций и свойств объекта **иерархии** можно выполнить следующие действия:

  - Определите **иерархию** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .

  - Возвращает осмысленную строку, которая описывает **иерархию** со свойством [Description](description-property-ado-md.md) .

  - Возвращает объекты [уровня](level-object-ado-md.md) , составляющие иерархию, **** с коллекцией [Levels](levels-collection-ado-md.md) .

  - Используйте стандартную коллекцию [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об объекте **иерархии** .

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
<td><p>Аллмембер</p></td>
<td><p>Элемент на высшем уровне свертки в иерархии.</p></td>
</tr>
<tr class="even">
<td><p>Каталогнаме</p></td>
<td><p>Имя каталога, к которому принадлежит куб.</p></td>
</tr>
<tr class="odd">
<td><p>Кубенаме</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="even">
<td><p>DefaultMember</p></td>
<td><p>Уникальное имя элемента по умолчанию для этой иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>Описание</p></td>
<td><p>Понятное описание иерархии.</p></td>
</tr>
<tr class="even">
<td><p>Дименсионтипе</p></td>
<td><p>Тип измерения, к которому относится данная иерархия.</p></td>
</tr>
<tr class="odd">
<td><p>Дименсионуникуенаме</p></td>
<td><p>Неоднозначное имя измерения.</p></td>
</tr>
<tr class="even">
<td><p>Хиерарчикаптион</p></td>
<td><p>Метка или заголовок, связанные с иерархией.</p></td>
</tr>
<tr class="odd">
<td><p>Хиерарчикардиналити</p></td>
<td><p>Число элементов в иерархии.</p></td>
</tr>
<tr class="even">
<td><p>Хиерарчигуид</p></td>
<td><p>GUID иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>Хиерарчинаме</p></td>
<td><p>Имя иерархии.</p></td>
</tr>
<tr class="even">
<td><p>Хиерарчюникуенаме</p></td>
<td><p>Неоднозначное имя иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит куб.</p></td>
</tr>
</tbody>
</table>

