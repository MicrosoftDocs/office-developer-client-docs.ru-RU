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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300688"
---
# <a name="recordopenoptionsenum"></a><span data-ttu-id="661d3-102">RecordOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="661d3-102">RecordOpenOptionsEnum</span></span>


<span data-ttu-id="661d3-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="661d3-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="661d3-104">Задает параметры открытия [записи](record-object-ado.md).</span><span class="sxs-lookup"><span data-stu-id="661d3-104">Specifies options for opening a [Record](record-object-ado.md).</span></span> <span data-ttu-id="661d3-105">Эти значения можно объединять с помощью или.</span><span class="sxs-lookup"><span data-stu-id="661d3-105">These values may be combined by using OR.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="661d3-106">Константа</span><span class="sxs-lookup"><span data-stu-id="661d3-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="661d3-107">Значение</span><span class="sxs-lookup"><span data-stu-id="661d3-107">Value</span></span></p></th>
<th><p><span data-ttu-id="661d3-108">Описание</span><span class="sxs-lookup"><span data-stu-id="661d3-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="661d3-109"><strong>адделайфетчфиелдс</strong></span><span class="sxs-lookup"><span data-stu-id="661d3-109"><strong>adDelayFetchFields</strong></span></span></p></td>
<td><p><span data-ttu-id="661d3-110">0x8000</span><span class="sxs-lookup"><span data-stu-id="661d3-110">0x8000</span></span></p></td>
<td><p><span data-ttu-id="661d3-111">Указывает поставщику, что поля, связанные с <strong>записью</strong> , не должны извлекаться изначально, но их можно получить при первой попытке доступа к полю.</span><span class="sxs-lookup"><span data-stu-id="661d3-111">Indicates to the provider that the fields associated with the <strong>Record</strong> need not be retrieved initially, but can be retrieved at the first attempt to access the field.</span></span> <span data-ttu-id="661d3-112">Поведение по умолчанию, определяемое отсутствием этого флага, — получение всех полей объекта <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="661d3-112">The default behavior, indicated by the absence of this flag, is to retrieve all the <strong>Record</strong> object fields.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661d3-113"><strong>адделайфетчстреам</strong></span><span class="sxs-lookup"><span data-stu-id="661d3-113"><strong>adDelayFetchStream</strong></span></span></p></td>
<td><p><span data-ttu-id="661d3-114">0x4000</span><span class="sxs-lookup"><span data-stu-id="661d3-114">0x4000</span></span></p></td>
<td><p><span data-ttu-id="661d3-115">Указывает поставщику, что по умолчанию не требуется извлекать поток, связанный с <strong>записью</strong> .</span><span class="sxs-lookup"><span data-stu-id="661d3-115">Indicates to the provider that the default stream associated with the <strong>Record</strong> need not be retrieved initially.</span></span> <span data-ttu-id="661d3-116">Поведение по умолчанию, определяемое отсутствием этого флага, заключается в получении потока по умолчанию, связанного с объектом <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="661d3-116">The default behavior, indicated by the absence of this flag, is to retrieve the default stream associated with the <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661d3-117"><strong>адопенасинк</strong></span><span class="sxs-lookup"><span data-stu-id="661d3-117"><strong>adOpenAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="661d3-118">0x1000</span><span class="sxs-lookup"><span data-stu-id="661d3-118">0x1000</span></span></p></td>
<td><p><span data-ttu-id="661d3-119">Указывает, что объект <strong>Record</strong> открыт в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="661d3-119">Indicates that the <strong>Record</strong> object is opened in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661d3-120"><strong>адопенексекутекомманд</strong></span><span class="sxs-lookup"><span data-stu-id="661d3-120"><strong>adOpenExecuteCommand</strong></span></span></p></td>
<td><p><span data-ttu-id="661d3-121">0x10000</span><span class="sxs-lookup"><span data-stu-id="661d3-121">0x10000</span></span></p></td>
<td><p><span data-ttu-id="661d3-122">Указывает, что строка источника содержит текст команды, которую необходимо выполнить.</span><span class="sxs-lookup"><span data-stu-id="661d3-122">Indicates that the Source string contains command text that should be executed.</span></span> <span data-ttu-id="661d3-123">Это значение эквивалентно параметру <strong>адкмдтекст</strong> для объекта <strong>Recordset. Open</strong>.</span><span class="sxs-lookup"><span data-stu-id="661d3-123">This value is equivalent to the <strong>adCmdText</strong> option on <strong>Recordset.Open</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="661d3-124"><strong>адопенрекордунспеЦифиед</strong></span><span class="sxs-lookup"><span data-stu-id="661d3-124"><strong>adOpenRecordUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="661d3-125">–1</span><span class="sxs-lookup"><span data-stu-id="661d3-125">-1</span></span></p></td>
<td><p><span data-ttu-id="661d3-126">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="661d3-126">Default.</span></span> <span data-ttu-id="661d3-127">Указывает, что параметры не указаны.</span><span class="sxs-lookup"><span data-stu-id="661d3-127">Indicates no options are specified.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="661d3-128"><strong>адопенаутпут</strong></span><span class="sxs-lookup"><span data-stu-id="661d3-128"><strong>adOpenOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="661d3-129">0x800000</span><span class="sxs-lookup"><span data-stu-id="661d3-129">0x800000</span></span></p></td>
<td><p><span data-ttu-id="661d3-130">Указывает, что если источник указывает на узел, содержащий исполняемый скрипт (например,. Страница ASP), тогда открытая <strong>запись</strong> будет содержать результаты выполненного скрипта.</span><span class="sxs-lookup"><span data-stu-id="661d3-130">Indicates that if the source points to a node that contains an executable script (such as an .ASP page), then the opened <strong>Record</strong> will contain the results of the executed script.</span></span> <span data-ttu-id="661d3-131">Это значение является допустимым только для записей, не являющихся коллекциями.</span><span class="sxs-lookup"><span data-stu-id="661d3-131">This value is only valid with non-collection records.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="661d3-132">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="661d3-132">ADO/WFC equivalent</span></span>

<span data-ttu-id="661d3-133">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="661d3-133">These constants do not have ADO/WFC equivalents.</span></span>

