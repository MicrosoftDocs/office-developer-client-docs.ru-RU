---
title: Характеристики курсоров и блокировок
TOCTitle: Cursor and lock characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 41a42aa3b0c49a5d871fa7b079a26c7d8076116a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295291"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="8b780-102">Характеристики курсоров и блокировок</span><span class="sxs-lookup"><span data-stu-id="8b780-102">Cursor and lock characteristics</span></span>

<span data-ttu-id="8b780-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8b780-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8b780-104">Хотя характеристики курсора зависят от возможностей поставщика, следующие преимущества и недостатки обычно применяются к различным типам курсоров и блокировок.</span><span class="sxs-lookup"><span data-stu-id="8b780-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8b780-105">Тип курсора или блокировки</span><span class="sxs-lookup"><span data-stu-id="8b780-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="8b780-106">Преимущества</span><span class="sxs-lookup"><span data-stu-id="8b780-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="8b780-107">Недостатки</span><span class="sxs-lookup"><span data-stu-id="8b780-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8b780-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="8b780-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-109">Низкие требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="8b780-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-110">Не удается прокрутить назад</span><span class="sxs-lookup"><span data-stu-id="8b780-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="8b780-111">Нет данных совмее-</span><span class="sxs-lookup"><span data-stu-id="8b780-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b780-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="8b780-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-113">Прокручиваемая</span><span class="sxs-lookup"><span data-stu-id="8b780-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-114">Нет данных совмее-</span><span class="sxs-lookup"><span data-stu-id="8b780-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b780-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="8b780-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-116">Некоторые данные concurrency</span><span class="sxs-lookup"><span data-stu-id="8b780-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="8b780-117">Прокручиваемая</span><span class="sxs-lookup"><span data-stu-id="8b780-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-118">Более высокие требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="8b780-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="8b780-119">Отсутствует в сценарии отключения</span><span class="sxs-lookup"><span data-stu-id="8b780-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b780-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="8b780-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-121">Высокая емка данных</span><span class="sxs-lookup"><span data-stu-id="8b780-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="8b780-122">Прокручиваемая</span><span class="sxs-lookup"><span data-stu-id="8b780-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-123">Самые высокие требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="8b780-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="8b780-124">Отсутствует в сценарии отключения</span><span class="sxs-lookup"><span data-stu-id="8b780-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b780-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="8b780-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-126">Низкие требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="8b780-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="8b780-127">Высокая масштабируемость</span><span class="sxs-lookup"><span data-stu-id="8b780-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-128">Данные, которые не могут быть updatable с помощью курсора</span><span class="sxs-lookup"><span data-stu-id="8b780-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b780-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="8b780-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-130">Пакетные обновления</span><span class="sxs-lookup"><span data-stu-id="8b780-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="8b780-131">Разрешает отключенные сценарии</span><span class="sxs-lookup"><span data-stu-id="8b780-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="8b780-132">Другие пользователи, которые могут получить доступ к данным</span><span class="sxs-lookup"><span data-stu-id="8b780-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-133">Данные могут быть изменены несколькими пользователями одновременно</span><span class="sxs-lookup"><span data-stu-id="8b780-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8b780-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="8b780-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-135">Данные не могут быть изменены другими пользователями во время блокировки</span><span class="sxs-lookup"><span data-stu-id="8b780-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-136">Запретить другим пользователям доступ к данным во время блокировки</span><span class="sxs-lookup"><span data-stu-id="8b780-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8b780-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="8b780-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-138">Другие пользователи, которые могут получать доступ к данным</span><span class="sxs-lookup"><span data-stu-id="8b780-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="8b780-139">Данные могут быть изменены несколькими пользователями одновременно</span><span class="sxs-lookup"><span data-stu-id="8b780-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

