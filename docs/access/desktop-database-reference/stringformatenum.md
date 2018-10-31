---
title: StringFormatEnum (Справочник по для настольных баз данных Access)
TOCTitle: StringFormatEnum
ms:assetid: ab069d67-d983-f390-5d45-876a9f9d9691
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249794(v=office.15)
ms:contentKeyID: 48546964
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 8a3b798fd0d10a3bb2c1c4bd03419a6d506bbf8b
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863040"
---
# <a name="stringformatenum"></a>StringFormatEnum

**Применимо к**: Access 2013 | Office 2013

Задает формат при извлечении [набора записей](recordset-object-ado.md) как строку.

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
<td><p><strong>adClipString</strong></p></td>
<td><p>2</p></td>
<td><p>Разделяет строк по <em>RowDelimiter</em>столбцов по <em>ColumnDelimiter</em>и пустых значений по <em>NullExpr</em>. Эти три параметра метода <a href="getstring-method-ado.md">GetString</a> являются допустимыми только с <em>StringFormat</em> из <strong>adClipString</strong>.</p></td>
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
<td><p>AdoEnums.StringFormat.CLIPSTRING</p></td>
</tr>
</tbody>
</table>

