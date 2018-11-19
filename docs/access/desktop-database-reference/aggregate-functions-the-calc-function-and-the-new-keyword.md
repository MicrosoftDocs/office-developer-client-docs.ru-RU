---
title: Агрегатные функции, функция CALC и ключевое слово NEW
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fb3e667a23d5bfd1d3dda5b4eb8dbd60a47e36ba
ms.sourcegitcommit: 45feafb3b55de0402dddf5548c0c1c43a0eabafd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/07/2018
ms.locfileid: "26025989"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a>Агрегатные функции, функция CALC и ключевое слово NEW


**Применимо к**: Access 2013, Office 2013

Формирование данных поддерживает следующие функции. Имя, присвоенное главы, содержащую столбец, чтобы работать — это *псевдоним главы*.

Псевдонима главы может быть полным, состоящий из каждой главы имя столбца, приводя к главе, содержащая *имя столбца,* все разделенных точками. Например если главе родительского chap1, содержит дочерних главы, chap2, которая содержит столбец Сумма, сумма, а затем полным именем будет chap1.chap2.amt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Агрегатные функции</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Сумма (<em>псевдоним главы</em>.<em> Имя столбца</em>)</p></td>
<td><p>Вычисление суммы всех значений в указанном столбце.</p></td>
</tr>
<tr class="even">
<td><p>AVG (<em>псевдоним главы</em>.<em> Имя столбца</em>)</p></td>
<td><p>Вычисляет среднее значение указанного столбца.</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число (<em>псевдоним главы</em>.<em> Имя столбца</em>)</p></td>
<td><p>Вычисляет максимальное значение в указанном столбце.</p></td>
</tr>
<tr class="even">
<td><p>MIN (<em>псевдоним главы</em>.<em> Имя столбца</em>)</p></td>
<td><p>Вычисляет минимальное значение в указанном столбце.</p></td>
</tr>
<tr class="odd">
<td><p>COUNT (<em>псевдоним главы</em>[.<em> Имя столбца</em>])</p></td>
<td><p>Подсчитывает количество строк в указанном псевдоним. Если столбец указан, только строки, для которых этот столбец не равно Null включаются в подсчет.</p></td>
</tr>
<tr class="even">
<td><p>STDEV (<em>псевдоним главы</em>.<em> Имя столбца</em>)</p></td>
<td><p>Вычисляет стандартное отклонение в указанном столбце.</p></td>
</tr>
<tr class="odd">
<td><p>ЛЮБОЙ (<em>псевдоним главы</em>.<em> Имя столбца</em>)</p></td>
<td><p>Значение указанного столбца. Какие-либо имеет значение прогнозируемый только в том случае, если значение столбца является общим для всех строк в главе.</p><p><strong>Примечание</strong>: Если столбец не содержит такое же значение для всех строк в главе, команда ФИГУРЫ произвольно возвращает одно из значений в качестве значения любой функции.</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Расчетного выражения</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Вычисление (<em>выражение</em>)</p></td>
<td><p>Вычисляет произвольного выражения, но только в той строке <strong>набора записей</strong> , содержащий функция CALC. Любое выражение, с помощью этих <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений (VBA) функции</a> разрешены.</p></td>
</tr>
</tbody>
</table>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>НОВОЕ ключевое слово</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>НОВЫЙ <em>Тип поля</em> [(<em>Ширина</em> | <em>масштаба</em> | <em>точности</em> | <em>Ошибка</em> [, <em>масштаба</em> | <em>Ошибка</em>])]</p></td>
<td><p>Добавляет пустой столбец указанного типа <strong>набора записей</strong>.</p></td>
</tr>
</tbody>
</table>

<br/>

*Тип поля* , переданные с НОВЫМ ключевым словом может быть любой из следующих типов данных.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Типы данных OLE DB </p></th>
<th><p>Тип данных ADO equivalent(s)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBTYPE_BSTR</p></td>
<td><p>adBSTR</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_BOOL</p></td>
<td><p>adBoolean</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DECIMAL</p></td>
<td><p>adDecimal</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI1</p></td>
<td><p>adUnsignedTinyInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_I1</p></td>
<td><p>adTinyInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI2</p></td>
<td><p>adUnsignedSmallInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI4</p></td>
<td><p>adUnsignedInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_I8</p></td>
<td><p>adBigInt</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI8</p></td>
<td><p>adUnsignedBigInt</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_GUID</p></td>
<td><p>adGuid</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_BYTES</p></td>
<td><p>adBinary, AdVarBinary, adLongVarBinary</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_STR</p></td>
<td><p>adChar, adVarChar, adLongVarChar</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_WSTR</p></td>
<td><p>adWChar, adVarWChar, adLongVarWChar</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_NUMERIC</p></td>
<td><p>adNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBDATE</p></td>
<td><p>adDBDate</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_DBTIME</p></td>
<td><p>adDBTime</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBTIMESTAMP</p></td>
<td><p>adDBTimeStamp</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_VARNUMERIC</p></td>
<td><p>adVarNumeric</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_FILETIME</p></td>
<td><p>adFileTime</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_ERROR</p></td>
<td><p>adError</p></td>
</tr>
</tbody>
</table>


Если новое поле имеет тип decimal (в OLE DB DBTYPE\_DECIMAL, или в ADO, adDecimal), необходимо указать значения точности и масштаба.

