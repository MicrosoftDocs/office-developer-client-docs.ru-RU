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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295487"
---
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="41796-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="41796-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="41796-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="41796-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="41796-104">Указывает поведение метода [CopyRecord.](copyrecord-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="41796-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="41796-105">Константа</span><span class="sxs-lookup"><span data-stu-id="41796-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="41796-106">Значение</span><span class="sxs-lookup"><span data-stu-id="41796-106">Value</span></span></p></th>
<th><p><span data-ttu-id="41796-107">Описание</span><span class="sxs-lookup"><span data-stu-id="41796-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="41796-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="41796-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="41796-109">4 </span><span class="sxs-lookup"><span data-stu-id="41796-109">4</span></span></p></td>
<td><p><span data-ttu-id="41796-110">Указывает, что <em></em> поставщик источника пытается смоделировать копию с помощью операций загрузки и отправки, если этот метод не удается из-за того, что назначение находится на другом сервере или служба службы отличается от source <em>.</em> <em></em></span><span class="sxs-lookup"><span data-stu-id="41796-110">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>.</span></span> <span data-ttu-id="41796-111">Обратите внимание, что различные возможности поставщиков могут помешать производительности или потерять данные.</span><span class="sxs-lookup"><span data-stu-id="41796-111">Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41796-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="41796-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="41796-113">2 </span><span class="sxs-lookup"><span data-stu-id="41796-113">2</span></span></p></td>
<td><p><span data-ttu-id="41796-114">Копирует текущий каталог, но ни один из его подкадиректоров, в место назначения.</span><span class="sxs-lookup"><span data-stu-id="41796-114">Copies the current directory, but none of its subdirectories, to the destination.</span></span> <span data-ttu-id="41796-115">Операция копирования не является рекурсивной.</span><span class="sxs-lookup"><span data-stu-id="41796-115">The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="41796-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="41796-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="41796-117">1 </span><span class="sxs-lookup"><span data-stu-id="41796-117">1</span></span></p></td>
<td><p><span data-ttu-id="41796-118">Переоценка файла или каталога, если пункт <em>назначения</em> указывает на существующий файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="41796-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="41796-119"><strong>adCopyUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="41796-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="41796-120">–1</span><span class="sxs-lookup"><span data-stu-id="41796-120">-1</span></span></p></td>
<td><p><span data-ttu-id="41796-121">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41796-121">Default.</span></span> <span data-ttu-id="41796-122">Выполняет операцию копирования по умолчанию: операция не выполняется, если файл назначения или каталог уже существует, а операция рекурсивно копируется.</span><span class="sxs-lookup"><span data-stu-id="41796-122">Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="41796-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="41796-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="41796-124">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="41796-124">These constants do not have ADO/WFC equivalents.</span></span>

