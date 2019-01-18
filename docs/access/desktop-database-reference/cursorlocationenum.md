---
title: CursorLocationEnum (Справочник по для настольных баз данных Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 95e5744d5e19e7c3d40de19e240bbe338b2d5d55
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28701132"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="51031-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="51031-102">CursorLocationEnum</span></span>

<span data-ttu-id="51031-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="51031-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="51031-104">Указывает расположение службы курсора.</span><span class="sxs-lookup"><span data-stu-id="51031-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51031-105">Константа</span><span class="sxs-lookup"><span data-stu-id="51031-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="51031-106">Значение</span><span class="sxs-lookup"><span data-stu-id="51031-106">Value</span></span></p></th>
<th><p><span data-ttu-id="51031-107">Описание</span><span class="sxs-lookup"><span data-stu-id="51031-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51031-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="51031-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="51031-109">3</span><span class="sxs-lookup"><span data-stu-id="51031-109">3</span></span></p></td>
<td><p><span data-ttu-id="51031-110">Используется в телефонном локальный курсор библиотеки записей на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="51031-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="51031-111">Локальный курсор служб часто позволит множество функций, которые не разрешается-драйвер курсоры, с помощью этого параметра может предоставить преимущество по отношению к функции, которые будут включены.</span><span class="sxs-lookup"><span data-stu-id="51031-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="51031-112">Для обеспечения обратной совместимости также поддерживается синоним <strong>adUseClientBatch</strong> .</span><span class="sxs-lookup"><span data-stu-id="51031-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51031-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="51031-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="51031-114">1</span><span class="sxs-lookup"><span data-stu-id="51031-114">1</span></span></p></td>
<td><p><span data-ttu-id="51031-115">Не используйте службы курсора.</span><span class="sxs-lookup"><span data-stu-id="51031-115">Does not use cursor services.</span></span> <span data-ttu-id="51031-116">(Этой константы является устаревшим и отображается только для обратной совместимости).</span><span class="sxs-lookup"><span data-stu-id="51031-116">(This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51031-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="51031-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="51031-118">2</span><span class="sxs-lookup"><span data-stu-id="51031-118">2</span></span></p></td>
<td><p><span data-ttu-id="51031-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51031-119">Default.</span></span> <span data-ttu-id="51031-120">Использует поставщик данных или курсоры драйвер.</span><span class="sxs-lookup"><span data-stu-id="51031-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="51031-121">Эти курсоры иногда гибкой и позволяют для дополнительных знаков для изменения других пользователей к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="51031-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="51031-122">Тем не менее некоторые функции <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Службы Microsoft курсора для OLE DB</a> (например, этом отдельные объекты <a href="recordset-object-ado.md">набора записей</a> ) нельзя моделируемые с записей на стороне сервера, и эти функции будут недоступны при использовании этого параметра.</span><span class="sxs-lookup"><span data-stu-id="51031-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="51031-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="51031-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="51031-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="51031-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="51031-125">Константа</span><span class="sxs-lookup"><span data-stu-id="51031-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51031-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="51031-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51031-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="51031-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51031-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="51031-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

