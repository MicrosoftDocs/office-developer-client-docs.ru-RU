---
title: Свойство Database.CollatingOrder (DAO)
TOCTitle: CollatingOrder Property
ms:assetid: 7f6c35bf-e5f9-8423-608e-bc072ca09141
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196459(v=office.15)
ms:contentKeyID: 48545901
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8e3219d9691fa61fd1ae234cecd273ec9720ed9e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923870"
---
# <a name="databasecollatingorder-property-dao"></a><span data-ttu-id="7561c-102">Свойство Database.CollatingOrder (DAO)</span><span class="sxs-lookup"><span data-stu-id="7561c-102">Database.CollatingOrder property (DAO)</span></span>


<span data-ttu-id="7561c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7561c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7561c-104">Возвращает значение, указывающее последовательность порядок сортировки в текст для сравнения строк или сортировка (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7561c-104">Returns a value that specifies the sequence of the sort order in text for string comparison or sorting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="7561c-105">Только для чтения **времени**.</span><span class="sxs-lookup"><span data-stu-id="7561c-105">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="7561c-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7561c-106">Syntax</span></span>

<span data-ttu-id="7561c-107">*выражение* . CollatingOrder</span><span class="sxs-lookup"><span data-stu-id="7561c-107">*expression* .CollatingOrder</span></span>

<span data-ttu-id="7561c-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="7561c-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="7561c-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="7561c-109">Remarks</span></span>

<span data-ttu-id="7561c-110">Возвращаемое значение — **длинное целое** значение или константа, которая может иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="7561c-110">The return value is a **Long** value or constant that can be one of the following values.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7561c-111">Constant</span><span class="sxs-lookup"><span data-stu-id="7561c-111">Constant</span></span></p></th>
<th><p><span data-ttu-id="7561c-112">Порядок сортировки</span><span class="sxs-lookup"><span data-stu-id="7561c-112">Sort order</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7561c-113"><strong>dbSortGeneral</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-113"><strong>dbSortGeneral</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-114">Общие (английский, французский, немецкий, португальский, итальянский и современных на испанском языке)</span><span class="sxs-lookup"><span data-stu-id="7561c-114">General (English, French, German, Portuguese, Italian, and Modern Spanish)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-115"><strong>dbSortArabic</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-115"><strong>dbSortArabic</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-116">арабский;</span><span class="sxs-lookup"><span data-stu-id="7561c-116">Arabic</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-117"><strong>dbSortChineseSimplified</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-117"><strong>dbSortChineseSimplified</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-118">Китайский (упрощенное письмо)</span><span class="sxs-lookup"><span data-stu-id="7561c-118">Simplified Chinese</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-119"><strong>dbSortChineseTraditional</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-119"><strong>dbSortChineseTraditional</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-120">Китайский (традиционное письмо)</span><span class="sxs-lookup"><span data-stu-id="7561c-120">Traditional Chinese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-121"><strong>dbSortCyrillic</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-121"><strong>dbSortCyrillic</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-122">русский;</span><span class="sxs-lookup"><span data-stu-id="7561c-122">Russian</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-123"><strong>dbSortCzech</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-123"><strong>dbSortCzech</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-124">чешский;</span><span class="sxs-lookup"><span data-stu-id="7561c-124">Czech</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-125"><strong>dbSortDutch</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-125"><strong>dbSortDutch</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-126">голландский;</span><span class="sxs-lookup"><span data-stu-id="7561c-126">Dutch</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-127"><strong>dbSortGreek</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-127"><strong>dbSortGreek</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-128">греческий;</span><span class="sxs-lookup"><span data-stu-id="7561c-128">Greek</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-129"><strong>dbSortHebrew</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-129"><strong>dbSortHebrew</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-130">иврит;</span><span class="sxs-lookup"><span data-stu-id="7561c-130">Hebrew</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-131"><strong>dbSortHungarian</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-131"><strong>dbSortHungarian</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-132">венгерский;</span><span class="sxs-lookup"><span data-stu-id="7561c-132">Hungarian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-133"><strong>dbSortIcelandic</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-133"><strong>dbSortIcelandic</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-134">Исландский</span><span class="sxs-lookup"><span data-stu-id="7561c-134">Icelandic</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-135"><strong>dbSortJapanese</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-135"><strong>dbSortJapanese</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-136">японский;</span><span class="sxs-lookup"><span data-stu-id="7561c-136">Japanese</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-137"><strong>dbSortKorean</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-137"><strong>dbSortKorean</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-138">корейский;</span><span class="sxs-lookup"><span data-stu-id="7561c-138">Korean</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-139"><strong>dbSortNeutral</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-139"><strong>dbSortNeutral</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-140">Neutral</span><span class="sxs-lookup"><span data-stu-id="7561c-140">Neutral</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-141"><strong>dbSortNorwDan</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-141"><strong>dbSortNorwDan</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-142">Датский и норвежский</span><span class="sxs-lookup"><span data-stu-id="7561c-142">Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-143"><strong>dbSortPDXIntl</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-143"><strong>dbSortPDXIntl</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-144">Международный Paradox</span><span class="sxs-lookup"><span data-stu-id="7561c-144">Paradox International</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-145"><strong>dbSortPDXNor</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-145"><strong>dbSortPDXNor</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-146">Датский и норвежский Paradox</span><span class="sxs-lookup"><span data-stu-id="7561c-146">Paradox Norwegian or Danish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-147"><strong>dbSortPDXSwe</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-147"><strong>dbSortPDXSwe</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-148">Финский и шведский Paradox</span><span class="sxs-lookup"><span data-stu-id="7561c-148">Paradox Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-149"><strong>dbSortPolish</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-149"><strong>dbSortPolish</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-150">польский;</span><span class="sxs-lookup"><span data-stu-id="7561c-150">Polish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-151"><strong>dbSortSlovenian</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-151"><strong>dbSortSlovenian</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-152">словенский;</span><span class="sxs-lookup"><span data-stu-id="7561c-152">Slovenian</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-153"><strong>dbSortSpanish</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-153"><strong>dbSortSpanish</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-154">испанский;</span><span class="sxs-lookup"><span data-stu-id="7561c-154">Spanish</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-155"><strong>dbSortSwedFin</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-155"><strong>dbSortSwedFin</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-156">Финский и шведский</span><span class="sxs-lookup"><span data-stu-id="7561c-156">Swedish or Finnish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-157"><strong>dbSortThai</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-157"><strong>dbSortThai</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-158">тайский;</span><span class="sxs-lookup"><span data-stu-id="7561c-158">Thai</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7561c-159"><strong>dbSortTurkish</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-159"><strong>dbSortTurkish</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-160">турецкий;</span><span class="sxs-lookup"><span data-stu-id="7561c-160">Turkish</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7561c-161"><strong>dbSortUndefined</strong></span><span class="sxs-lookup"><span data-stu-id="7561c-161"><strong>dbSortUndefined</strong></span></span></p></td>
<td><p><span data-ttu-id="7561c-162">Неопределенный или неизвестный</span><span class="sxs-lookup"><span data-stu-id="7561c-162">Undefined or unknown</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7561c-163">Настройка свойства **CollatingOrder** соответствует языкового стандарта аргумента метода **CreateDatabase** при создании базы данных или метода **CompactDatabase** при последним сжатие базы данных.</span><span class="sxs-lookup"><span data-stu-id="7561c-163">The **CollatingOrder** property setting corresponds to the locale argument of the **CreateDatabase** method when the database was created or the **CompactDatabase** method when the database was most recently compacted.</span></span>

<span data-ttu-id="7561c-164">Проверьте значение свойства **CollatingOrder** объекта **базы данных** или **полей** для определения метода сравнения строк для поля или базы данных.</span><span class="sxs-lookup"><span data-stu-id="7561c-164">Check the **CollatingOrder** property setting of a **Database** or **Field** object to determine the string comparison method for the database or field.</span></span> <span data-ttu-id="7561c-165">Можно задать свойство **CollatingOrder** новый, unappended объекта **поля** , если требуется параметра объекта **поля** отличаются в зависимости от типа объекта **базы данных** , содержащей его.</span><span class="sxs-lookup"><span data-stu-id="7561c-165">You can set the **CollatingOrder** property of a new, unappended **Field** object if you want the setting of the **Field** object to differ from that of the **Database** object that contains it.</span></span>

