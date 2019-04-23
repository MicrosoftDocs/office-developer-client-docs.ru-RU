---
title: ADCPROP_ASYNCTHREADPRIORITY_ENUM
TOCTitle: ADCPROP_ASYNCTHREADPRIORITY_ENUM
ms:assetid: b15006dd-22d5-fcf3-8196-9e24ea9d55a7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249844(v=office.15)
ms:contentKeyID: 48547143
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 53e51f2386658ee975ec8847f7e5550ac22bbd8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281903"
---
# <a name="adcpropasyncthreadpriorityenum"></a><span data-ttu-id="67b53-102">Перечисление АДКПРОП\_асинксреадприорити\_</span><span class="sxs-lookup"><span data-stu-id="67b53-102">ADCPROP\_ASYNCTHREADPRIORITY\_ENUM</span></span>

<span data-ttu-id="67b53-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="67b53-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="67b53-104">Для объекта [RECORDSET](recordset-object-ado.md) RDS указывает приоритет выполнения асинхронного потока, который получает данные.</span><span class="sxs-lookup"><span data-stu-id="67b53-104">For an RDS [Recordset](recordset-object-ado.md) object, specifies the execution priority of the asynchronous thread that retrieves data.</span></span>

<span data-ttu-id="67b53-105">Используйте эти константы с динамическим свойством **Recordset** "**приоритет фонового потока**", на который ссылается индекс динамического свойства ADO и задокументированы в документации [службы курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) .</span><span class="sxs-lookup"><span data-stu-id="67b53-105">Use these constants with the **Recordset** "**Background Thread Priority**" dynamic property, which is referenced in the ADO Dynamic Property Index and documented in the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) documentation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67b53-106">Константа</span><span class="sxs-lookup"><span data-stu-id="67b53-106">Constant</span></span></p></th>
<th><p><span data-ttu-id="67b53-107">Значение</span><span class="sxs-lookup"><span data-stu-id="67b53-107">Value</span></span></p></th>
<th><p><span data-ttu-id="67b53-108">Описание</span><span class="sxs-lookup"><span data-stu-id="67b53-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67b53-109"><strong>Адприоритябовенормал</strong></span><span class="sxs-lookup"><span data-stu-id="67b53-109"><strong>adPriorityAboveNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="67b53-110">SP4</span><span class="sxs-lookup"><span data-stu-id="67b53-110">4</span></span></p></td>
<td><p><span data-ttu-id="67b53-111">Задает приоритет между обычным и максимальным приоритетом.</span><span class="sxs-lookup"><span data-stu-id="67b53-111">Sets priority between normal and highest.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67b53-112"><strong>Адприоритибеловнормал</strong></span><span class="sxs-lookup"><span data-stu-id="67b53-112"><strong>adPriorityBelowNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="67b53-113">2</span><span class="sxs-lookup"><span data-stu-id="67b53-113">2</span></span></p></td>
<td><p><span data-ttu-id="67b53-114">Задает приоритет между самым низким и нормальным.</span><span class="sxs-lookup"><span data-stu-id="67b53-114">Sets priority between lowest and normal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67b53-115"><strong>Адприоритихигхест</strong></span><span class="sxs-lookup"><span data-stu-id="67b53-115"><strong>adPriorityHighest</strong></span></span></p></td>
<td><p><span data-ttu-id="67b53-116">17:00</span><span class="sxs-lookup"><span data-stu-id="67b53-116">5</span></span></p></td>
<td><p><span data-ttu-id="67b53-117">Задает максимально возможный приоритет.</span><span class="sxs-lookup"><span data-stu-id="67b53-117">Sets priority to the highest possible.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67b53-118"><strong>Адприоритиловест</strong></span><span class="sxs-lookup"><span data-stu-id="67b53-118"><strong>AdPriorityLowest</strong></span></span></p></td>
<td><p><span data-ttu-id="67b53-119">1,1</span><span class="sxs-lookup"><span data-stu-id="67b53-119">1</span></span></p></td>
<td><p><span data-ttu-id="67b53-120">Устанавливает минимально возможный приоритет.</span><span class="sxs-lookup"><span data-stu-id="67b53-120">Sets priority to the lowest possible.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67b53-121"><strong>Адприоритинормал</strong></span><span class="sxs-lookup"><span data-stu-id="67b53-121"><strong>adPriorityNormal</strong></span></span></p></td>
<td><p><span data-ttu-id="67b53-122">4</span><span class="sxs-lookup"><span data-stu-id="67b53-122">3</span></span></p></td>
<td><p><span data-ttu-id="67b53-123">Устанавливает для приоритета значение Обычная.</span><span class="sxs-lookup"><span data-stu-id="67b53-123">Sets priority to normal.</span></span></p></td>
</tr>
</tbody>
</table>

### <a name="adowfc-equivalent"></a><span data-ttu-id="67b53-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="67b53-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="67b53-125">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="67b53-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="67b53-126">Константа</span><span class="sxs-lookup"><span data-stu-id="67b53-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="67b53-127">Адоенумс. Адкпропасинксреадприорити. АБОВЕНОРМАЛ</span><span class="sxs-lookup"><span data-stu-id="67b53-127">AdoEnums.AdcPropAsyncThreadPriority.ABOVENORMAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67b53-128">Адоенумс. Адкпропасинксреадприорити. БЕЛОВНОРМАЛ</span><span class="sxs-lookup"><span data-stu-id="67b53-128">AdoEnums.AdcPropAsyncThreadPriority.BELOWNORMAL</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67b53-129">Адоенумс. Адкпропасинксреадприорити. ВЫСШИй</span><span class="sxs-lookup"><span data-stu-id="67b53-129">AdoEnums.AdcPropAsyncThreadPriority.HIGHEST</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="67b53-130">Адоенумс. Адкпропасинксреадприорити. НИЗШИй</span><span class="sxs-lookup"><span data-stu-id="67b53-130">AdoEnums.AdcPropAsyncThreadPriority.LOWEST</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="67b53-131">Адоенумс. Адкпропасинксреадприорити. NORMAL</span><span class="sxs-lookup"><span data-stu-id="67b53-131">AdoEnums.AdcPropAsyncThreadPriority.NORMAL</span></span></p></td>
</tr>
</tbody>
</table>

