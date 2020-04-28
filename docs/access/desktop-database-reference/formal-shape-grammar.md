---
title: Формальная грамматика фигур
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d30ff9146146bb0457a5aa383b2b720a4fdaeb78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292323"
---
# <a name="formal-shape-grammar"></a>Формальная грамматика фигур

**Область применения**: Access 2013, Office 2013

Это формальное грамматическая грамматика для создания любой команды Shape:

  - Обязательные грамматические термины — это текстовые строки, разделенные угловыми скобками ("\<\>").

  - Необязательные термины разделяются квадратными скобками ("\[ \]").

  - Альтернативы указываются с помощью виргуле ("|").

  - Повторяющиеся варианты обозначаются многоточием ("...").

  - *Альфа* — это строка букв в алфавитном порядке.

  - *Digit* указывает строку чисел.

  - *Юникод — цифра* указывает строку цифр Юникода.

Все остальные термины являются литералами.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Термин</p></th>
<th><p>Определение</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>&lt;Shape – Command&gt;</p></td>
<td><p>Shape [&lt;Table — exp&gt; [[AS] &lt;псевдоним&gt;]] [&lt;Shape — действие&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Таблица — exp&gt;</p></td>
<td><p>{&lt;Provider – Command — Text&gt;} |<br />
(&lt;Shape-Command&gt;) |<br />
Таблица &lt;, заключенная в кавычки — имя&gt; |<br />
&lt;имя, заключенное в кавычки&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Shape — действие&gt;</p></td>
<td><p>Добавление &lt;псевдонима для поля со списком&gt; |</p>
<p>Вычислить &lt;псевдоним поля — список&gt; [по &lt;полю "список&gt;"]</p></td>
</tr>
<tr class="even">
<td><p>&lt;псевдоним поля списка&gt;</p></td>
<td><p>&lt;псевдоним поля&gt; [, &lt;псевдоним поля...] &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;поле с псевдонимом&gt;</p></td>
<td><p>&lt;Field — exp&gt; [[AS] &lt;псевдоним&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;поле — exp&gt;</p></td>
<td><p>(&lt;отношение-exp&gt;) |</p>
<p>&lt;вычисляемый exp&gt; |</p>
<p>&lt;Aggregate — exp&gt; |</p>
<p>&lt;New — exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;Таблица — exp&gt; [[AS] &lt;псевдоним&gt;]</p>
<p>&lt;Таблица — exp&gt; [[AS] &lt;псевдоним&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;отношение — Конд — список&gt;</p></td>
<td><p>&lt;relation — Конд&gt; [, &lt;relation – Конд&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;отношение — Конд&gt;</p></td>
<td><p>&lt;поле — имя&gt; &lt;дочерней ссылки&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;дочерняя ссылка&gt;</p></td>
<td><p>&lt;имя поля&gt; |</p>
<p>ПАРАМЕТР &lt;param — ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Param — ref&gt;</p></td>
<td><p>&lt;значение&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Список полей&gt;</p></td>
<td><p>&lt;Field: Name&gt; [, &lt;Field Name&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Aggregate — exp&gt;</p></td>
<td><p>SUM (&lt;полное-поле-имя&gt;) |</p>
<p>AVG (&lt;полное-поле-имя&gt;) |</p>
<p>MIN (&lt;полное-поле-имя&gt;) |</p>
<p>MAX (&lt;полное-поле-имя&gt;) |</p>
<p>Count (&lt;уточненное имя&gt; | &lt;&gt;псевдонима) |</p>
<p>СТАНДОТКЛОН (&lt;полное-поле-имя&gt;) |</p>
<p>ANY (&lt;полное-имя&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;вычисляемый exp&gt;</p></td>
<td><p>CALC (&lt;выражение&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;полное имя поля&gt;</p></td>
<td><p>&lt;псевдоним&gt;. [&lt;Alias&gt;...] &lt;имя поля&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;смешан&gt;</p></td>
<td><p>&lt;имя, заключенное в кавычки&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;имя поля&gt;</p></td>
<td><p>&lt;в кавычках —&gt; имя [[AS &lt;]&gt;псевдоним]</p></td>
</tr>
<tr class="even">
<td><p>&lt;имя, заключенное в кавычки&gt;</p></td>
<td><p>&quot;&lt;substring&gt;&quot; |</p>
<p>'&lt;строка&gt;' |</p>
<p>[&lt;строка&gt;] |</p>
<p>&lt;расширением&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;полное имя&gt;</p></td>
<td><p>Alias [. alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;расширением&gt;</p></td>
<td><p>альфа-канал [альфа | цифра | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;значение&gt;</p></td>
<td><p>цифра [цифра...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;New — exp&gt;</p></td>
<td><p>New &lt;Field-Type&gt; [(&lt;число&gt; [, &lt;число&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;тип поля&gt;</p></td>
<td><p>Тип данных OLE DB или ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;substring&gt;</p></td>
<td><p>Unicode – char [Unicode – char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;выражение&gt;</p></td>
<td><p>Выражение Visual Basic для приложений, операнды которого являются другими столбцами, не являющимися ВЫЧИСЛЯЕМыми, в одной строке.</p></td>
</tr>
</tbody>
</table>

