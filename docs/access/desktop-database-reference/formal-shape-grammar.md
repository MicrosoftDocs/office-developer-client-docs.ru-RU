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

  - Необходимые грамматические термины — это текстовые строки, разделимые угловой скобкой (" \< \> ").

  - Необязательные термины поотрихуются квадратными скобками (" \[ \] ").

  - Альтернативы указываются вигольным видео ("|").

  - Повторяющиеся альтернативы указываются многоязыком ("...").

  - *Альфа-адрес* указывает строку алфавитных букв.

  - *Цифра* означает строку чисел.

  - *В цифре Юникода* указывается строка цифр юникода.

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
<td><p>&lt;shape-command&gt;</p></td>
<td><p>SHAPE [ &lt; table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;table-exp&gt;</p></td>
<td><p>{ &lt; provider-command-text &gt; } |<br />
( &lt; shape-command &gt; ) |<br />
TABLE &lt; quoted-name&gt; |<br />
&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;shape-action&gt;</p></td>
<td><p>APPEND &lt; aliased-field-list&gt; |</p>
<p>COMPUTE &lt; aliased-field-list &gt; [BY &lt; field-list &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;aliased-field-list&gt;</p></td>
<td><p>&lt;aliased-field &gt; [, &lt; aliased-field... &gt; ]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aliased-field&gt;</p></td>
<td><p>&lt;field-exp &gt; [[AS] &lt; alias &gt; ]</p></td>
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
<td><p>&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</p>
<p>&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</p></td>
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
<td><p>&lt;field-name&gt; |</p>
<p>PARAMETER &lt; param-ref&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;param-ref&gt;</p></td>
<td><p>&lt;number&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;field-list&gt;</p></td>
<td><p>&lt;field-name &gt; [, &lt; field-name &gt; ]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;aggregate-exp&gt;</p></td>
<td><p>SUM( &lt; qualified-field-name &gt; ) |</p>
<p>AVG( &lt; qualified-field-name &gt; ) |</p>
<p>MIN( &lt; qualified-field-name &gt; ) |</p>
<p>MAX( &lt; qualified-field-name &gt; ) |</p>
<p>COUNT( &lt; qualified-alias &gt;  |  &lt; qualified-name &gt; ) |</p>
<p>STDEV( &lt; qualified-field-name &gt; ) |</p>
<p>ANY( &lt; qualified-field-name &gt; )</p></td>
</tr>
<tr class="even">
<td><p>&lt;calculated-exp&gt;</p></td>
<td><p>CALC( &lt; выражение &gt; )</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-field-name&gt;</p></td>
<td><p>&lt;псевдоним &gt; .[ &lt; псевдоним &gt; ...] &lt; field-name&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;псевдоним&gt;</p></td>
<td><p>&lt;quoted-name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;field-name&gt;</p></td>
<td><p>&lt;quoted-name &gt; [[AS] &lt; alias &gt; ]</p></td>
</tr>
<tr class="even">
<td><p>&lt;quoted-name&gt;</p></td>
<td><p>&quot;&lt;string&gt;&quot; |</p>
<p>' &lt; string &gt; ' |</p>
<p>[ &lt; string &gt; ] |</p>
<p>&lt;name&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;qualified-name&gt;</p></td>
<td><p>alias[.alias...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;name&gt;</p></td>
<td><p>alpha [ alpha | digit | _ | # | : | ...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;number&gt;</p></td>
<td><p>цифра [цифра...]</p></td>
</tr>
<tr class="even">
<td><p>&lt;new-exp&gt;</p></td>
<td><p>NEW &lt; field-type &gt; [( &lt; number &gt; [, number &lt; &gt; ])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;field-type&gt;</p></td>
<td><p>Тип данных OLE DB или ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;string&gt;</p></td>
<td><p>unicode-char [unicode-char...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;выражение&gt;</p></td>
<td><p>Выражение Visual Basic для приложений, операнды которого являются другими столбцами, не относямися к CALC, в той же строке.</p></td>
</tr>
</tbody>
</table>

