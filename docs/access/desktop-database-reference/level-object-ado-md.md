---
title: Объект уровня (ADO MD)
TOCTitle: Level Object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d6137e35d43153d7d9d36f23e1bdbe9fc80a442d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881442"
---
# <a name="level-object-ado-md"></a>Объект уровня (ADO MD)


**Применимо к**: Access 2013, Office 2013

Содержит набор элементов, каждый из которых содержит один и тот же ранг в иерархии.

## <a name="remarks"></a>Замечания

Со свойствами объекта **уровень** и семейств сайтов выполните следующее:

  - Определите **уровень** с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) .

  - Возвращает строку, используемую при отображении **уровень** с свойство [Caption](caption-property-ado-md.md) .

  - Возвращает удобной для восприятия строку, которая описывает **уровень** с помощью свойства [Description](description-property-ado-md.md) .

  - Возвращают объекты [элементов](member-object-ado-md.md) , которые составляют **уровня** в коллекции [элементов](members-collection-ado-md.md) .

  - Возвращает число уровней из корневой папки **уровень** со свойством [глубины](depth-property-ado-md.md) .

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
<td><p>Имя куба</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="odd">
<td><p>Описание</p></td>
<td><p>Понятное описание уровня.</p></td>
</tr>
<tr class="even">
<td><p>DimensionUniqueName</p></td>
<td><p>Однозначное имя <a href="dimension-object-ado-md.md">измерения</a>.</p></td>
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
<td><p>Количество элементов на этом уровне.</p></td>
</tr>
<tr class="even">
<td><p>LevelGUID</p></td>
<td><p>Идентификатор GUID уровня.</p></td>
</tr>
<tr class="odd">
<td><p>LevelName</p></td>
<td><p>Имя уровня.</p></td>
</tr>
<tr class="even">
<td><p>LevelNumber</p></td>
<td><p>Расстояние между на уровне и корень иерархии.</p></td>
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

