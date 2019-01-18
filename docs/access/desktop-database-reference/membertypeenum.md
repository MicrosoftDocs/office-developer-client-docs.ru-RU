---
title: MemberTypeEnum (Справочник по для настольных баз данных Access)
TOCTitle: MemberTypeEnum
ms:assetid: 3b6f9fff-fe54-b917-9404-927e3a627e0b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249150(v=office.15)
ms:contentKeyID: 48544286
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 82d507457d9242daa92cc0218c87bae4d82759a3
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28718506"
---
# <a name="membertypeenum"></a><span data-ttu-id="ca5e9-102">MemberTypeEnum</span><span class="sxs-lookup"><span data-stu-id="ca5e9-102">MemberTypeEnum</span></span>

<span data-ttu-id="ca5e9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ca5e9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ca5e9-104">Задает свойство [типа](type-property-ado-md.md) объекта [члена](member-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="ca5e9-104">Specifies the setting for the [Type](type-property-ado-md.md) property of a [Member](member-object-ado-md.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ca5e9-105">Константа</span><span class="sxs-lookup"><span data-stu-id="ca5e9-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="ca5e9-106">Значение</span><span class="sxs-lookup"><span data-stu-id="ca5e9-106">Value</span></span></p></th>
<th><p><span data-ttu-id="ca5e9-107">Описание</span><span class="sxs-lookup"><span data-stu-id="ca5e9-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ca5e9-108"><strong>adMemberAll</strong></span><span class="sxs-lookup"><span data-stu-id="ca5e9-108"><strong>adMemberAll</strong></span></span></p></td>
<td><p><span data-ttu-id="ca5e9-109">4</span><span class="sxs-lookup"><span data-stu-id="ca5e9-109">4</span></span></p></td>
<td><p><span data-ttu-id="ca5e9-110">Указывает, что <strong>объект</strong> представляет все элементы уровня.</span><span class="sxs-lookup"><span data-stu-id="ca5e9-110">Indicates that the <strong>Member</strong> object represents all members of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca5e9-111"><strong>adMemberFormula</strong></span><span class="sxs-lookup"><span data-stu-id="ca5e9-111"><strong>adMemberFormula</strong></span></span></p></td>
<td><p><span data-ttu-id="ca5e9-112">3</span><span class="sxs-lookup"><span data-stu-id="ca5e9-112">3</span></span></p></td>
<td><p><span data-ttu-id="ca5e9-113">Указывает, что объект <strong>члена</strong> выражен в формуле.</span><span class="sxs-lookup"><span data-stu-id="ca5e9-113">Indicates that the <strong>Member</strong> object is calculated using a formula expression.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca5e9-114"><strong>adMemberMeasure</strong></span><span class="sxs-lookup"><span data-stu-id="ca5e9-114"><strong>adMemberMeasure</strong></span></span></p></td>
<td><p><span data-ttu-id="ca5e9-115">2</span><span class="sxs-lookup"><span data-stu-id="ca5e9-115">2</span></span></p></td>
<td><p><span data-ttu-id="ca5e9-116">Указывает, что объект <strong>члена</strong> относится к измерению меры и представляет количественный атрибут.</span><span class="sxs-lookup"><span data-stu-id="ca5e9-116">Indicates that the <strong>Member</strong> object belongs to the Measures dimension and represents a quantitative attribute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ca5e9-117"><strong>adMemberRegular</strong></span><span class="sxs-lookup"><span data-stu-id="ca5e9-117"><strong>adMemberRegular</strong></span></span></p></td>
<td><p><span data-ttu-id="ca5e9-118">1</span><span class="sxs-lookup"><span data-stu-id="ca5e9-118">1</span></span></p></td>
<td><p><span data-ttu-id="ca5e9-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ca5e9-119">Default.</span></span> <span data-ttu-id="ca5e9-120">Указывает, что <strong>объект</strong> представляет экземпляр объекта юридическим лицом.</span><span class="sxs-lookup"><span data-stu-id="ca5e9-120">Indicates that the <strong>Member</strong> object represents an instance of a business entity.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ca5e9-121"><strong>adMemberUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="ca5e9-121"><strong>adMemberUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="ca5e9-122">0</span><span class="sxs-lookup"><span data-stu-id="ca5e9-122">0</span></span></p></td>
<td><p><span data-ttu-id="ca5e9-123">Не может определить тип элемента.</span><span class="sxs-lookup"><span data-stu-id="ca5e9-123">Cannot determine the type of the member.</span></span></p></td>
</tr>
</tbody>
</table>

