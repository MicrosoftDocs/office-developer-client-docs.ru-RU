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
# <a name="formal-shape-grammar"></a><span data-ttu-id="4bf19-102">Формальная грамматика фигур</span><span class="sxs-lookup"><span data-stu-id="4bf19-102">Formal shape grammar</span></span>

<span data-ttu-id="4bf19-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bf19-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bf19-104">Это формальное грамматическая грамматика для создания любой команды Shape:</span><span class="sxs-lookup"><span data-stu-id="4bf19-104">This is the formal grammar for creating any shape command:</span></span>

  - <span data-ttu-id="4bf19-105">Обязательные грамматические термины — это текстовые строки, разделенные угловыми скобками ("\<\>").</span><span class="sxs-lookup"><span data-stu-id="4bf19-105">Required grammatical terms are text strings delimited by angle brackets ("\<\>").</span></span>

  - <span data-ttu-id="4bf19-106">Необязательные термины разделяются квадратными скобками ("\[ \]").</span><span class="sxs-lookup"><span data-stu-id="4bf19-106">Optional terms are delimited by square brackets ("\[ \]").</span></span>

  - <span data-ttu-id="4bf19-107">Альтернативы указываются с помощью виргуле ("|").</span><span class="sxs-lookup"><span data-stu-id="4bf19-107">Alternatives are indicated by a virgule ("|").</span></span>

  - <span data-ttu-id="4bf19-108">Повторяющиеся варианты обозначаются многоточием ("...").</span><span class="sxs-lookup"><span data-stu-id="4bf19-108">Repeating alternatives are indicated by an ellipsis ("...").</span></span>

  - <span data-ttu-id="4bf19-109">*Альфа* — это строка букв в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="4bf19-109">*Alpha* indicates a string of alphabetical letters.</span></span>

  - <span data-ttu-id="4bf19-110">*Digit* указывает строку чисел.</span><span class="sxs-lookup"><span data-stu-id="4bf19-110">*Digit* indicates a string of numbers.</span></span>

  - <span data-ttu-id="4bf19-111">*Юникод — цифра* указывает строку цифр Юникода.</span><span class="sxs-lookup"><span data-stu-id="4bf19-111">*Unicode-digit* indicates a string of unicode digits.</span></span>

