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
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="51431-102">Метод DBEngine.SetOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="51431-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="51431-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51431-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51431-104">Временно переопределяет значения для ключей двигателя базы данных Microsoft Access в реестре Windows (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="51431-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="51431-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51431-105">Syntax</span></span>

<span data-ttu-id="51431-106">*выражения* . SetOption ***(Параметр***, ***Значение***)</span><span class="sxs-lookup"><span data-stu-id="51431-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="51431-107">*выражение*: выражение, возвращающее объект **DBEngine**.</span><span class="sxs-lookup"><span data-stu-id="51431-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="51431-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="51431-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51431-109">Имя</span><span class="sxs-lookup"><span data-stu-id="51431-109">Name</span></span></p></th>
<th><p><span data-ttu-id="51431-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="51431-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="51431-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="51431-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="51431-112">Описание</span><span class="sxs-lookup"><span data-stu-id="51431-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51431-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="51431-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="51431-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51431-114">Required</span></span></p></td>
<td><p><span data-ttu-id="51431-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="51431-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-116">Константа, как описано в Примечание.</span><span class="sxs-lookup"><span data-stu-id="51431-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51431-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="51431-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="51431-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="51431-118">Required</span></span></p></td>
<td><p><span data-ttu-id="51431-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="51431-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-120">Значение, которое необходимо установить.</span><span class="sxs-lookup"><span data-stu-id="51431-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="51431-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="51431-121">Remarks</span></span>

<span data-ttu-id="51431-122">Каждая константа ссылается на соответствующий ключ реестра в пути HKEY LOCAL MACHINE \_ \_ SOFTWARE Microsoft Office \\ \\ \\ \\ 12.0 \\ Access Connectivity Engine \\ Engines \\ ACE (то есть **dbSharedAsyncDelay** соответствует ключевому программному обеспечению локальной машины HKEY Microsoft Office 12.0 Двигатели подключения доступа \_ \_ \\ \\ \\ \\ \\ \\ \\ ACE \\ SharedAsyncDelay и т. д.).</span><span class="sxs-lookup"><span data-stu-id="51431-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51431-123">Константа</span><span class="sxs-lookup"><span data-stu-id="51431-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="51431-124">Описание</span><span class="sxs-lookup"><span data-stu-id="51431-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51431-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="51431-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-126">Клавиша PageTimeout</span><span class="sxs-lookup"><span data-stu-id="51431-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51431-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="51431-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-128">Ключ SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="51431-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51431-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="51431-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-130">Ключ ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="51431-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51431-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="51431-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-132">Ключ LockRetry</span><span class="sxs-lookup"><span data-stu-id="51431-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51431-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="51431-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-134">Ключ UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="51431-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51431-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="51431-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-136">Клавиша ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="51431-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51431-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="51431-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-138">Ключ MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="51431-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51431-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="51431-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-140">Ключ MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="51431-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51431-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="51431-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-142">Ключ LockDelay</span><span class="sxs-lookup"><span data-stu-id="51431-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51431-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="51431-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-144">Ключ RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="51431-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51431-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="51431-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="51431-146">Клавиша FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="51431-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="51431-147">Используйте метод **SetOption** для переопределения значений реестра во время работы.</span><span class="sxs-lookup"><span data-stu-id="51431-147">Use the **SetOption** method to override registry values at run-time.</span></span> <span data-ttu-id="51431-148">Новые значения, установленные с помощью метода **SetOption,** остаются в силе до тех пор, пока не будут изменены другим вызовом **SetOption** или до закрытия объекта **DBEngine.**</span><span class="sxs-lookup"><span data-stu-id="51431-148">New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

