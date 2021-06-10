---
title: CursorLocationEnum (Ссылка на настольные базы данных)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295214"
---
# <a name="cursorlocationenum"></a>CursorLocationEnum

**Область применения**: Access 2013, Office 2013

Указывает расположение службы курсоров.

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
<td><p><strong>adUseClient</strong></p></td>
<td><p>3</p></td>
<td><p>Использует курсоры с клиентской стороны, предоставленные локальной библиотекой курсоров. Локальные службы курсоров часто позволяют использовать множество функций, которые не могут быть предоставлены драйверами, поэтому использование этого параметра может предоставить преимущество в отношении функций, которые будут включены. Для обратной совместимости также поддерживается <strong>синоним adUseClientBatch.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>adUseNone</strong></p></td>
<td><p>1</p></td>
<td><p>Не использует службы курсора. (Эта константа устарела и появляется исключительно для обратной совместимости.)</p></td>
</tr>
<tr class="odd">
<td><p><strong>adUseServer</strong></p></td>
<td><p>2</p></td>
<td><p>Значение, используемое по умолчанию. Использует курсоры поставщика данных или предоставленные драйвером. Эти курсоры иногда очень гибкие и позволяют дополнительно чувствительность к изменениям, внесенным другими пользователями в источник данных. Однако некоторые функции службы <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor для OLE DB</a> (например, отсоединимые объекты <a href="recordset-object-ado.md">Recordset)</a> нельзя имитировать с помощью курсоров на стороне сервера, и эти функции будут недоступны в этом параметре.</p></td>
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
<td><p>AdoEnums.CursorLocation.CLIENT</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.CursorLocation.NONE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.CursorLocation.SERVER</p></td>
</tr>
</tbody>
</table>

