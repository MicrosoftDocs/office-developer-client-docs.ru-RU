---
title: Свойство Field2.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: cb1d6fc9-a2a6-54c2-abf5-48b609e38738
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834380(v=office.15)
ms:contentKeyID: 48547709
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 02711fbbf39b058bb88e9568716169825ae4a923
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700733"
---
# <a name="field2collatingorder-property-dao"></a><span data-ttu-id="a9352-102">Свойство Field2.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="a9352-102">Field2.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="a9352-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a9352-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a9352-104">Возвращает значение, указывающее последовательность порядок сортировки в текст для сравнения строк или сортировка (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="a9352-104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="a9352-105">Только для чтения **времени**.</span><span class="sxs-lookup"><span data-stu-id="a9352-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9352-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a9352-106">Syntax</span></span>

<span data-ttu-id="a9352-107">*выражение* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="a9352-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="a9352-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="a9352-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9352-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="a9352-109">Remarks</span></span>

<span data-ttu-id="a9352-110">Возвращаемое значение — **длинное целое** значение или константа, которая может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a9352-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9352-111">Константа</span><span class="sxs-lookup"><span data-stu-id="a9352-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="a9352-112">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="a9352-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9352-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-114">Общие (английский, французский, немецкий, португальский, итальянский и современных на испанском языке)</span><span class="sxs-lookup"><span data-stu-id="a9352-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-116">арабский;</span><span class="sxs-lookup"><span data-stu-id="a9352-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-118">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="a9352-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-120">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="a9352-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-122">русский;</span><span class="sxs-lookup"><span data-stu-id="a9352-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-124">чешский;</span><span class="sxs-lookup"><span data-stu-id="a9352-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-126">голландский;</span><span class="sxs-lookup"><span data-stu-id="a9352-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-128">греческий;</span><span class="sxs-lookup"><span data-stu-id="a9352-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-130">иврит;</span><span class="sxs-lookup"><span data-stu-id="a9352-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-132">венгерский;</span><span class="sxs-lookup"><span data-stu-id="a9352-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-134">Исландский</span><span class="sxs-lookup"><span data-stu-id="a9352-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-136">японский;</span><span class="sxs-lookup"><span data-stu-id="a9352-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-138">корейский;</span><span class="sxs-lookup"><span data-stu-id="a9352-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-140">Нейтральный</span><span class="sxs-lookup"><span data-stu-id="a9352-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-142">Датский и норвежский</span><span class="sxs-lookup"><span data-stu-id="a9352-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-144">Международный Paradox</span><span class="sxs-lookup"><span data-stu-id="a9352-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-146">Датский и норвежский Paradox</span><span class="sxs-lookup"><span data-stu-id="a9352-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-148">Финский и шведский Paradox</span><span class="sxs-lookup"><span data-stu-id="a9352-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-150">польский;</span><span class="sxs-lookup"><span data-stu-id="a9352-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-152">словенский;</span><span class="sxs-lookup"><span data-stu-id="a9352-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-154">испанский;</span><span class="sxs-lookup"><span data-stu-id="a9352-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-156">Финский и шведский</span><span class="sxs-lookup"><span data-stu-id="a9352-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-158">тайский;</span><span class="sxs-lookup"><span data-stu-id="a9352-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-160">турецкий;</span><span class="sxs-lookup"><span data-stu-id="a9352-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="a9352-162">Неопределенный или неизвестный</span><span class="sxs-lookup"><span data-stu-id="a9352-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9352-163">Доступность свойство **CollatingOrder** зависит от объекта, который содержит коллекцию **полей** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="a9352-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a9352-164">Если принадлежит коллекции полей</span><span class="sxs-lookup"><span data-stu-id="a9352-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="a9352-165">Затем — CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="a9352-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a9352-166">Объект <strong>индекса</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a9352-167">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a9352-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-168">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a9352-169">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9352-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-170">Объект <strong>набора записей</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a9352-171">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9352-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a9352-172"><strong>Отношения</strong> объектов</span><span class="sxs-lookup"><span data-stu-id="a9352-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a9352-173">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="a9352-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a9352-174">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="a9352-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="a9352-175">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="a9352-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a9352-176">Настройка свойства **CollatingOrder** соответствует языкового стандарта аргумента метода **CreateDatabase** при создании базы данных или метода **CompactDatabase** при последним сжатие базы данных.</span><span class="sxs-lookup"><span data-stu-id="a9352-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="a9352-177">Параметры свойства **CollatingOrder** и **атрибуты** объекта **поле2** в коллекции **полей** **индекс** объекта вместе определяют последовательность и направление сортировки в индекс.</span><span class="sxs-lookup"><span data-stu-id="a9352-177">The **CollatingOrder** and **Attributes** property settings of a **Field2** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index.</span></span> <span data-ttu-id="a9352-178">Тем не менее, невозможно задать порядок сортировки для конкретного индекса, его можно задать только для всей таблицы.</span><span class="sxs-lookup"><span data-stu-id="a9352-178">However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

