---
title: Свойство Database. Коллатингордер (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 21d775c0abac5d2afddd6b0930816c8d6d381ff0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295018"
---
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="ff9ed-102">Свойство Database. Коллатингордер (DAO)</span><span class="sxs-lookup"><span data-stu-id="ff9ed-102">Database.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="ff9ed-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ff9ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ff9ed-104">Возвращает значение, задающее последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="ff9ed-104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="ff9ed-105">Только для чтения, **Long**.</span><span class="sxs-lookup"><span data-stu-id="ff9ed-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff9ed-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ff9ed-106">Syntax</span></span>

<span data-ttu-id="ff9ed-107">*Expression* . Коллатингордер</span><span class="sxs-lookup"><span data-stu-id="ff9ed-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="ff9ed-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="ff9ed-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="ff9ed-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="ff9ed-109">Remarks</span></span>

<span data-ttu-id="ff9ed-110">Возвращаемое значение — это **длинное** значение или константа, которая может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="ff9ed-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ff9ed-111">Константа</span><span class="sxs-lookup"><span data-stu-id="ff9ed-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="ff9ed-112">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="ff9ed-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-113"><strong>Дбсортженерал</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-114">Общие (английский, французский, немецкий, португальский, итальянский и современная Испанская)</span><span class="sxs-lookup"><span data-stu-id="ff9ed-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-115"><strong>Дбсортарабик</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-116">арабский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-117"><strong>Дбсортчинесесимплифиед</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-118">китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="ff9ed-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-119"><strong>Дбсортчинесетрадитионал</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-120">китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="ff9ed-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-121"><strong>Дбсортцириллик</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-122">русский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-123"><strong>Дбсорткзеч</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-124">чешский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-125"><strong>Дбсортдутч</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-126">голландский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-127"><strong>Дбсортгрик</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-128">греческий;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-129"><strong>Дбсорсебрев</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-130">иврит;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-131"><strong>Дбсорсунгариан</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-132">венгерский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-133"><strong>Дбсортицеландик</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-134">Исландский</span><span class="sxs-lookup"><span data-stu-id="ff9ed-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-135"><strong>Дбсортжапанесе</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-136">японский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-137"><strong>Дбсорткореан</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-138">корейский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-139"><strong>Дбсортнеутрал</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-140">Нейтральный</span><span class="sxs-lookup"><span data-stu-id="ff9ed-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-141"><strong>Дбсортнорвдан</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-142">Норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="ff9ed-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-143"><strong>Дбсортпдксинтл</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-144">Международная связь Paradox</span><span class="sxs-lookup"><span data-stu-id="ff9ed-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-145"><strong>Дбсортпдкснор</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-146">Paradox норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="ff9ed-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-147"><strong>Дбсортпдкссве</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-148">Paradox шведский или Финский</span><span class="sxs-lookup"><span data-stu-id="ff9ed-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-149"><strong>Дбсортполиш</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-150">польский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-151"><strong>Дбсортсловениан</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-152">словенский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-153"><strong>Дбсортспаниш</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-154">испанский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-155"><strong>Дбсортсведфин</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-156">Шведский или Финский</span><span class="sxs-lookup"><span data-stu-id="ff9ed-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-157"><strong>Дбсортсаи</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-158">тайский;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ff9ed-159"><strong>Дбсорттуркиш</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-160">турецкий;</span><span class="sxs-lookup"><span data-stu-id="ff9ed-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ff9ed-161"><strong>Дбсортундефинед</strong></span><span class="sxs-lookup"><span data-stu-id="ff9ed-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="ff9ed-162">Неопределенное или неизвестное</span><span class="sxs-lookup"><span data-stu-id="ff9ed-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ff9ed-163">Значение свойства **коллатингордер** соответствует аргументу языкового стандарта метода **CreateDatabase** при создании базы данных или методе **CompactDatabase** при последнем сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="ff9ed-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="ff9ed-164">Проверьте значение свойства **коллатингордер** объекта **базы данных** или **поля** , чтобы определить метод сравнения строк для базы данных или поля.</span><span class="sxs-lookup"><span data-stu-id="ff9ed-164">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field.</span></span> <span data-ttu-id="ff9ed-165">Вы можете задать свойство **коллатингордер** нового, неприсоединенного объекта **field** , если необходимо, чтобы параметр объекта **field** отличался от того объекта **базы данных** , который содержит его.</span><span class="sxs-lookup"><span data-stu-id="ff9ed-165">You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

