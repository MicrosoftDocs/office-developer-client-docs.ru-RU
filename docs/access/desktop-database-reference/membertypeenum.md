---
title: Мембертипинум (Справочник по базам данных Access на компьютере)
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
# <a name="membertypeenum"></a><span data-ttu-id="f6ac8-102">MemberTypeEnum</span><span class="sxs-lookup"><span data-stu-id="f6ac8-102">MemberTypeEnum</span></span>

<span data-ttu-id="f6ac8-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f6ac8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f6ac8-104">Задает параметр для свойства [Type](type-property-ado-md.md) объекта [member](member-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="f6ac8-104">Specifies the setting for the [Type](type-property-ado-md.md) property of a [Member](member-object-ado-md.md) object.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f6ac8-105">Константа</span><span class="sxs-lookup"><span data-stu-id="f6ac8-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="f6ac8-106">Значение</span><span class="sxs-lookup"><span data-stu-id="f6ac8-106">Value</span></span></p></th>
<th><p><span data-ttu-id="f6ac8-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f6ac8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f6ac8-108"><strong>Адмембералл</strong></span><span class="sxs-lookup"><span data-stu-id="f6ac8-108"><strong>adMemberAll</strong></span></span></p></td>
<td><p><span data-ttu-id="f6ac8-109">SP4</span><span class="sxs-lookup"><span data-stu-id="f6ac8-109">4</span></span></p></td>
<td><p><span data-ttu-id="f6ac8-110">Указывает, что объект <strong>member</strong> представляет все члены уровня.</span><span class="sxs-lookup"><span data-stu-id="f6ac8-110">Indicates that the <strong>Member</strong> object represents all members of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ac8-111"><strong>Адмемберформула</strong></span><span class="sxs-lookup"><span data-stu-id="f6ac8-111"><strong>adMemberFormula</strong></span></span></p></td>
<td><p><span data-ttu-id="f6ac8-112">4</span><span class="sxs-lookup"><span data-stu-id="f6ac8-112">3</span></span></p></td>
<td><p><span data-ttu-id="f6ac8-113">Указывает, что объект <strong>member</strong> вычисляется с помощью выражения формулы.</span><span class="sxs-lookup"><span data-stu-id="f6ac8-113">Indicates that the <strong>Member</strong> object is calculated using a formula expression.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ac8-114"><strong>Адмембермеасуре</strong></span><span class="sxs-lookup"><span data-stu-id="f6ac8-114"><strong>adMemberMeasure</strong></span></span></p></td>
<td><p><span data-ttu-id="f6ac8-115">2</span><span class="sxs-lookup"><span data-stu-id="f6ac8-115">2</span></span></p></td>
<td><p><span data-ttu-id="f6ac8-116">Указывает, что объект <strong>member</strong> принадлежит измерению Measures и представляет количественный атрибут.</span><span class="sxs-lookup"><span data-stu-id="f6ac8-116">Indicates that the <strong>Member</strong> object belongs to the Measures dimension and represents a quantitative attribute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f6ac8-117"><strong>Адмемберрегулар</strong></span><span class="sxs-lookup"><span data-stu-id="f6ac8-117"><strong>adMemberRegular</strong></span></span></p></td>
<td><p><span data-ttu-id="f6ac8-118">1,1</span><span class="sxs-lookup"><span data-stu-id="f6ac8-118">1</span></span></p></td>
<td><p><span data-ttu-id="f6ac8-119">Значение, используемое по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f6ac8-119">Default.</span></span> <span data-ttu-id="f6ac8-120">Указывает, что объект <strong>member</strong> представляет экземпляр бизнес-объекта.</span><span class="sxs-lookup"><span data-stu-id="f6ac8-120">Indicates that the <strong>Member</strong> object represents an instance of a business entity.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f6ac8-121"><strong>Адмемберункновн</strong></span><span class="sxs-lookup"><span data-stu-id="f6ac8-121"><strong>adMemberUnknown</strong></span></span></p></td>
<td><p><span data-ttu-id="f6ac8-122">нуль</span><span class="sxs-lookup"><span data-stu-id="f6ac8-122">0</span></span></p></td>
<td><p><span data-ttu-id="f6ac8-123">Не удается определить тип члена.</span><span class="sxs-lookup"><span data-stu-id="f6ac8-123">Cannot determine the type of the member.</span></span></p></td>
</tr>
</tbody>
</table>

