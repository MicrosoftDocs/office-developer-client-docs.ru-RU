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

Это формальная грамматика для создания любой команды фигуры:

  - Необходимые грамматические термины — это текстовые строки, делимитированные угловой скобками \< \> ("").

  - Необязательные термины делимитированы квадратными скобками \[ \] ("").

  - Альтернативы указываются виргулем ("|").

  - Повторяемая альтернатива указывается эллипсисом ("...").

  - *Альфа* указывает строку алфавитных букв.

  - *Цифры* указывают строку чисел.

  - *Однозначный код* указывает строку однокодовой цифры.

Все остальные термины являются буквальными.

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
<td><p>&lt;shape-command&gt;</p></td>
<td><p>SHAPE &lt; [table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;table-exp&gt;</p></td>
<td><p>&lt;{provider-command-text &gt; } |<br />
&lt;(shape-command) &gt; |<br />
Table &lt; quoted-name&gt; |<br />
&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;shape-action&gt;</p></td>
<td><p>&lt;Aliased-field-list APPEND&gt; |</p>
<p>Compute &lt; aliased-field-list &gt; [BY &lt; field-list] &gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;aliased-field-list&gt;</p></td>
<td><p>&lt;aliased-field &gt; [, &lt; aliased-field...] &gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aliased-field&gt;</p></td>
<td><p>&lt;псевдоним &gt; field-exp &lt; [AS] &gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-exp&gt;</p></td>
<td><p>( &lt; relation-exp &gt; ) |</p>
<p>&lt;calculated-exp&gt; |</p>
<p>&lt;aggregate-exp&gt; |</p>
<p>&lt;new-exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;псевдоним &gt; table-exp [[AS] &lt; &gt; ]</p>
<p>&lt;псевдоним &gt; table-exp [[AS] &lt; &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;relation-cond-list&gt;</p></td>
<td><p>&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation-cond&gt;</p></td>
<td><p>&lt;field-name &gt; TO &lt; child-ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;child-ref&gt;</p></td>
<td><p>&lt;имя поля&gt; |</p>
<p>ПАРАМЕТР &lt; param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-ref&gt;</p></td>
<td><p>&lt;число&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-list&gt;</p></td>
<td><p>&lt;имя &gt; поля [, &lt; имя &gt; поля]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aggregate-exp&gt;</p></td>
<td><p>&lt;SUM(qualified-field-name) &gt; |</p>
<p>AVG &lt; (qualified-field-name) &gt; |</p>
<p>MIN &lt; (qualified-field-name) &gt; |</p>
<p>MAX &lt; (qualified-field-name) &gt; |</p>
<p>COUNT &lt; (квалифицированное &gt;  |  &lt; псевдонимное &gt; имя) |</p>
<p>STDEV &lt; (qualified-field-name) &gt; |</p>
<p>&lt;ANY(qualified-field-name) &gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculated-exp&gt;</p></td>
<td><p>CALC &lt; &gt; (выражение)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-field-name&gt;</p></td>
<td><p>&lt;псевдоним &gt; .[ &lt; псевдоним &gt; ...] &lt; имя поля&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;псевдоним&gt;</p></td>
<td><p>&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;имя поля&gt;</p></td>
<td><p>&lt;псевдоним quoted-name &gt; [[AS] &lt; &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;quoted-name&gt;</p></td>
<td><p>&quot;&lt;строка&gt;&quot; |</p>
<p>' &lt; string &gt; ' |</p>
<p>&lt; &gt; [строка] |</p>
<p>&lt;имя&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-name&gt;</p></td>
<td><p>псевдоним [.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;имя&gt;</p></td>
<td><p>альфа [альфа | цифры | _ | # | : | ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;число&gt;</p></td>
<td><p>цифры [цифры...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;new-exp&gt;</p></td>
<td><p>NEW &lt; field-type &gt; [( &lt; number &gt; [, number &lt; &gt; ])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;тип поля&gt;</p></td>
<td><p>Тип данных OLE DB или ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;string&gt;</p></td>
<td><p>unicode-char [unicode-char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;выражение&gt;</p></td>
<td><p>Выражение Visual Basic для приложений, операндами которого являются другие столбцы, не относяльные к CALC, в одной строке.</p></td>
</tr>
</tbody>
</table>

