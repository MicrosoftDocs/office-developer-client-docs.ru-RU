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
# <a name="parameterdirectionenum"></a><span data-ttu-id="7d56d-102">ParameterDirectionEnum</span><span class="sxs-lookup"><span data-stu-id="7d56d-102">ParameterDirectionEnum</span></span>


<span data-ttu-id="7d56d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d56d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7d56d-104">Указывает, представляет ли [параметр](parameter-object-ado.md) входной параметр, выходной параметр, входной и выходной параметры, а также возвращаемое значение из хранимой процедуры.</span><span class="sxs-lookup"><span data-stu-id="7d56d-104">Specifies whether the [Parameter](parameter-object-ado.md) represents an input parameter, an output parameter, both an input and an output parameter, or the return value from a stored procedure.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d56d-105">Константа</span><span class="sxs-lookup"><span data-stu-id="7d56d-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7d56d-106">Значение</span><span class="sxs-lookup"><span data-stu-id="7d56d-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7d56d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7d56d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d56d-108"><strong>Адпараминпут</strong></span><span class="sxs-lookup"><span data-stu-id="7d56d-108"><strong>adParamInput</strong></span></span></p></td>
<td><p><span data-ttu-id="7d56d-109">1,1</span><span class="sxs-lookup"><span data-stu-id="7d56d-109">1</span></span></p></td>
<td><p><span data-ttu-id="7d56d-110">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7d56d-110">Default.</span></span> <span data-ttu-id="7d56d-111">Указывает, что параметр представляет входной параметр.</span><span class="sxs-lookup"><span data-stu-id="7d56d-111">Indicates that the parameter represents an input parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d56d-112"><strong>Адпараминпутаутпут</strong></span><span class="sxs-lookup"><span data-stu-id="7d56d-112"><strong>adParamInputOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="7d56d-113">4</span><span class="sxs-lookup"><span data-stu-id="7d56d-113">3</span></span></p></td>
<td><p><span data-ttu-id="7d56d-114">Указывает, что параметр представляет оба входного и выходного параметра.</span><span class="sxs-lookup"><span data-stu-id="7d56d-114">Indicates that the parameter represents both an input and output parameter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d56d-115"><strong>Адпарамаутпут</strong></span><span class="sxs-lookup"><span data-stu-id="7d56d-115"><strong>adParamOutput</strong></span></span></p></td>
<td><p><span data-ttu-id="7d56d-116">2</span><span class="sxs-lookup"><span data-stu-id="7d56d-116">2</span></span></p></td>
<td><p><span data-ttu-id="7d56d-117">Указывает, что параметр представляет выходной параметр.</span><span class="sxs-lookup"><span data-stu-id="7d56d-117">Indicates that the parameter represents an output parameter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d56d-118"><strong>Адпарамретурнвалуе</strong></span><span class="sxs-lookup"><span data-stu-id="7d56d-118"><strong>adParamReturnValue</strong></span></span></p></td>
<td><p><span data-ttu-id="7d56d-119">SP4</span><span class="sxs-lookup"><span data-stu-id="7d56d-119">4</span></span></p></td>
<td><p><span data-ttu-id="7d56d-120">Указывает, что параметр представляет возвращаемое значение.</span><span class="sxs-lookup"><span data-stu-id="7d56d-120">Indicates that the parameter represents a return value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d56d-121"><strong>Адпарамункновн</strong></span><span class="sxs-lookup"><span data-stu-id="7d56d-121"><strong>adParamUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="7d56d-122">нуль</span><span class="sxs-lookup"><span data-stu-id="7d56d-122">0</span></span></p></td>
<td><p><span data-ttu-id="7d56d-123">Указывает, что направление параметра неизвестно.</span><span class="sxs-lookup"><span data-stu-id="7d56d-123">Indicates that the parameter direction is unknown.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="7d56d-124">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="7d56d-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="7d56d-125">Пакет: **com. MS. WFC. Data**</span><span class="sxs-lookup"><span data-stu-id="7d56d-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d56d-126">Константа</span><span class="sxs-lookup"><span data-stu-id="7d56d-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d56d-127">Адоенумс. Параметердиректион. INPUT</span><span class="sxs-lookup"><span data-stu-id="7d56d-127">AdoEnums.ParameterDirection.INPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d56d-128">Адоенумс. Параметердиректион. процессы</span><span class="sxs-lookup"><span data-stu-id="7d56d-128">AdoEnums.ParameterDirection.INPUTOUTPUT</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d56d-129">Адоенумс. Параметердиректион. OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d56d-129">AdoEnums.ParameterDirection.OUTPUT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d56d-130">Адоенумс. Параметердиректион. RETURNVALUE</span><span class="sxs-lookup"><span data-stu-id="7d56d-130">AdoEnums.ParameterDirection.RETURNVALUE</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d56d-131">Адоенумс. Параметердиректион. UNKNOWN</span><span class="sxs-lookup"><span data-stu-id="7d56d-131">AdoEnums.ParameterDirection.UNKNOWN</span></span></p></td>
</tr>
</tbody>
</table>

