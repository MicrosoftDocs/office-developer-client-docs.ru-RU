---
title: Объект CubeDef (ADO MD)
TOCTitle: CubeDef Object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f7dc244483c3111e6e354496f1ffbbd12f463800
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25878298"
---
# <a name="cubedef-object-ado-md"></a>Объект CubeDef (ADO MD)


**Применимо к**: Access 2013, Office 2013

Представляет куб из многомерных схемы, содержащая набор связанных измерений.

## <a name="remarks"></a>Замечания

Со свойствами объекта **CubeDef** и семейств сайтов выполните следующее:

  - Определение **CubeDef** с помощью свойства [Name](name-property-ado-md.md) .

  - Возвращает строку, которая описывает куба с помощью свойства [Description](description-property-ado-md.md) .

  - Возвращает измерения, которые будут включены в куб с коллекцией [измерения](dimensions-collection-ado-md.md) .

  - Получение дополнительных сведений о **CubeDef** с помощью стандартных ADO [Свойства](properties-collection-ado.md) коллекции.

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
<td><p>CreatedOn</p></td>
<td><p>Дата и время создания куба.</p></td>
</tr>
<tr class="odd">
<td><p>CubeGUID</p></td>
<td><p>Куб GUID.</p></td>
</tr>
<tr class="even">
<td><p>Имя куба</p></td>
<td><p>Имя куба.</p></td>
</tr>
<tr class="odd">
<td><p>CubeType</p></td>
<td><p>Тип куба.</p></td>
</tr>
<tr class="even">
<td><p>DataUpdatedBy</p></td>
<td><p>Идентификатор пользователя пользователь, выполняющий последнего обновления данных.</p></td>
</tr>
<tr class="odd">
<td><p>Описание</p></td>
<td><p>Понятное описание куба.</p></td>
</tr>
<tr class="even">
<td><p>LastSchemaUpdate</p></td>
<td><p>Дата и время последнего обновления схемы.</p></td>
</tr>
<tr class="odd">
<td><p>SchemaName</p></td>
<td><p>Имя схемы, к которой принадлежит этот куб.</p></td>
</tr>
<tr class="even">
<td><p>SchemaUpdatedBy</p></td>
<td><p>Идентификатор пользователя пользователь, выполняющий последнее обновление схемы.</p></td>
</tr>
</tbody>
</table>

