---
title: PositionEnum (Справочник по для настольных баз данных Access)
TOCTitle: PositionEnum
ms:assetid: 2a6f294b-74f2-b951-e32a-79ff5e782204
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249054(v=office.15)
ms:contentKeyID: 48543907
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2c2ef44c804a413b85bcf393e1487ff4423c40f0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480277"
---
# <a name="positionenum"></a>PositionEnum


**Применимо к**: Access 2013 | Office 2013

Указывает текущую позицию указателя записи в наборе [записей](recordset-object-ado.md).

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
<td><p><strong>adPosBOF</strong></p></td>
<td><p>-2</p></td>
<td><p>Указывает, что указатель текущей записи BOF (то есть, свойство <a href="bof-eof-properties-ado.md">BOF</a> имеет <strong>значение True</strong>).</p></td>
</tr>
<tr class="even">
<td><p><strong>adPosEOF</strong></p></td>
<td><p>от -3</p></td>
<td><p>Указывает, что указатель текущей записи в конец файла (то есть, свойство <a href="bof-eof-properties-ado.md">EOF</a> имеет <strong>значение True</strong>).</p></td>
</tr>
<tr class="odd">
<td><p><strong>adPosUnknown</strong></p></td>
<td><p>-1</p></td>
<td><p>Показывает, что <strong>записей</strong> пуст, текущей позиции не известен, или поставщик не поддерживает свойство <a href="absolutepage-property-ado.md">AbsolutePage</a> или <a href="absoluteposition-property-ado.md">AbsolutePosition</a> .</p></td>
</tr>
</tbody>
</table>


**Эквивалент ADO/WFC**

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
<td><p>AdoEnums.Position.BOF</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Position.EOF</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Position.UNKNOWN</p></td>
</tr>
</tbody>
</table>

