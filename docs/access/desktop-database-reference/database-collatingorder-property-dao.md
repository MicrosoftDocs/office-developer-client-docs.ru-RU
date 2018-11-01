---
title: Database.CollatingOrder Property (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1eddad35508fb3182b50ecdca2f0fb413569aa12
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25889534"
---
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="16071-102">Database.CollatingOrder Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="16071-102">Database.CollatingOrder Property (DAO)</span></span>


<span data-ttu-id="16071-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="16071-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="16071-104">Возвращает значение, указывающее последовательность порядок сортировки в текст для сравнения строк или сортировка (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="16071-104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="16071-105">Только для чтения **времени**.</span><span class="sxs-lookup"><span data-stu-id="16071-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="16071-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="16071-106">Syntax</span></span>

<span data-ttu-id="16071-107">*выражение* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="16071-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="16071-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="16071-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="16071-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="16071-109">Remarks</span></span>

<span data-ttu-id="16071-110">Возвращаемое значение — **длинное целое** значение или константа, которая может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="16071-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="16071-111">Constant</span><span class="sxs-lookup"><span data-stu-id="16071-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="16071-112">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="16071-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="16071-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="16071-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-114">Общие (английский, французский, немецкий, португальский, итальянский и современных на испанском языке)</span><span class="sxs-lookup"><span data-stu-id="16071-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="16071-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-116">арабский;</span><span class="sxs-lookup"><span data-stu-id="16071-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="16071-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-118">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="16071-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="16071-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-120">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="16071-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="16071-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-122">русский;</span><span class="sxs-lookup"><span data-stu-id="16071-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="16071-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-124">чешский;</span><span class="sxs-lookup"><span data-stu-id="16071-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="16071-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-126">голландский;</span><span class="sxs-lookup"><span data-stu-id="16071-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="16071-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-128">греческий;</span><span class="sxs-lookup"><span data-stu-id="16071-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="16071-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-130">иврит;</span><span class="sxs-lookup"><span data-stu-id="16071-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="16071-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-132">венгерский;</span><span class="sxs-lookup"><span data-stu-id="16071-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="16071-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-134">Исландский</span><span class="sxs-lookup"><span data-stu-id="16071-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="16071-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-136">японский;</span><span class="sxs-lookup"><span data-stu-id="16071-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="16071-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-138">корейский;</span><span class="sxs-lookup"><span data-stu-id="16071-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="16071-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-140">Neutral</span><span class="sxs-lookup"><span data-stu-id="16071-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="16071-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-142">Датский и норвежский</span><span class="sxs-lookup"><span data-stu-id="16071-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="16071-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-144">Международный Paradox</span><span class="sxs-lookup"><span data-stu-id="16071-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="16071-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-146">Датский и норвежский Paradox</span><span class="sxs-lookup"><span data-stu-id="16071-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="16071-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-148">Финский и шведский Paradox</span><span class="sxs-lookup"><span data-stu-id="16071-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="16071-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-150">польский;</span><span class="sxs-lookup"><span data-stu-id="16071-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="16071-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-152">словенский;</span><span class="sxs-lookup"><span data-stu-id="16071-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="16071-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-154">испанский;</span><span class="sxs-lookup"><span data-stu-id="16071-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="16071-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-156">Финский и шведский</span><span class="sxs-lookup"><span data-stu-id="16071-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="16071-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-158">тайский;</span><span class="sxs-lookup"><span data-stu-id="16071-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="16071-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="16071-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-160">турецкий;</span><span class="sxs-lookup"><span data-stu-id="16071-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="16071-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="16071-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="16071-162">Неопределенный или неизвестный</span><span class="sxs-lookup"><span data-stu-id="16071-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="16071-163">Настройка свойства **CollatingOrder** соответствует языкового стандарта аргумента метода **CreateDatabase** при создании базы данных или метода **CompactDatabase** при последним сжатие базы данных.</span><span class="sxs-lookup"><span data-stu-id="16071-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="16071-164">Проверьте значение свойства **CollatingOrder** объекта **базы данных** или **полей** для определения метода сравнения строк для поля или базы данных.</span><span class="sxs-lookup"><span data-stu-id="16071-164">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field.</span></span> <span data-ttu-id="16071-165">Можно задать свойство **CollatingOrder** новый, unappended объекта **поля** , если требуется параметра объекта **поля** отличаются в зависимости от типа объекта **базы данных** , содержащей его.</span><span class="sxs-lookup"><span data-stu-id="16071-165">You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

