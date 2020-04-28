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

Содержит набор элементов, каждый из которых имеет одинаковый ранг в иерархии.

## <a name="remarks"></a>Примечания

С помощью коллекций и свойств объекта **Level** можно выполнить следующие действия:

  - Определите **уровень** с помощью свойств [Name](name-property-ado-md.md) и [UniqueName](uniquename-property-ado-md.md) .

  - Возвращает строку, используемую при отображении **уровня** со свойством [Caption](caption-property-ado-md.md) .

  - Возвращает осмысленную строку, описывающую **уровень** с помощью свойства [Description](description-property-ado-md.md) .

  - Возвращает объекты [member](member-object-ado-md.md) , составляющие **уровень** , с коллекцией [Members](members-collection-ado-md.md) .

  - Возвращает количество уровней из корня **уровня** со свойством [Depth](depth-property-ado-md.md) .

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
<td><p>кубенаме</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="odd">
<td><p>Описание</p></td>
<td><p>Понятное описание уровня.</p></td>
</tr>
<tr class="even">
<td><p>дименсионуникуенаме</p></td>
<td><p>Неоднозначное имя <a href="dimension-object-ado-md.md">измерения</a>.</p></td>
</tr>
<tr class="odd">
<td><p>хиерарчюникуенаме</p></td>
<td><p>Неоднозначное имя иерархии.</p></td>
</tr>
<tr class="even">
<td><p>левелкаптион</p></td>
<td><p>Метка или заголовок, связанные с уровнем.</p></td>
</tr>
<tr class="odd">
<td><p>левелкардиналити</p></td>
<td><p>Количество элементов на уровне.</p></td>
</tr>
<tr class="even">
<td><p>левелгуид</p></td>
<td><p>GUID уровня.</p></td>
</tr>
<tr class="odd">
<td><p>LevelName</p></td>
<td><p>Имя уровня.</p></td>
</tr>
<tr class="even">
<td><p>левелнумбер</p></td>
<td><p>Расстояние между уровнем и корнем иерархии.</p></td>
</tr>
<tr class="odd">
<td><p>левелтипе</p></td>
<td><p>Тип уровня.</p></td>
</tr>
<tr class="even">
<td><p>левелуникуенаме</p></td>
<td><p>Неоднозначное имя уровня.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит куб.</p></td>
</tr>
</tbody>
</table>

