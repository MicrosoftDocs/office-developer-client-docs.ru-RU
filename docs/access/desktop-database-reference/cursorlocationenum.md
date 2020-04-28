---
title: Курсорлокатионенум (Справочник по базам данных Access на компьютере)
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
# <a name="cursorlocationenum"></a><span data-ttu-id="7c7de-102">CursorLocationEnum</span><span class="sxs-lookup"><span data-stu-id="7c7de-102">CursorLocationEnum</span></span>

<span data-ttu-id="7c7de-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7c7de-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7c7de-104">Указывает расположение службы курсора.</span><span class="sxs-lookup"><span data-stu-id="7c7de-104">Specifies the location of the cursor service.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c7de-105">Константа</span><span class="sxs-lookup"><span data-stu-id="7c7de-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7c7de-106">Значение</span><span class="sxs-lookup"><span data-stu-id="7c7de-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7c7de-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7c7de-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c7de-108"><strong>адусеклиент</strong></span><span class="sxs-lookup"><span data-stu-id="7c7de-108"><strong>adUseClient</strong></span></span></p></td>
<td><p><span data-ttu-id="7c7de-109">4</span><span class="sxs-lookup"><span data-stu-id="7c7de-109">3</span></span></p></td>
<td><p><span data-ttu-id="7c7de-110">Использует курсоры на стороне клиента, предоставляемые библиотекой локальных курсоров.</span><span class="sxs-lookup"><span data-stu-id="7c7de-110">Uses client-side cursors supplied by a local cursor library.</span></span> <span data-ttu-id="7c7de-111">Службы локальных курсоров часто поддерживают множество функций, которые могут быть недоступны в драйверах, поэтому использование этого параметра может привести к преимуществам в отношении функций, которые будут включены.</span><span class="sxs-lookup"><span data-stu-id="7c7de-111">Local cursor services often will allow many features that driver-supplied cursors may not, so using this setting may provide an advantage with respect to features that will be enabled.</span></span> <span data-ttu-id="7c7de-112">Для обеспечения обратной совместимости также поддерживается <strong>адусеклиентбатч</strong> синонимов.</span><span class="sxs-lookup"><span data-stu-id="7c7de-112">For backward compatibility, the synonym <strong>adUseClientBatch</strong> is also supported.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7de-113"><strong>адусеноне</strong></span><span class="sxs-lookup"><span data-stu-id="7c7de-113"><strong>adUseNone</strong></span></span></p></td>
<td><p><span data-ttu-id="7c7de-114">1,1</span><span class="sxs-lookup"><span data-stu-id="7c7de-114">1</span></span></p></td>
<td><p><span data-ttu-id="7c7de-115">Не использует службы курсоров.</span><span class="sxs-lookup"><span data-stu-id="7c7de-115">Does not use cursor services.</span></span> <span data-ttu-id="7c7de-116">(Эта константа является устаревшей и отображается исключительно в целях обратной совместимости.)</span><span class="sxs-lookup"><span data-stu-id="7c7de-116">(This constant is obsolete and appears solely for the sake of backward compatibility.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7de-117"><strong>адусесервер</strong></span><span class="sxs-lookup"><span data-stu-id="7c7de-117"><strong>adUseServer</strong></span></span></p></td>
<td><p><span data-ttu-id="7c7de-118">2</span><span class="sxs-lookup"><span data-stu-id="7c7de-118">2</span></span></p></td>
<td><p><span data-ttu-id="7c7de-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7c7de-119">Default.</span></span> <span data-ttu-id="7c7de-120">Использует курсоры, предоставляемые поставщиком данных или драйверами.</span><span class="sxs-lookup"><span data-stu-id="7c7de-120">Uses data-provider or driver-supplied cursors.</span></span> <span data-ttu-id="7c7de-121">В некоторых случаях эти курсоры являются очень гибкими и позволяют изменять другие чувствительность к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="7c7de-121">These cursors are sometimes very flexible and allow for additional sensitivity to changes others make to the data source.</span></span> <span data-ttu-id="7c7de-122">Однако некоторые функции <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">службы курсора Майкрософт для OLE DB</a> (например, несвязанные объекты <a href="recordset-object-ado.md">Recordset</a> ) не могут быть смоделированы с помощью серверных курсоров, и эти функции будут недоступны в этом параметре.</span><span class="sxs-lookup"><span data-stu-id="7c7de-122">However, some features of the <a href="microsoft-cursor-service-for-ole-db-ado-service-component.md">Microsoft Cursor Service for OLE DB</a> (such as disassociated <a href="recordset-object-ado.md">Recordset</a> objects) cannot be simulated with server-side cursors, and these features will be unavailable with this setting.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="7c7de-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="7c7de-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="7c7de-124">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="7c7de-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7c7de-125">Константа</span><span class="sxs-lookup"><span data-stu-id="7c7de-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7c7de-126">Адоенумс. CursorLocation. CLIENT</span><span class="sxs-lookup"><span data-stu-id="7c7de-126">AdoEnums.CursorLocation.CLIENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7c7de-127">Адоенумс. CursorLocation. NONE</span><span class="sxs-lookup"><span data-stu-id="7c7de-127">AdoEnums.CursorLocation.NONE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7c7de-128">Адоенумс. CursorLocation. SERVER</span><span class="sxs-lookup"><span data-stu-id="7c7de-128">AdoEnums.CursorLocation.SERVER</span></span></p></td>
</tr>
</tbody>
</table>

