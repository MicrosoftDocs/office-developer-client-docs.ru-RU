---
title: Официальные фигуры грамматики
TOCTitle: Formal shape grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0de4f2eca0b5dd607cb9d93cc7e90f4af0ba8d89
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945539"
---
# <a name="formal-shape-grammar"></a>Официальные фигуры грамматики

**Применимо к**: Access 2013, Office 2013

Это официальную грамматики для создания любой фигуры команд:

  - Необходимые условия грамматических требуются текстовые строки угловые скобки (»\<\>«).

  - Дополнительные термины разделяются квадратные скобки (»\[ \]«).

  - Альтернативы обозначены делительная черта (» |»).

  - Повторяющиеся альтернативы обозначены многоточие («...»).

  - *Буква* указывает строку алфавитном букв.

  - *Цифра* указывает строку номеров.

  - *Юникод цифра* указывает строки знаков Юникод.

Все остальные слова, литералы.

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
<td><p>&lt;Команда фигуры&gt;</p></td>
<td><p>ФИГУРА [&lt;таблице exp&gt; [[AS] &lt;псевдоним&gt;]] [&lt;действия фигуры&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;в таблице exp&gt;</p></td>
<td><p>{&lt;текст команды поставщика&gt;} |<br />
(&lt;фигуры command&gt;) |<br />
В ТАБЛИЦЕ &lt;quoted имя&gt; |<br />
&lt;в кавычках имя&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Действие фигуры&gt;</p></td>
<td><p>ДОБАВЛЕНИЕ &lt;список полей псевдонимом&gt; |</p>
<p>ВЫЧИСЛЕНИЕ &lt;список полей псевдонимом&gt; [по &lt;список полей&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Список полей псевдонимом&gt;</p></td>
<td><p>&lt;Псевдонимы поля&gt; [, &lt;псевдонимы поля... &gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;псевдоним поля&gt;</p></td>
<td><p>&lt;поле exp&gt; [[AS] &lt;псевдоним&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;поле exp&gt;</p></td>
<td><p>(&lt;отношения exp&gt;) |</p>
<p>&lt;вычисляется exp&gt; |</p>
<p>&lt;выполняется статистическая обработка exp&gt; |</p>
<p>&lt;новые exp&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;relation_exp&gt;</p></td>
<td><p>&lt;в таблице exp&gt; [[AS] &lt;псевдоним&gt;]</p>
<p>&lt;в таблице exp&gt; [[AS] &lt;псевдоним&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;отношения cond списка&gt;</p></td>
<td><p>&lt;отношения cond&gt; [, &lt;отношения cond&gt;...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;отношения cond&gt;</p></td>
<td><p>&lt;Имя поля&gt; Кому &lt;дочерних ref&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;параметры ref дочерних&gt;</p></td>
<td><p>&lt;Имя поля&gt; |</p>
<p>ПАРАМЕТР &lt;ref параметров&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;параметр ref&gt;</p></td>
<td><p>&lt;номер&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;Список полей&gt;</p></td>
<td><p>&lt;Имя поля&gt; [, &lt;имя поля&gt;]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;выполняется статистическая обработка exp&gt;</p></td>
<td><p>Сумма (&lt;-поля имя с указанием&gt;) |</p>
<p>AVG (&lt;-поля имя с указанием&gt;) |</p>
<p>MIN (&lt;-поля имя с указанием&gt;) |</p>
<p>Максимальное число (&lt;-поля имя с указанием&gt;) |</p>
<p>COUNT (&lt;рекомендованные псевдоним&gt; | &lt;имя с указанием&gt;) |</p>
<p>STDEV (&lt;-поля имя с указанием&gt;) |</p>
<p>ЛЮБОЙ (&lt;-поля имя с указанием&gt;)</p></td>
</tr>
<tr class="even">
<td><p>&lt;вычисляется exp&gt;</p></td>
<td><p>Вычисление (&lt;выражение&gt;)</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Рекомендованные--имя поля&gt;</p></td>
<td><p>&lt;псевдоним&gt;. [&lt;псевдоним&gt;...] &lt;имя поля&gt;</p></td>
</tr>
<tr class="even">
<td><p>&lt;псевдоним&gt;</p></td>
<td><p>&lt;в кавычках имя&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Имя поля&gt;</p></td>
<td><p>&lt;в кавычках, имя&gt; [[AS] &lt;псевдоним&gt;]</p></td>
</tr>
<tr class="even">
<td><p>&lt;в кавычках имя&gt;</p></td>
<td><p>&quot;&lt;Строка&gt;&quot; |</p>
<p>"&lt;строка&gt;" |</p>
<p>[&lt;строка&gt;] |</p>
<p>&lt;Имя&gt;</p></td>
</tr>
<tr class="odd">
<td><p>&lt;имя с указанием&gt;</p></td>
<td><p>псевдоним [.alias]</p></td>
</tr>
<tr class="even">
<td><p>&lt;Имя&gt;</p></td>
<td><p>буква [буква | цифры | _ | # |: |...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;номер&gt;</p></td>
<td><p>цифры [цифра]</p></td>
</tr>
<tr class="even">
<td><p>&lt;новые exp&gt;</p></td>
<td><p>НОВЫЕ &lt;типа поля&gt; [(&lt;номер&gt; [, &lt;номер&gt;])]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;Тип поля&gt;</p></td>
<td><p>Тип данных OLE DB или ADO.</p></td>
</tr>
<tr class="even">
<td><p>&lt;Строка&gt;</p></td>
<td><p>символ Юникода [символ unicode...]</p></td>
</tr>
<tr class="odd">
<td><p>&lt;expression&gt;</p></td>
<td><p>Visual Basic для приложений выражения операнды которых являются другие не Вычисление столбцов в той же строке.</p></td>
</tr>
</tbody>
</table>

