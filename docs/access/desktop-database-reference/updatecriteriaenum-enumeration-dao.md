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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28725961"
---
# <a name="updatecriteriaenum-enumeration-dao"></a><span data-ttu-id="496c0-102">Перечисление UpdateCriteriaEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="496c0-102">UpdateCriteriaEnum enumeration (DAO)</span></span>


<span data-ttu-id="496c0-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="496c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="496c0-104">Используется с методом **UpdateOptions** для указания способа создания пакета обновления.</span><span class="sxs-lookup"><span data-stu-id="496c0-104">Used with the **UpdateOptions** method to specify how a batch update is constructed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="496c0-105">Имя</span><span class="sxs-lookup"><span data-stu-id="496c0-105">Name</span></span></p></th>
<th><p><span data-ttu-id="496c0-106">Значение</span><span class="sxs-lookup"><span data-stu-id="496c0-106">Value</span></span></p></th>
<th><p><span data-ttu-id="496c0-107">Описание</span><span class="sxs-lookup"><span data-stu-id="496c0-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="496c0-108">dbCriteriaAllCols</span><span class="sxs-lookup"><span data-stu-id="496c0-108">dbCriteriaAllCols</span></span></p></td>
<td><p><span data-ttu-id="496c0-109">4</span><span class="sxs-lookup"><span data-stu-id="496c0-109">4</span></span></p></td>
<td><p><span data-ttu-id="496c0-110">Использует столбцы ключа и все столбцы в списке место предложение.</span><span class="sxs-lookup"><span data-stu-id="496c0-110">Uses the key column(s) and all the columns in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="496c0-111">dbCriteriaDeleteInsert</span><span class="sxs-lookup"><span data-stu-id="496c0-111">dbCriteriaDeleteInsert</span></span></p></td>
<td><p><span data-ttu-id="496c0-112">16</span><span class="sxs-lookup"><span data-stu-id="496c0-112">16</span></span></p></td>
<td><p><span data-ttu-id="496c0-113">Использует пару операторов INSERT и DELETE для каждой измененной строки.</span><span class="sxs-lookup"><span data-stu-id="496c0-113">Uses a pair of DELETE and INSERT statements for each modified row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="496c0-114">dbCriteriaKey</span><span class="sxs-lookup"><span data-stu-id="496c0-114">dbCriteriaKey</span></span></p></td>
<td><p><span data-ttu-id="496c0-115">1</span><span class="sxs-lookup"><span data-stu-id="496c0-115">1</span></span></p></td>
<td><p><span data-ttu-id="496c0-116">Используется только что ключевых столбцов в списке место предложение.</span><span class="sxs-lookup"><span data-stu-id="496c0-116">Uses just the key column(s) in the where clause.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="496c0-117">dbCriteriaModValues</span><span class="sxs-lookup"><span data-stu-id="496c0-117">dbCriteriaModValues</span></span></p></td>
<td><p><span data-ttu-id="496c0-118">2</span><span class="sxs-lookup"><span data-stu-id="496c0-118">2</span></span></p></td>
<td><p><span data-ttu-id="496c0-119">Использует столбцы ключа и всех обновленных столбцов в списке место предложение.</span><span class="sxs-lookup"><span data-stu-id="496c0-119">Uses the key column(s) and all updated columns in the where clause.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="496c0-120">dbCriteriaTimestamp</span><span class="sxs-lookup"><span data-stu-id="496c0-120">dbCriteriaTimestamp</span></span></p></td>
<td><p><span data-ttu-id="496c0-121">8</span><span class="sxs-lookup"><span data-stu-id="496c0-121">8</span></span></p></td>
<td><p><span data-ttu-id="496c0-122">Использует столбце метка времени, если он доступен (создаст ошибку времени выполнения при нет столбца timestamp в наборе результатов).</span><span class="sxs-lookup"><span data-stu-id="496c0-122">Uses just the timestamp column if available (will generate a run-time error if no timestamp column is in the result set).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="496c0-123">dbCriteriaUpdate</span><span class="sxs-lookup"><span data-stu-id="496c0-123">dbCriteriaUpdate</span></span></p></td>
<td><p><span data-ttu-id="496c0-124">32</span><span class="sxs-lookup"><span data-stu-id="496c0-124">32</span></span></p></td>
<td><p><span data-ttu-id="496c0-125">Инструкция UPDATE для каждой измененной строки.</span><span class="sxs-lookup"><span data-stu-id="496c0-125">Uses an UPDATE statement for each modified row.</span></span></p></td>
</tr>
</tbody>
</table>

