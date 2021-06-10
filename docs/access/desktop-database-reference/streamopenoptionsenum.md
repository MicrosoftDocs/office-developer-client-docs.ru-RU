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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314751"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="04741-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="04741-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="04741-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="04741-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="04741-104">Указывает параметры открытия объекта [Stream.](stream-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="04741-104">Specifies options for opening a [Stream](stream-object-ado.md) object.</span></span> <span data-ttu-id="04741-105">Эти значения можно сочетать с операцией OR.</span><span class="sxs-lookup"><span data-stu-id="04741-105">The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="04741-106">Константа</span><span class="sxs-lookup"><span data-stu-id="04741-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="04741-107">Значение</span><span class="sxs-lookup"><span data-stu-id="04741-107">Value</span></span></p></th>
<th><p><span data-ttu-id="04741-108">Описание</span><span class="sxs-lookup"><span data-stu-id="04741-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="04741-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="04741-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="04741-110">1</span><span class="sxs-lookup"><span data-stu-id="04741-110">1</span></span></p></td>
<td><p><span data-ttu-id="04741-111">Открывает объект <strong>Stream</strong> в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="04741-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="04741-112"><strong>adOpenStreamFromRecord</strong></span><span class="sxs-lookup"><span data-stu-id="04741-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="04741-113">4 </span><span class="sxs-lookup"><span data-stu-id="04741-113">4</span></span></p></td>
<td><p><span data-ttu-id="04741-114">Определяет содержимое параметра <em>Source</em> для уже открытого объекта <a href="record-object-ado.md">Record.</a></span><span class="sxs-lookup"><span data-stu-id="04741-114">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object.</span></span> <span data-ttu-id="04741-115">По умолчанию необходимо рассматривать <em>Source</em> как URL-адрес, который указывает непосредственно на узел в структуре дерева.</span><span class="sxs-lookup"><span data-stu-id="04741-115">The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure.</span></span> <span data-ttu-id="04741-116">По умолчанию открывается поток, связанный с этим узлом.</span><span class="sxs-lookup"><span data-stu-id="04741-116">The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="04741-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="04741-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="04741-118">–1</span><span class="sxs-lookup"><span data-stu-id="04741-118">-1</span></span></p></td>
<td><p><span data-ttu-id="04741-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04741-119">Default.</span></span> <span data-ttu-id="04741-120">Указывает открытие объекта <strong>Stream</strong> с помощью параметров по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04741-120">Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="04741-121">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="04741-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="04741-122">Эти константы не имеют эквивалентов ADO/WFC.</span><span class="sxs-lookup"><span data-stu-id="04741-122">These constants do not have ADO/WFC equivalents.</span></span>

