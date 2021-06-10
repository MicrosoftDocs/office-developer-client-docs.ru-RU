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
# <a name="formal-shape-grammar"></a><span data-ttu-id="088c8-102">Формальная грамматика фигур</span><span class="sxs-lookup"><span data-stu-id="088c8-102">Formal shape grammar</span></span>

<span data-ttu-id="088c8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="088c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="088c8-104">Это формальная грамматика для создания любой команды фигуры:</span><span class="sxs-lookup"><span data-stu-id="088c8-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="088c8-105">Необходимые грамматические термины — это текстовые строки, делимитированные угловой скобками \< \> ("").</span><span class="sxs-lookup"><span data-stu-id="088c8-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="088c8-106">Необязательные термины делимитированы квадратными скобками \[ \] ("").</span><span class="sxs-lookup"><span data-stu-id="088c8-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="088c8-107">Альтернативы указываются виргулем ("|").</span><span class="sxs-lookup"><span data-stu-id="088c8-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="088c8-108">Повторяемая альтернатива указывается эллипсисом ("...").</span><span class="sxs-lookup"><span data-stu-id="088c8-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="088c8-109">*Альфа* указывает строку алфавитных букв.</span><span class="sxs-lookup"><span data-stu-id="088c8-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="088c8-110">*Цифры* указывают строку чисел.</span><span class="sxs-lookup"><span data-stu-id="088c8-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="088c8-111">*Однозначный код* указывает строку однокодовой цифры.</span><span class="sxs-lookup"><span data-stu-id="088c8-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="088c8-112">Все остальные термины являются буквальными.</span><span class="sxs-lookup"><span data-stu-id="088c8-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="088c8-113">Термин</span><span class="sxs-lookup"><span data-stu-id="088c8-113">Term</span></span></p></th>
<th><p><span data-ttu-id="088c8-114">Определение</span><span class="sxs-lookup"><span data-stu-id="088c8-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="088c8-115">&lt;shape-command&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-116">SHAPE &lt; [table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</span><span class="sxs-lookup"><span data-stu-id="088c8-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-117">&lt;table-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-118">&lt;{provider-command-text &gt; } |</span><span class="sxs-lookup"><span data-stu-id="088c8-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="088c8-119">&lt;(shape-command) &gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="088c8-120">Table &lt; quoted-name&gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="088c8-121">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-122">&lt;shape-action&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-123">&lt;Aliased-field-list APPEND&gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="088c8-124">Compute &lt; aliased-field-list &gt; [BY &lt; field-list] &gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-125">&lt;aliased-field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-126">&lt;aliased-field &gt; [, &lt; aliased-field...] &gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-127">&lt;aliased-field&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-128">&lt;псевдоним &gt; field-exp &lt; [AS] &gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-129">&lt;field-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-130">( &lt; relation-exp &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="088c8-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="088c8-131">&lt;calculated-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="088c8-132">&lt;aggregate-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="088c8-133">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-135">&lt;псевдоним &gt; table-exp [[AS] &lt; &gt; ]</span><span class="sxs-lookup"><span data-stu-id="088c8-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="088c8-136">&lt;псевдоним &gt; table-exp [[AS] &lt; &gt; ]</span><span class="sxs-lookup"><span data-stu-id="088c8-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-137">&lt;relation-cond-list&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-138">&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...]</span><span class="sxs-lookup"><span data-stu-id="088c8-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-139">&lt;relation-cond&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-140">&lt;field-name &gt; TO &lt; child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-141">&lt;child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-142">&lt;имя поля&gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="088c8-143">ПАРАМЕТР &lt; param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-144">&lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-145">&lt;число&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-146">&lt;field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-147">&lt;имя &gt; поля [, &lt; имя &gt; поля]</span><span class="sxs-lookup"><span data-stu-id="088c8-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-148">&lt;aggregate-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-149">&lt;SUM(qualified-field-name) &gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="088c8-150">AVG &lt; (qualified-field-name) &gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="088c8-151">MIN &lt; (qualified-field-name) &gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="088c8-152">MAX &lt; (qualified-field-name) &gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="088c8-153">COUNT &lt; (квалифицированное &gt;  |  &lt; псевдонимное &gt; имя) |</span><span class="sxs-lookup"><span data-stu-id="088c8-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="088c8-154">STDEV &lt; (qualified-field-name) &gt; |</span><span class="sxs-lookup"><span data-stu-id="088c8-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="088c8-155">&lt;ANY(qualified-field-name) &gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-156">&lt;calculated-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-157">CALC &lt; &gt; (выражение)</span><span class="sxs-lookup"><span data-stu-id="088c8-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-158">&lt;qualified-field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-159">&lt;псевдоним &gt; .[ &lt; псевдоним &gt; ...] &lt; имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-160">&lt;псевдоним&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-161">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-162">&lt;имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-163">&lt;псевдоним quoted-name &gt; [[AS] &lt; &gt; ]</span><span class="sxs-lookup"><span data-stu-id="088c8-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-164">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-165">&quot;&lt;строка&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="088c8-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="088c8-166">' &lt; string &gt; ' |</span><span class="sxs-lookup"><span data-stu-id="088c8-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="088c8-167">&lt; &gt; [строка] |</span><span class="sxs-lookup"><span data-stu-id="088c8-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="088c8-168">&lt;имя&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-169">&lt;qualified-name&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-170">псевдоним [.alias...]</span><span class="sxs-lookup"><span data-stu-id="088c8-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-171">&lt;имя&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-172">альфа [альфа | цифры | _ | # | : | ...]</span><span class="sxs-lookup"><span data-stu-id="088c8-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-173">&lt;число&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-174">цифры [цифры...]</span><span class="sxs-lookup"><span data-stu-id="088c8-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-175">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-176">NEW &lt; field-type &gt; [( &lt; number &gt; [, number &lt; &gt; ])]</span><span class="sxs-lookup"><span data-stu-id="088c8-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-177">&lt;тип поля&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-178">Тип данных OLE DB или ADO.</span><span class="sxs-lookup"><span data-stu-id="088c8-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="088c8-179">&lt;string&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-180">unicode-char [unicode-char...]</span><span class="sxs-lookup"><span data-stu-id="088c8-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="088c8-181">&lt;выражение&gt;</span><span class="sxs-lookup"><span data-stu-id="088c8-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="088c8-182">Выражение Visual Basic для приложений, операндами которого являются другие столбцы, не относяльные к CALC, в одной строке.</span><span class="sxs-lookup"><span data-stu-id="088c8-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

