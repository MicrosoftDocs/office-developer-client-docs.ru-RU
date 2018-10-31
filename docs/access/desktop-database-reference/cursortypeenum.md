---
title: CursorTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: CursorTypeEnum
ms:assetid: 7c5fa8b2-85ea-a0a7-41f1-a78650aced3e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249519(v=office.15)
ms:contentKeyID: 48545835
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: c394f8000f1d4ae7867d83974e0e186616145fb5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25864030"
---
# <a name="cursortypeenum"></a>CursorTypeEnum

**Применимо к**: Access 2013 | Office 2013

Указывает тип курсора, используемого в объекте [набора записей](recordset-object-ado.md) .

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
<td><p>С помощью динамического курсора. Видны добавления, изменения и удаления другими пользователями, а все типы перемещения по <strong>набору записей</strong> , разрешены, за исключением закладки, если их не поддерживает поставщик.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenForwardOnly</strong></p></td>
<td><p>0</p></td>
<td><p>Значение, используемое по умолчанию. Используется только для прямого курсора. Совпадает с статический курсор, за исключением того, что вы можно только просмотреть записей. Это повышает производительность, если вам нужно сделать только один проход по <strong>набора записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenKeyset</strong></p></td>
<td><p>1</p></td>
<td><p>Использует курсор набора ключей. Как динамический курсор, за исключением того, что нельзя просматривать записи, которые другие пользователи добавляют, несмотря на то, что записи, которые другие пользователи удалять недоступны из набора <strong>записей</strong>. Изменения данных другие пользователи по-прежнему видимы.</p></td>
</tr>
<tr class="even">
<td><p><strong>adOpenStatic</strong></p></td>
<td><p>3</p></td>
<td><p>Использует статический курсор. Статические копия набора записей, которые можно использовать для поиска данных и создания отчетов. Дополнения, изменения или удаления другие пользователи не отображаются.</p></td>
</tr>
<tr class="odd">
<td><p><strong>adOpenUnspecified</strong></p></td>
<td><p>-1</p></td>
<td><p>Не указан тип курсора.</p></td>
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
<th><p>Constant</p></th>
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

