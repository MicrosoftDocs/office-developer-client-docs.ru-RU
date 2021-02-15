---
title: Свойство Field.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: a2607ace-a660-899b-eae8-4612ce2f87f8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820980(v=office.15)
ms:contentKeyID: 48546758
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052897
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3d016d779472ec9809d3ac5c77158c2c1d994f3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293128"
---
# <a name="fieldcollatingorder-property-dao"></a><span data-ttu-id="b619d-102">Свойство Field.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="b619d-102">Field.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="b619d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b619d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b619d-104">Возвращает значение, которое указывает последовательность порядка сортировки в тексте для сравнения или сортировки строк (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b619d-104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="b619d-105">Только для чтения, **Long**.</span><span class="sxs-lookup"><span data-stu-id="b619d-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b619d-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b619d-106">Syntax</span></span>

<span data-ttu-id="b619d-107">*выражение .* CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="b619d-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="b619d-108">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="b619d-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="b619d-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="b619d-109">Remarks</span></span>

<span data-ttu-id="b619d-110">Возвращаемая величина — это **длинное** значение или константа, которые могут быть одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="b619d-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b619d-111">Константа</span><span class="sxs-lookup"><span data-stu-id="b619d-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="b619d-112">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="b619d-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b619d-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-114">Общие (английский, французский, немецкий, португальский, итальянский и современный испанский)</span><span class="sxs-lookup"><span data-stu-id="b619d-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-116">Арабский</span><span class="sxs-lookup"><span data-stu-id="b619d-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-118">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="b619d-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-120">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="b619d-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-122">Русский</span><span class="sxs-lookup"><span data-stu-id="b619d-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-124">Чешский</span><span class="sxs-lookup"><span data-stu-id="b619d-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-126">Голландский</span><span class="sxs-lookup"><span data-stu-id="b619d-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-128">Греческий</span><span class="sxs-lookup"><span data-stu-id="b619d-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-130">Иврит</span><span class="sxs-lookup"><span data-stu-id="b619d-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-131"><strong>dbSortHungung</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-132">Венгерский</span><span class="sxs-lookup"><span data-stu-id="b619d-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-134">Исландский</span><span class="sxs-lookup"><span data-stu-id="b619d-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-136">Японский</span><span class="sxs-lookup"><span data-stu-id="b619d-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-138">Корейский</span><span class="sxs-lookup"><span data-stu-id="b619d-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-140">Нейтральный</span><span class="sxs-lookup"><span data-stu-id="b619d-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-141"><strong>dbSortNorw Демили</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-142">Норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="b619d-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="b619d-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-146">Норвежский или датский ( paradox)</span><span class="sxs-lookup"><span data-stu-id="b619d-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-148">Paradox Шведский или финский</span><span class="sxs-lookup"><span data-stu-id="b619d-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-149"><strong>dbSort Дефис</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-150">Польский</span><span class="sxs-lookup"><span data-stu-id="b619d-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-152">Словенский</span><span class="sxs-lookup"><span data-stu-id="b619d-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-154">Испанский</span><span class="sxs-lookup"><span data-stu-id="b619d-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-156">Шведский или финский</span><span class="sxs-lookup"><span data-stu-id="b619d-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-158">Тайский</span><span class="sxs-lookup"><span data-stu-id="b619d-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-160">Турецкий</span><span class="sxs-lookup"><span data-stu-id="b619d-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="b619d-162">Неопределенный или неизвестный</span><span class="sxs-lookup"><span data-stu-id="b619d-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b619d-163">Доступность свойства **CollatingOrder** зависит от объекта, содержающего коллекцию **Fields,** как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="b619d-163">The availability of the **CollatingOrder** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b619d-164">Если коллекция Fields принадлежит к</span><span class="sxs-lookup"><span data-stu-id="b619d-164">If the Fields collection belongs to an</span></span></p></th>
<th><p><span data-ttu-id="b619d-165">Затем CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="b619d-165">Then CollatingOrder is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b619d-166">Объект <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-166"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b619d-167">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b619d-167">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-168">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-168"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b619d-169">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b619d-169">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-170">Объект <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-170"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b619d-171">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b619d-171">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b619d-172">Объект <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-172"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b619d-173">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="b619d-173">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b619d-174">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="b619d-174"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="b619d-175">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="b619d-175">Read-only</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b619d-176">Параметр **свойства CollatingOrder** соответствует аргументу locale метода **CreateDatabase** при создании базы данных или **методу CompactDatabase** при последней сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="b619d-176">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="b619d-177">Параметры **свойства CollatingOrder** и **Attributes** объекта **Field** в коллекции **Fields** объекта **Index** вместе определяют последовательность и направление порядка сортировки в индексе.</span><span class="sxs-lookup"><span data-stu-id="b619d-177">The **CollatingOrder** and **Attributes** property settings of a **Field** object in a **Fields** collection of an **Index** object together determine the sequence and direction of the sort order in an index.</span></span> <span data-ttu-id="b619d-178">Однако вы не можете настроить порядок совмества для отдельного индекса— вы можете настроить его только для всей таблицы.</span><span class="sxs-lookup"><span data-stu-id="b619d-178">However, you can't set a collating order for an individual index— you can only set it for an entire table.</span></span>

