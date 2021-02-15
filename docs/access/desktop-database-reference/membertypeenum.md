---
title: MemberTypeEnum (справочник по базе данных Access для настольных ПК)
TOCTitle: MemberTypeEnum
ms:assetid: 3b6f9fff-fe54-b917-9404-927e3a627e0b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249150(v=office.15)
ms:contentKeyID: 48544286
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 82d507457d9242daa92cc0218c87bae4d82759a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289206"
---
# <a name="membertypeenum"></a><span data-ttu-id="32c06-102">MemberTypeEnum</span><span class="sxs-lookup"><span data-stu-id="32c06-102">MemberTypeEnum</span></span>

<span data-ttu-id="32c06-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="32c06-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="32c06-104">Указывает параметр для свойства [Type](type-property-ado-md.md) объекта [Member.](member-object-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="32c06-104">Specifies the setting for the [Type](type-property-ado-md.md) property of a [Member](member-object-ado-md.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="32c06-105">Константа</span><span class="sxs-lookup"><span data-stu-id="32c06-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="32c06-106">Значение</span><span class="sxs-lookup"><span data-stu-id="32c06-106">Value</span></span></p></th>
<th><p><span data-ttu-id="32c06-107">Описание</span><span class="sxs-lookup"><span data-stu-id="32c06-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="32c06-108"><strong>adMemberAll</strong></span><span class="sxs-lookup"><span data-stu-id="32c06-108"><strong>adMemberAll</strong></span></span></p></td>
<td><p><span data-ttu-id="32c06-109">4 </span><span class="sxs-lookup"><span data-stu-id="32c06-109">4</span></span></p></td>
<td><p><span data-ttu-id="32c06-110">Указывает, что <strong>объект Member</strong> представляет все члены уровня.</span><span class="sxs-lookup"><span data-stu-id="32c06-110">Indicates that the <strong>Member</strong> object represents all members of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32c06-111"><strong>adMemberFormula</strong></span><span class="sxs-lookup"><span data-stu-id="32c06-111"><strong>adMemberFormula</strong></span></span></p></td>
<td><p><span data-ttu-id="32c06-112">3 </span><span class="sxs-lookup"><span data-stu-id="32c06-112">3</span></span></p></td>
<td><p><span data-ttu-id="32c06-113">Указывает, что объект <strong>Member</strong> вычисляется с помощью выражения формулы.</span><span class="sxs-lookup"><span data-stu-id="32c06-113">Indicates that the <strong>Member</strong> object is calculated using a formula expression.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32c06-114"><strong>adMemberMeasure</strong></span><span class="sxs-lookup"><span data-stu-id="32c06-114"><strong>adMemberMeasure</strong></span></span></p></td>
<td><p><span data-ttu-id="32c06-115">2 </span><span class="sxs-lookup"><span data-stu-id="32c06-115">2</span></span></p></td>
<td><p><span data-ttu-id="32c06-116">Указывает, что объект <strong>Member</strong> относится к измерению Measures и представляет атрибут атрибута-атрибута.</span><span class="sxs-lookup"><span data-stu-id="32c06-116">Indicates that the <strong>Member</strong> object belongs to the Measures dimension and represents a quantitative attribute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="32c06-117"><strong>adMemberRegular</strong></span><span class="sxs-lookup"><span data-stu-id="32c06-117"><strong>adMemberRegular</strong></span></span></p></td>
<td><p><span data-ttu-id="32c06-118">1 </span><span class="sxs-lookup"><span data-stu-id="32c06-118">1</span></span></p></td>
<td><p><span data-ttu-id="32c06-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="32c06-119">Default.</span></span> <span data-ttu-id="32c06-120">Указывает, что <strong>объект Member</strong> представляет экземпляр бизнес-сущности.</span><span class="sxs-lookup"><span data-stu-id="32c06-120">Indicates that the <strong>Member</strong> object represents an instance of a business entity.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="32c06-121"><strong>adMemberUnknown</strong></span><span class="sxs-lookup"><span data-stu-id="32c06-121"><strong>adMemberUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="32c06-122">0</span><span class="sxs-lookup"><span data-stu-id="32c06-122">0</span></span></p></td>
<td><p><span data-ttu-id="32c06-123">Не удается определить тип члена.</span><span class="sxs-lookup"><span data-stu-id="32c06-123">Cannot determine the type of the member.</span></span></p></td>
</tr>
</tbody>
</table>

