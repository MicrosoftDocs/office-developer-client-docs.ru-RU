---
title: Свойство field2. Коллатингордер (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: cb1d6fc9-a2a6-54c2-abf5-48b609e38738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834380(v=office.15)
ms:contentKeyID: 48547709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02711fbbf39b058bb88e9568716169825ae4a923
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292869"
---
# <a name="field2collatingorder-property-dao"></a><span data-ttu-id="a0d84-102">Свойство field2. Коллатингордер (DAO)</span><span class="sxs-lookup"><span data-stu-id="a0d84-102">Field2.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="a0d84-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a0d84-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a0d84-104">Возвращает значение, задающее последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a0d84-104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="a0d84-105">Только для чтения, **Long**.</span><span class="sxs-lookup"><span data-stu-id="a0d84-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0d84-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a0d84-106">Syntax</span></span>

<span data-ttu-id="a0d84-107">*Expression* . Коллатингордер</span><span class="sxs-lookup"><span data-stu-id="a0d84-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="a0d84-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="a0d84-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a0d84-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0d84-109">Remarks</span></span>

<span data-ttu-id="a0d84-110">Возвращаемое значение — это **длинное** значение или константа, которая может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a0d84-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0d84-111">Константа</span><span class="sxs-lookup"><span data-stu-id="a0d84-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="a0d84-112">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="a0d84-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-113"><strong>Дбсортженерал</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-114">Общие (английский, французский, немецкий, португальский, итальянский и современная Испанская)</span><span class="sxs-lookup"><span data-stu-id="a0d84-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-115"><strong>Дбсортарабик</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-116">арабский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-117"><strong>Дбсортчинесесимплифиед</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-118">китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="a0d84-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-119"><strong>Дбсортчинесетрадитионал</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-120">китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="a0d84-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-121"><strong>Дбсортцириллик</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-122">русский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-123"><strong>Дбсорткзеч</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-124">чешский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-125"><strong>Дбсортдутч</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-126">голландский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-127"><strong>Дбсортгрик</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-128">греческий;</span><span class="sxs-lookup"><span data-stu-id="a0d84-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-129"><strong>Дбсорсебрев</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-130">иврит;</span><span class="sxs-lookup"><span data-stu-id="a0d84-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-131"><strong>Дбсорсунгариан</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-132">венгерский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-133"><strong>Дбсортицеландик</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-134">Исландский</span><span class="sxs-lookup"><span data-stu-id="a0d84-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-135"><strong>Дбсортжапанесе</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-136">японский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-137"><strong>Дбсорткореан</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-138">корейский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-139"><strong>Дбсортнеутрал</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-140">Нейтральный</span><span class="sxs-lookup"><span data-stu-id="a0d84-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-141"><strong>Дбсортнорвдан</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-142">Норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="a0d84-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-143"><strong>Дбсортпдксинтл</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-144">Международная связь Paradox</span><span class="sxs-lookup"><span data-stu-id="a0d84-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-145"><strong>Дбсортпдкснор</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-146">Paradox норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="a0d84-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-147"><strong>Дбсортпдкссве</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-148">Paradox шведский или Финский</span><span class="sxs-lookup"><span data-stu-id="a0d84-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-149"><strong>Дбсортполиш</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-150">польский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-151"><strong>Дбсортсловениан</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-152">словенский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-153"><strong>Дбсортспаниш</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-154">испанский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-155"><strong>Дбсортсведфин</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-156">Шведский или Финский</span><span class="sxs-lookup"><span data-stu-id="a0d84-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-157"><strong>Дбсортсаи</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-158">тайский;</span><span class="sxs-lookup"><span data-stu-id="a0d84-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-159"><strong>Дбсорттуркиш</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-160">турецкий;</span><span class="sxs-lookup"><span data-stu-id="a0d84-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-161"><strong>Дбсортундефинед</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="a0d84-162">Неопределенное или неизвестное</span><span class="sxs-lookup"><span data-stu-id="a0d84-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0d84-163">Доступность свойства **коллатингордер** зависит от объекта, содержащего коллекцию Fields, как \*\*\*\* показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a0d84-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a0d84-164">Если коллекция Fields принадлежит к элементу</span><span class="sxs-lookup"><span data-stu-id="a0d84-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="a0d84-165">Затем Коллатингордер</span><span class="sxs-lookup"><span data-stu-id="a0d84-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-166">Объект <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a0d84-167">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a0d84-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-168">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a0d84-169">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0d84-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-170">Объект <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a0d84-171">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0d84-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a0d84-172">Объект <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a0d84-173">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a0d84-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a0d84-174">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a0d84-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a0d84-175">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a0d84-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a0d84-176">Значение свойства **коллатингордер** соответствует аргументу языкового стандарта метода **CreateDatabase** при создании базы данных или методе **CompactDatabase** при последнем сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="a0d84-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="a0d84-177">Параметры свойств **коллатингордер** и **Attributes** объекта **field2** в коллекции Fields \*\*\*\* объекта **index** вместе определяют последовательность и направление порядка сортировки в индексе.</span><span class="sxs-lookup"><span data-stu-id="a0d84-177">The **CollatingOrder** and **Attributes** property settings of a **Field2** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index.</span></span> <span data-ttu-id="a0d84-178">Однако вы не можете задать порядок сортировки для отдельного индекса — его можно задать только для всей таблицы.</span><span class="sxs-lookup"><span data-stu-id="a0d84-178">However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

