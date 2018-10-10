---
title: AllowNullsEnum (Справочник по для настольных баз данных Access)
TOCTitle: AllowNullsEnum
ms:assetid: 7bb42b38-6b3b-5930-b1d7-16323a3bdf37
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249515(v=office.15)
ms:contentKeyID: 48545819
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04e67584e0f0c2eeb5a12e34fdf98a84cc1da852
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481445"
---
# <a name="allownullsenum"></a><span data-ttu-id="634ab-102">AllowNullsEnum</span><span class="sxs-lookup"><span data-stu-id="634ab-102">AllowNullsEnum</span></span>


<span data-ttu-id="634ab-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="634ab-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="634ab-104">Указывает, индексированные записи с пустым значением.</span><span class="sxs-lookup"><span data-stu-id="634ab-104">Specifies whether records with null values are indexed.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="634ab-105">Константа</span><span class="sxs-lookup"><span data-stu-id="634ab-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="634ab-106">Значение</span><span class="sxs-lookup"><span data-stu-id="634ab-106">Value</span></span></p></th>
<th><p><span data-ttu-id="634ab-107">Описание</span><span class="sxs-lookup"><span data-stu-id="634ab-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="634ab-108"><strong>adIndexNullsAllow</strong></span><span class="sxs-lookup"><span data-stu-id="634ab-108"><strong>adIndexNullsAllow</strong></span></span></p></td>
<td><p><span data-ttu-id="634ab-109">0</span><span class="sxs-lookup"><span data-stu-id="634ab-109">0</span></span></p></td>
<td><p><span data-ttu-id="634ab-110">Индекс разрешает записей, в которых ключевые столбцы имеют значение null.</span><span class="sxs-lookup"><span data-stu-id="634ab-110">The index does allow entries in which the key columns are null.</span></span> <span data-ttu-id="634ab-111">Нулевое значение, введенное в столбце ключа, запись вставляется в индексе.</span><span class="sxs-lookup"><span data-stu-id="634ab-111">If a null value is entered in a key column, the entry is inserted into the index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634ab-112"><strong>adIndexNullsDisallow</strong></span><span class="sxs-lookup"><span data-stu-id="634ab-112"><strong>adIndexNullsDisallow</strong></span></span></p></td>
<td><p><span data-ttu-id="634ab-113">1</span><span class="sxs-lookup"><span data-stu-id="634ab-113">1</span></span></p></td>
<td><p><span data-ttu-id="634ab-114">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="634ab-114">Default.</span></span> <span data-ttu-id="634ab-115">Индекс не разрешает записей, в которых ключевые столбцы имеют значение null.</span><span class="sxs-lookup"><span data-stu-id="634ab-115">The index does not allow entries in which the key columns are null.</span></span> <span data-ttu-id="634ab-116">Нулевое значение, введенное в столбце ключа, произойдет ошибка.</span><span class="sxs-lookup"><span data-stu-id="634ab-116">If a null value is entered in a key column, an error will occur.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="634ab-117"><strong>adIndexNullsIgnore</strong></span><span class="sxs-lookup"><span data-stu-id="634ab-117"><strong>adIndexNullsIgnore</strong></span></span></p></td>
<td><p><span data-ttu-id="634ab-118">2</span><span class="sxs-lookup"><span data-stu-id="634ab-118">2</span></span></p></td>
<td><p><span data-ttu-id="634ab-119">Индекс не вставляет операции, содержащие значение null, ключи.</span><span class="sxs-lookup"><span data-stu-id="634ab-119">The index does not insert entries containing null keys.</span></span> <span data-ttu-id="634ab-120">Нулевое значение, введенное в столбце ключа, операция обрабатывается и ошибка не происходит.</span><span class="sxs-lookup"><span data-stu-id="634ab-120">If a null value is entered in a key column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="634ab-121"><strong>adIndexNullsIgnoreAny</strong></span><span class="sxs-lookup"><span data-stu-id="634ab-121"><strong>adIndexNullsIgnoreAny</strong></span></span></p></td>
<td><p><span data-ttu-id="634ab-122">4</span><span class="sxs-lookup"><span data-stu-id="634ab-122">4</span></span></p></td>
<td><p><span data-ttu-id="634ab-123">Индекс не вставляет записей, где некоторые ключевые столбец имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="634ab-123">The index does not insert entries where some key column has a null value.</span></span> <span data-ttu-id="634ab-124">Для индекса с несколькими столбцами ключей и нулевое значение, введенное в несколько столбцов, операция учитывается, и ошибка не происходит.</span><span class="sxs-lookup"><span data-stu-id="634ab-124">For an index having a multi-column key, if a null value is entered in some column, the entry is ignored and no error occurs.</span></span></p></td>
</tr>
</tbody>
</table>

