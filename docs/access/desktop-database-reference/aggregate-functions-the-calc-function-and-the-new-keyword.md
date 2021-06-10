---
title: Агрегатные функции, функция CALC и ключевое слово NEW
TOCTitle: Aggregate functions, the CALC function, and the NEW keyword
ms:assetid: c91fef19-bf41-8d04-f195-5470fb18393f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249977(v=office.15)
ms:contentKeyID: 48547669
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 25f52489430465235a928fff3c38469ec6ba83ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297195"
---
# <a name="aggregate-functions-the-calc-function-and-the-new-keyword"></a>Агрегатные функции, функция CALC и ключевое слово NEW


**Область применения**: Access 2013, Office 2013

Формирование данных поддерживает следующие функции. Имя, назначенное главе, содержащей столбец, на котором будет работать столбец, является *псевдонимом главы*.

Псевдоним главы может быть полностью квалифицированным, состоящим из каждого имени столбца главы, ведущего к *главе,* содержащей имя столбца, разделенное по периодам. Например, если в родительской главе chap1 содержится детская глава chap2, которая содержит столбец суммы, амт, то квалифицированным именем будет chap1.chap2.amt.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Агрегатные функции</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>SUM<em>(псевдоним главы.</em><em> column-name</em>)</p></td>
<td><p>Вычисляет сумму всех значений в указанном столбце.</p></td>
</tr>
<tr class="even">
<td><p>AVG<em>(псевдоним главы.</em><em> column-name</em>)</p></td>
<td><p>Вычисляет среднее значение всех значений указанного столбца.</p></td>
</tr>
<tr class="odd">
<td><p>MAX<em>(псевдоним главы.</em><em> column-name</em>)</p></td>
<td><p>Вычисляет максимальное значение в указанном столбце.</p></td>
</tr>
<tr class="even">
<td><p>MIN<em>(псевдоним главы.</em><em> column-name</em>)</p></td>
<td><p>Вычисляет минимальное значение указанного столбца.</p></td>
</tr>
<tr class="odd">
<td><p>COUNT<em>(псевдоним главы</em>[.<em> столбец-имя</em>])</p></td>
<td><p>Подсчитывают количество строк в указанном псевдониме. Если указан столбец, в графу включаются только строки, для которых этот столбец не является Null.</p></td>
</tr>
<tr class="even">
<td><p>STDEV<em>(псевдоним главы.</em><em> column-name</em>)</p></td>
<td><p>Вычисляет стандартное отклонение в указанном столбце.</p></td>
</tr>
<tr class="odd">
<td><p>ANY<em>(псевдоним главы.</em><em> column-name</em>)</p></td>
<td><p>Значение указанного столбца. ANY имеет предсказуемое значение только в том случае, если значение столбца одинаково для всех строк в главе.</p><p><strong>ПРИМЕЧАНИЕ.</strong>Если в столбце не содержится одинаковое значение для всех строк в главе, команда SHAPE произвольно возвращает одно из значений для значения функции ANY.</p></td>
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
<th><p>Вычислимая экспрессия</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CALC<em>(выражение)</em></p></td>
<td><p>Вычисляет произвольное выражение, но только в строке <strong>Recordset,</strong> содержащей функцию CALC. Любое выражение с <a href="visual-basic-for-applications-functions.md">Visual Basic для приложений (VBA) Функции</a> разрешено.</p></td>
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
<th><p>Ключевое слово NEW</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>NEW <em>field-type</em> [(<em>ошибка</em>точности масштабирования  |  <em></em>  |  <em></em>  |  <em></em> ширины [, <em>ошибка</em>  |  <em>масштабирования])]</em></p></td>
<td><p>Добавляет пустой столбец указанного типа в <strong>набор Recordset.</strong></p></td>
</tr>
</tbody>
</table>

<br/>

Тип *поля, переданный* с помощью ключевого слова NEW, может быть любым из следующих типов данных.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Типы данных OLE DB</p></th>
<th><p>Эквивалент типа данных ADO (s)</p></th>
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


Когда новое поле имеет десятичной тип (в OLE DB, DBTYPE \_ DECIMAL или в ADO, adDecimal), необходимо указать точность и значения масштабирования.

