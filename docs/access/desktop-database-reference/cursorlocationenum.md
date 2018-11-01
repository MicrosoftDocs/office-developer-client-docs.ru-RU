---
title: CursorLocationEnum (Справочник по для настольных баз данных Access)
TOCTitle: CursorLocationEnum
ms:assetid: 520cc738-998b-ce80-6362-0df310c40c39
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249268(v=office.15)
ms:contentKeyID: 48544836
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 63b4ae569ce76c480725853e119b4807dd121758
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882821"
---
# <a name="cursorlocationenum"></a><span data-ttu-id="3633a-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="3633a-102">CursorLocationEnum</span></span>

<span data-ttu-id="3633a-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3633a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3633a-104">Указывает расположение службы курсора.</span><span class="sxs-lookup"><span data-stu-id="3633a-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3633a-105">Константа</span><span class="sxs-lookup"><span data-stu-id="3633a-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="3633a-106">Значение</span><span class="sxs-lookup"><span data-stu-id="3633a-106">Value</span></span></p></th>
<th><p><span data-ttu-id="3633a-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3633a-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3633a-108"><strong>adUseClient</strong></span><span class="sxs-lookup"><span data-stu-id="3633a-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="3633a-109">3</span><span class="sxs-lookup"><span data-stu-id="3633a-109">3</span></span></p></td>
<td><p><span data-ttu-id="3633a-110">Используется в телефонном локальный курсор библиотеки записей на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="3633a-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="3633a-111">Локальный курсор служб часто позволит множество функций, которые не разрешается-драйвер курсоры, с помощью этого параметра может предоставить преимущество по отношению к функции, которые будут включены.</span><span class="sxs-lookup"><span data-stu-id="3633a-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="3633a-112">Для обеспечения обратной совместимости также поддерживается синоним <strong>adUseClientBatch</strong> .</span><span class="sxs-lookup"><span data-stu-id="3633a-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3633a-113"><strong>adUseNone</strong></span><span class="sxs-lookup"><span data-stu-id="3633a-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="3633a-114">1</span><span class="sxs-lookup"><span data-stu-id="3633a-114">1</span></span></p></td>
<td><p><span data-ttu-id="3633a-115">Не используйте службы курсора.</span><span class="sxs-lookup"><span data-stu-id="3633a-115">Does not use cursor services.</span></span> <span data-ttu-id="3633a-116">(Этой константы является устаревшим и отображается только для обратной совместимости).</span><span class="sxs-lookup"><span data-stu-id="3633a-116">(This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3633a-117"><strong>adUseServer</strong></span><span class="sxs-lookup"><span data-stu-id="3633a-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="3633a-118">2</span><span class="sxs-lookup"><span data-stu-id="3633a-118">2</span></span></p></td>
<td><p><span data-ttu-id="3633a-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3633a-119">Default.</span></span> <span data-ttu-id="3633a-120">Использует поставщик данных или курсоры драйвер.</span><span class="sxs-lookup"><span data-stu-id="3633a-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="3633a-121">Эти курсоры иногда гибкой и позволяют для дополнительных знаков для изменения других пользователей к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="3633a-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="3633a-122">Тем не менее некоторые функции <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Службы Microsoft курсора для OLE DB</a> (например, этом отдельные объекты <a href="recordset-object-ado.md">набора записей</a> ) нельзя моделируемые с записей на стороне сервера, и эти функции будут недоступны при использовании этого параметра.</span><span class="sxs-lookup"><span data-stu-id="3633a-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="3633a-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="3633a-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="3633a-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="3633a-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3633a-125">Constant</span><span class="sxs-lookup"><span data-stu-id="3633a-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3633a-126">AdoEnums.CursorLocation.CLIENT</span><span class="sxs-lookup"><span data-stu-id="3633a-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3633a-127">AdoEnums.CursorLocation.NONE</span><span class="sxs-lookup"><span data-stu-id="3633a-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3633a-128">AdoEnums.CursorLocation.SERVER</span><span class="sxs-lookup"><span data-stu-id="3633a-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

