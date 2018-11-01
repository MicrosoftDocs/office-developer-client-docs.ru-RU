---
title: PropertyAttributesEnum
TOCTitle: PropertyAttributesEnum
ms:assetid: cbe93f65-a3ee-4741-1ac7-1c98ac53cdde
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250012(v=office.15)
ms:contentKeyID: 48547726
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 19a5f34734f98b84e9a232dd06bd4f35f016a58f
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25877508"
---
# <a name="propertyattributesenum"></a><span data-ttu-id="cadd6-102">PropertyAttributesEnum</span><span class="sxs-lookup"><span data-stu-id="cadd6-102">PropertyAttributesEnum</span></span>


<span data-ttu-id="cadd6-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cadd6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cadd6-104">Указывает атрибуты [Свойства](property-object-ado.md) объекта.</span><span class="sxs-lookup"><span data-stu-id="cadd6-104">Specifies the attributes of a [Property](property-object-ado.md) object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cadd6-105">Константа</span><span class="sxs-lookup"><span data-stu-id="cadd6-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="cadd6-106">Значение</span><span class="sxs-lookup"><span data-stu-id="cadd6-106">Value</span></span></p></th>
<th><p><span data-ttu-id="cadd6-107">Описание</span><span class="sxs-lookup"><span data-stu-id="cadd6-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cadd6-108"><strong>adPropNotSupported</strong></span><span class="sxs-lookup"><span data-stu-id="cadd6-108"><strong>adPropNotSupported</strong></span></span></p></td>
<td><p><span data-ttu-id="cadd6-109">0</span><span class="sxs-lookup"><span data-stu-id="cadd6-109">0</span></span></p></td>
<td><p><span data-ttu-id="cadd6-110">Указывает, что свойство не поддерживается поставщиком.</span><span class="sxs-lookup"><span data-stu-id="cadd6-110">Indicates that the property is not supported by the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cadd6-111"><strong>adPropRequired</strong></span><span class="sxs-lookup"><span data-stu-id="cadd6-111"><strong>adPropRequired</strong></span></span></p></td>
<td><p><span data-ttu-id="cadd6-112">1</span><span class="sxs-lookup"><span data-stu-id="cadd6-112">1</span></span></p></td>
<td><p><span data-ttu-id="cadd6-113">Указывает, что пользователь должен указать значение для этого свойства перед инициализацией источника данных.</span><span class="sxs-lookup"><span data-stu-id="cadd6-113">Indicates that the user must specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cadd6-114"><strong>adPropOptional</strong></span><span class="sxs-lookup"><span data-stu-id="cadd6-114"><strong>adPropOptional</strong></span></span></p></td>
<td><p><span data-ttu-id="cadd6-115">2</span><span class="sxs-lookup"><span data-stu-id="cadd6-115">2</span></span></p></td>
<td><p><span data-ttu-id="cadd6-116">Указывает, что пользователю необходимо указать значение для этого свойства перед инициализацией источника данных.</span><span class="sxs-lookup"><span data-stu-id="cadd6-116">Indicates that the user does not need to specify a value for this property before the data source is initialized.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cadd6-117"><strong>adPropRead</strong></span><span class="sxs-lookup"><span data-stu-id="cadd6-117"><strong>adPropRead</strong></span></span></p></td>
<td><p><span data-ttu-id="cadd6-118">512</span><span class="sxs-lookup"><span data-stu-id="cadd6-118">512</span></span></p></td>
<td><p><span data-ttu-id="cadd6-119">Указывает, что пользователи могут читать свойства.</span><span class="sxs-lookup"><span data-stu-id="cadd6-119">Indicates that the user can read the property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cadd6-120"><strong>adPropWrite</strong></span><span class="sxs-lookup"><span data-stu-id="cadd6-120"><strong>adPropWrite</strong></span></span></p></td>
<td><p><span data-ttu-id="cadd6-121">1024</span><span class="sxs-lookup"><span data-stu-id="cadd6-121">1024</span></span></p></td>
<td><p><span data-ttu-id="cadd6-122">Указывает, что пользователь может задать свойства.</span><span class="sxs-lookup"><span data-stu-id="cadd6-122">Indicates that the user can set the property.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="cadd6-123">Эквивалент ADO/WFC</span><span class="sxs-lookup"><span data-stu-id="cadd6-123">ADO/WFC equivalent</span></span>

<span data-ttu-id="cadd6-124">Пакет: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="cadd6-124">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="cadd6-125">Constant</span><span class="sxs-lookup"><span data-stu-id="cadd6-125">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cadd6-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="cadd6-126">AdoEnums.PropertyAttributes.NOTSUPPORTED</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cadd6-127">AdoEnums.PropertyAttributes.REQUIRED</span><span class="sxs-lookup"><span data-stu-id="cadd6-127">AdoEnums.PropertyAttributes.REQUIRED</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cadd6-128">AdoEnums.PropertyAttributes.OPTIONAL</span><span class="sxs-lookup"><span data-stu-id="cadd6-128">AdoEnums.PropertyAttributes.OPTIONAL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cadd6-129">AdoEnums.PropertyAttributes.READ</span><span class="sxs-lookup"><span data-stu-id="cadd6-129">AdoEnums.PropertyAttributes.READ</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cadd6-130">AdoEnums.PropertyAttributes.WRITE</span><span class="sxs-lookup"><span data-stu-id="cadd6-130">AdoEnums.PropertyAttributes.WRITE</span></span></p></td>
</tr>
</tbody>
</table>

