---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: f335f8572fbade23b949abacce8dd3690d205e32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28721222"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="50d8e-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="50d8e-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="50d8e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="50d8e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="50d8e-104">Задает параметры открытия объект [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="50d8e-104">Specifies options for opening a [Stream](stream-object-ado.md) object.</span></span> <span data-ttu-id="50d8e-105">Значения может использоваться совместно с операция OR.</span><span class="sxs-lookup"><span data-stu-id="50d8e-105">The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="50d8e-106">Константа</span><span class="sxs-lookup"><span data-stu-id="50d8e-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="50d8e-107">Значение</span><span class="sxs-lookup"><span data-stu-id="50d8e-107">Value</span></span></p></th>
<th><p><span data-ttu-id="50d8e-108">Описание</span><span class="sxs-lookup"><span data-stu-id="50d8e-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="50d8e-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="50d8e-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="50d8e-110">1</span><span class="sxs-lookup"><span data-stu-id="50d8e-110">1</span></span></p></td>
<td><p><span data-ttu-id="50d8e-111">Открывает объект <strong>Stream</strong> в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="50d8e-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="50d8e-112"><strong>adOpenStreamFromRecord</strong></span><span class="sxs-lookup"><span data-stu-id="50d8e-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="50d8e-113">4</span><span class="sxs-lookup"><span data-stu-id="50d8e-113">4</span></span></p></td>
<td><p><span data-ttu-id="50d8e-114">Определяет содержимое параметра <em>источника</em> в уже открытой объекта <a href="record-object-ado.md">записи</a> .</span><span class="sxs-lookup"><span data-stu-id="50d8e-114">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object.</span></span> <span data-ttu-id="50d8e-115">Поведение по умолчанию — это следует считать <em>исходный</em> URL-адрес, который указывает узел в древовидной структуре.</span><span class="sxs-lookup"><span data-stu-id="50d8e-115">The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure.</span></span> <span data-ttu-id="50d8e-116">Открывается поток по умолчанию, связанные с этим узлом.</span><span class="sxs-lookup"><span data-stu-id="50d8e-116">The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="50d8e-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="50d8e-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="50d8e-118">–1</span><span class="sxs-lookup"><span data-stu-id="50d8e-118">-1</span></span></p></td>
<td><p><span data-ttu-id="50d8e-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="50d8e-119">Default.</span></span> <span data-ttu-id="50d8e-120">Указывает, открыв объект <strong>Stream</strong> с параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="50d8e-120">Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="50d8e-121">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="50d8e-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="50d8e-122">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="50d8e-122">These constants do not have ADO/WFC equivalents.</span></span>

