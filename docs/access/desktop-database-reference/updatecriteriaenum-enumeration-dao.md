---
title: Переопределение UpdateCriteriaEnum (DAO)
TOCTitle: UpdateCriteriaEnum Enumeration
ms:assetid: 1f83a0c6-bdc8-9c3e-380b-524f611f6476
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845853(v=office.15)
ms:contentKeyID: 48543644
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e27eb1bdfb9b393df76af8bdf54bc7f05fd82c2e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306372"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="50851-102">Переопределение UpdateCriteriaEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="50851-102">UpdateCriteriaEnum enumeration (DAO)</span></span>


<span data-ttu-id="50851-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50851-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50851-104">Используется с **методом UpdateOptions,** чтобы указать, как строится пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="50851-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50851-105">Имя</span><span class="sxs-lookup"><span data-stu-id="50851-105">Name</span></span></p></th>
<th><p><span data-ttu-id="50851-106">Значение</span><span class="sxs-lookup"><span data-stu-id="50851-106">Value</span></span></p></th>
<th><p><span data-ttu-id="50851-107">Описание</span><span class="sxs-lookup"><span data-stu-id="50851-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50851-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="50851-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="50851-109">4 </span><span class="sxs-lookup"><span data-stu-id="50851-109">4</span></span></p></td>
<td><p><span data-ttu-id="50851-110">Использует столбец клавиши (s) и все столбцы в пункте where.</span><span class="sxs-lookup"><span data-stu-id="50851-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50851-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="50851-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="50851-112">16 </span><span class="sxs-lookup"><span data-stu-id="50851-112">16</span></span></p></td>
<td><p><span data-ttu-id="50851-113">Использует пару заявлений DELETE и INSERT для каждой измененной строки.</span><span class="sxs-lookup"><span data-stu-id="50851-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50851-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="50851-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="50851-115">1</span><span class="sxs-lookup"><span data-stu-id="50851-115">1</span></span></p></td>
<td><p><span data-ttu-id="50851-116">Использует только столбец клавиши (ы) в пункте где.</span><span class="sxs-lookup"><span data-stu-id="50851-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50851-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="50851-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="50851-118">2</span><span class="sxs-lookup"><span data-stu-id="50851-118">2</span></span></p></td>
<td><p><span data-ttu-id="50851-119">Использует столбец клавиши (s) и все обновленные столбцы в пункте где.</span><span class="sxs-lookup"><span data-stu-id="50851-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50851-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="50851-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="50851-121">8 </span><span class="sxs-lookup"><span data-stu-id="50851-121">8</span></span></p></td>
<td><p><span data-ttu-id="50851-122">Использует только столбец timestamp, если это доступно (будет создавать ошибку времени запуска, если столбец timestamp не находится в наборе результатов).</span><span class="sxs-lookup"><span data-stu-id="50851-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50851-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="50851-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="50851-124">32</span><span class="sxs-lookup"><span data-stu-id="50851-124">32</span></span></p></td>
<td><p><span data-ttu-id="50851-125">Использует заявление UPDATE для каждой измененной строки.</span><span class="sxs-lookup"><span data-stu-id="50851-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

