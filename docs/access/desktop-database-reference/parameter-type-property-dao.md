---
title: Свойство Parameter. Type (DAO)
TOCTitle: Type Property
ms:assetid: 68205cd6-eb45-56a3-593f-e1203472037b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195248(v=office.15)
ms:contentKeyID: 48545377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 208d0a5097b8473fef60b94f972f2c8579150fc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288023"
---
# <a name="parametertype-property-dao"></a>Свойство Parameter. Type (DAO)


**Область применения**: Access 2013, Office 2013

Задает или возвращает значение, которое указывает операционный тип или тип данных объекта. Чтение и запись **целоГо числа**.

## <a name="syntax"></a>Синтаксис

*Expression* . Тип

*Expression (выражение* ) Переменная, представляющая объект **Parameter** .

## <a name="remarks"></a>Замечания

Параметр или возвращаемое значение — это константа, указывающая операционный тип данных. Для объекта **[Parameter](parameter-object-dao.md)** в рабочей области Microsoft Access свойство доступно только для чтения.

В приведенной ниже таблице описаны возможные параметры и возвращаемые значения для объекта **Parameter** .

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
<td><p>Большое целое число</p></td>
</tr>
<tr class="even">
<td><p><strong>dbBinary</strong></p></td>
<td><p>Binary</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbBoolean</strong></p></td>
<td><p>Boolean</p></td>
</tr>
<tr class="even">
<td><p><strong>dbByte</strong></p></td>
<td><p>Байт</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbChar</strong></p></td>
<td><p>Char</p></td>
</tr>
<tr class="even">
<td><p><strong>dbCurrency</strong></p></td>
<td><p>Денежный</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDate</strong></p></td>
<td><p>Дата/время</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecimal</strong></p></td>
<td><p>Десятичное число</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDouble</strong></p></td>
<td><p>Двойное с плавающей точкой</p></td>
</tr>
<tr class="even">
<td><p><strong>dbFloat</strong></p></td>
<td><p>Float</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbGUID</strong></p></td>
<td><p>GUID</p></td>
</tr>
<tr class="even">
<td><p><strong>dbInteger</strong></p></td>
<td><p>Целое число</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLong</strong></p></td>
<td><p>Long</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLongBinary</strong></p></td>
<td><p>Большой двоичный файл (объект OLE)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbMemo</strong></p></td>
<td><p>Memo</p></td>
</tr>
<tr class="even">
<td><p><strong>dbNumeric</strong></p></td>
<td><p>Numeric</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbSingle</strong></p></td>
<td><p>Одинарное с плавающей точкой</p></td>
</tr>
<tr class="even">
<td><p><strong>dbText</strong></p></td>
<td><p>Text</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbTime</strong></p></td>
<td><p>Time</p></td>
</tr>
<tr class="even">
<td><p><strong>dbTimeStamp</strong></p></td>
<td><p>ОтМетка времени</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVarBinary</strong></p></td>
<td><p>Типа</p></td>
</tr>
</tbody>
</table>


При добавлении нового **поля**, **параметра**или объекта **Свойства** в коллекцию объекта **[index](index-object-dao.md)**, **QueryDef**, **Recordset**или **tabledef** возникает ошибка, если базовая база данных не поддерживается. тип данных, указанный для нового объекта.

