---
title: CursorLocationEnum (Ссылка на настольные базы данных)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295214"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="6d857-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="6d857-102">CursorLocationEnum</span></span>

<span data-ttu-id="6d857-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6d857-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6d857-104">Указывает расположение службы курсоров.</span><span class="sxs-lookup"><span data-stu-id="6d857-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d857-105">Константа</span><span class="sxs-lookup"><span data-stu-id="6d857-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="6d857-106">Значение</span><span class="sxs-lookup"><span data-stu-id="6d857-106">Value</span></span></p></th>
<th><p><span data-ttu-id="6d857-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6d857-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d857-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="6d857-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="6d857-109">3</span><span class="sxs-lookup"><span data-stu-id="6d857-109">3</span></span></p></td>
<td><p><span data-ttu-id="6d857-110">Использует курсоры с клиентской стороны, предоставленные локальной библиотекой курсоров.</span><span class="sxs-lookup"><span data-stu-id="6d857-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="6d857-111">Локальные службы курсоров часто позволяют использовать множество функций, которые не могут быть предоставлены драйверами, поэтому использование этого параметра может предоставить преимущество в отношении функций, которые будут включены.</span><span class="sxs-lookup"><span data-stu-id="6d857-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="6d857-112">Для обратной совместимости также поддерживается <strong>синоним adUseClientBatch.</strong></span><span class="sxs-lookup"><span data-stu-id="6d857-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d857-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="6d857-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="6d857-114">1</span><span class="sxs-lookup"><span data-stu-id="6d857-114">1</span></span></p></td>
<td><p><span data-ttu-id="6d857-115">Не использует службы курсора.</span><span class="sxs-lookup"><span data-stu-id="6d857-115">Does not use cursor services.</span></span> <span data-ttu-id="6d857-116">(Эта константа устарела и появляется исключительно для обратной совместимости.)</span><span class="sxs-lookup"><span data-stu-id="6d857-116">(This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d857-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="6d857-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="6d857-118">2</span><span class="sxs-lookup"><span data-stu-id="6d857-118">2</span></span></p></td>
<td><p><span data-ttu-id="6d857-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6d857-119">Default.</span></span> <span data-ttu-id="6d857-120">Использует курсоры поставщика данных или предоставленные драйвером.</span><span class="sxs-lookup"><span data-stu-id="6d857-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="6d857-121">Эти курсоры иногда очень гибкие и позволяют дополнительно чувствительность к изменениям, внесенным другими пользователями в источник данных.</span><span class="sxs-lookup"><span data-stu-id="6d857-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="6d857-122">Однако некоторые функции службы <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor для OLE DB</a> (например, отсоединимые объекты <a href="recordset-object-ado.md">Recordset)</a> нельзя имитировать с помощью курсоров на стороне сервера, и эти функции будут недоступны в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="6d857-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="6d857-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="6d857-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="6d857-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="6d857-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6d857-125">Константа</span><span class="sxs-lookup"><span data-stu-id="6d857-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d857-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="6d857-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d857-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="6d857-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d857-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="6d857-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

