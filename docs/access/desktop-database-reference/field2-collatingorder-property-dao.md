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
# <a name="field2collatingorder-property-dao"></a><span data-ttu-id="17fe4-102">Свойство field2. Коллатингордер (DAO)</span><span class="sxs-lookup"><span data-stu-id="17fe4-102">Field2.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="17fe4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="17fe4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="17fe4-104">Возвращает значение, задающее последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="17fe4-104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="17fe4-105">Только для чтения, **Long**.</span><span class="sxs-lookup"><span data-stu-id="17fe4-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="17fe4-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="17fe4-106">Syntax</span></span>

<span data-ttu-id="17fe4-107">*Expression* . коллатингордер</span><span class="sxs-lookup"><span data-stu-id="17fe4-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="17fe4-108">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="17fe4-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="17fe4-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="17fe4-109">Remarks</span></span>

<span data-ttu-id="17fe4-110">Возвращаемое значение — это **длинное** значение или константа, которая может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="17fe4-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17fe4-111">Константа</span><span class="sxs-lookup"><span data-stu-id="17fe4-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="17fe4-112">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="17fe4-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-113"><strong>дбсортженерал</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-114">Общие (английский, французский, немецкий, португальский, итальянский и современная Испанская)</span><span class="sxs-lookup"><span data-stu-id="17fe4-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-115"><strong>дбсортарабик</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-116">Арабский</span><span class="sxs-lookup"><span data-stu-id="17fe4-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-117"><strong>дбсортчинесесимплифиед</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-118">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="17fe4-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-119"><strong>дбсортчинесетрадитионал</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-120">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="17fe4-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-121"><strong>дбсортцириллик</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-122">Русский</span><span class="sxs-lookup"><span data-stu-id="17fe4-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-123"><strong>дбсорткзеч</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-124">Чешский</span><span class="sxs-lookup"><span data-stu-id="17fe4-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-125"><strong>дбсортдутч</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-126">Голландский</span><span class="sxs-lookup"><span data-stu-id="17fe4-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-127"><strong>дбсортгрик</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-128">Греческий</span><span class="sxs-lookup"><span data-stu-id="17fe4-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-129"><strong>дбсорсебрев</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-130">Иврит</span><span class="sxs-lookup"><span data-stu-id="17fe4-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-131"><strong>дбсорсунгариан</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-132">Венгерский</span><span class="sxs-lookup"><span data-stu-id="17fe4-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-133"><strong>дбсортицеландик</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-134">Исландский</span><span class="sxs-lookup"><span data-stu-id="17fe4-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-135"><strong>дбсортжапанесе</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-136">Японский</span><span class="sxs-lookup"><span data-stu-id="17fe4-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-137"><strong>дбсорткореан</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-138">Корейский</span><span class="sxs-lookup"><span data-stu-id="17fe4-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-139"><strong>дбсортнеутрал</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-140">Нейтральный</span><span class="sxs-lookup"><span data-stu-id="17fe4-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-141"><strong>дбсортнорвдан</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-142">Норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="17fe4-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-143"><strong>дбсортпдксинтл</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-144">Международная связь Paradox</span><span class="sxs-lookup"><span data-stu-id="17fe4-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-145"><strong>дбсортпдкснор</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-146">Paradox норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="17fe4-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-147"><strong>дбсортпдкссве</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-148">Paradox шведский или Финский</span><span class="sxs-lookup"><span data-stu-id="17fe4-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-149"><strong>дбсортполиш</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-150">Польский</span><span class="sxs-lookup"><span data-stu-id="17fe4-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-151"><strong>дбсортсловениан</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-152">Словенский</span><span class="sxs-lookup"><span data-stu-id="17fe4-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-153"><strong>дбсортспаниш</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-154">Испанский</span><span class="sxs-lookup"><span data-stu-id="17fe4-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-155"><strong>дбсортсведфин</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-156">Шведский или Финский</span><span class="sxs-lookup"><span data-stu-id="17fe4-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-157"><strong>дбсортсаи</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-158">Тайский</span><span class="sxs-lookup"><span data-stu-id="17fe4-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-159"><strong>дбсорттуркиш</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-160">Турецкий</span><span class="sxs-lookup"><span data-stu-id="17fe4-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-161"><strong>дбсортундефинед</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="17fe4-162">Неопределенное или неизвестное</span><span class="sxs-lookup"><span data-stu-id="17fe4-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17fe4-163">Доступность свойства **коллатингордер** зависит от объекта, содержащего коллекцию **Fields** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="17fe4-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="17fe4-164">Если коллекция Fields принадлежит к элементу</span><span class="sxs-lookup"><span data-stu-id="17fe4-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="17fe4-165">Затем Коллатингордер</span><span class="sxs-lookup"><span data-stu-id="17fe4-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-166">Объект <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="17fe4-167">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="17fe4-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-168">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="17fe4-169">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="17fe4-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-170">Объект <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="17fe4-171">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="17fe4-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="17fe4-172">Объект <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="17fe4-173">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="17fe4-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="17fe4-174">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="17fe4-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="17fe4-175">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="17fe4-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="17fe4-176">Значение свойства **коллатингордер** соответствует аргументу языкового стандарта метода **CreateDatabase** при создании базы данных или методе **CompactDatabase** при последнем сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="17fe4-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="17fe4-177">Параметры свойств **коллатингордер** и **Attributes** объекта **field2** в коллекции **Fields** объекта **index** вместе определяют последовательность и направление порядка сортировки в индексе.</span><span class="sxs-lookup"><span data-stu-id="17fe4-177">The **CollatingOrder** and **Attributes** property settings of a **Field2** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index.</span></span> <span data-ttu-id="17fe4-178">Однако вы не можете задать порядок сортировки для отдельного индекса — его можно задать только для всей таблицы.</span><span class="sxs-lookup"><span data-stu-id="17fe4-178">However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

