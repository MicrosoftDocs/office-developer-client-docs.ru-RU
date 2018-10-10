---
title: Cursor and Lock Characteristics
TOCTitle: Cursor and Lock Characteristics
ms:assetid: 5f8b6700-14f6-d342-42f6-cc8e89c71a1a
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249347(v=office.15)
ms:contentKeyID: 48545164
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 50eadc486d00436a51b9f7341ef6e0ad2587a015
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479744"
---
# <a name="cursor-and-lock-characteristics"></a><span data-ttu-id="2405d-102">Cursor and Lock Characteristics</span><span class="sxs-lookup"><span data-stu-id="2405d-102">Cursor and Lock Characteristics</span></span>


<span data-ttu-id="2405d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="2405d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="2405d-104">Во время характеристики курсора зависят от возможностей поставщика, следующие преимущества и недостатки обычно относятся к различные типы курсоров и блокировок.</span><span class="sxs-lookup"><span data-stu-id="2405d-104">While the characteristics of a cursor depend upon capabilities of the provider, the following advantages and disadvantages generally apply to the various types of cursors and locks.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2405d-105">Тип курсора или блокировки</span><span class="sxs-lookup"><span data-stu-id="2405d-105">Cursor or lock type</span></span></p></th>
<th><p><span data-ttu-id="2405d-106">Преимущества</span><span class="sxs-lookup"><span data-stu-id="2405d-106">Advantages</span></span></p></th>
<th><p><span data-ttu-id="2405d-107">Недостатки</span><span class="sxs-lookup"><span data-stu-id="2405d-107">Disadvantages</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2405d-108"><strong>adOpenForwardOnly</strong></span><span class="sxs-lookup"><span data-stu-id="2405d-108"><strong>adOpenForwardOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-109">Требования к нехватки ресурсов</span><span class="sxs-lookup"><span data-stu-id="2405d-109">Low resource requirements</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-110">Не удается Прокрутка назад</span><span class="sxs-lookup"><span data-stu-id="2405d-110">Cannot scroll backward</span></span></p></li>
<li><p><span data-ttu-id="2405d-111">Нет данных параллелизма</span><span class="sxs-lookup"><span data-stu-id="2405d-111">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2405d-112"><strong>adOpenStatic</strong></span><span class="sxs-lookup"><span data-stu-id="2405d-112"><strong>adOpenStatic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-113">Прокручиваемой</span><span class="sxs-lookup"><span data-stu-id="2405d-113">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-114">Нет данных параллелизма</span><span class="sxs-lookup"><span data-stu-id="2405d-114">No data concurrency</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2405d-115"><strong>adOpenKeyset</strong></span><span class="sxs-lookup"><span data-stu-id="2405d-115"><strong>adOpenKeyset</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-116">Некоторые данные параллелизма</span><span class="sxs-lookup"><span data-stu-id="2405d-116">Some data concurrency</span></span></p></li>
<li><p><span data-ttu-id="2405d-117">Прокручиваемой</span><span class="sxs-lookup"><span data-stu-id="2405d-117">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-118">Выше требований к ресурсам</span><span class="sxs-lookup"><span data-stu-id="2405d-118">Higher resource requirements</span></span></p></li>
<li><p><span data-ttu-id="2405d-119">Недоступно в отключенные сценарии</span><span class="sxs-lookup"><span data-stu-id="2405d-119">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2405d-120"><strong>adOpenDynamic</strong></span><span class="sxs-lookup"><span data-stu-id="2405d-120"><strong>adOpenDynamic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-121">Параллелизм высокой данных</span><span class="sxs-lookup"><span data-stu-id="2405d-121">High data concurrency</span></span></p></li>
<li><p><span data-ttu-id="2405d-122">Прокручиваемой</span><span class="sxs-lookup"><span data-stu-id="2405d-122">Scrollable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-123">Наибольший требований к ресурсам</span><span class="sxs-lookup"><span data-stu-id="2405d-123">Highest resource requirements</span></span></p></li>
<li><p><span data-ttu-id="2405d-124">Недоступно в отключенные сценарии</span><span class="sxs-lookup"><span data-stu-id="2405d-124">Not available in disconnected scenario</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2405d-125"><strong>adLockReadOnly</strong></span><span class="sxs-lookup"><span data-stu-id="2405d-125"><strong>adLockReadOnly</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-126">Требования к нехватки ресурсов</span><span class="sxs-lookup"><span data-stu-id="2405d-126">Low resource requirements</span></span></p></li>
<li><p><span data-ttu-id="2405d-127">Хорошо масштабируемое</span><span class="sxs-lookup"><span data-stu-id="2405d-127">Highly scalable</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-128">Данные не обновляемых до текущей позиции</span><span class="sxs-lookup"><span data-stu-id="2405d-128">Data not updatable through cursor</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2405d-129"><strong>adLockBatchOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="2405d-129"><strong>adLockBatchOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-130">Пакет обновления</span><span class="sxs-lookup"><span data-stu-id="2405d-130">Batch updates</span></span></p></li>
<li><p><span data-ttu-id="2405d-131">Позволяет без подключения к сети</span><span class="sxs-lookup"><span data-stu-id="2405d-131">Allows disconnected scenarios</span></span></p></li>
<li><p><span data-ttu-id="2405d-132">Другие пользователи могут получить доступ к данным</span><span class="sxs-lookup"><span data-stu-id="2405d-132">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-133">Данные могут быть изменены несколькими пользователями одновременно</span><span class="sxs-lookup"><span data-stu-id="2405d-133">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2405d-134"><strong>adLockPessimistic</strong></span><span class="sxs-lookup"><span data-stu-id="2405d-134"><strong>adLockPessimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-135">Данные не могут менять другие пользователи во время блокировки</span><span class="sxs-lookup"><span data-stu-id="2405d-135">Data cannot be changed by other users while locked</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-136">Пользователям запрещается доступ к данным во время блокировки</span><span class="sxs-lookup"><span data-stu-id="2405d-136">Prevents other users from accessing data while locked</span></span></p></li>
</ul>
<p></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2405d-137"><strong>adLockOptimistic</strong></span><span class="sxs-lookup"><span data-stu-id="2405d-137"><strong>adLockOptimistic</strong></span></span></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-138">Другие пользователи могут получить доступ к данным</span><span class="sxs-lookup"><span data-stu-id="2405d-138">Other users able to access data</span></span></p></li>
</ul>
<p></p></td>
<td><p></p>
<ul>
<li><p><span data-ttu-id="2405d-139">Данные могут быть изменены несколькими пользователями одновременно</span><span class="sxs-lookup"><span data-stu-id="2405d-139">Data can be changed by multiple users at once</span></span></p></li>
</ul>
<p></p></td>
</tr>
</tbody>
</table>

