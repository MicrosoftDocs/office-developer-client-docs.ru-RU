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
# <a name="copyrecordoptionsenum"></a><span data-ttu-id="4bc66-102">CopyRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="4bc66-102">CopyRecordOptionsEnum</span></span>


<span data-ttu-id="4bc66-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4bc66-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4bc66-104">Указывает поведение метода [CopyRecord.](copyrecord-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="4bc66-104">Specifies the behavior of the [CopyRecord](copyrecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4bc66-105">Константа</span><span class="sxs-lookup"><span data-stu-id="4bc66-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="4bc66-106">Значение</span><span class="sxs-lookup"><span data-stu-id="4bc66-106">Value</span></span></p></th>
<th><p><span data-ttu-id="4bc66-107">Описание</span><span class="sxs-lookup"><span data-stu-id="4bc66-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4bc66-108"><strong>adCopyAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="4bc66-108"><strong>adCopyAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="4bc66-109">4 </span><span class="sxs-lookup"><span data-stu-id="4bc66-109">4</span></span></p></td>
<td><p><span data-ttu-id="4bc66-110">Указывает, что <em></em> поставщик исходных данных пытается смоделировать копию с помощью операций загрузки и загрузки, если этот метод не удается из-за того, что <em>Destination</em> находится на другом сервере или находится на службе у другого поставщика, чем <em>Source</em>.</span><span class="sxs-lookup"><span data-stu-id="4bc66-110">Indicates that the <em>Source</em> provider attempts to simulate the copy using download and upload operations if this method fails due to <em>Destination</em> being on a different server or is serviced by a different provider than <em>Source</em>.</span></span> <span data-ttu-id="4bc66-111">Обратите внимание, что различные возможности поставщика могут препятствовать производительности или терять данные.</span><span class="sxs-lookup"><span data-stu-id="4bc66-111">Note that differing provider capabilities may hamper performance or lose data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bc66-112"><strong>adCopyNonRecursive</strong></span><span class="sxs-lookup"><span data-stu-id="4bc66-112"><strong>adCopyNonRecursive</strong></span></span></p></td>
<td><p><span data-ttu-id="4bc66-113">2</span><span class="sxs-lookup"><span data-stu-id="4bc66-113">2</span></span></p></td>
<td><p><span data-ttu-id="4bc66-114">Копирует текущий каталог, но ни один из его поднаправлений в пункт назначения.</span><span class="sxs-lookup"><span data-stu-id="4bc66-114">Copies the current directory, but none of its subdirectories, to the destination.</span></span> <span data-ttu-id="4bc66-115">Операция копирования не является повторяемой.</span><span class="sxs-lookup"><span data-stu-id="4bc66-115">The copy operation is not recursive.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4bc66-116"><strong>adCopyOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="4bc66-116"><strong>adCopyOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="4bc66-117">1</span><span class="sxs-lookup"><span data-stu-id="4bc66-117">1</span></span></p></td>
<td><p><span data-ttu-id="4bc66-118">Переоценка файла или каталога, если <em>пункт Назначения</em> указывает на существующий файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="4bc66-118">Overwrites the file or directory if the <em>Destination</em> points to an existing file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4bc66-119"><strong>adCopyUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="4bc66-119"><strong>adCopyUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="4bc66-120">–1</span><span class="sxs-lookup"><span data-stu-id="4bc66-120">-1</span></span></p></td>
<td><p><span data-ttu-id="4bc66-121">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4bc66-121">Default.</span></span> <span data-ttu-id="4bc66-122">Выполняет операцию копирования по умолчанию: операция сбой, если файл назначения или каталог уже существует, и операция копирует повторно.</span><span class="sxs-lookup"><span data-stu-id="4bc66-122">Performs the default copy operation: The operation fails if the destination file or directory already exists, and the operation copies recursively.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="4bc66-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="4bc66-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="4bc66-124">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="4bc66-124">These constants do not have ADO/WFC equivalents.</span></span>

