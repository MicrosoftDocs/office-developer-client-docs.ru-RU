---
title: Свойство Database.Version (DAO)
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
# <a name="databaseversion-property-dao"></a><span data-ttu-id="eec13-102">Свойство Database.Version (DAO)</span><span class="sxs-lookup"><span data-stu-id="eec13-102">Database.Version property (DAO)</span></span>

<span data-ttu-id="eec13-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="eec13-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="eec13-104">В рабочей области Microsoft Access возвращается весяк двигателя базы данных Microsoft Jet или Microsoft Access, создав базу данных.</span><span class="sxs-lookup"><span data-stu-id="eec13-104">In a Microsoft Access workspace, returns the vesion of the Microsoft Jet or Microsoft Access database engine that created the database.</span></span> <span data-ttu-id="eec13-105">Только для чтения, **String**.</span><span class="sxs-lookup"><span data-stu-id="eec13-105">Read-only **String**.</span></span>

## <a name="syntax"></a><span data-ttu-id="eec13-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="eec13-106">Syntax</span></span>

<span data-ttu-id="eec13-107">*выражения* . Версия</span><span class="sxs-lookup"><span data-stu-id="eec13-107">*expression* .Version</span></span>

<span data-ttu-id="eec13-108">*выражение*: переменная, представляющая объект **Database**.</span><span class="sxs-lookup"><span data-stu-id="eec13-108">*expression* A variable that represents a **Database** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="eec13-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="eec13-109">Remarks</span></span>

<span data-ttu-id="eec13-110">Возвращаемая величина — это строка, которая оценивает номер версии, отформатированный следующим образом.</span><span class="sxs-lookup"><span data-stu-id="eec13-110">The return value is a String that evaluates to a version number, formatted as follows.</span></span>

- <span data-ttu-id="eec13-111">Рабочее пространство Microsoft Access представляет номер версии в форме *"major.minor".*</span><span class="sxs-lookup"><span data-stu-id="eec13-111">Microsoft Access workspace represents the version number in the form "*major.minor*".</span></span> <span data-ttu-id="eec13-112">Например, "3.0".</span><span class="sxs-lookup"><span data-stu-id="eec13-112">For example, "3.0".</span></span> <span data-ttu-id="eec13-113">Номер версии продукта состоит из номера версии (3), периода и номера выпуска (0).</span><span class="sxs-lookup"><span data-stu-id="eec13-113">The product version number consists of the version number (3), a period, and the release number (0).</span></span>

