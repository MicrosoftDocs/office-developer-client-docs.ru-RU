---
title: Свойство Property.Type (DAO)
TOCTitle: Type Property
ms:assetid: bf8258ca-08b5-c4f9-e6d7-114e4300b2ef
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822796(v=office.15)
ms:contentKeyID: 48547490
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4280b89102e06b2ecc09a783840e671b0af9ff73
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302902"
---
# <a name="propertytype-property-dao"></a>Свойство Property.Type (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, указывающее операционный тип или тип данных объекта. Для чтения и записи, **Integer**.

## <a name="syntax"></a>Синтаксис

*выражение* .Type

*выражение* Переменная, представляюная объект **Property.**

## <a name="remarks"></a>Примечания

Параметр или возвращаемое значение является константой, указывающей операционный тип или тип данных. Для объекта **[Property](property-object-dao.md)** это свойство считывать и записывать, пока объект не будет appended к коллекции или другому объекту, после чего он будет только для чтения.

Для объекта **Property** возможные параметры и возвращаемые значения описаны в следующей таблице.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbBigInt</strong></p></td>
<td><p>Большое целое</p></td>
</tr>
<tr class="even">
<td><p><strong>dbBinary</strong></p></td>
<td><p>Двоичный</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbBoolean</strong></p></td>
<td><p>Логический</p></td>
</tr>
<tr class="even">
<td><p><strong>dbByte</strong></p></td>
<td><p>Байт</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbChar</strong></p></td>
<td><p>Знак</p></td>
</tr>
<tr class="even">
<td><p><strong>dbCurrency</strong></p></td>
<td><p>Денежный</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDate</strong></p></td>
<td><p>Дата и время</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecimal</strong></p></td>
<td><p>Десятичный</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDouble</strong></p></td>
<td><p>Двойное</p></td>
</tr>
<tr class="even">
<td><p><strong>dbFloat</strong></p></td>
<td><p>С плавающей запятой</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbGUID</strong></p></td>
<td><p>Глобальный уникальный идентификатор (GUID)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInteger</strong></p></td>
<td><p>Целое</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLong</strong></p></td>
<td><p>Длинное целое</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLongBinary</strong></p></td>
<td><p>Длинное двоичное (объект OLE)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMemo</strong></p></td>
<td><p>Memo</p></td>
</tr>
<tr class="even">
<td><p><strong>dbNumeric</strong></p></td>
<td><p>Числовой</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSingle</strong></p></td>
<td><p>Одинарное</p></td>
</tr>
<tr class="even">
<td><p><strong>dbText</strong></p></td>
<td><p>Текст</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbTime</strong></p></td>
<td><p>Время</p></td>
</tr>
<tr class="even">
<td><p><strong>dbTimeStamp</strong></p></td>
<td><p>Метка времени</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVarBinary</strong></p></td>
<td><p>VarBinary</p></td>
</tr>
</tbody>
</table>


Когда новый объект **Field**, **Parameter** или **Property** добавляется в коллекцию объектов **[Index](index-object-dao.md)**, **QueryDef**, **Recordset** или **TableDef**, возникает ошибка, если основная база данных не поддерживает тип данных, указанный для нового объекта.

