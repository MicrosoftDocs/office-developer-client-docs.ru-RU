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

Функция формирования данных поддерживает следующие функции. Имя, присвоенное разделу, содержащему столбец, с которым выполняется работа, — это *псевдоним главы*.

Название главы — псевдоним может быть полностью полным, состоящим из каждого имени столбца главы, которое начинается с раздела *, содержащего имя столбца,* разделенных точками. Например, если родительская глава, Chap1, содержит дочернюю главу, Chap2, которая содержит столбец Amount (сумма), то полное имя будет Chap1. Chap2. AMT.

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
<td><p>SUM (<em>Chapter-Alias</em>.<em> column-name</em>)</p></td>
<td><p>Вычисляет сумму всех значений в указанном столбце.</p></td>
</tr>
<tr class="even">
<td><p>AVG (<em>Chapter-Alias</em>.<em> column-name</em>)</p></td>
<td><p>Вычисляет среднее для всех значений в указанном столбце.</p></td>
</tr>
<tr class="odd">
<td><p>MAX (<em>Chapter-Alias</em>.<em> column-name</em>)</p></td>
<td><p>Вычисляет максимальное значение в указанном столбце.</p></td>
</tr>
<tr class="even">
<td><p>MIN (<em>Chapter-Alias</em>.<em> column-name</em>)</p></td>
<td><p>Вычисляет минимальное значение в указанном столбце.</p></td>
</tr>
<tr class="odd">
<td><p>COUNT (<em>Chapter-Alias</em>[.<em> column-name</em>])</p></td>
<td><p>Подсчитывает количество строк в указанном псевдониме. Если указан столбец, в число включаются только те строки, для которых этот столбец имеет значение, отличное от NULL.</p></td>
</tr>
<tr class="even">
<td><p>СТАНДОТКЛОН (<em>Chapter-Alias</em>.<em> column-name</em>)</p></td>
<td><p>Вычисляет стандартное отклонение в указанном столбце.</p></td>
</tr>
<tr class="odd">
<td><p>ANY (<em>Chapter-Alias</em>.<em> column-name</em>)</p></td>
<td><p>Значение указанного столбца. Значение ANY имеет прогнозируемое значение, только если значение столбца одинаково для всех строк в главе.</p><p><strong>Note</strong>: если столбец содержит одно и то же значение для всех строк в главе, команда Shape произвольно возвращает одно из значений в качестве значения функции Any.</p></td>
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
<th><p>Вычисляемое выражение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>CALC (<em>выражение</em>)</p></td>
<td><p>Вычисляет произвольное выражение, но только для строки <strong>Recordset</strong> , СОДЕРЖАЩЕЙ функцию Calc. Любое выражение, использующее эти <a href="visual-basic-for-applications-functions.md">функции Visual Basic для приложений (VBA)</a> , разрешено.</p></td>
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
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>New <em>field-Type</em> [(<em>Ошибка</em> <em>точности</em> | <em>масштабирования</em> | <em>ширины</em> | , ошибка <em>масштабирования</em> | <em>error</em>])]</p></td>
<td><p>Добавляет в <strong>набор записей</strong>пустой столбец указанного типа.</p></td>
</tr>
</tbody>
</table>

<br/>

*Типом поля* , передаваемым с помощью ключевого слова New, может быть любой из следующих типов данных.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Типы данных OLE DB</p></th>
<th><p>Эквиваленты типов данных ADO</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>DBTYPE_BSTR</p></td>
<td><p>адбстр</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_BOOL</p></td>
<td><p>адбулеан</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DECIMAL</p></td>
<td><p>аддеЦимал</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI1</p></td>
<td><p>адунсигнедтининт</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_I1</p></td>
<td><p>адтининт</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI2</p></td>
<td><p>адунсигнедсмаллинт</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI4</p></td>
<td><p>адунсигнединт</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_I8</p></td>
<td><p>адбигинт</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI8</p></td>
<td><p>адунсигнедбигинт</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_GUID</p></td>
<td><p>адгуид</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_BYTES</p></td>
<td><p>Адбинари, Адварбинари, Адлонгварбинари</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_STR</p></td>
<td><p>Адчар, Адварчар, Адлонгварчар</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_WSTR</p></td>
<td><p>Адвчар, Адварвчар, Адлонгварвчар</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_NUMERIC</p></td>
<td><p>аднумерик</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBDATE</p></td>
<td><p>аддбдате</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_DBTIME</p></td>
<td><p>аддбтиме</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_DBTIMESTAMP</p></td>
<td><p>аддбтиместамп</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_VARNUMERIC</p></td>
<td><p>адварнумерик</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_FILETIME</p></td>
<td><p>адфилетиме</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_ERROR</p></td>
<td><p>адеррор</p></td>
</tr>
</tbody>
</table>


Если новое поле имеет тип Decimal (в OLE DB, DBTYPE\_Decimal или в ADO, аддеЦимал), необходимо указать значения точности и масштаба.

