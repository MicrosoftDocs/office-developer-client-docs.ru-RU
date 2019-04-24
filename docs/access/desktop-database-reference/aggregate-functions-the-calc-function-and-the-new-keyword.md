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
<td><p>ПодСчитывает количество строк в указанном псевдониме. Если указан столбец, в число включаются только те строки, для которых этот столбец имеет значение, отличное от NULL.</p></td>
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
<td><p>New <em>field-Type</em> [(<em>Ошибка</em> <em>точности</em> | <em>масштабирования</em> | <em>ширины</em> | , ошибка <em>масштабирования</em> | <em></em>])]</p></td>
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
<td><p>ДБТИПЕ_БСТР</p></td>
<td><p>Адбстр</p></td>
</tr>
<tr class="even">
<td><p>ДБТИПЕ_БУЛ</p></td>
<td><p>Адбулеан</p></td>
</tr>
<tr class="odd">
<td><p>ДБТИПЕ_ДЕЦИМАЛ</p></td>
<td><p>АддеЦимал</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI1</p></td>
<td><p>Адунсигнедтининт</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_I1</p></td>
<td><p>Адтининт</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_UI2</p></td>
<td><p>Адунсигнедсмаллинт</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI4</p></td>
<td><p>Адунсигнединт</p></td>
</tr>
<tr class="even">
<td><p>DBTYPE_I8</p></td>
<td><p>Адбигинт</p></td>
</tr>
<tr class="odd">
<td><p>DBTYPE_UI8</p></td>
<td><p>Адунсигнедбигинт</p></td>
</tr>
<tr class="even">
<td><p>ДБТИПЕ_ГУИД</p></td>
<td><p>Адгуид</p></td>
</tr>
<tr class="odd">
<td><p>ДБТИПЕ_БИТЕС</p></td>
<td><p>Адбинари, Адварбинари, Адлонгварбинари</p></td>
</tr>
<tr class="even">
<td><p>ДБТИПЕ_СТР</p></td>
<td><p>Адчар, Адварчар, Адлонгварчар</p></td>
</tr>
<tr class="odd">
<td><p>ДБТИПЕ_ВСТР</p></td>
<td><p>Адвчар, Адварвчар, Адлонгварвчар</p></td>
</tr>
<tr class="even">
<td><p>ДБТИПЕ_НУМЕРИК</p></td>
<td><p>Аднумерик</p></td>
</tr>
<tr class="odd">
<td><p>ДБТИПЕ_ДБДАТЕ</p></td>
<td><p>Аддбдате</p></td>
</tr>
<tr class="even">
<td><p>ДБТИПЕ_ДБТИМЕ</p></td>
<td><p>Аддбтиме</p></td>
</tr>
<tr class="odd">
<td><p>ДБТИПЕ_ДБТИМЕСТАМП</p></td>
<td><p>Аддбтиместамп</p></td>
</tr>
<tr class="even">
<td><p>ДБТИПЕ_ВАРНУМЕРИК</p></td>
<td><p>Адварнумерик</p></td>
</tr>
<tr class="odd">
<td><p>ДБТИПЕ_ФИЛЕТИМЕ</p></td>
<td><p>Адфилетиме</p></td>
</tr>
<tr class="even">
<td><p>ДБТИПЕ_ЕРРОР</p></td>
<td><p>Адеррор</p></td>
</tr>
</tbody>
</table>


Если новое поле имеет тип Decimal (в OLE DB, DBTYPE\_Decimal или в ADO, аддеЦимал), необходимо указать значения точности и масштаба.

