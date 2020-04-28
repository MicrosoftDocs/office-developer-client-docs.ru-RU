---
title: Перечисление UpdateCriteriaEnum (DAO)
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
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="bc9e8-102">Перечисление UpdateCriteriaEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="bc9e8-102">UpdateCriteriaEnum enumeration (DAO)</span></span>


<span data-ttu-id="bc9e8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bc9e8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc9e8-104">Используется с методом **UpdateOptions** для указания способа создания пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bc9e8-105">Имя</span><span class="sxs-lookup"><span data-stu-id="bc9e8-105">Name</span></span></p></th>
<th><p><span data-ttu-id="bc9e8-106">Значение</span><span class="sxs-lookup"><span data-stu-id="bc9e8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="bc9e8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="bc9e8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc9e8-108">дбкритериааллколс</span><span class="sxs-lookup"><span data-stu-id="bc9e8-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-109">4 </span><span class="sxs-lookup"><span data-stu-id="bc9e8-109">4</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-110">Использует ключевые столбцы и все столбцы в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc9e8-111">дбкритериаделетеинсерт</span><span class="sxs-lookup"><span data-stu-id="bc9e8-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-112">16 </span><span class="sxs-lookup"><span data-stu-id="bc9e8-112">16</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-113">Использует сочетание операторов DELETE и INSERT для каждой измененной строки.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc9e8-114">дбкритериакэй</span><span class="sxs-lookup"><span data-stu-id="bc9e8-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-115">1,1</span><span class="sxs-lookup"><span data-stu-id="bc9e8-115">1</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-116">Использует только ключевые столбцы в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc9e8-117">дбкритериамодвалуес</span><span class="sxs-lookup"><span data-stu-id="bc9e8-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-118">2</span><span class="sxs-lookup"><span data-stu-id="bc9e8-118">2</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-119">Использует ключевые столбцы и все обновленные столбцы в предложении WHERE.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc9e8-120">дбкритериатиместамп</span><span class="sxs-lookup"><span data-stu-id="bc9e8-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-121">8 </span><span class="sxs-lookup"><span data-stu-id="bc9e8-121">8</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-122">Использует только столбец timestamp (если он доступен) (при отсутствии столбца timestamp в наборе результатов будет создано сообщение об ошибке во время выполнения).</span><span class="sxs-lookup"><span data-stu-id="bc9e8-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc9e8-123">дбкритериаупдате</span><span class="sxs-lookup"><span data-stu-id="bc9e8-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-124">32</span><span class="sxs-lookup"><span data-stu-id="bc9e8-124">32</span></span></p></td>
<td><p><span data-ttu-id="bc9e8-125">Использует инструкцию UPDATE для каждой измененной строки.</span><span class="sxs-lookup"><span data-stu-id="bc9e8-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