<span data-ttu-id="eec13-114">В следующей таблице показано, какая версия двигателя базы данных была включена в различные версии продуктов Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="eec13-114">The following table shows which version of the database engine was included with various versions of Microsoft products.</span></span>

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
<th><p><span data-ttu-id="eec13-115">ядро СУБД</span><span class="sxs-lookup"><span data-stu-id="eec13-115">Database Engine</span></span></p></th>
<th><p><span data-ttu-id="eec13-116">Версия (год выпуска)</span><span class="sxs-lookup"><span data-stu-id="eec13-116">Version (year released)</span></span></p></th>
<th><p><span data-ttu-id="eec13-117">Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="eec13-117">Microsoft Access</span></span></p></th>
<th><p><span data-ttu-id="eec13-118">Microsoft Visual Basic</span><span class="sxs-lookup"><span data-stu-id="eec13-118">Microsoft Visual Basic</span></span></p></th>
<th><p><span data-ttu-id="eec13-119">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="eec13-119">Microsoft Excel</span></span></p></th>
<th><p><span data-ttu-id="eec13-120">Microsoft Visual C++</span><span class="sxs-lookup"><span data-stu-id="eec13-120">Microsoft Visual C++</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eec13-121">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="eec13-121">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="eec13-122">1.0 (1992)</span><span class="sxs-lookup"><span data-stu-id="eec13-122">1.0 (1992)</span></span></p></td>
<td><p><span data-ttu-id="eec13-123">1.0</span><span class="sxs-lookup"><span data-stu-id="eec13-123">1.0</span></span></p></td>
<td><p><span data-ttu-id="eec13-124">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-124">N/A</span></span></p></td>
<td><p><span data-ttu-id="eec13-125">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-125">N/A</span></span></p></td>
<td><p><span data-ttu-id="eec13-126">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-126">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eec13-127">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="eec13-127">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="eec13-128">1.1 (1993)</span><span class="sxs-lookup"><span data-stu-id="eec13-128">1.1 (1993)</span></span></p></td>
<td><p><span data-ttu-id="eec13-129">1.1</span><span class="sxs-lookup"><span data-stu-id="eec13-129">1.1</span></span></p></td>
<td><p><span data-ttu-id="eec13-130">3.0</span><span class="sxs-lookup"><span data-stu-id="eec13-130">3.0</span></span></p></td>
<td><p><span data-ttu-id="eec13-131">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-131">N/A</span></span></p></td>
<td><p><span data-ttu-id="eec13-132">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-132">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eec13-133">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="eec13-133">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="eec13-134">2.0 (1994)</span><span class="sxs-lookup"><span data-stu-id="eec13-134">2.0 (1994)</span></span></p></td>
<td><p><span data-ttu-id="eec13-135">2.0</span><span class="sxs-lookup"><span data-stu-id="eec13-135">2.0</span></span></p></td>
<td><p><span data-ttu-id="eec13-136">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-136">N/A</span></span></p></td>
<td><p><span data-ttu-id="eec13-137">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-137">N/A</span></span></p></td>
<td><p><span data-ttu-id="eec13-138">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-138">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eec13-139">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="eec13-139">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="eec13-140">2.5 (1995)</span><span class="sxs-lookup"><span data-stu-id="eec13-140">2.5 (1995)</span></span></p></td>
<td><p><span data-ttu-id="eec13-141">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-141">N/A</span></span></p></td>
<td><p><span data-ttu-id="eec13-142">4.0 (16-битная)</span><span class="sxs-lookup"><span data-stu-id="eec13-142">4.0 (16-bit)</span></span></p></td>
<td><p><span data-ttu-id="eec13-143">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-143">N/A</span></span></p></td>
<td><p><span data-ttu-id="eec13-144">Н/Д</span><span class="sxs-lookup"><span data-stu-id="eec13-144">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eec13-145">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="eec13-145">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="eec13-146">3.0 (1995)</span><span class="sxs-lookup"><span data-stu-id="eec13-146">3.0 (1995)</span></span></p></td>
<td><p><span data-ttu-id="eec13-147">'95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="eec13-147">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="eec13-148">4.0 (32-битная)</span><span class="sxs-lookup"><span data-stu-id="eec13-148">4.0 (32-bit)</span></span></p></td>
<td><p><span data-ttu-id="eec13-149">'95 (7.0)</span><span class="sxs-lookup"><span data-stu-id="eec13-149">‘95 (7.0)</span></span></p></td>
<td><p><span data-ttu-id="eec13-150">4.x</span><span class="sxs-lookup"><span data-stu-id="eec13-150">4.x</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eec13-151">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="eec13-151">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="eec13-152">3.5 (1996)</span><span class="sxs-lookup"><span data-stu-id="eec13-152">3.5 (1996)</span></span></p></td>
<td><p><span data-ttu-id="eec13-153">'97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="eec13-153">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="eec13-154">5.0</span><span class="sxs-lookup"><span data-stu-id="eec13-154">5.0</span></span></p></td>
<td><p><span data-ttu-id="eec13-155">'97 (8.0)</span><span class="sxs-lookup"><span data-stu-id="eec13-155">‘97 (8.0)</span></span></p></td>
<td><p><span data-ttu-id="eec13-156">5.0</span><span class="sxs-lookup"><span data-stu-id="eec13-156">5.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="eec13-157">Microsoft Jet</span><span class="sxs-lookup"><span data-stu-id="eec13-157">Microsoft Jet</span></span></p></td>
<td><p><span data-ttu-id="eec13-158">4.0 (2000)</span><span class="sxs-lookup"><span data-stu-id="eec13-158">4.0 (2000)</span></span></p></td>
<td><p><span data-ttu-id="eec13-159">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="eec13-159">2000 (9.0)</span></span></p></td>
<td><p></p></td>
<td><p><span data-ttu-id="eec13-160">2000 (9.0)</span><span class="sxs-lookup"><span data-stu-id="eec13-160">2000 (9.0)</span></span></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eec13-161">Двигатель базы данных Microsoft Access</span><span class="sxs-lookup"><span data-stu-id="eec13-161">Microsoft Access database engine</span></span></p></td>
<td><p><span data-ttu-id="eec13-162">12.0 (2007)</span><span class="sxs-lookup"><span data-stu-id="eec13-162">12.0 (2007)</span></span></p></td>
<td><p><span data-ttu-id="eec13-163">2007</span><span class="sxs-lookup"><span data-stu-id="eec13-163">2007</span></span></p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>

