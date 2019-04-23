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
# <a name="moverecordoptionsenum"></a><span data-ttu-id="be0fa-102">MoveRecordOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="be0fa-102">MoveRecordOptionsEnum</span></span>


<span data-ttu-id="be0fa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="be0fa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be0fa-104">Задает поведение метода [MoveRecord](moverecord-method-ado.md) объекта [Record](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="be0fa-104">Specifies the behavior of the [Record](record-object-ado.md) object [MoveRecord](moverecord-method-ado.md) method.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="be0fa-105">Константа</span><span class="sxs-lookup"><span data-stu-id="be0fa-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="be0fa-106">Значение</span><span class="sxs-lookup"><span data-stu-id="be0fa-106">Value</span></span></p></th>
<th><p><span data-ttu-id="be0fa-107">Описание</span><span class="sxs-lookup"><span data-stu-id="be0fa-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="be0fa-108"><strong>АдмовеунспеЦифиед</strong></span><span class="sxs-lookup"><span data-stu-id="be0fa-108"><strong>adMoveUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="be0fa-109">–1</span><span class="sxs-lookup"><span data-stu-id="be0fa-109">-1</span></span></p></td>
<td><p><span data-ttu-id="be0fa-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="be0fa-110">Default.</span></span> <span data-ttu-id="be0fa-111">Выполняет операцию перемещения по умолчанию: операция завершается с ошибкой, если конечный файл или каталог уже существует, а операция обновляет гипертекстовые ссылки.</span><span class="sxs-lookup"><span data-stu-id="be0fa-111">Performs the default move operation: The operation fails if the destination file or directory already exists, and the operation updates hypertext links.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be0fa-112"><strong>Адмовеоверврите</strong></span><span class="sxs-lookup"><span data-stu-id="be0fa-112"><strong>adMoveOverWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="be0fa-113">1,1</span><span class="sxs-lookup"><span data-stu-id="be0fa-113">1</span></span></p></td>
<td><p><span data-ttu-id="be0fa-114">Перезаписывает конечный файл или каталог, даже если он уже существует.</span><span class="sxs-lookup"><span data-stu-id="be0fa-114">Overwrites the destination file or directory, even if it already exists.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="be0fa-115"><strong>Адмоведонтупдателинкс</strong></span><span class="sxs-lookup"><span data-stu-id="be0fa-115"><strong>adMoveDontUpdateLinks</strong></span></span></p></td>
<td><p><span data-ttu-id="be0fa-116">2</span><span class="sxs-lookup"><span data-stu-id="be0fa-116">2</span></span></p></td>
<td><p><span data-ttu-id="be0fa-117">Изменяет поведение метода <strong>MoveRecord</strong> по умолчанию, не обновляя гипертекстовые ссылки исходной <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="be0fa-117">Modifies the default behavior of <strong>MoveRecord</strong> method by not updating the hypertext links of the source <strong>Record</strong>.</span></span> <span data-ttu-id="be0fa-118">Поведение по умолчанию зависит от возможностей поставщика.</span><span class="sxs-lookup"><span data-stu-id="be0fa-118">The default behavior depends on the capabilities of the provider.</span></span> <span data-ttu-id="be0fa-119">Операция перемещения обновляет ссылки, если поставщик поддерживает эту возможность.</span><span class="sxs-lookup"><span data-stu-id="be0fa-119">Move operation updates links if the provider is capable.</span></span> <span data-ttu-id="be0fa-120">Если поставщик не может исправить ссылки или это значение не указано, то перемещение выполняется, даже если ссылки не были исправлены.</span><span class="sxs-lookup"><span data-stu-id="be0fa-120">If the provider cannot fix links or if this value is not specified, then the move succeeds even when links have not been fixed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="be0fa-121"><strong>Адмовеалловемулатион</strong></span><span class="sxs-lookup"><span data-stu-id="be0fa-121"><strong>adMoveAllowEmulation</strong></span></span></p></td>
<td><p><span data-ttu-id="be0fa-122">SP4</span><span class="sxs-lookup"><span data-stu-id="be0fa-122">4</span></span></p></td>
<td><p><span data-ttu-id="be0fa-123">ЗаПрашивает, чтобы поставщик пытался имитировать перемещение (с помощью операций скачивания, отправки и удаления).</span><span class="sxs-lookup"><span data-stu-id="be0fa-123">Requests that the provider attempt to simulate the move (using download, upload, and delete operations).</span></span> <span data-ttu-id="be0fa-124">Если не удается переместить <strong>запись</strong> , так как конечный URL-адрес находится на другом сервере или обслуживается другим поставщиком, чем исходный, это может привести к увеличению задержки или потере данных из-за различных возможностей поставщика при перемещении ресурсов. между поставщиками.</span><span class="sxs-lookup"><span data-stu-id="be0fa-124">If the attempt to move the <strong>Record</strong> fails because the destination URL is on a different server or serviced by a different provider than the source, this may cause increased latency or data loss, due to different provider capabilities when moving resources between providers.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="be0fa-125">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="be0fa-125">ADO/WFC equivalent</span></span>

<span data-ttu-id="be0fa-126">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="be0fa-126">These constants do not have ADO/WFC equivalents.</span></span>

