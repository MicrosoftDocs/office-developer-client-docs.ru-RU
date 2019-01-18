---
title: RecordOpenOptionsEnum
TOCTitle: RecordOpenOptionsEnum
ms:assetid: 44a69719-0789-a084-fb96-21468e270205
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249207(v=office.15)
ms:contentKeyID: 48544534
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caaf755ebd63f1805d0c77ef79a0f5863a85050e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708768"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="26a67-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="26a67-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="26a67-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="26a67-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="26a67-104">Задает параметры открытия для [записи](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="26a67-104">Specifies options for opening a [Record](record-object-ado.md).</span></span> <span data-ttu-id="26a67-105">Эти значения можно объединять с помощью или.</span><span class="sxs-lookup"><span data-stu-id="26a67-105">These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="26a67-106">Константа</span><span class="sxs-lookup"><span data-stu-id="26a67-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="26a67-107">Значение</span><span class="sxs-lookup"><span data-stu-id="26a67-107">Value</span></span></p></th>
<th><p><span data-ttu-id="26a67-108">Описание</span><span class="sxs-lookup"><span data-stu-id="26a67-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="26a67-109"><strong>adDelayFetchFields</strong></span><span class="sxs-lookup"><span data-stu-id="26a67-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="26a67-110">0x8000</span><span class="sxs-lookup"><span data-stu-id="26a67-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="26a67-111">Указывает поставщик, что поля, связанные с <strong>записи</strong> не требуется сначала получить, но могут быть получены во первая попытка получить доступ к полю.</span><span class="sxs-lookup"><span data-stu-id="26a67-111">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field.</span></span> <span data-ttu-id="26a67-112">— Это поведение по умолчанию, указанный в параметре отсутствия этот флаг для извлечения всех полей объекта <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="26a67-112">The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26a67-113"><strong>adDelayFetchStream</strong></span><span class="sxs-lookup"><span data-stu-id="26a67-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="26a67-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="26a67-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="26a67-115">Указывает поставщику на то, что поток по умолчанию, связанные с <strong>записи</strong> должны не удалось получить данные, изначально.</span><span class="sxs-lookup"><span data-stu-id="26a67-115">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially.</span></span> <span data-ttu-id="26a67-116">— Это поведение по умолчанию, указанный в параметре отсутствия этот флаг для извлечения потока по умолчанию, связанного с объектом <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="26a67-116">The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26a67-117"><strong>adOpenAsync</strong></span><span class="sxs-lookup"><span data-stu-id="26a67-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="26a67-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="26a67-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="26a67-119">Указывает, что объект <strong>записи</strong> открыт в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="26a67-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26a67-120"><strong>adOpenExecuteCommand</strong></span><span class="sxs-lookup"><span data-stu-id="26a67-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="26a67-121">0x10000</span><span class="sxs-lookup"><span data-stu-id="26a67-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="26a67-122">Указывает, что исходная строка содержит текст команды, которая должна выполняться.</span><span class="sxs-lookup"><span data-stu-id="26a67-122">Indicates that the Source string contains command text that should be executed.</span></span> <span data-ttu-id="26a67-123">Это значение эквивалентно параметру <strong>adCmdText</strong> на <strong>Recordset.Open</strong>.</span><span class="sxs-lookup"><span data-stu-id="26a67-123">This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="26a67-124"><strong>adOpenRecordUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="26a67-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="26a67-125">–1</span><span class="sxs-lookup"><span data-stu-id="26a67-125">-1</span></span></p></td>
<td><p><span data-ttu-id="26a67-126">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="26a67-126">Default.</span></span> <span data-ttu-id="26a67-127">Указывает, что параметры не заданы.</span><span class="sxs-lookup"><span data-stu-id="26a67-127">Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="26a67-128"><strong>adOpenOutput</strong></span><span class="sxs-lookup"><span data-stu-id="26a67-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="26a67-129">0x800000</span><span class="sxs-lookup"><span data-stu-id="26a67-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="26a67-130">Указывает, что если источник указывает на узле, содержащем исполняемый файл сценария (например,. Страница ASP), а затем открытой <strong>записи</strong> будет содержать результаты выполненного сценария.</span><span class="sxs-lookup"><span data-stu-id="26a67-130">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script.</span></span> <span data-ttu-id="26a67-131">Это значение допустимо только с записями без семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="26a67-131">This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="26a67-132">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="26a67-132">ADO/WFC equivalent</span></span>

<span data-ttu-id="26a67-133">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="26a67-133">These constants do not have ADO/WFC equivalents.</span></span>

