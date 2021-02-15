---
title: Свойство Database.CollatingOrder (DAO)
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
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="55fb9-102">Свойство Database.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="55fb9-102">Database.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="55fb9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55fb9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55fb9-104">Возвращает значение, которое указывает последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55fb9-104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="55fb9-105">Только для чтения, **Long**.</span><span class="sxs-lookup"><span data-stu-id="55fb9-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="55fb9-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="55fb9-106">Syntax</span></span>

<span data-ttu-id="55fb9-107">*выражение .* CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="55fb9-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="55fb9-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="55fb9-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="55fb9-109">Заметки</span><span class="sxs-lookup"><span data-stu-id="55fb9-109">Remarks</span></span>

<span data-ttu-id="55fb9-110">Возвращаемая величина — это **длинное** значение или константа, которые могут быть одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="55fb9-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55fb9-111">Константа</span><span class="sxs-lookup"><span data-stu-id="55fb9-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="55fb9-112">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="55fb9-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-114">Общие (английский, французский, немецкий, португальский, итальянский и современный испанский)</span><span class="sxs-lookup"><span data-stu-id="55fb9-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-116">Арабский</span><span class="sxs-lookup"><span data-stu-id="55fb9-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-118">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="55fb9-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-120">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="55fb9-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-122">Русский</span><span class="sxs-lookup"><span data-stu-id="55fb9-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-124">Чешский</span><span class="sxs-lookup"><span data-stu-id="55fb9-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-126">Голландский</span><span class="sxs-lookup"><span data-stu-id="55fb9-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-128">Греческий</span><span class="sxs-lookup"><span data-stu-id="55fb9-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-130">Иврит</span><span class="sxs-lookup"><span data-stu-id="55fb9-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-131"><strong>dbSortHung де</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-132">Венгерский</span><span class="sxs-lookup"><span data-stu-id="55fb9-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-134">Исландский</span><span class="sxs-lookup"><span data-stu-id="55fb9-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-136">Японский</span><span class="sxs-lookup"><span data-stu-id="55fb9-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-138">Корейский</span><span class="sxs-lookup"><span data-stu-id="55fb9-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-140">Нейтральный</span><span class="sxs-lookup"><span data-stu-id="55fb9-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-141"><strong>dbSortNorw Демили</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-142">Норвежский или датский</span><span class="sxs-lookup"><span data-stu-id="55fb9-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-144">Paradox International</span><span class="sxs-lookup"><span data-stu-id="55fb9-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-146">Норвежский или датский (норвежский)</span><span class="sxs-lookup"><span data-stu-id="55fb9-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-148">Paradox Шведский или финский</span><span class="sxs-lookup"><span data-stu-id="55fb9-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-149"><strong>dbSort Дефис</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-150">Польский</span><span class="sxs-lookup"><span data-stu-id="55fb9-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-152">Словенский</span><span class="sxs-lookup"><span data-stu-id="55fb9-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-154">Испанский</span><span class="sxs-lookup"><span data-stu-id="55fb9-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-156">Шведский или финский</span><span class="sxs-lookup"><span data-stu-id="55fb9-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-158">Тайский</span><span class="sxs-lookup"><span data-stu-id="55fb9-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55fb9-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-160">Турецкий</span><span class="sxs-lookup"><span data-stu-id="55fb9-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55fb9-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="55fb9-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="55fb9-162">Неопределенный или неизвестный</span><span class="sxs-lookup"><span data-stu-id="55fb9-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="55fb9-163">Параметр **свойства CollatingOrder** соответствует аргументу locale метода **CreateDatabase** при создании базы данных или **методу CompactDatabase** при последней сжатии базы данных.</span><span class="sxs-lookup"><span data-stu-id="55fb9-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="55fb9-164">Проверьте параметр **свойства CollatingOrder** объекта **Database** или **Field,** чтобы определить метод сравнения строк для базы данных или поля.</span><span class="sxs-lookup"><span data-stu-id="55fb9-164">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field.</span></span> <span data-ttu-id="55fb9-165">Вы можете настроить свойство **CollatingOrder** нового ненастроенного объекта **Field,** если хотите, чтобы параметр объекта **Field** отличался от параметра объекта **Database,** содержающего его.</span><span class="sxs-lookup"><span data-stu-id="55fb9-165">You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

