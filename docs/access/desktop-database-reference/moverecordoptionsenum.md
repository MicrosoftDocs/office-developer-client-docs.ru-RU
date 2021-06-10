---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5bd8196670513156011d69f08eacf790fa4a0a03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288674"
---
# <a name="moverecordoptionsenum"></a><span data-ttu-id="e45b5-102">MoveRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="e45b5-102">MoveRecordOptionsEnum</span></span>


<span data-ttu-id="e45b5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e45b5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e45b5-104">Указывает поведение метода [Объекта](record-object-ado.md) [Записи MoveRecord.](moverecord-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="e45b5-104">Specifies the behavior of the [Record](record-object-ado.md) object [MoveRecord](moverecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e45b5-105">Константа</span><span class="sxs-lookup"><span data-stu-id="e45b5-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="e45b5-106">Значение</span><span class="sxs-lookup"><span data-stu-id="e45b5-106">Value</span></span></p></th>
<th><p><span data-ttu-id="e45b5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="e45b5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e45b5-108"><strong>adMoveUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="e45b5-108"><strong>adMoveUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="e45b5-109">–1</span><span class="sxs-lookup"><span data-stu-id="e45b5-109">-1</span></span></p></td>
<td><p><span data-ttu-id="e45b5-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e45b5-110">Default.</span></span> <span data-ttu-id="e45b5-111">Выполняет операцию перемещения по умолчанию: операция не выполняется, если файл назначения или каталог уже существует, и операция обновляет ссылки на гипертекст.</span><span class="sxs-lookup"><span data-stu-id="e45b5-111">Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e45b5-112"><strong>adMoveOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="e45b5-112"><strong>adMoveOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="e45b5-113">1</span><span class="sxs-lookup"><span data-stu-id="e45b5-113">1</span></span></p></td>
<td><p><span data-ttu-id="e45b5-114">Переоценка файла назначения или каталога, даже если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="e45b5-114">Overwrites the destination file or directory, even if it already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e45b5-115"><strong>adMoveDontUpdateLinks</strong></span><span class="sxs-lookup"><span data-stu-id="e45b5-115"><strong>adMoveDontUpdateLinks</strong></span></span></p></td>
<td><p><span data-ttu-id="e45b5-116">2</span><span class="sxs-lookup"><span data-stu-id="e45b5-116">2</span></span></p></td>
<td><p><span data-ttu-id="e45b5-117">Изменяет поведение метода <strong>MoveRecord</strong> по умолчанию, не обновляя гипертекстовых ссылок исходных <strong>записей.</strong></span><span class="sxs-lookup"><span data-stu-id="e45b5-117">Modifies the default behavior of <strong>MoveRecord</strong> method by not updating the hypertext links of the source <strong>Record</strong>.</span></span> <span data-ttu-id="e45b5-118">Поведение по умолчанию зависит от возможностей поставщика.</span><span class="sxs-lookup"><span data-stu-id="e45b5-118">The default behavior depends on the capabilities of the provider.</span></span> <span data-ttu-id="e45b5-119">Перемещение ссылок на обновления операций, если поставщик способен.</span><span class="sxs-lookup"><span data-stu-id="e45b5-119">Move operation updates links if the provider is capable.</span></span> <span data-ttu-id="e45b5-120">Если поставщик не может исправить ссылки или если это значение не указано, перемещение успешно, даже если ссылки не исправлены.</span><span class="sxs-lookup"><span data-stu-id="e45b5-120">If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e45b5-121"><strong>adMoveAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="e45b5-121"><strong>adMoveAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="e45b5-122">4 </span><span class="sxs-lookup"><span data-stu-id="e45b5-122">4</span></span></p></td>
<td><p><span data-ttu-id="e45b5-123">Запросы, которые поставщик пытается имитировать перемещение (с помощью скачивания, загрузки и удаления операций).</span><span class="sxs-lookup"><span data-stu-id="e45b5-123">Requests that the provider attempt to simulate the move (using download, upload, and delete operations).</span></span> <span data-ttu-id="e45b5-124">Если попытка переместить <strong></strong> запись не удалась из-за того, что URL-адрес назначения находится на другом сервере или обслужен другим поставщиком, чем источник, это может привести к увеличению задержки или потере данных из-за различных возможностей поставщика при перемещении ресурсов между поставщиками.</span><span class="sxs-lookup"><span data-stu-id="e45b5-124">If the attempt to move the <strong>Record</strong> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="e45b5-125">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="e45b5-125">ADO/WFC equivalent</span></span>

<span data-ttu-id="e45b5-126">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="e45b5-126">These constants do not have ADO/WFC equivalents.</span></span>

