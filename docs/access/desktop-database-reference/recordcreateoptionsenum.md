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
# <a name="recordcreateoptionsenum"></a><span data-ttu-id="49798-102">RecordCreateOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="49798-102">RecordCreateOptionsEnum</span></span>


<span data-ttu-id="49798-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="49798-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="49798-104">Указывает, следует ли открыть существующую **запись** или создать новую **запись** для метода [Open](open-method-ado-record.md) объекта [Record](record-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="49798-104">Specifies whether an existing **Record** should be opened or a new **Record** created for the [Record](record-object-ado.md) object [Open](open-method-ado-record.md) method.</span></span> <span data-ttu-id="49798-105">Значения можно сочетать с помощью оператора AND.</span><span class="sxs-lookup"><span data-stu-id="49798-105">The values can be combined with an AND operator.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="49798-106">Константа</span><span class="sxs-lookup"><span data-stu-id="49798-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="49798-107">Значение</span><span class="sxs-lookup"><span data-stu-id="49798-107">Value</span></span></p></th>
<th><p><span data-ttu-id="49798-108">Описание</span><span class="sxs-lookup"><span data-stu-id="49798-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="49798-109"><strong>Адкреатеколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="49798-109"><strong>adCreateCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="49798-110">0x2000</span><span class="sxs-lookup"><span data-stu-id="49798-110">0x2000</span></span></p></td>
<td><p><span data-ttu-id="49798-111">Создает новую <strong>запись</strong> в узле, указанном с помощью параметра <em>Source</em> , вместо того, чтобы открывать существующую <strong>запись</strong>.</span><span class="sxs-lookup"><span data-stu-id="49798-111">Creates a new <strong>Record</strong> at the node specified by <em>Source</em> parameter, instead of opening an existing <strong>Record</strong>.</span></span> <span data-ttu-id="49798-112">Если источник указывает на существующий узел, возникнет ошибка во время выполнения, если <strong>адкреатеколлектион</strong> не объединен с <strong>адопенифексистс</strong> или <strong>адкреатеоверврите</strong>.</span><span class="sxs-lookup"><span data-stu-id="49798-112">If the source points to an existing node, then a run-time error occurs, unless <strong>adCreateCollection</strong> is combined with <strong>adOpenIfExists</strong> or <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49798-113"><strong>Адкреатенонколлектион</strong></span><span class="sxs-lookup"><span data-stu-id="49798-113"><strong>adCreateNonCollection</strong></span></span></p></td>
<td><p><span data-ttu-id="49798-114">нуль</span><span class="sxs-lookup"><span data-stu-id="49798-114">0</span></span></p></td>
<td><p><span data-ttu-id="49798-115">Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">адсимплерекорд</a>.</span><span class="sxs-lookup"><span data-stu-id="49798-115">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adSimpleRecord</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49798-116"><strong>Адкреатеоверврите</strong></span><span class="sxs-lookup"><span data-stu-id="49798-116"><strong>adCreateOverwrite</strong></span></span></p></td>
<td><p><span data-ttu-id="49798-117">0x4000000</span><span class="sxs-lookup"><span data-stu-id="49798-117">0x4000000</span></span></p></td>
<td><p><span data-ttu-id="49798-118">Изменяет флаги создания <strong>адкреатеколлектион</strong>, <strong>адкреатенонколлектион</strong>и <strong>адкреатеструктдок</strong>.</span><span class="sxs-lookup"><span data-stu-id="49798-118">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="49798-119">Когда или используется с этим значением и одним из значений флагов создания, если URL-адрес источника указывает на существующий узел или <strong>запись</strong>, то существующая <strong>запись</strong> перезаписывается, а вместо нее создается новая.</span><span class="sxs-lookup"><span data-stu-id="49798-119">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong>, then the existing <strong>Record</strong> is overwritten and a new one is created in its place.</span></span> <span data-ttu-id="49798-120">Это значение не может использоваться вместе с <strong>адопенифексистс</strong>.</span><span class="sxs-lookup"><span data-stu-id="49798-120">This value cannot be used together with <strong>adOpenIfExists</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49798-121"><strong>Адкреатеструктдок</strong></span><span class="sxs-lookup"><span data-stu-id="49798-121"><strong>adCreateStructDoc</strong></span></span></p></td>
<td><p><span data-ttu-id="49798-122">0x80000000</span><span class="sxs-lookup"><span data-stu-id="49798-122">0x80000000</span></span></p></td>
<td><p><span data-ttu-id="49798-123">Создает новую <strong>запись</strong> типа <a href="recordtypeenum.md">адструктдок</a>, а не открывает существующую <strong>запись</strong>.</span><span class="sxs-lookup"><span data-stu-id="49798-123">Creates a new <strong>Record</strong> of type <a href="recordtypeenum.md">adStructDoc</a>, instead of opening an existing <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="49798-124"><strong>Адфаилифнотексистс</strong></span><span class="sxs-lookup"><span data-stu-id="49798-124"><strong>adFailIfNotExists</strong></span></span></p></td>
<td><p><span data-ttu-id="49798-125">–1</span><span class="sxs-lookup"><span data-stu-id="49798-125">-1</span></span></p></td>
<td><p><span data-ttu-id="49798-126">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="49798-126">Default.</span></span> <span data-ttu-id="49798-127">Приводит к ошибке во время выполнения, если <em>источник</em> указывает на несуществующий узел.</span><span class="sxs-lookup"><span data-stu-id="49798-127">Results in a run-time error if <em>Source</em> points to a non-existent node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="49798-128"><strong>Адопенифексистс</strong></span><span class="sxs-lookup"><span data-stu-id="49798-128"><strong>adOpenIfExists</strong></span></span></p></td>
<td><p><span data-ttu-id="49798-129">0x2000000</span><span class="sxs-lookup"><span data-stu-id="49798-129">0x2000000</span></span></p></td>
<td><p><span data-ttu-id="49798-130">Изменяет флаги создания <strong>адкреатеколлектион</strong>, <strong>адкреатенонколлектион</strong>и <strong>адкреатеструктдок</strong>.</span><span class="sxs-lookup"><span data-stu-id="49798-130">Modifies the creation flags <strong>adCreateCollection</strong>, <strong>adCreateNonCollection</strong>, and <strong>adCreateStructDoc</strong>.</span></span> <span data-ttu-id="49798-131">Когда или используется с этим значением и одним из значений флагов создания, если URL-адрес источника указывает на существующий узел или объект <strong>Record</strong> , то поставщик должен открыть существующую <strong>запись</strong> вместо создания новой.</span><span class="sxs-lookup"><span data-stu-id="49798-131">When OR is used with this value and one of the creation flag values, if the source URL points to an existing node or <strong>Record</strong> object, then the provider must open the existing <strong>Record</strong> instead of creating a new one.</span></span> <span data-ttu-id="49798-132">Это значение не может использоваться вместе с <strong>адкреатеоверврите</strong>.</span><span class="sxs-lookup"><span data-stu-id="49798-132">This value cannot be used together with <strong>adCreateOverwrite</strong>.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="49798-133">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="49798-133">ADO/WFC equivalent</span></span>

<span data-ttu-id="49798-134">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="49798-134">These constants do not have ADO/WFC equivalents.</span></span>

