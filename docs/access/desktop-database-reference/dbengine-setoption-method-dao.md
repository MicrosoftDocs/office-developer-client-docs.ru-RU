---
title: Метод DBEngine.SetOption (DAO)
TOCTitle: SetOption Method
ms:assetid: ea55c10c-2385-1b7e-0cba-32982c9b6643
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836236(v=office.15)
ms:contentKeyID: 48548461
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1088781
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 5875a8935b1b44c3c36b29344af32df552f6e01c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294199"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="c94b9-102">Метод DBEngine.SetOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="c94b9-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="c94b9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c94b9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="c94b9-104">Временно переопределяет значения ключей ядер ядер баз данных Microsoft Access в реестре Windows (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c94b9-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c94b9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c94b9-105">Syntax</span></span>

<span data-ttu-id="c94b9-106">*выражение .* SetOption(***Option***, ***Value***)</span><span class="sxs-lookup"><span data-stu-id="c94b9-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="c94b9-107">*выражение*: выражение, возвращающее объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="c94b9-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="c94b9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="c94b9-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c94b9-109">Имя</span><span class="sxs-lookup"><span data-stu-id="c94b9-109">Name</span></span></p></th>
<th><p><span data-ttu-id="c94b9-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="c94b9-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="c94b9-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="c94b9-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="c94b9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="c94b9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c94b9-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="c94b9-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="c94b9-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="c94b9-114">Required</span></span></p></td>
<td><p><span data-ttu-id="c94b9-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-116">Константа, как описано в примечах.</span><span class="sxs-lookup"><span data-stu-id="c94b9-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c94b9-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="c94b9-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="c94b9-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="c94b9-118">Required</span></span></p></td>
<td><p><span data-ttu-id="c94b9-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-120">Значение, которое вы хотите установить.</span><span class="sxs-lookup"><span data-stu-id="c94b9-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="c94b9-121">Заметки</span><span class="sxs-lookup"><span data-stu-id="c94b9-121">Remarks</span></span>

<span data-ttu-id="c94b9-122">Каждая константа ссылается на соответствующий раздел реестра в пути HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Office \_ \\ \\ \\ \\ 12.0 \\ Access Connectivity \\ Engines \\ ACE (то есть **dbSharedAsyncDelay** соответствует ключу HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Office \_ \\ \\ \\ \\ 12.0 \\ Access Connectivity \\ Engines \\ ACE \\ SharedAsyncDelay и т. д.).</span><span class="sxs-lookup"><span data-stu-id="c94b9-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c94b9-123">Константа</span><span class="sxs-lookup"><span data-stu-id="c94b9-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="c94b9-124">Описание</span><span class="sxs-lookup"><span data-stu-id="c94b9-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c94b9-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-126">Ключ PageTimeout</span><span class="sxs-lookup"><span data-stu-id="c94b9-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c94b9-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-128">Ключ SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="c94b9-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c94b9-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-130">Ключ ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="c94b9-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c94b9-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-132">Ключ LockRetry</span><span class="sxs-lookup"><span data-stu-id="c94b9-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c94b9-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-134">Ключ UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="c94b9-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c94b9-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-136">Ключ ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="c94b9-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c94b9-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-138">Ключ MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="c94b9-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c94b9-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-140">Ключ MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="c94b9-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c94b9-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-142">Ключ LockDelay</span><span class="sxs-lookup"><span data-stu-id="c94b9-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c94b9-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-144">Ключ RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="c94b9-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c94b9-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="c94b9-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="c94b9-146">Ключ FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="c94b9-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c94b9-147">Используйте метод **SetOption** для переопределения значений реестра во время работы.</span><span class="sxs-lookup"><span data-stu-id="c94b9-147">Use the **SetOption** method to override registry values at run-time.</span></span> <span data-ttu-id="c94b9-148">Новые значения, установленные с помощью метода **SetOption,** остаются в силе до тех пор, пока не будут изменены другим вызовом **SetOption** или пока объект **DBEngine** не будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="c94b9-148">New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

