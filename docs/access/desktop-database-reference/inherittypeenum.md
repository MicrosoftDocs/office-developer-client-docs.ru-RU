---
title: InheritTypeEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: InheritTypeEnum
ms:assetid: aa505c66-5871-10a8-35a7-cb30bb5dc21a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249787(v=office.15)
ms:contentKeyID: 48546944
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba1a78e49d44bce0c489e4f5259ec9699543e231
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291416"
---
# <a name="inherittypeenum"></a>InheritTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает, как объекты наследуют разрешения, заданные с [помощью SetPermissions.](setpermissions-method-adox.md)

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adInheritBoth</strong></p></td>
<td><p>3 </p></td>
<td><p>Объекты и другие контейнеры, содержащиеся в основном объекте, наследуют запись.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritContainers</strong></p></td>
<td><p>2 </p></td>
<td><p>Другие контейнеры, содержащиеся в основном объекте, наследуют запись.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritNone</strong></p></td>
<td><p>0</p></td>
<td><p>Значение, используемое по умолчанию. Наследование не происходит.</p></td>
</tr>
<tr class="even">
<td><p><strong>adInheritNoPropagate</strong></p></td>
<td><p>4 </p></td>
<td><p>Флаги <strong>adInheritObjects</strong> и <strong>adInheritContainers</strong> не распространяются на унаследованные записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adInheritObjects</strong></p></td>
<td><p>1 </p></td>
<td><p>Не контейнерные объекты в контейнере наследуют разрешения.</p></td>
</tr>
</tbody>
</table>

