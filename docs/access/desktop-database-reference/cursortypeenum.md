---
title: CursorTypeEnum (Ссылка на настольные базы данных)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 0bcaaa1298f12d72c5e836dcfe1e74cdcda68d19
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295165"
---
# <a name="cursortypeenum"></a>CursorTypeEnum

**Область применения**: Access 2013, Office 2013

Указывает тип курсора, используемого в [объекте Recordset.](recordset-object-ado.md)

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
<td><p><strong>adOpenDynamic</strong></p></td>
<td><p>2</p></td>
<td><p>Использует динамический курсор. Видны добавления, изменения и удаления других пользователей, а также разрешены все типы перемещения через <strong>Набор</strong> записей, за исключением закладок, если поставщик не поддерживает их.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>0</p></td>
<td><p>Значение, используемое по умолчанию. Использует курсор только для нападающих. Идентично статическому курсору, за исключением того, что можно прокручивать только записи. Это повышает производительность, если требуется сделать только один проход через <strong>набор Recordset.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p>1</p></td>
<td><p>Использует курсор наборов ключей. Как динамический курсор, за исключением того, что вы не можете видеть записи, которые добавляют другие пользователи, хотя записи, которые другие пользователи удаляют, недоступны из <strong>вашего Набор записей</strong>. Изменения данных другими пользователями по-прежнему видны.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p>3</p></td>
<td><p>Использует статический курсор. Статическая копия набора записей, которые можно использовать для поиска данных или создания отчетов. Добавления, изменения или удаления других пользователей не видны.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenUnspecified</strong></p></td>
<td><p>–1</p></td>
<td><p>Не указывает тип курсора.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>AdoEnums.CursorType.DYNAMIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.FORWARDONLY</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.KEYSET</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorType.STATIC</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorType.UNSPECIFIED</p></td>
</tr>
</tbody>
</table>

