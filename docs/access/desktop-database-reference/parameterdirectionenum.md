---
title: ParameterDirectionEnum
TOCTitle: ParameterDirectionEnum
ms:assetid: 73a97522-010e-d8f4-1a30-15df2469cad4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249473(v=office.15)
ms:contentKeyID: 48545643
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fac07165416841691ee7bc3ca5dfcdc366861023
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32287974"
---
# <a name="parameterdirectionenum"></a><span data-ttu-id="521ab-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="521ab-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="521ab-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="521ab-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="521ab-104">Указывает, представляет [](parameter-object-ado.md) ли параметр входной параметр, выходной параметр, входной и выходной параметры, или возвращаемого значения из хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="521ab-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="521ab-105">Константа</span><span class="sxs-lookup"><span data-stu-id="521ab-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="521ab-106">Значение</span><span class="sxs-lookup"><span data-stu-id="521ab-106">Value</span></span></p></th>
<th><p><span data-ttu-id="521ab-107">Описание</span><span class="sxs-lookup"><span data-stu-id="521ab-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="521ab-108"><strong>adParamInput</strong></span><span class="sxs-lookup"><span data-stu-id="521ab-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="521ab-109">1 </span><span class="sxs-lookup"><span data-stu-id="521ab-109">1</span></span></p></td>
<td><p><span data-ttu-id="521ab-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="521ab-110">Default.</span></span> <span data-ttu-id="521ab-111">Указывает, что параметр представляет входной параметр.</span><span class="sxs-lookup"><span data-stu-id="521ab-111">Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="521ab-112"><strong>adParamInputOutput</strong></span><span class="sxs-lookup"><span data-stu-id="521ab-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="521ab-113">3 </span><span class="sxs-lookup"><span data-stu-id="521ab-113">3</span></span></p></td>
<td><p><span data-ttu-id="521ab-114">Указывает, что параметр представляет как входной, так и выходной параметр.</span><span class="sxs-lookup"><span data-stu-id="521ab-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="521ab-115"><strong>adParamOutput</strong></span><span class="sxs-lookup"><span data-stu-id="521ab-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="521ab-116">2 </span><span class="sxs-lookup"><span data-stu-id="521ab-116">2</span></span></p></td>
<td><p><span data-ttu-id="521ab-117">Указывает, что параметр представляет выходной параметр.</span><span class="sxs-lookup"><span data-stu-id="521ab-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="521ab-118"><strong>adParamReturnValue</strong></span><span class="sxs-lookup"><span data-stu-id="521ab-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="521ab-119">4 </span><span class="sxs-lookup"><span data-stu-id="521ab-119">4</span></span></p></td>
<td><p><span data-ttu-id="521ab-120">Указывает, что параметр представляет возвращаемую величину.</span><span class="sxs-lookup"><span data-stu-id="521ab-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="521ab-121"><strong>adParamUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="521ab-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="521ab-122">0</span><span class="sxs-lookup"><span data-stu-id="521ab-122">0</span></span></p></td>
<td><p><span data-ttu-id="521ab-123">Указывает, что направление параметра неизвестно.</span><span class="sxs-lookup"><span data-stu-id="521ab-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="521ab-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="521ab-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="521ab-125">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="521ab-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="521ab-126">Константа</span><span class="sxs-lookup"><span data-stu-id="521ab-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="521ab-127">AdoEnums.ParameterDirection.INPUT</span><span class="sxs-lookup"><span data-stu-id="521ab-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="521ab-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span><span class="sxs-lookup"><span data-stu-id="521ab-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="521ab-129">AdoEnums.ParameterDirection.OUTPUT</span><span class="sxs-lookup"><span data-stu-id="521ab-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="521ab-130">AdoEnums.ParameterDirection.RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="521ab-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="521ab-131">AdoEnums.ParameterDirection.UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="521ab-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

