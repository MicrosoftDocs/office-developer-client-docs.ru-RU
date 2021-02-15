---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1bc0d378428c00882c49f7783892ca2bf4d4638c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300695"
---
# <a name="recordcreateoptionsenum"></a><span data-ttu-id="ace87-102">RecordCreateOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="ace87-102">RecordCreateOptionsEnum</span></span>


<span data-ttu-id="ace87-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ace87-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ace87-104">Указывает, следует ли  открывать существующую запись  или новую запись, созданную для метода Open объекта [Record.](record-object-ado.md) [](open-method-ado-record.md)</span><span class="sxs-lookup"><span data-stu-id="ace87-104">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="ace87-105">Значения можно объединить с оператором AND.</span><span class="sxs-lookup"><span data-stu-id="ace87-105">The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ace87-106">Константа</span><span class="sxs-lookup"><span data-stu-id="ace87-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="ace87-107">Значение</span><span class="sxs-lookup"><span data-stu-id="ace87-107">Value</span></span></p></th>
<th><p><span data-ttu-id="ace87-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ace87-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ace87-109"><strong>adCreateCollection</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-109"><strong>adCreateCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="ace87-110">0x2000</span><span class="sxs-lookup"><span data-stu-id="ace87-110">0x2000</span></span></p></td>
<td><p><span data-ttu-id="ace87-111">Создает новую запись <strong>на</strong> узле, указанном с помощью параметра <em>Source,</em> вместо открытия существующей <strong>записи.</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-111">Creates a new <strong>Record</strong> at the node specified by <em>Source</em> parameter, instead of opening an existing <strong>Record</strong>.</span></span> <span data-ttu-id="ace87-112">Если источник указывает на существующий узел, возникает ошибка во время запуска, если только <strong>adCreateCollection</strong> не объединен с <strong>adOpenIfExists</strong> или <strong>adCreateOverwrite.</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-112">If the source points to an existing node, then a run-time error occurs, unless <strong>adCreateCollection</strong> is combined with <strong>adOpenIfExists</strong> or <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace87-113"><strong>adCreateNonCollection</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-113"><strong>adCreateNonCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="ace87-114">0</span><span class="sxs-lookup"><span data-stu-id="ace87-114">0</span></span></p></td>
<td><p><span data-ttu-id="ace87-115">Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">adSimpleRecord.</a></span><span class="sxs-lookup"><span data-stu-id="ace87-115">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adSimpleRecord</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace87-116"><strong>adCreateOverwrite</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-116"><strong>adCreateOverwrite</strong></span></span></p></td>
<td><p><span data-ttu-id="ace87-117">0x4000000</span><span class="sxs-lookup"><span data-stu-id="ace87-117">0x4000000</span></span></p></td>
<td><p><span data-ttu-id="ace87-118">Изменяет флаги создания <strong>adCreateCollection,</strong> <strong>adCreateNonCollection</strong>и <strong>adCreateStructDoc.</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-118">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="ace87-119">Если при или используется с этим значением и одним из значений флага создания, если <strong></strong> исходный URL-адрес указывает на существующий узел или <strong>запись,</strong>то существующая запись перезаписывается и создается новая.</span><span class="sxs-lookup"><span data-stu-id="ace87-119">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong>, then the existing <strong>Record</strong> is overwritten and a new one is created in its place.</span></span> <span data-ttu-id="ace87-120">Это значение нельзя использовать вместе с <strong>adOpenIfExists.</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-120">This value cannot be used together with <strong>adOpenIfExists</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace87-121"><strong>adCreateStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-121"><strong>adCreateStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="ace87-122">0x80000000</span><span class="sxs-lookup"><span data-stu-id="ace87-122">0x80000000</span></span></p></td>
<td><p><span data-ttu-id="ace87-123">Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">adStructDoc</a>вместо открытия существующей <strong>записи.</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-123">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adStructDoc</a>, instead of opening an existing <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ace87-124"><strong>adFailIfNotExists</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-124"><strong>adFailIfNotExists</strong></span></span></p></td>
<td><p><span data-ttu-id="ace87-125">–1</span><span class="sxs-lookup"><span data-stu-id="ace87-125">-1</span></span></p></td>
<td><p><span data-ttu-id="ace87-126">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ace87-126">Default.</span></span> <span data-ttu-id="ace87-127">Приводит к ошибке во время работы, <em>если источник</em> указывает на несуществующий узел.</span><span class="sxs-lookup"><span data-stu-id="ace87-127">Results in a run-time error if <em>Source</em> points to a non-existent node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ace87-128"><strong>adOpenIfExists</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-128"><strong>adOpenIfExists</strong></span></span></p></td>
<td><p><span data-ttu-id="ace87-129">0x2000000</span><span class="sxs-lookup"><span data-stu-id="ace87-129">0x2000000</span></span></p></td>
<td><p><span data-ttu-id="ace87-130">Изменяет флаги создания <strong>adCreateCollection,</strong> <strong>adCreateNonCollection</strong>и <strong>adCreateStructDoc.</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-130">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="ace87-131">Если при or используется с этим значением и одним из значений флага создания, если исходный URL-адрес указывает на существующий узел или объект <strong>Record,</strong> поставщик должен открыть существующую запись вместо создания новой. <strong></strong></span><span class="sxs-lookup"><span data-stu-id="ace87-131">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong> object, then the provider must open the existing <strong>Record</strong> instead of creating a new one.</span></span> <span data-ttu-id="ace87-132">Это значение нельзя использовать вместе с <strong>adCreateOverwrite.</strong></span><span class="sxs-lookup"><span data-stu-id="ace87-132">This value cannot be used together with <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="ace87-133">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="ace87-133">ADO/WFC equivalent</span></span>

<span data-ttu-id="ace87-134">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="ace87-134">These constants do not have ADO/WFC equivalents.</span></span>

