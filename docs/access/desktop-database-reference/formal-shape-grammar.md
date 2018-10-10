---
title: Formal Shape Grammar
TOCTitle: Formal Shape Grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 06548b96a3c23014f23b5123965476c5d1149b6d
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482843"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="421a7-102">Formal Shape Grammar</span><span class="sxs-lookup"><span data-stu-id="421a7-102">Formal Shape Grammar</span></span>


<span data-ttu-id="421a7-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="421a7-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="421a7-104">Это официальную грамматики для создания любой фигуры команд:</span><span class="sxs-lookup"><span data-stu-id="421a7-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="421a7-105">Необходимые условия грамматических требуются текстовые строки угловые скобки (»\<\>«).</span><span class="sxs-lookup"><span data-stu-id="421a7-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="421a7-106">Дополнительные термины разделяются квадратные скобки (»\[ \]«).</span><span class="sxs-lookup"><span data-stu-id="421a7-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="421a7-107">Альтернативы обозначены делительная черта (» |»).</span><span class="sxs-lookup"><span data-stu-id="421a7-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="421a7-108">Повторяющиеся альтернативы обозначены многоточие («...»).</span><span class="sxs-lookup"><span data-stu-id="421a7-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="421a7-109">*Буква* указывает строку алфавитном букв.</span><span class="sxs-lookup"><span data-stu-id="421a7-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="421a7-110">*Цифра* указывает строку номеров.</span><span class="sxs-lookup"><span data-stu-id="421a7-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="421a7-111">*Юникод цифра* указывает строки знаков Юникод.</span><span class="sxs-lookup"><span data-stu-id="421a7-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="421a7-112">Все остальные слова, литералы.</span><span class="sxs-lookup"><span data-stu-id="421a7-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="421a7-113">Термин</span><span class="sxs-lookup"><span data-stu-id="421a7-113">Term</span></span></p></th>
<th><p><span data-ttu-id="421a7-114">Определение</span><span class="sxs-lookup"><span data-stu-id="421a7-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="421a7-115">&lt;Команда фигуры&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-116">ФИГУРА [&lt;таблице exp&gt; [[AS] &lt;псевдоним&gt;]] [&lt;действия фигуры&gt;]</span><span class="sxs-lookup"><span data-stu-id="421a7-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-117">&lt;в таблице exp&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-118">{&lt;текст команды поставщика&gt;} |</span><span class="sxs-lookup"><span data-stu-id="421a7-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="421a7-119">(&lt;фигуры command&gt;) |</span><span class="sxs-lookup"><span data-stu-id="421a7-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="421a7-120">В ТАБЛИЦЕ &lt;quoted имя&gt; |</span><span class="sxs-lookup"><span data-stu-id="421a7-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="421a7-121">&lt;в кавычках имя&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-122">&lt;Действие фигуры&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-123">ДОБАВЛЕНИЕ &lt;список полей псевдонимом&gt; |</span><span class="sxs-lookup"><span data-stu-id="421a7-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="421a7-124">ВЫЧИСЛЕНИЕ &lt;список полей псевдонимом&gt; [по &lt;список полей&gt;]</span><span class="sxs-lookup"><span data-stu-id="421a7-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-125">&lt;Список полей псевдонимом&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-126">&lt;Псевдонимы поля&gt; [, &lt;псевдонимы поля... &gt;]</span><span class="sxs-lookup"><span data-stu-id="421a7-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-127">&lt;псевдоним поля&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-128">&lt;поле exp&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="421a7-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-129">&lt;поле exp&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-130">(&lt;отношения exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="421a7-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="421a7-131">&lt;вычисляется exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="421a7-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="421a7-132">&lt;выполняется статистическая обработка exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="421a7-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="421a7-133">&lt;новые exp&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-135">&lt;в таблице exp&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="421a7-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="421a7-136">&lt;в таблице exp&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="421a7-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-137">&lt;отношения cond списка&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-138">&lt;отношения cond&gt; [, &lt;отношения cond&gt;...]</span><span class="sxs-lookup"><span data-stu-id="421a7-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-139">&lt;отношения cond&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-140">&lt;Имя поля&gt; Кому &lt;дочерних ref&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-141">&lt;параметры ref дочерних&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-142">&lt;Имя поля&gt; |</span><span class="sxs-lookup"><span data-stu-id="421a7-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="421a7-143">ПАРАМЕТР &lt;ref параметров&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-144">&lt;параметр ref&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-145">&lt;номер&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-146">&lt;Список полей&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-147">&lt;Имя поля&gt; [, &lt;имя поля&gt;]</span><span class="sxs-lookup"><span data-stu-id="421a7-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-148">&lt;выполняется статистическая обработка exp&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-149">Сумма (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="421a7-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="421a7-150">AVG (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="421a7-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="421a7-151">MIN (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="421a7-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="421a7-152">Максимальное число (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="421a7-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="421a7-153">COUNT (&lt;рекомендованные псевдоним&gt; | &lt;имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="421a7-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="421a7-154">STDEV (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="421a7-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="421a7-155">ЛЮБОЙ (&lt;-поля имя с указанием&gt;)</span><span class="sxs-lookup"><span data-stu-id="421a7-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-156">&lt;вычисляется exp&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-157">Вычисление (&lt;выражение&gt;)</span><span class="sxs-lookup"><span data-stu-id="421a7-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-158">&lt;Рекомендованные--имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-159">&lt;псевдоним&gt;. [&lt;псевдоним&gt;...] &lt;имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-160">&lt;псевдоним&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-161">&lt;в кавычках имя&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-162">&lt;Имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-163">&lt;в кавычках, имя&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="421a7-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-164">&lt;в кавычках имя&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-165">&quot;&lt;Строка&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="421a7-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="421a7-166">"&lt;строка&gt;" |</span><span class="sxs-lookup"><span data-stu-id="421a7-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="421a7-167">[&lt;строка&gt;] |</span><span class="sxs-lookup"><span data-stu-id="421a7-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="421a7-168">&lt;Имя&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-169">&lt;имя с указанием&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-170">псевдоним [.alias]</span><span class="sxs-lookup"><span data-stu-id="421a7-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-171">&lt;Имя&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-172">буква [буква | цифры | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="421a7-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-173">&lt;номер&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-174">цифры [цифра]</span><span class="sxs-lookup"><span data-stu-id="421a7-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-175">&lt;новые exp&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-176">НОВЫЕ &lt;типа поля&gt; [(&lt;номер&gt; [, &lt;номер&gt;])]</span><span class="sxs-lookup"><span data-stu-id="421a7-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-177">&lt;Тип поля&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-178">Тип данных OLE DB или ADO.</span><span class="sxs-lookup"><span data-stu-id="421a7-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="421a7-179">&lt;Строка&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-180">символ Юникода [символ unicode...]</span><span class="sxs-lookup"><span data-stu-id="421a7-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="421a7-181">&lt;expression&gt;</span><span class="sxs-lookup"><span data-stu-id="421a7-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="421a7-182">Visual Basic для приложений выражения операнды которых являются другие не Вычисление столбцов в той же строке.</span><span class="sxs-lookup"><span data-stu-id="421a7-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

