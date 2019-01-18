---
title: 'Метод: DBEngine.SetOption (DAO)'
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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699893"
---
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="4040e-102">Метод: DBEngine.SetOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="4040e-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="4040e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4040e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4040e-104">Временно переопределяет значения для клавиш ядра базы данных Microsoft Access в реестре Windows (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4040e-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4040e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4040e-105">Syntax</span></span>

<span data-ttu-id="4040e-106">*выражение* . SetOption (***вариант***, ***значение***)</span><span class="sxs-lookup"><span data-stu-id="4040e-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="4040e-107">*выражение* Выражение, возвращающее объект **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="4040e-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4040e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4040e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4040e-109">Имя</span><span class="sxs-lookup"><span data-stu-id="4040e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4040e-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="4040e-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4040e-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4040e-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4040e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4040e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4040e-113"><em>Option</em></span><span class="sxs-lookup"><span data-stu-id="4040e-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="4040e-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4040e-114">Required</span></span></p></td>
<td><p><span data-ttu-id="4040e-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-116">Константа, как описано в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="4040e-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4040e-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="4040e-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="4040e-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="4040e-118">Required</span></span></p></td>
<td><p><span data-ttu-id="4040e-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-120">Значение, которое требуется для параметра.</span><span class="sxs-lookup"><span data-stu-id="4040e-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="4040e-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="4040e-121">Remarks</span></span>

<span data-ttu-id="4040e-122">Каждая константа ссылается на соответствующий раздел реестра в поле путь HKEY\_ЛОКАЛЬНОГО\_МАШИНЫ\\программного обеспечения\\Microsoft\\Office\\12.0\\ядро доступа подключения к\\обработчики\\ACE (то есть, **dbSharedAsyncDelay** соответствующий ключ HKEY\_ЛОКАЛЬНОГО\_МАШИНЫ\\программного обеспечения\\Microsoft\\Office\\12.0\\модуль подключения к Access\\обработчики\\элемент управления ДОСТУПОМ \\SharedAsyncDelay, и так далее).</span><span class="sxs-lookup"><span data-stu-id="4040e-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4040e-123">Константа</span><span class="sxs-lookup"><span data-stu-id="4040e-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="4040e-124">Описание</span><span class="sxs-lookup"><span data-stu-id="4040e-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4040e-125"><strong>dbPageTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-126">Клавиша PageTimeout</span><span class="sxs-lookup"><span data-stu-id="4040e-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4040e-127"><strong>dbSharedAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-128">Клавиша SharedAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="4040e-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4040e-129"><strong>dbExclusiveAsyncDelay</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-130">Клавиша ExclusiveAsyncDelay</span><span class="sxs-lookup"><span data-stu-id="4040e-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4040e-131"><strong>dbLockRetry</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-132">Клавиша LockRetry</span><span class="sxs-lookup"><span data-stu-id="4040e-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4040e-133"><strong>dbUserCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-134">Клавиша UserCommitSync</span><span class="sxs-lookup"><span data-stu-id="4040e-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4040e-135"><strong>dbImplicitCommitSync</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-136">Клавиша ImplicitCommitSync</span><span class="sxs-lookup"><span data-stu-id="4040e-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4040e-137"><strong>dbMaxBufferSize</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-138">Клавиша MaxBufferSize</span><span class="sxs-lookup"><span data-stu-id="4040e-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4040e-139"><strong>dbMaxLocksPerFile</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-140">Клавиша MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="4040e-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4040e-141"><strong>dbLockDelay</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-142">Клавиша LockDelay</span><span class="sxs-lookup"><span data-stu-id="4040e-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4040e-143"><strong>dbRecycleLVs</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-144">Клавиша RecycleLVs</span><span class="sxs-lookup"><span data-stu-id="4040e-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4040e-145"><strong>dbFlushTransactionTimeout</strong></span><span class="sxs-lookup"><span data-stu-id="4040e-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="4040e-146">Клавиша FlushTransactionTimeout</span><span class="sxs-lookup"><span data-stu-id="4040e-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4040e-147">Используйте метод **SetOption** переопределение значения реестра во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4040e-147">Use the **SetOption** method to override registry values at run-time.</span></span> <span data-ttu-id="4040e-148">Новые значения, установленных с помощью метода **SetOption** остаются в силе до еще раз изменена другой вызов **SetOption** или закрытии объекта **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="4040e-148">New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

