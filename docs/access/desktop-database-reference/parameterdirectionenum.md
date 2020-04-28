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
# <a name="parameterdirectionenum"></a><span data-ttu-id="2d542-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="2d542-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="2d542-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2d542-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2d542-104">Указывает, представляет ли [параметр](parameter-object-ado.md) входной параметр, выходной параметр, входной и выходной параметры, а также возвращаемое значение из хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="2d542-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d542-105">Константа</span><span class="sxs-lookup"><span data-stu-id="2d542-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="2d542-106">Значение</span><span class="sxs-lookup"><span data-stu-id="2d542-106">Value</span></span></p></th>
<th><p><span data-ttu-id="2d542-107">Описание</span><span class="sxs-lookup"><span data-stu-id="2d542-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d542-108"><strong>адпараминпут</strong></span><span class="sxs-lookup"><span data-stu-id="2d542-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="2d542-109">1,1</span><span class="sxs-lookup"><span data-stu-id="2d542-109">1</span></span></p></td>
<td><p><span data-ttu-id="2d542-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d542-110">Default.</span></span> <span data-ttu-id="2d542-111">Указывает, что параметр представляет входной параметр.</span><span class="sxs-lookup"><span data-stu-id="2d542-111">Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d542-112"><strong>адпараминпутаутпут</strong></span><span class="sxs-lookup"><span data-stu-id="2d542-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="2d542-113">4</span><span class="sxs-lookup"><span data-stu-id="2d542-113">3</span></span></p></td>
<td><p><span data-ttu-id="2d542-114">Указывает, что параметр представляет оба входного и выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="2d542-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d542-115"><strong>адпарамаутпут</strong></span><span class="sxs-lookup"><span data-stu-id="2d542-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="2d542-116">2</span><span class="sxs-lookup"><span data-stu-id="2d542-116">2</span></span></p></td>
<td><p><span data-ttu-id="2d542-117">Указывает, что параметр представляет выходной параметр.</span><span class="sxs-lookup"><span data-stu-id="2d542-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d542-118"><strong>адпарамретурнвалуе</strong></span><span class="sxs-lookup"><span data-stu-id="2d542-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="2d542-119">4 </span><span class="sxs-lookup"><span data-stu-id="2d542-119">4</span></span></p></td>
<td><p><span data-ttu-id="2d542-120">Указывает, что параметр представляет возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="2d542-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d542-121"><strong>адпарамункновн</strong></span><span class="sxs-lookup"><span data-stu-id="2d542-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="2d542-122">нуль</span><span class="sxs-lookup"><span data-stu-id="2d542-122">0</span></span></p></td>
<td><p><span data-ttu-id="2d542-123">Указывает, что направление параметра неизвестно.</span><span class="sxs-lookup"><span data-stu-id="2d542-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="2d542-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="2d542-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="2d542-125">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="2d542-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2d542-126">Константа</span><span class="sxs-lookup"><span data-stu-id="2d542-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2d542-127">Адоенумс. Параметердиректион. INPUT</span><span class="sxs-lookup"><span data-stu-id="2d542-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d542-128">Адоенумс. Параметердиректион. процессы</span><span class="sxs-lookup"><span data-stu-id="2d542-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d542-129">Адоенумс. Параметердиректион. OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d542-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2d542-130">Адоенумс. Параметердиректион. RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="2d542-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2d542-131">Адоенумс. Параметердиректион. UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="2d542-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

