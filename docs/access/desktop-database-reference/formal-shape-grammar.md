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
# <a name="formal-shape-grammar"></a><span data-ttu-id="551e5-102">Формальная грамматика фигур</span><span class="sxs-lookup"><span data-stu-id="551e5-102">Formal shape grammar</span></span>

<span data-ttu-id="551e5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="551e5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="551e5-104">Это формальная грамматика для создания любой команды фигуры:</span><span class="sxs-lookup"><span data-stu-id="551e5-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="551e5-105">Необходимые грамматические термины — это текстовые строки, разделимые угловой скобкой (" \< \> ").</span><span class="sxs-lookup"><span data-stu-id="551e5-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="551e5-106">Необязательные термины поотрихуются квадратными скобками (" \[ \] ").</span><span class="sxs-lookup"><span data-stu-id="551e5-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="551e5-107">Альтернативы указываются вигольным видео ("|").</span><span class="sxs-lookup"><span data-stu-id="551e5-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="551e5-108">Повторяющиеся альтернативы указываются многоязыком ("...").</span><span class="sxs-lookup"><span data-stu-id="551e5-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="551e5-109">*Альфа-адрес* указывает строку алфавитных букв.</span><span class="sxs-lookup"><span data-stu-id="551e5-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="551e5-110">*Цифра* означает строку чисел.</span><span class="sxs-lookup"><span data-stu-id="551e5-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="551e5-111">*В цифре Юникода* указывается строка цифр юникода.</span><span class="sxs-lookup"><span data-stu-id="551e5-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="551e5-112">Все остальные термины являются литералами.</span><span class="sxs-lookup"><span data-stu-id="551e5-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="551e5-113">Термин</span><span class="sxs-lookup"><span data-stu-id="551e5-113">Term</span></span></p></th>
<th><p><span data-ttu-id="551e5-114">Определение</span><span class="sxs-lookup"><span data-stu-id="551e5-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="551e5-115">&lt;shape-command&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-116">SHAPE [ &lt; table-exp &gt; [[AS] &lt; alias &gt; ]][ &lt; shape-action &gt; ]</span><span class="sxs-lookup"><span data-stu-id="551e5-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-117">&lt;table-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-118">{ &lt; provider-command-text &gt; } |</span><span class="sxs-lookup"><span data-stu-id="551e5-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="551e5-119">( &lt; shape-command &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="551e5-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="551e5-120">TABLE &lt; quoted-name&gt; |</span><span class="sxs-lookup"><span data-stu-id="551e5-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="551e5-121">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-122">&lt;shape-action&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-123">APPEND &lt; aliased-field-list&gt; |</span><span class="sxs-lookup"><span data-stu-id="551e5-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="551e5-124">COMPUTE &lt; aliased-field-list &gt; [BY &lt; field-list &gt; ]</span><span class="sxs-lookup"><span data-stu-id="551e5-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-125">&lt;aliased-field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-126">&lt;aliased-field &gt; [, &lt; aliased-field... &gt; ]</span><span class="sxs-lookup"><span data-stu-id="551e5-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-127">&lt;aliased-field&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-128">&lt;field-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="551e5-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-129">&lt;field-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-130">( &lt; relation-exp &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="551e5-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="551e5-131">&lt;calculated-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="551e5-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="551e5-132">&lt;aggregate-exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="551e5-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="551e5-133">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-135">&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="551e5-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="551e5-136">&lt;table-exp &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="551e5-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-137">&lt;relation-cond-list&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-138">&lt;relation-cond &gt; [, &lt; relation-cond &gt; ...]</span><span class="sxs-lookup"><span data-stu-id="551e5-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-139">&lt;relation-cond&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-140">&lt;field-name &gt; TO &lt; child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-141">&lt;child-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-142">&lt;field-name&gt; |</span><span class="sxs-lookup"><span data-stu-id="551e5-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="551e5-143">PARAMETER &lt; param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-144">&lt;param-ref&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-145">&lt;number&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-146">&lt;field-list&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-147">&lt;field-name &gt; [, &lt; field-name &gt; ]</span><span class="sxs-lookup"><span data-stu-id="551e5-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-148">&lt;aggregate-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-149">SUM( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="551e5-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="551e5-150">AVG( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="551e5-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="551e5-151">MIN( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="551e5-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="551e5-152">MAX( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="551e5-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="551e5-153">COUNT( &lt; qualified-alias &gt;  |  &lt; qualified-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="551e5-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="551e5-154">STDEV( &lt; qualified-field-name &gt; ) |</span><span class="sxs-lookup"><span data-stu-id="551e5-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="551e5-155">ANY( &lt; qualified-field-name &gt; )</span><span class="sxs-lookup"><span data-stu-id="551e5-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-156">&lt;calculated-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-157">CALC( &lt; выражение &gt; )</span><span class="sxs-lookup"><span data-stu-id="551e5-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-158">&lt;qualified-field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-159">&lt;псевдоним &gt; .[ &lt; псевдоним &gt; ...] &lt; field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-160">&lt;псевдоним&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-161">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-162">&lt;field-name&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-163">&lt;quoted-name &gt; [[AS] &lt; alias &gt; ]</span><span class="sxs-lookup"><span data-stu-id="551e5-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-164">&lt;quoted-name&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-165">&quot;&lt;string&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="551e5-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="551e5-166">' &lt; string &gt; ' |</span><span class="sxs-lookup"><span data-stu-id="551e5-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="551e5-167">[ &lt; string &gt; ] |</span><span class="sxs-lookup"><span data-stu-id="551e5-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="551e5-168">&lt;name&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-169">&lt;qualified-name&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-170">alias[.alias...]</span><span class="sxs-lookup"><span data-stu-id="551e5-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-171">&lt;name&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-172">alpha [ alpha | digit | _ | # | : | ...]</span><span class="sxs-lookup"><span data-stu-id="551e5-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-173">&lt;number&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-174">цифра [цифра...]</span><span class="sxs-lookup"><span data-stu-id="551e5-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-175">&lt;new-exp&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-176">NEW &lt; field-type &gt; [( &lt; number &gt; [, number &lt; &gt; ])]</span><span class="sxs-lookup"><span data-stu-id="551e5-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-177">&lt;field-type&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-178">Тип данных OLE DB или ADO.</span><span class="sxs-lookup"><span data-stu-id="551e5-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="551e5-179">&lt;string&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-180">unicode-char [unicode-char...]</span><span class="sxs-lookup"><span data-stu-id="551e5-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="551e5-181">&lt;выражение&gt;</span><span class="sxs-lookup"><span data-stu-id="551e5-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="551e5-182">Выражение Visual Basic для приложений, операнды которого являются другими столбцами, не относямися к CALC, в той же строке.</span><span class="sxs-lookup"><span data-stu-id="551e5-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