<span data-ttu-id="4bf19-112">Все остальные термины являются литералами.</span><span class="sxs-lookup"><span data-stu-id="4bf19-112">All other terms are literals.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bf19-113">Термин</span><span class="sxs-lookup"><span data-stu-id="4bf19-113">Term</span></span></p></th>
<th><p><span data-ttu-id="4bf19-114">Определение</span><span class="sxs-lookup"><span data-stu-id="4bf19-114">Definition</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-115">&lt;Shape – Command&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-115">&lt;shape-command&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-116">Shape [&lt;Table — exp&gt; [[AS] &lt;псевдоним&gt;]] [&lt;Shape — действие&gt;]</span><span class="sxs-lookup"><span data-stu-id="4bf19-116">SHAPE [&lt;table-exp&gt; [[AS] &lt;alias&gt;]][&lt;shape-action&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-117">&lt;Таблица — exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-117">&lt;table-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-118">{&lt;Provider – Command — Text&gt;} |</span><span class="sxs-lookup"><span data-stu-id="4bf19-118">{&lt;provider-command-text&gt;} |</span></span><br />
<span data-ttu-id="4bf19-119">(&lt;Shape-Command&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4bf19-119">(&lt;shape-command&gt;) |</span></span><br />
<span data-ttu-id="4bf19-120">Таблица &lt;, заключенная в кавычки — имя&gt; |</span><span class="sxs-lookup"><span data-stu-id="4bf19-120">TABLE &lt;quoted-name&gt; |</span></span><br />
<span data-ttu-id="4bf19-121">&lt;имя, заключенное в кавычки&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-121">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-122">&lt;Shape — действие&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-122">&lt;shape-action&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-123">Добавление &lt;псевдонима для поля со списком&gt; |</span><span class="sxs-lookup"><span data-stu-id="4bf19-123">APPEND &lt;aliased-field-list&gt; |</span></span></p>
<p><span data-ttu-id="4bf19-124">Вычислить &lt;псевдоним поля — список&gt; [по &lt;полю "список&gt;"]</span><span class="sxs-lookup"><span data-stu-id="4bf19-124">COMPUTE &lt;aliased-field-list&gt; [BY &lt;field-list&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-125">&lt;псевдоним поля списка&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-125">&lt;aliased-field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-126">&lt;псевдоним поля&gt; [, &lt;псевдоним поля...] &gt;]</span><span class="sxs-lookup"><span data-stu-id="4bf19-126">&lt;aliased-field&gt; [, &lt;aliased-field...&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-127">&lt;поле с псевдонимом&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-127">&lt;aliased-field&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-128">&lt;Field — exp&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="4bf19-128">&lt;field-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-129">&lt;поле — exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-129">&lt;field-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-130">(&lt;отношение-exp&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4bf19-130">(&lt;relation-exp&gt;) |</span></span></p>
<p><span data-ttu-id="4bf19-131">&lt;вычисляемый exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="4bf19-131">&lt;calculated-exp&gt; |</span></span></p>
<p><span data-ttu-id="4bf19-132">&lt;Aggregate — exp&gt; |</span><span class="sxs-lookup"><span data-stu-id="4bf19-132">&lt;aggregate-exp&gt; |</span></span></p>
<p><span data-ttu-id="4bf19-133">&lt;New — exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-133">&lt;new-exp&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-134">&lt;relation_exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-134">&lt;relation_exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-135">&lt;Таблица — exp&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="4bf19-135">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p>
<p><span data-ttu-id="4bf19-136">&lt;Таблица — exp&gt; [[AS] &lt;псевдоним&gt;]</span><span class="sxs-lookup"><span data-stu-id="4bf19-136">&lt;table-exp&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-137">&lt;отношение — Конд — список&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-137">&lt;relation-cond-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-138">&lt;relation — Конд&gt; [, &lt;relation – Конд&gt;...]</span><span class="sxs-lookup"><span data-stu-id="4bf19-138">&lt;relation-cond&gt; [, &lt;relation-cond&gt;...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-139">&lt;отношение — Конд&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-139">&lt;relation-cond&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-140">&lt;поле — имя&gt; &lt;дочерней ссылки&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-140">&lt;field-name&gt; TO &lt;child-ref&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-141">&lt;дочерняя ссылка&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-141">&lt;child-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-142">&lt;имя поля&gt; |</span><span class="sxs-lookup"><span data-stu-id="4bf19-142">&lt;field-name&gt; |</span></span></p>
<p><span data-ttu-id="4bf19-143">ПАРАМЕТР &lt;param — ref&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-143">PARAMETER &lt;param-ref&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-144">&lt;Param — ref&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-144">&lt;param-ref&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-145">&lt;значение&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-145">&lt;number&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-146">&lt;Список полей&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-146">&lt;field-list&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-147">&lt;Field: Name&gt; [, &lt;Field Name&gt;]</span><span class="sxs-lookup"><span data-stu-id="4bf19-147">&lt;field-name&gt; [, &lt;field-name&gt;]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-148">&lt;Aggregate — exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-148">&lt;aggregate-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-149">SUM (&lt;полное-поле-имя&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4bf19-149">SUM(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4bf19-150">AVG (&lt;полное-поле-имя&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4bf19-150">AVG(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4bf19-151">MIN (&lt;полное-поле-имя&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4bf19-151">MIN(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4bf19-152">MAX (&lt;полное-поле-имя&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4bf19-152">MAX(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4bf19-153">Count (&lt;уточненное имя&gt; | &lt;&gt;псевдонима) |</span><span class="sxs-lookup"><span data-stu-id="4bf19-153">COUNT(&lt;qualified-alias&gt; | &lt;qualified-name&gt;) |</span></span></p>
<p><span data-ttu-id="4bf19-154">СТАНДОТКЛОН (&lt;полное-поле-имя&gt;) |</span><span class="sxs-lookup"><span data-stu-id="4bf19-154">STDEV(&lt;qualified-field-name&gt;) |</span></span></p>
<p><span data-ttu-id="4bf19-155">ANY (&lt;полное-имя&gt;)</span><span class="sxs-lookup"><span data-stu-id="4bf19-155">ANY(&lt;qualified-field-name&gt;)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-156">&lt;вычисляемый exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-156">&lt;calculated-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-157">CALC (&lt;выражение&gt;)</span><span class="sxs-lookup"><span data-stu-id="4bf19-157">CALC(&lt;expression&gt;)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-158">&lt;полное имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-158">&lt;qualified-field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-159">&lt;псевдоним&gt;. [&lt;Alias&gt;...] &lt;имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-159">&lt;alias&gt;.[&lt;alias&gt;...]&lt;field-name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-160">&lt;смешан&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-160">&lt;alias&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-161">&lt;имя, заключенное в кавычки&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-161">&lt;quoted-name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-162">&lt;имя поля&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-162">&lt;field-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-163">&lt;в кавычках —&gt; имя [[AS &lt;]&gt;псевдоним]</span><span class="sxs-lookup"><span data-stu-id="4bf19-163">&lt;quoted-name&gt; [[AS] &lt;alias&gt;]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-164">&lt;имя, заключенное в кавычки&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-164">&lt;quoted-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-165">&quot;&lt;substring&gt;&quot; |</span><span class="sxs-lookup"><span data-stu-id="4bf19-165">&quot;&lt;string&gt;&quot; |</span></span></p>
<p><span data-ttu-id="4bf19-166">'&lt;строка&gt;' |</span><span class="sxs-lookup"><span data-stu-id="4bf19-166">'&lt;string&gt;' |</span></span></p>
<p><span data-ttu-id="4bf19-167">[&lt;строка&gt;] |</span><span class="sxs-lookup"><span data-stu-id="4bf19-167">[&lt;string&gt;] |</span></span></p>
<p><span data-ttu-id="4bf19-168">&lt;расширением&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-168">&lt;name&gt;</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-169">&lt;полное имя&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-169">&lt;qualified-name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-170">Alias [. alias...]</span><span class="sxs-lookup"><span data-stu-id="4bf19-170">alias[.alias...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-171">&lt;расширением&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-171">&lt;name&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-172">альфа-канал [альфа | цифра | _ | # |: |...]</span><span class="sxs-lookup"><span data-stu-id="4bf19-172">alpha [ alpha | digit | _ | # | : | ...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-173">&lt;значение&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-173">&lt;number&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-174">цифра [цифра...]</span><span class="sxs-lookup"><span data-stu-id="4bf19-174">digit [digit...]</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-175">&lt;New — exp&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-175">&lt;new-exp&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-176">New &lt;Field-Type&gt; [(&lt;число&gt; [, &lt;число&gt;])]</span><span class="sxs-lookup"><span data-stu-id="4bf19-176">NEW &lt;field-type&gt; [(&lt;number&gt; [, &lt;number&gt;])]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-177">&lt;тип поля&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-177">&lt;field-type&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-178">Тип данных OLE DB или ADO.</span><span class="sxs-lookup"><span data-stu-id="4bf19-178">An OLE DB or ADO data type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bf19-179">&lt;substring&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-179">&lt;string&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-180">Unicode – char [Unicode – char...]</span><span class="sxs-lookup"><span data-stu-id="4bf19-180">unicode-char [unicode-char...]</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bf19-181">&lt;выражение&gt;</span><span class="sxs-lookup"><span data-stu-id="4bf19-181">&lt;expression&gt;</span></span></p></td>
<td><p><span data-ttu-id="4bf19-182">Выражение Visual Basic для приложений, операнды которого являются другими столбцами, не являющимися ВЫЧИСЛЯЕМыми, в одной строке.</span><span class="sxs-lookup"><span data-stu-id="4bf19-182">A Visual Basic for Applications expression whose operands are other non-CALC columns in the same row.</span></span></p></td>
</tr>
</tbody>
</table>

