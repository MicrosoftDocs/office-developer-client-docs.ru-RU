---
title: RecordCreateOptionsEnum
TOCTitle: RecordCreateOptionsEnum
ms:assetid: 153dc8ff-680c-1482-d386-4c4b33ffc589
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248917(v=office.15)
ms:contentKeyID: 48543405
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b3315fc0b6d72689e36530b7e7daf7b94732459f
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481571"
---
# <a name="recordcreateoptionsenum"></a><span data-ttu-id="c214a-102">RecordCreateOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="c214a-102">RecordCreateOptionsEnum</span></span>


<span data-ttu-id="c214a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="c214a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="c214a-104">Указывает, должен быть открыт существующей **записи** или создана новая **запись** для объекта [записи](record-object-ado.md) метода [Open](open-method-ado-record.md) .</span><span class="sxs-lookup"><span data-stu-id="c214a-104">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="c214a-105">Значения может использоваться совместно с оператора AND.</span><span class="sxs-lookup"><span data-stu-id="c214a-105">The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="c214a-106">Константа</span><span class="sxs-lookup"><span data-stu-id="c214a-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="c214a-107">Значение</span><span class="sxs-lookup"><span data-stu-id="c214a-107">Value</span></span></p></th>
<th><p><span data-ttu-id="c214a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="c214a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c214a-109"><strong>adCreateCollection</strong></span><span class="sxs-lookup"><span data-stu-id="c214a-109"><strong>adCreateCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="c214a-110">0x2000</span><span class="sxs-lookup"><span data-stu-id="c214a-110">0x2000</span></span></p></td>
<td><p><span data-ttu-id="c214a-111">Создает новую <strong>запись</strong> в узле, заданное параметром <em>источника</em> , не открывая существующей <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="c214a-111">Creates a new <strong>Record</strong> at the node specified by <em>Source</em> parameter, instead of opening an existing <strong>Record</strong>.</span></span> <span data-ttu-id="c214a-112">Если источник указывает на существующий узел, во время выполнения возникает ошибка, если не <strong>adCreateCollection</strong> в сочетании с <strong>adOpenIfExists</strong> или <strong>adCreateOverwrite</strong>.</span><span class="sxs-lookup"><span data-stu-id="c214a-112">If the source points to an existing node, then a run-time error occurs, unless <strong>adCreateCollection</strong> is combined with <strong>adOpenIfExists</strong> or <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c214a-113"><strong>adCreateNonCollection</strong></span><span class="sxs-lookup"><span data-stu-id="c214a-113"><strong>adCreateNonCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="c214a-114">0</span><span class="sxs-lookup"><span data-stu-id="c214a-114">0</span></span></p></td>
<td><p><span data-ttu-id="c214a-115">Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">adSimpleRecord</a>.</span><span class="sxs-lookup"><span data-stu-id="c214a-115">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adSimpleRecord</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c214a-116"><strong>adCreateOverwrite</strong></span><span class="sxs-lookup"><span data-stu-id="c214a-116"><strong>adCreateOverwrite</strong></span></span></p></td>
<td><p><span data-ttu-id="c214a-117">0x4000000</span><span class="sxs-lookup"><span data-stu-id="c214a-117">0x4000000</span></span></p></td>
<td><p><span data-ttu-id="c214a-118">Изменяет флаги создания <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>и <strong>adCreateStructDoc</strong>.</span><span class="sxs-lookup"><span data-stu-id="c214a-118">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="c214a-119">Когда или будет использоваться с этим значением и одно из значений флаг создания, если источник указывает URL-адрес существующего узла или <strong>записи</strong>, а затем перезаписать существующие <strong>записи</strong> и на его месте создается новый.</span><span class="sxs-lookup"><span data-stu-id="c214a-119">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong>, then the existing <strong>Record</strong> is overwritten and a new one is created in its place.</span></span> <span data-ttu-id="c214a-120">Это значение не может использоваться вместе с <strong>adOpenIfExists</strong>.</span><span class="sxs-lookup"><span data-stu-id="c214a-120">This value cannot be used together with <strong>adOpenIfExists</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c214a-121"><strong>adCreateStructDoc</strong></span><span class="sxs-lookup"><span data-stu-id="c214a-121"><strong>adCreateStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="c214a-122">0x80000000</span><span class="sxs-lookup"><span data-stu-id="c214a-122">0x80000000</span></span></p></td>
<td><p><span data-ttu-id="c214a-123">Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">adStructDoc</a>, не открывая существующей <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="c214a-123">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adStructDoc</a>, instead of opening an existing <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c214a-124"><strong>adFailIfNotExists</strong></span><span class="sxs-lookup"><span data-stu-id="c214a-124"><strong>adFailIfNotExists</strong></span></span></p></td>
<td><p><span data-ttu-id="c214a-125">-1</span><span class="sxs-lookup"><span data-stu-id="c214a-125">-1</span></span></p></td>
<td><p><span data-ttu-id="c214a-126">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c214a-126">Default.</span></span> <span data-ttu-id="c214a-127">Приводит к ошибке времени выполнения, если <em>источник</em> указывает на несуществующий узел.</span><span class="sxs-lookup"><span data-stu-id="c214a-127">Results in a run-time error if <em>Source</em> points to a non-existent node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c214a-128"><strong>adOpenIfExists</strong></span><span class="sxs-lookup"><span data-stu-id="c214a-128"><strong>adOpenIfExists</strong></span></span></p></td>
<td><p><span data-ttu-id="c214a-129">0x2000000</span><span class="sxs-lookup"><span data-stu-id="c214a-129">0x2000000</span></span></p></td>
<td><p><span data-ttu-id="c214a-130">Изменяет флаги создания <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>и <strong>adCreateStructDoc</strong>.</span><span class="sxs-lookup"><span data-stu-id="c214a-130">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="c214a-131">Когда или будет использоваться с этим значением и одно из значений флаг создания, если источник указывает URL-адрес существующего узла или объект <strong>записи</strong> , а затем поставщика необходимо открыть существующей <strong>записи</strong> вместо создания нового.</span><span class="sxs-lookup"><span data-stu-id="c214a-131">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong> object, then the provider must open the existing <strong>Record</strong> instead of creating a new one.</span></span> <span data-ttu-id="c214a-132">Это значение не может использоваться вместе с <strong>adCreateOverwrite</strong>.</span><span class="sxs-lookup"><span data-stu-id="c214a-132">This value cannot be used together with <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="c214a-133">**Эквивалент ADO/WFC**</span><span class="sxs-lookup"><span data-stu-id="c214a-133">**ADO/WFC Equivalent**</span></span>

<span data-ttu-id="c214a-134">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="c214a-134">These constants do not have ADO/WFC equivalents.</span></span>

