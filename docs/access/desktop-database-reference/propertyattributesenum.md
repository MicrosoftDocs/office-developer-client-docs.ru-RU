---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c929bcf5dc7f5267c2e7d3a8dac5ed6bfb55b20b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302879"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="b4a23-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="b4a23-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="b4a23-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4a23-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b4a23-104">Указывает атрибуты объекта [Property.](property-object-ado.md)</span><span class="sxs-lookup"><span data-stu-id="b4a23-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4a23-105">Константа</span><span class="sxs-lookup"><span data-stu-id="b4a23-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="b4a23-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b4a23-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b4a23-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b4a23-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4a23-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="b4a23-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a23-109">0</span><span class="sxs-lookup"><span data-stu-id="b4a23-109">0</span></span></p></td>
<td><p><span data-ttu-id="b4a23-110">Указывает, что свойство не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="b4a23-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a23-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="b4a23-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a23-112">1 </span><span class="sxs-lookup"><span data-stu-id="b4a23-112">1</span></span></p></td>
<td><p><span data-ttu-id="b4a23-113">Указывает, что пользователь должен указать значение для этого свойства до инициализации источника данных.</span><span class="sxs-lookup"><span data-stu-id="b4a23-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4a23-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="b4a23-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a23-115">2 </span><span class="sxs-lookup"><span data-stu-id="b4a23-115">2</span></span></p></td>
<td><p><span data-ttu-id="b4a23-116">Указывает, что пользователю не нужно указывать значение для этого свойства до инициализации источника данных.</span><span class="sxs-lookup"><span data-stu-id="b4a23-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a23-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="b4a23-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a23-118">512</span><span class="sxs-lookup"><span data-stu-id="b4a23-118">512</span></span></p></td>
<td><p><span data-ttu-id="b4a23-119">Указывает, что пользователь может прочитать свойство.</span><span class="sxs-lookup"><span data-stu-id="b4a23-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4a23-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="b4a23-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="b4a23-121">1024</span><span class="sxs-lookup"><span data-stu-id="b4a23-121">1024</span></span></p></td>
<td><p><span data-ttu-id="b4a23-122">Указывает, что пользователь может установить свойство.</span><span class="sxs-lookup"><span data-stu-id="b4a23-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="b4a23-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="b4a23-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="b4a23-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="b4a23-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b4a23-125">Константа</span><span class="sxs-lookup"><span data-stu-id="b4a23-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b4a23-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="b4a23-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a23-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="b4a23-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4a23-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="b4a23-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b4a23-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="b4a23-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b4a23-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="b4a23-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

