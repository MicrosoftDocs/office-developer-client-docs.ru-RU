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
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="26217-102">Характеристики курсоров и блокировок</span><span class="sxs-lookup"><span data-stu-id="26217-102">Cursor and lock characteristics</span></span>

<span data-ttu-id="26217-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26217-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26217-104">Несмотря на то, что характеристики курсора зависят от возможностей поставщика, следующие преимущества и недостатки обычно применяются к различным типам курсоров и блокировок.</span><span class="sxs-lookup"><span data-stu-id="26217-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26217-105">Тип курсора или блокировки</span><span class="sxs-lookup"><span data-stu-id="26217-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="26217-106">Преимущества</span><span class="sxs-lookup"><span data-stu-id="26217-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="26217-107">Недостатки</span><span class="sxs-lookup"><span data-stu-id="26217-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26217-108"><strong>адопенфорвардонли</strong></span><span class="sxs-lookup"><span data-stu-id="26217-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-109">Недорогие требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="26217-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-110">Не удается прокрутить назад</span><span class="sxs-lookup"><span data-stu-id="26217-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="26217-111">Без параллельной обработки данных</span><span class="sxs-lookup"><span data-stu-id="26217-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26217-112"><strong>адопенстатик</strong></span><span class="sxs-lookup"><span data-stu-id="26217-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-113">Прокручиваемой</span><span class="sxs-lookup"><span data-stu-id="26217-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-114">Без параллельной обработки данных</span><span class="sxs-lookup"><span data-stu-id="26217-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26217-115"><strong>адопенкэйсет</strong></span><span class="sxs-lookup"><span data-stu-id="26217-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-116">Часть параллелизма данных</span><span class="sxs-lookup"><span data-stu-id="26217-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="26217-117">Прокручиваемой</span><span class="sxs-lookup"><span data-stu-id="26217-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-118">Более высокие требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="26217-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="26217-119">Недоступно в сценарии отключения</span><span class="sxs-lookup"><span data-stu-id="26217-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26217-120"><strong>адопендинамик</strong></span><span class="sxs-lookup"><span data-stu-id="26217-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-121">Высокая степень параллелизма данных</span><span class="sxs-lookup"><span data-stu-id="26217-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="26217-122">Прокручиваемой</span><span class="sxs-lookup"><span data-stu-id="26217-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-123">Максимальные требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="26217-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="26217-124">Недоступно в сценарии отключения</span><span class="sxs-lookup"><span data-stu-id="26217-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26217-125"><strong>адлоккреадонли</strong></span><span class="sxs-lookup"><span data-stu-id="26217-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-126">Недорогие требования к ресурсам</span><span class="sxs-lookup"><span data-stu-id="26217-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="26217-127">Высокая масштабируемость</span><span class="sxs-lookup"><span data-stu-id="26217-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-128">Данные не обновляются с помощью курсора</span><span class="sxs-lookup"><span data-stu-id="26217-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26217-129"><strong>адлоккбатчоптимистик</strong></span><span class="sxs-lookup"><span data-stu-id="26217-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-130">Пакетные обновления</span><span class="sxs-lookup"><span data-stu-id="26217-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="26217-131">Разрешает сценарии с отключенной отсоединением</span><span class="sxs-lookup"><span data-stu-id="26217-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="26217-132">Другие пользователи, которые могут получать доступ к данным</span><span class="sxs-lookup"><span data-stu-id="26217-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-133">Данные могут быть изменены несколькими пользователями одновременно</span><span class="sxs-lookup"><span data-stu-id="26217-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26217-134"><strong>адлоккпессимистик</strong></span><span class="sxs-lookup"><span data-stu-id="26217-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-135">Данные не могут быть изменены другими пользователями, если они заблокированы</span><span class="sxs-lookup"><span data-stu-id="26217-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-136">Запрещает другим пользователям доступ к данным во время блокировки</span><span class="sxs-lookup"><span data-stu-id="26217-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26217-137"><strong>адлоккоптимистик</strong></span><span class="sxs-lookup"><span data-stu-id="26217-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-138">Другие пользователи, которые могут получать доступ к данным</span><span class="sxs-lookup"><span data-stu-id="26217-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="26217-139">Данные могут быть изменены несколькими пользователями одновременно</span><span class="sxs-lookup"><span data-stu-id="26217-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

