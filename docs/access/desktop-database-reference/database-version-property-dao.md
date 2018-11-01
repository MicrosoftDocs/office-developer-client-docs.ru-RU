---
title: Database.Version Property (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8ce28decf2d20c608067a2fa3791d8dce0ce61f8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25876269"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="933e3-102">Database.Version Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="933e3-102">Database.Version Property (DAO)</span></span>


<span data-ttu-id="933e3-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="933e3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="933e3-104">В рабочей области Microsoft Access возвращает vesion ядро базы данных Microsoft Access или Microsoft Jet созданной базе данных.</span><span class="sxs-lookup"><span data-stu-id="933e3-104">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database.</span></span> <span data-ttu-id="933e3-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="933e3-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="933e3-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="933e3-106">Syntax</span></span>

<span data-ttu-id="933e3-107">*выражение* . Версия</span><span class="sxs-lookup"><span data-stu-id="933e3-107">*expression* .Version</span></span>

<span data-ttu-id="933e3-108">*выражение* Переменная, которая представляет собой объект **базы данных** .</span><span class="sxs-lookup"><span data-stu-id="933e3-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="933e3-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="933e3-109">Remarks</span></span>

<span data-ttu-id="933e3-110">Возвращаемое значение — это строка, которое оценивается как номер версии, следующий формат.</span><span class="sxs-lookup"><span data-stu-id="933e3-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

  - <span data-ttu-id="933e3-111">Рабочая область для Microsoft Access представляет номер версии в форме «*major.minor*».</span><span class="sxs-lookup"><span data-stu-id="933e3-111">Microsoft Access workspace represents the version number in the form "*major.minor*".</span></span> <span data-ttu-id="933e3-112">Например «3.0».</span><span class="sxs-lookup"><span data-stu-id="933e3-112">For example, "3.0".</span></span> <span data-ttu-id="933e3-113">Номер версии продукта состоит из номера версии (3), за период и номер версии (0).</span><span class="sxs-lookup"><span data-stu-id="933e3-113">The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="933e3-114">В следующей таблице показаны версии ядра базы данных была включена в различных версиях продуктов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="933e3-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="933e3-115">Компонент Database Engine</span><span class="sxs-lookup"><span data-stu-id="933e3-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="933e3-116">Версия (год выпуска)</span><span class="sxs-lookup"><span data-stu-id="933e3-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="933e3-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="933e3-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="933e3-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="933e3-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="933e3-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="933e3-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="933e3-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="933e3-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="933e3-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933e3-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933e3-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="933e3-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="933e3-123">1.0</span><span class="sxs-lookup"><span data-stu-id="933e3-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="933e3-124">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="933e3-125">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="933e3-126">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="933e3-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933e3-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933e3-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="933e3-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="933e3-129">1.1</span><span class="sxs-lookup"><span data-stu-id="933e3-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="933e3-130">3.0</span><span class="sxs-lookup"><span data-stu-id="933e3-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="933e3-131">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="933e3-132">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="933e3-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933e3-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933e3-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="933e3-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="933e3-135">2.0</span><span class="sxs-lookup"><span data-stu-id="933e3-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="933e3-136">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="933e3-137">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="933e3-138">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="933e3-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933e3-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933e3-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="933e3-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="933e3-141">Н/Д</span><span class="sxs-lookup"><span data-stu-id="933e3-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="933e3-142">4.0 (16-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="933e3-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="933e3-143">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="933e3-144">Нет</span><span class="sxs-lookup"><span data-stu-id="933e3-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="933e3-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933e3-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933e3-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="933e3-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="933e3-147">"95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="933e3-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="933e3-148">4.0 (32-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="933e3-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="933e3-149">"95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="933e3-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="933e3-150">4.x</span><span class="sxs-lookup"><span data-stu-id="933e3-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="933e3-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933e3-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933e3-152">3.5 (1996 г.)</span><span class="sxs-lookup"><span data-stu-id="933e3-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="933e3-153">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="933e3-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="933e3-154">5.0</span><span class="sxs-lookup"><span data-stu-id="933e3-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="933e3-155">' 97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="933e3-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="933e3-156">5.0</span><span class="sxs-lookup"><span data-stu-id="933e3-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="933e3-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="933e3-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="933e3-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="933e3-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="933e3-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="933e3-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="933e3-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="933e3-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="933e3-161">Ядро СУБД Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="933e3-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="933e3-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="933e3-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="933e3-163">2007</span><span class="sxs-lookup"><span data-stu-id="933e3-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

