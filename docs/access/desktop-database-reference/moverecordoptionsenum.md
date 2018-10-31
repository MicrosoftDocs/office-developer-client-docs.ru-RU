---
title: MoveRecordOptionsEnum
TOCTitle: MoveRecordOptionsEnum
ms:assetid: 2785bca0-777c-a802-51d7-6f5cf0fb4210
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249039(v=office.15)
ms:contentKeyID: 48543842
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fc621f620a7d55571aa55296a4d294fff9566bf5
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862242"
---
# <a name="moverecordoptionsenum"></a><span data-ttu-id="09a55-102">MoveRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="09a55-102">MoveRecordOptionsEnum</span></span>


<span data-ttu-id="09a55-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="09a55-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="09a55-104">Задает поведение объекта [записи](record-object-ado.md) метод [MoveRecord](moverecord-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="09a55-104">Specifies the behavior of the [Record](record-object-ado.md) object [MoveRecord](moverecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="09a55-105">Константа</span><span class="sxs-lookup"><span data-stu-id="09a55-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="09a55-106">Значение</span><span class="sxs-lookup"><span data-stu-id="09a55-106">Value</span></span></p></th>
<th><p><span data-ttu-id="09a55-107">Описание</span><span class="sxs-lookup"><span data-stu-id="09a55-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09a55-108"><strong>adMoveUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="09a55-108"><strong>adMoveUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="09a55-109">-1</span><span class="sxs-lookup"><span data-stu-id="09a55-109">-1</span></span></p></td>
<td><p><span data-ttu-id="09a55-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="09a55-110">Default.</span></span> <span data-ttu-id="09a55-111">Выполняет операцию перемещения по умолчанию: операция не выполняется, если конечный файл или каталог уже существует, а операция обновляет ссылкам.</span><span class="sxs-lookup"><span data-stu-id="09a55-111">Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a55-112"><strong>adMoveOverWrite</strong></span><span class="sxs-lookup"><span data-stu-id="09a55-112"><strong>adMoveOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="09a55-113">1</span><span class="sxs-lookup"><span data-stu-id="09a55-113">1</span></span></p></td>
<td><p><span data-ttu-id="09a55-114">Перезапись файла или каталога назначения, даже в том случае, если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="09a55-114">Overwrites the destination file or directory, even if it already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09a55-115"><strong>adMoveDontUpdateLinks</strong></span><span class="sxs-lookup"><span data-stu-id="09a55-115"><strong>adMoveDontUpdateLinks</strong></span></span></p></td>
<td><p><span data-ttu-id="09a55-116">2</span><span class="sxs-lookup"><span data-stu-id="09a55-116">2</span></span></p></td>
<td><p><span data-ttu-id="09a55-117">Выполняется изменение поведения по умолчанию метод <strong>MoveRecord</strong> , не изменив ссылки гипертекста источника <strong>записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="09a55-117">Modifies the default behavior of <strong>MoveRecord</strong> method by not updating the hypertext links of the source <strong>Record</strong>.</span></span> <span data-ttu-id="09a55-118">Поведение по умолчанию зависит от возможностей поставщика.</span><span class="sxs-lookup"><span data-stu-id="09a55-118">The default behavior depends on the capabilities of the provider.</span></span> <span data-ttu-id="09a55-119">Операции перемещения обновляет ссылки, если поставщик поддерживает.</span><span class="sxs-lookup"><span data-stu-id="09a55-119">Move operation updates links if the provider is capable.</span></span> <span data-ttu-id="09a55-120">Если поставщик не удается исправить ссылки или если это значение не указано, перемещение успешно, даже если ссылки не исправлены.</span><span class="sxs-lookup"><span data-stu-id="09a55-120">If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09a55-121"><strong>adMoveAllowEmulation</strong></span><span class="sxs-lookup"><span data-stu-id="09a55-121"><strong>adMoveAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="09a55-122">4</span><span class="sxs-lookup"><span data-stu-id="09a55-122">4</span></span></p></td>
<td><p><span data-ttu-id="09a55-123">Запросы, что поставщик попытка моделировать move (с помощью загрузки, отправляемых операций и удаления).</span><span class="sxs-lookup"><span data-stu-id="09a55-123">Requests that the provider attempt to simulate the move (using download, upload, and delete operations).</span></span> <span data-ttu-id="09a55-124">Если попытка переместить <strong>записи</strong> не удается выполнить из-за конечный URL-адрес на другом сервере, или обслуживаемых другого поставщика, чем источник, это может привести к увеличению задержки или потерю данных, из-за возможности другого поставщика при перемещении ресурсы между поставщиками.</span><span class="sxs-lookup"><span data-stu-id="09a55-124">If the attempt to move the <strong>Record</strong> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="09a55-125">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="09a55-125">ADO/WFC equivalent</span></span>

<span data-ttu-id="09a55-126">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="09a55-126">These constants do not have ADO/WFC equivalents.</span></span>

