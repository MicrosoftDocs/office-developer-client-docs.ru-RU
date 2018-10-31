---
title: StreamOpenOptionsEnum
TOCTitle: StreamOpenOptionsEnum
ms:assetid: d4bbd6be-41f1-cdf2-9d8f-b77ce83fb88e
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250069(v=office.15)
ms:contentKeyID: 48547951
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ceea7d20620de16f435ad1b17f642957013ce33c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862977"
---
# <a name="streamopenoptionsenum"></a><span data-ttu-id="15b5d-102">StreamOpenOptionsEnum</span><span class="sxs-lookup"><span data-stu-id="15b5d-102">StreamOpenOptionsEnum</span></span>


<span data-ttu-id="15b5d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="15b5d-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="15b5d-104">Задает параметры открытия объект [Stream](stream-object-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="15b5d-104">Specifies options for opening a [Stream](stream-object-ado.md) object.</span></span> <span data-ttu-id="15b5d-105">Значения может использоваться совместно с операция OR.</span><span class="sxs-lookup"><span data-stu-id="15b5d-105">The values can be combined with an OR operation.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="15b5d-106">Константа</span><span class="sxs-lookup"><span data-stu-id="15b5d-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="15b5d-107">Значение</span><span class="sxs-lookup"><span data-stu-id="15b5d-107">Value</span></span></p></th>
<th><p><span data-ttu-id="15b5d-108">Описание</span><span class="sxs-lookup"><span data-stu-id="15b5d-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15b5d-109"><strong>adOpenStreamAsync</strong></span><span class="sxs-lookup"><span data-stu-id="15b5d-109"><strong>adOpenStreamAsync</strong></span></span></p></td>
<td><p><span data-ttu-id="15b5d-110">1</span><span class="sxs-lookup"><span data-stu-id="15b5d-110">1</span></span></p></td>
<td><p><span data-ttu-id="15b5d-111">Открывает объект <strong>Stream</strong> в асинхронном режиме.</span><span class="sxs-lookup"><span data-stu-id="15b5d-111">Opens the <strong>Stream</strong> object in asynchronous mode.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15b5d-112"><strong>adOpenStreamFromRecord</strong></span><span class="sxs-lookup"><span data-stu-id="15b5d-112"><strong>adOpenStreamFromRecord</strong></span></span></p></td>
<td><p><span data-ttu-id="15b5d-113">4</span><span class="sxs-lookup"><span data-stu-id="15b5d-113">4</span></span></p></td>
<td><p><span data-ttu-id="15b5d-114">Определяет содержимое параметра <em>источника</em> в уже открытой объекта <a href="record-object-ado.md">записи</a> .</span><span class="sxs-lookup"><span data-stu-id="15b5d-114">Identifies the contents of the <em>Source</em> parameter to be an already open <a href="record-object-ado.md">Record</a> object.</span></span> <span data-ttu-id="15b5d-115">Поведение по умолчанию — это следует считать <em>исходный</em> URL-адрес, который указывает узел в древовидной структуре.</span><span class="sxs-lookup"><span data-stu-id="15b5d-115">The default behavior is to treat <em>Source</em> as a URL that points directly to a node in a tree structure.</span></span> <span data-ttu-id="15b5d-116">Открывается поток по умолчанию, связанные с этим узлом.</span><span class="sxs-lookup"><span data-stu-id="15b5d-116">The default stream associated with that node is opened.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15b5d-117"><strong>adOpenStreamUnspecified</strong></span><span class="sxs-lookup"><span data-stu-id="15b5d-117"><strong>adOpenStreamUnspecified</strong></span></span></p></td>
<td><p><span data-ttu-id="15b5d-118">-1</span><span class="sxs-lookup"><span data-stu-id="15b5d-118">-1</span></span></p></td>
<td><p><span data-ttu-id="15b5d-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15b5d-119">Default.</span></span> <span data-ttu-id="15b5d-120">Указывает, открыв объект <strong>Stream</strong> с параметрами по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="15b5d-120">Specifies opening the <strong>Stream</strong> object with default options.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="15b5d-121">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="15b5d-121">ADO/WFC equivalent</span></span>

<span data-ttu-id="15b5d-122">Эти константы нет ADO/WFC эквивалентами.</span><span class="sxs-lookup"><span data-stu-id="15b5d-122">These constants do not have ADO/WFC equivalents.</span></span>

