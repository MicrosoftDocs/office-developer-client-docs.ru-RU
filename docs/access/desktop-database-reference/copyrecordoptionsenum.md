---
title: CopyRecordOptionsEnum
TOCTitle: CopyRecordOptionsEnum
ms:assetid: ab9426e9-0e4e-6c85-43cf-e4a205a7c4c0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249795(v=office.15)
ms:contentKeyID: 48546975
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: eb1637d1757a8507c6b6abb2a0c71867e3d1177b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703848"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="e69ff-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="e69ff-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="e69ff-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e69ff-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e69ff-104">Задает поведение метода [CopyRecord](copyrecord-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="e69ff-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e69ff-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e69ff-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e69ff-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e69ff-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e69ff-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e69ff-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e69ff-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="e69ff-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="e69ff-109">4</span><span class="sxs-lookup"><span data-stu-id="e69ff-109">4</span></span></p></td>
<td><p><span data-ttu-id="e69ff-110">Указывает, что поставщик <em>источника</em> пытается моделирования копии, с помощью загрузки и отправьте операции, если этот метод не удается выполнить из-за <em>назначения</em> , на другом сервере, или обслуживаемых другого поставщика, чем <em>источник</em>.</span><span class="sxs-lookup"><span data-stu-id="e69ff-110">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>.</span></span> <span data-ttu-id="e69ff-111">Обратите внимание, что разные возможности поставщика может препятствовать производительности или потери данных.</span><span class="sxs-lookup"><span data-stu-id="e69ff-111">Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e69ff-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="e69ff-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="e69ff-113">2</span><span class="sxs-lookup"><span data-stu-id="e69ff-113">2</span></span></p></td>
<td><p><span data-ttu-id="e69ff-114">Копирует текущий каталог, но ни один из его подкаталогов в место назначения.</span><span class="sxs-lookup"><span data-stu-id="e69ff-114">Copies the current directory, but none of its subdirectories, to the destination.</span></span> <span data-ttu-id="e69ff-115">Операция копирования не рекурсивный.</span><span class="sxs-lookup"><span data-stu-id="e69ff-115">The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e69ff-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="e69ff-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="e69ff-117">1</span><span class="sxs-lookup"><span data-stu-id="e69ff-117">1</span></span></p></td>
<td><p><span data-ttu-id="e69ff-118">Перезапись файла или папки <em>назначения</em> указывает на существующий файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="e69ff-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e69ff-119"><strong>adCopyUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="e69ff-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="e69ff-120">–1</span><span class="sxs-lookup"><span data-stu-id="e69ff-120">-1</span></span></p></td>
<td><p><span data-ttu-id="e69ff-121">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e69ff-121">Default.</span></span> <span data-ttu-id="e69ff-122">Выполняет операцию копирования по умолчанию: завершится неудачно, если конечный файл или каталог уже существует и рекурсивно копирует операции.</span><span class="sxs-lookup"><span data-stu-id="e69ff-122">Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e69ff-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e69ff-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="e69ff-124">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="e69ff-124">These constants do not have ADO/WFC equivalents.</span></span>

