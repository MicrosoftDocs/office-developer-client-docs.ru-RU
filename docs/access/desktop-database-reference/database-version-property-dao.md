---
title: Свойство Database. Version (DAO)
TOCTitle: Version Property
ms:assetid: 40faaa0c-e764-e968-f606-7e06ded80c3f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192887(v=office.15)
ms:contentKeyID: 48544440
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41b408f63522902fd1d4f806090eef7563a3492a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294654"
---
# <a name="databaseversion-property-dao"></a><span data-ttu-id="42635-102">Свойство Database. Version (DAO)</span><span class="sxs-lookup"><span data-stu-id="42635-102">Database.Version property (DAO)</span></span>

<span data-ttu-id="42635-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42635-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42635-104">В рабочей области Microsoft Access возвращает весион базы данных Microsoft Jet или ядра СУБД Microsoft Access, который создал базу данных.</span><span class="sxs-lookup"><span data-stu-id="42635-104">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database.</span></span> <span data-ttu-id="42635-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="42635-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="42635-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42635-106">Syntax</span></span>

<span data-ttu-id="42635-107">*Expression* . Версия</span><span class="sxs-lookup"><span data-stu-id="42635-107">*expression* .Version</span></span>

<span data-ttu-id="42635-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="42635-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="42635-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="42635-109">Remarks</span></span>

<span data-ttu-id="42635-110">Возвращаемое значение — это строка, в которой вычисляется номер версии, отформатированный следующим образом.</span><span class="sxs-lookup"><span data-stu-id="42635-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

- <span data-ttu-id="42635-111">Рабочая область Microsoft Access представляет номер версии в виде "*Major. Minor*".</span><span class="sxs-lookup"><span data-stu-id="42635-111">Microsoft Access workspace represents the version number in the form "*major.minor*".</span></span> <span data-ttu-id="42635-112">Например, "3,0".</span><span class="sxs-lookup"><span data-stu-id="42635-112">For example, "3.0".</span></span> <span data-ttu-id="42635-113">Номер версии продукта состоит из номера версии (3), точки и номера выпуска (0).</span><span class="sxs-lookup"><span data-stu-id="42635-113">The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="42635-114">В приведенной ниже таблице показано, какая версия ядра СУБД была включена в состав различных версий продуктов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="42635-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

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
<th><p><span data-ttu-id="42635-115">Ядро СУБД</span><span class="sxs-lookup"><span data-stu-id="42635-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="42635-116">Версия (год выпуска)</span><span class="sxs-lookup"><span data-stu-id="42635-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="42635-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="42635-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="42635-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="42635-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="42635-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="42635-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="42635-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="42635-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42635-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="42635-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="42635-122">1,0 (1992)</span><span class="sxs-lookup"><span data-stu-id="42635-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="42635-123">1.0</span><span class="sxs-lookup"><span data-stu-id="42635-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="42635-124">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="42635-125">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="42635-126">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42635-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="42635-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="42635-128">1,1 (1993)</span><span class="sxs-lookup"><span data-stu-id="42635-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="42635-129">1.1</span><span class="sxs-lookup"><span data-stu-id="42635-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="42635-130">3,0</span><span class="sxs-lookup"><span data-stu-id="42635-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="42635-131">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="42635-132">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42635-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="42635-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="42635-134">2,0 (1994)</span><span class="sxs-lookup"><span data-stu-id="42635-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="42635-135">2.0</span><span class="sxs-lookup"><span data-stu-id="42635-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="42635-136">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="42635-137">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="42635-138">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42635-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="42635-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="42635-140">2,5 (1995)</span><span class="sxs-lookup"><span data-stu-id="42635-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="42635-141">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="42635-142">4,0 (16-разрядная версия)</span><span class="sxs-lookup"><span data-stu-id="42635-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="42635-143">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="42635-144">Недоступно</span><span class="sxs-lookup"><span data-stu-id="42635-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42635-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="42635-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="42635-146">3,0 (1995)</span><span class="sxs-lookup"><span data-stu-id="42635-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="42635-147">' 95 (7,0)</span><span class="sxs-lookup"><span data-stu-id="42635-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="42635-148">4,0 (32-бит)</span><span class="sxs-lookup"><span data-stu-id="42635-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="42635-149">' 95 (7,0)</span><span class="sxs-lookup"><span data-stu-id="42635-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="42635-150">х</span><span class="sxs-lookup"><span data-stu-id="42635-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42635-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="42635-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="42635-152">3,5 (1996)</span><span class="sxs-lookup"><span data-stu-id="42635-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="42635-153">' 97 (8,0)</span><span class="sxs-lookup"><span data-stu-id="42635-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="42635-154">5,0</span><span class="sxs-lookup"><span data-stu-id="42635-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="42635-155">' 97 (8,0)</span><span class="sxs-lookup"><span data-stu-id="42635-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="42635-156">5,0</span><span class="sxs-lookup"><span data-stu-id="42635-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42635-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="42635-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="42635-158">4,0 (2000)</span><span class="sxs-lookup"><span data-stu-id="42635-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="42635-159">2000 (9,0)</span><span class="sxs-lookup"><span data-stu-id="42635-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="42635-160">2000 (9,0)</span><span class="sxs-lookup"><span data-stu-id="42635-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42635-161">Ядро СУБД Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="42635-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="42635-162">12,0 (2007)</span><span class="sxs-lookup"><span data-stu-id="42635-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="42635-163">2007</span><span class="sxs-lookup"><span data-stu-id="42635-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

