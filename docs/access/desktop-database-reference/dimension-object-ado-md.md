---
title: Объект измерения (ADO MD)
TOCTitle: Dimension Object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: e3581f9bce5e2e56b341928df3415a1b9b223beb
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25872888"
---
# <a name="dimension-object-ado-md"></a>Объект измерения (ADO MD)


**Применимо к**: Access 2013, Office 2013

Представляет один из измерения многомерного куба, содержащего иерархии один или несколько элементов.

## <a name="remarks"></a>Замечания

Со свойствами объекта **измерения** и семейств сайтов выполните следующее:

  - Определение **измерения** с помощью свойства [Name](name-property-ado-md.md) и [уникального имени](uniquename-property-ado-md.md) .

  - Возвращает удобной для восприятия строка, описывающая **измерения** с помощью свойства [Description](description-property-ado-md.md) .

  - Возвращает объекты [иерархии](hierarchy-object-ado-md.md) , которые составляют **измерения** с коллекцией [иерархии](hierarchies-collection-ado-md.md) .

  - Используйте коллекцию стандартный ADO [Свойства](properties-collection-ado.md) для получения дополнительных сведений об объекте **измерения** .

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
<td><p>DefaultHierarchy</p></td>
<td><p>Уникальное имя иерархии по умолчанию.</p></td>
</tr>
<tr class="even">
<td><p>Описание</p></td>
<td><p>Понятное описание куба.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionCaption</p></td>
<td><p>Метка или заголовок, связанный с измерения.</p></td>
</tr>
<tr class="even">
<td><p>DimensionCardinality</p></td>
<td><p>Количество элементов измерения.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionGUID</p></td>
<td><p>Идентификатор GUID, измерения.</p></td>
</tr>
<tr class="even">
<td><p>Имя измерения</p></td>
<td><p>Имя измерения.</p></td>
</tr>
<tr class="odd">
<td><p>DimensionOrdinal</p></td>
<td><p>Порядковый номер измерения между группы измерений, формирующих куба.</p></td>
</tr>
<tr class="even">
<td><p>DimensionType</p></td>
<td><p>Тип аналитики.</p></td>
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

