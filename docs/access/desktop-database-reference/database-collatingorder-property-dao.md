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
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="1e93a-102">Свойство Database. Коллатингордер (DAO)</span><span class="sxs-lookup"><span data-stu-id="1e93a-102">Database.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="1e93a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e93a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e93a-104">Возвращает значение, задающее последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="1e93a-104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="1e93a-105">Только для чтения, **Long**.</span><span class="sxs-lookup"><span data-stu-id="1e93a-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e93a-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1e93a-106">Syntax</span></span>

<span data-ttu-id="1e93a-107">*Expression* . коллатингордер</span><span class="sxs-lookup"><span data-stu-id="1e93a-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="1e93a-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="1e93a-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e93a-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e93a-109">Remarks</span></span>

<span data-ttu-id="1e93a-110">Возвращаемое значение — это **длинное** значение или константа, которая может принимать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="1e93a-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e93a-111">Константа</span><span class="sxs-lookup"><span data-stu-id="1e93a-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="1e93a-112">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="1e93a-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-113"><strong>дбсортженерал</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-114">Общие (английский, французский, немецкий, португальский, итальянский и современная Испанская)</span><span class="sxs-lookup"><span data-stu-id="1e93a-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-115"><strong>дбсортарабик</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-116">Арабский</span><span class="sxs-lookup"><span data-stu-id="1e93a-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-117"><strong>дбсортчинесесимплифиед</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-118">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="1e93a-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-119"><strong>дбсортчинесетрадитионал</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-120">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="1e93a-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-121"><strong>дбсортцириллик</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-122">Русский</span><span class="sxs-lookup"><span data-stu-id="1e93a-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-123"><strong>дбсорткзеч</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-124">Чешский</span><span class="sxs-lookup"><span data-stu-id="1e93a-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-125"><strong>дбсортдутч</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-126">Голландский</span><span class="sxs-lookup"><span data-stu-id="1e93a-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-127"><strong>дбсортгрик</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-128">Греческий</span><span class="sxs-lookup"><span data-stu-id="1e93a-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-129"><strong>дбсорсебрев</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-130">Иврит</span><span class="sxs-lookup"><span data-stu-id="1e93a-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-131"><strong>дбсорсунгариан</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-132">Венгерский</span><span class="sxs-lookup"><span data-stu-id="1e93a-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-133"><strong>дбсортицеландик</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-134">Исландский</span><span class="sxs-lookup"><span data-stu-id="1e93a-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-135"><strong>дбсортжапанесе</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-136">Японский</span><span class="sxs-lookup"><span data-stu-id="1e93a-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-137"><strong>дбсорткореан</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-138">Корейский</span><span class="sxs-lookup"><span data-stu-id="1e93a-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-139"><strong>дбсортнеутрал</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-140">Нейтральный</span><span class="sxs-lookup"><span data-stu-id="1e93a-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-141"><strong>дбсортнорвдан</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-142">Норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="1e93a-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-143"><strong>дбсортпдксинтл</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-144">Международная связь Paradox</span><span class="sxs-lookup"><span data-stu-id="1e93a-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-145"><strong>дбсортпдкснор</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-146">Paradox норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="1e93a-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-147"><strong>дбсортпдкссве</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-148">Paradox шведский или Финский</span><span class="sxs-lookup"><span data-stu-id="1e93a-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-149"><strong>дбсортполиш</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-150">Польский</span><span class="sxs-lookup"><span data-stu-id="1e93a-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-151"><strong>дбсортсловениан</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-152">Словенский</span><span class="sxs-lookup"><span data-stu-id="1e93a-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-153"><strong>дбсортспаниш</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-154">Испанский</span><span class="sxs-lookup"><span data-stu-id="1e93a-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-155"><strong>дбсортсведфин</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-156">Шведский или Финский</span><span class="sxs-lookup"><span data-stu-id="1e93a-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-157"><strong>дбсортсаи</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-158">Тайский</span><span class="sxs-lookup"><span data-stu-id="1e93a-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e93a-159"><strong>дбсорттуркиш</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-160">Турецкий</span><span class="sxs-lookup"><span data-stu-id="1e93a-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e93a-161"><strong>дбсортундефинед</strong></span><span class="sxs-lookup"><span data-stu-id="1e93a-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="1e93a-162">Неопределенное или неизвестное</span><span class="sxs-lookup"><span data-stu-id="1e93a-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1e93a-163">Значение свойства **коллатингордер** соответствует аргументу языкового стандарта метода **CreateDatabase** при создании базы данных или методе **CompactDatabase** при последнем сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="1e93a-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="1e93a-164">Проверьте значение свойства **коллатингордер** объекта **базы данных** или **поля** , чтобы определить метод сравнения строк для базы данных или поля.</span><span class="sxs-lookup"><span data-stu-id="1e93a-164">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field.</span></span> <span data-ttu-id="1e93a-165">Вы можете задать свойство **коллатингордер** нового, неприсоединенного объекта **field** , если необходимо, чтобы параметр объекта **field** отличался от того объекта **базы данных** , который содержит его.</span><span class="sxs-lookup"><span data-stu-id="1e93a-165">You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

