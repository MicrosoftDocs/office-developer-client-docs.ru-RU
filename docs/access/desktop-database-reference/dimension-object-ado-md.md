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

Представляет один из измерений многомерного куба, содержащий одну или несколько иерархий элементов.

## <a name="remarks"></a>Замечания

Используя коллекции и свойства объекта **измерения** , можно выполнить следующие действия:

  - Определите **размерность** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .

  - Возвращает осмысленную строку, описывающую **измерение** , с помощью свойства [Description](description-property-ado-md.md) .

  - Возвращает объекты [иерархии](hierarchy-object-ado-md.md) , которые составляют **измерение** , с помощью коллекции [иерархий](hierarchies-collection-ado-md.md) .

  - Используйте стандартные коллекции [свойств](properties-collection-ado.md) ADO для получения дополнительных сведений об объекте **измерения** .

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
<td><p>Каталогнаме</p></td>
<td><p>Имя каталога, к которому принадлежит куб.</p></td>
</tr>
<tr class="even">
<td><p>Кубенаме</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="odd">
<td><p>Дефаулсиерарчи</p></td>
<td><p>Уникальное имя иерархии по умолчанию.</p></td>
</tr>
<tr class="even">
<td><p>Описание</p></td>
<td><p>Понятное описание Куба.</p></td>
</tr>
<tr class="odd">
<td><p>Дименсионкаптион</p></td>
<td><p>Метка или подпись, связанная с измерением.</p></td>
</tr>
<tr class="even">
<td><p>Дименсионкардиналити</p></td>
<td><p>Число элементов в измерении.</p></td>
</tr>
<tr class="odd">
<td><p>Дименсионгуид</p></td>
<td><p>GUID измерения.</p></td>
</tr>
<tr class="even">
<td><p>Дименсионнаме</p></td>
<td><p>Имя измерения.</p></td>
</tr>
<tr class="odd">
<td><p>Дименсионординал</p></td>
<td><p>Порядковый номер измерения между группами измерений, которые формируют куб.</p></td>
</tr>
<tr class="even">
<td><p>Дименсионтипе</p></td>
<td><p>Тип измерения.</p></td>
</tr>
<tr class="odd">
<td><p>Дименсионуникуенаме</p></td>
<td><p>Неоднозначное имя измерения.</p></td>
</tr>
<tr class="even">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит куб.</p></td>
</tr>
</tbody>
</table>

