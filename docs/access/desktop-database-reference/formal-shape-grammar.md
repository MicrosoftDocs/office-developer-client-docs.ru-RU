---
title: Формальная грамматика фигур
TOCTitle: Formal Shape Grammar
ms:assetid: a3220569-8804-3dc3-7f9f-b4f8cdab1316
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249752(v=office.15)
ms:contentKeyID: 48546774
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f226faa303a4ff99a062449548478d32fc60612
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877151"
---
# <a name="formal-shape-grammar"></a><span data-ttu-id="5f7aa-102">Формальная грамматика фигур</span><span class="sxs-lookup"><span data-stu-id="5f7aa-102">Formal Shape Grammar</span></span>


<span data-ttu-id="5f7aa-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5f7aa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5f7aa-104">Это официальную грамматики для создания любой фигуры команд:</span><span class="sxs-lookup"><span data-stu-id="5f7aa-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="5f7aa-105">Необходимые условия грамматических требуются текстовые строки угловые скобки (»\<\>«).</span><span class="sxs-lookup"><span data-stu-id="5f7aa-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="5f7aa-106">Дополнительные термины разделяются квадратные скобки (»\[ \]«).</span><span class="sxs-lookup"><span data-stu-id="5f7aa-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="5f7aa-107">Альтернативы обозначены делительная черта (» |»).</span><span class="sxs-lookup"><span data-stu-id="5f7aa-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="5f7aa-108">Повторяющиеся альтернативы обозначены многоточие («...»).</span><span class="sxs-lookup"><span data-stu-id="5f7aa-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="5f7aa-109">*Буква* указывает строку алфавитном букв.</span><span class="sxs-lookup"><span data-stu-id="5f7aa-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="5f7aa-110">*Цифра* указывает строку номеров.</span><span class="sxs-lookup"><span data-stu-id="5f7aa-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="5f7aa-111">*Юникод цифра* указывает строки знаков Юникод.</span><span class="sxs-lookup"><span data-stu-id="5f7aa-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="5f7aa-112">Все остальные слова, литералы.</span><span class="sxs-lookup"><span data-stu-id="5f7aa-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5f7aa-113">Термин</span><span class="sxs-lookup"><span data-stu-id="5f7aa-113">Term</span></span></p></th>
<th><p><span data-ttu-id="5f7aa-114">Определение</span><span class="sxs-lookup"><span data-stu-id="5f7aa-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-115">&lt;Команда фигуры&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-116">ФИГУРА [&lt;таблице exp&gt; [[AS] &lt;псевдоним&gt;]] [&lt;действия фигуры&gt;]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-117">&lt;в таблице exp&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-118">{&lt;текст команды поставщика&gt;} |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="5f7aa-119">(&lt;фигуры command&gt;) |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="5f7aa-120">В ТАБЛИЦЕ &lt;quoted имя&gt; |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="5f7aa-121">&lt;в кавычках имя&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-122">&lt;Действие фигуры&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-123">ДОБАВЛЕНИЕ &lt;список полей псевдонимом&gt; |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="5f7aa-124">ВЫЧИСЛЕНИЕ &lt;список полей псевдонимом&gt; [по &lt;список полей&gt;]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-125">&lt;Список полей псевдонимом&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-126">&lt;Псевдонимы поля&gt; [, &lt;псевдонимы поля... &gt;]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-127">&lt;псевдоним поля&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-128">&lt;поле exp&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-129">&lt;поле exp&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-130">(&lt;отношения exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="5f7aa-131">&lt;вычисляется exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="5f7aa-132">&lt;выполняется статистическая обработка exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="5f7aa-133">&lt;новые exp&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-135">&lt;в таблице exp&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="5f7aa-136">&lt;в таблице exp&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-137">&lt;отношения cond списка&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-138">&lt;отношения cond&gt; [, &lt;отношения cond&gt;...]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-139">&lt;отношения cond&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-140">&lt;Имя поля&gt; Кому &lt;дочерних ref&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-141">&lt;параметры ref дочерних&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-142">&lt;Имя поля&gt; |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="5f7aa-143">ПАРАМЕТР &lt;ref параметров&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-144">&lt;параметр ref&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-145">&lt;номер&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-146">&lt;Список полей&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-147">&lt;Имя поля&gt; [, &lt;имя поля&gt;]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-148">&lt;выполняется статистическая обработка exp&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-149">Сумма (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="5f7aa-150">AVG (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="5f7aa-151">MIN (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="5f7aa-152">Максимальное число (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="5f7aa-153">COUNT (&lt;рекомендованные псевдоним&gt; | &lt;имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="5f7aa-154">STDEV (&lt;-поля имя с указанием&gt;) |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="5f7aa-155">ЛЮБОЙ (&lt;-поля имя с указанием&gt;)</span><span class="sxs-lookup"><span data-stu-id="5f7aa-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-156">&lt;вычисляется exp&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-157">Вычисление (&lt;выражение&gt;)</span><span class="sxs-lookup"><span data-stu-id="5f7aa-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-158">&lt;Рекомендованные--имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-159">&lt;псевдоним&gt;. [&lt;псевдоним&gt;...] &lt;имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-160">&lt;псевдоним&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-161">&lt;в кавычках имя&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-162">&lt;Имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-163">&lt;в кавычках, имя&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-164">&lt;в кавычках имя&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-165">&quot;&lt;Строка&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="5f7aa-166">"&lt;строка&gt;" |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="5f7aa-167">[&lt;строка&gt;] |</span><span class="sxs-lookup"><span data-stu-id="5f7aa-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="5f7aa-168">&lt;Имя&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-169">&lt;имя с указанием&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-170">псевдоним [.alias]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-171">&lt;Имя&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-172">буква [буква | цифры | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-173">&lt;номер&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-174">цифры [цифра]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-175">&lt;новые exp&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-176">НОВЫЕ &lt;типа поля&gt; [(&lt;номер&gt; [, &lt;номер&gt;])]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-177">&lt;Тип поля&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-178">Тип данных OLE DB или ADO.</span><span class="sxs-lookup"><span data-stu-id="5f7aa-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5f7aa-179">&lt;Строка&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-180">символ Юникода [символ unicode...]</span><span class="sxs-lookup"><span data-stu-id="5f7aa-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5f7aa-181">&lt;expression&gt;</span><span class="sxs-lookup"><span data-stu-id="5f7aa-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="5f7aa-182">Visual Basic для приложений выражения операнды которых являются другие не Вычисление столбцов в той же строке.</span><span class="sxs-lookup"><span data-stu-id="5f7aa-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

