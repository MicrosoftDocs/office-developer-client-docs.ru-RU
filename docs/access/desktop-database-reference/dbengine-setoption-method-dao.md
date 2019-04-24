---
title: Метод DBEngine. SetOption (DAO)
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
# <a name="dbenginesetoption-method-dao"></a><span data-ttu-id="aac59-102">Метод DBEngine. SetOption (DAO)</span><span class="sxs-lookup"><span data-stu-id="aac59-102">DBEngine.SetOption method (DAO)</span></span>

<span data-ttu-id="aac59-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="aac59-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="aac59-104">Временно переопределяет значения ключей ядра СУБД Microsoft Access в реестре Windows (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="aac59-104">Temporarily overrides values for the Microsoft Access database engine keys in the Windows Registry (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="aac59-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aac59-105">Syntax</span></span>

<span data-ttu-id="aac59-106">*Expression* . SetOption (***параметр***, ***значение***)</span><span class="sxs-lookup"><span data-stu-id="aac59-106">*expression* .SetOption(***Option***, ***Value***)</span></span>

<span data-ttu-id="aac59-107">*Expression (выражение* ) Выражение, возвращающее объект **DBEngine** .</span><span class="sxs-lookup"><span data-stu-id="aac59-107">*expression* An expression that returns a **DBEngine** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="aac59-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="aac59-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aac59-109">Имя</span><span class="sxs-lookup"><span data-stu-id="aac59-109">Name</span></span></p></th>
<th><p><span data-ttu-id="aac59-110">Обязательно/необязательно</span><span class="sxs-lookup"><span data-stu-id="aac59-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="aac59-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="aac59-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="aac59-112">Описание</span><span class="sxs-lookup"><span data-stu-id="aac59-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aac59-113"><em>Вариант</em></span><span class="sxs-lookup"><span data-stu-id="aac59-113"><em>Option</em></span></span></p></td>
<td><p><span data-ttu-id="aac59-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="aac59-114">Required</span></span></p></td>
<td><p><span data-ttu-id="aac59-115"><strong>Long</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-115"><strong>Long</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-116">Константа, описанная в разделе Примечания.</span><span class="sxs-lookup"><span data-stu-id="aac59-116">A constant as described in Remarks.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac59-117"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="aac59-117"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="aac59-118">Обязательный</span><span class="sxs-lookup"><span data-stu-id="aac59-118">Required</span></span></p></td>
<td><p><span data-ttu-id="aac59-119"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-119"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-120">Значение, которое необходимо присвоить параметру.</span><span class="sxs-lookup"><span data-stu-id="aac59-120">The value that you want to set option to.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="aac59-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="aac59-121">Remarks</span></span>

<span data-ttu-id="aac59-122">Каждая константа относится к соответствующему разделу реестра в пути\_к\_локальному компьютеру\\в\\пути\\к программному\\обеспечению\\\\Microsoft\\Office 12,0 Access Engines Engine (то есть **дбшаредасинкделай** соответствует ключевому программному\_обеспечению\\\\для локального\\\_компьютера\\hKey\\механизмы\\подключения к\\Microsoft Office 12,0 Access Engines \\Шаредасинкделай и т. д.).</span><span class="sxs-lookup"><span data-stu-id="aac59-122">Each constant refers to the corresponding registry key in the path HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE (that is, **dbSharedAsyncDelay** corresponds to the key HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Office\\12.0\\Access Connectivity Engine\\Engines\\ACE\\SharedAsyncDelay, and so on).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aac59-123">Константа</span><span class="sxs-lookup"><span data-stu-id="aac59-123">Constant</span></span></p></th>
<th><p><span data-ttu-id="aac59-124">Описание</span><span class="sxs-lookup"><span data-stu-id="aac59-124">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aac59-125"><strong>Дбпажетимеаут</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-125"><strong>dbPageTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-126">Ключ Пажетимеаут</span><span class="sxs-lookup"><span data-stu-id="aac59-126">The PageTimeout key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac59-127"><strong>Дбшаредасинкделай</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-127"><strong>dbSharedAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-128">Ключ Шаредасинкделай</span><span class="sxs-lookup"><span data-stu-id="aac59-128">The SharedAsyncDelay key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac59-129"><strong>Дбексклусивеасинкделай</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-129"><strong>dbExclusiveAsyncDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-130">Ключ Ексклусивеасинкделай</span><span class="sxs-lookup"><span data-stu-id="aac59-130">The ExclusiveAsyncDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac59-131"><strong>Дблоккретри</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-131"><strong>dbLockRetry</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-132">Ключ Локкретри</span><span class="sxs-lookup"><span data-stu-id="aac59-132">The LockRetry key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac59-133"><strong>Дбусеркоммитсинк</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-133"><strong>dbUserCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-134">Ключ Усеркоммитсинк</span><span class="sxs-lookup"><span data-stu-id="aac59-134">The UserCommitSync key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac59-135"><strong>ДбимплиЦиткоммитсинк</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-135"><strong>dbImplicitCommitSync</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-136">Ключ ИмплиЦиткоммитсинк</span><span class="sxs-lookup"><span data-stu-id="aac59-136">The ImplicitCommitSync key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac59-137"><strong>Дбмаксбуфферсизе</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-137"><strong>dbMaxBufferSize</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-138">Ключ Максбуфферсизе</span><span class="sxs-lookup"><span data-stu-id="aac59-138">The MaxBufferSize key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac59-139"><strong>Дбмакслокксперфиле</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-139"><strong>dbMaxLocksPerFile</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-140">Ключ MaxLocksPerFile</span><span class="sxs-lookup"><span data-stu-id="aac59-140">The MaxLocksPerFile key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac59-141"><strong>Дблоккделай</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-141"><strong>dbLockDelay</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-142">Ключ Локкделай</span><span class="sxs-lookup"><span data-stu-id="aac59-142">The LockDelay key</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aac59-143"><strong>Дбрециклелвс</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-143"><strong>dbRecycleLVs</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-144">Ключ Рециклелвс</span><span class="sxs-lookup"><span data-stu-id="aac59-144">The RecycleLVs key</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aac59-145"><strong>Дбфлуштрансактионтимеаут</strong></span><span class="sxs-lookup"><span data-stu-id="aac59-145"><strong>dbFlushTransactionTimeout</strong></span></span></p></td>
<td><p><span data-ttu-id="aac59-146">Ключ Флуштрансактионтимеаут</span><span class="sxs-lookup"><span data-stu-id="aac59-146">The FlushTransactionTimeout key</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="aac59-147">Метод **SetOption** используется для переопределения значений реестра во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="aac59-147">Use the **SetOption** method to override registry values at run-time.</span></span> <span data-ttu-id="aac59-148">Новые значения, установленные с помощью метода **SetOption** , действуют до тех пор, пока не будут изменены другим вызовом **SetOption** или пока объект **DBEngine** не будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="aac59-148">New values established with the **SetOption** method remain in effect until changed again by another **SetOption** call, or until the **DBEngine** object is closed.</span></span>

