---
title: RelationAttributeEnum Enumeration (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4c4d7a2b622e382461bcf1b4171a5aa85f036854
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482503"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="aa479-102">RelationAttributeEnum Enumeration (DAO)</span><span class="sxs-lookup"><span data-stu-id="aa479-102">RelationAttributeEnum Enumeration (DAO)</span></span>


<span data-ttu-id="aa479-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="aa479-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="aa479-104">Используется со свойством **атрибуты** для определения атрибутов объекта **связи** .</span><span class="sxs-lookup"><span data-stu-id="aa479-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="aa479-105">Имя</span><span class="sxs-lookup"><span data-stu-id="aa479-105">Name</span></span></p></th>
<th><p><span data-ttu-id="aa479-106">Значение</span><span class="sxs-lookup"><span data-stu-id="aa479-106">Value</span></span></p></th>
<th><p><span data-ttu-id="aa479-107">Описание</span><span class="sxs-lookup"><span data-stu-id="aa479-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa479-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="aa479-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="aa479-109">4096</span><span class="sxs-lookup"><span data-stu-id="aa479-109">4096</span></span></p></td>
<td><p><span data-ttu-id="aa479-110">Удаление cascade</span><span class="sxs-lookup"><span data-stu-id="aa479-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa479-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="aa479-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="aa479-112">2</span><span class="sxs-lookup"><span data-stu-id="aa479-112">2</span></span></p></td>
<td><p><span data-ttu-id="aa479-113">Отношение не применяется (не целостность данных)</span><span class="sxs-lookup"><span data-stu-id="aa479-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa479-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="aa479-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="aa479-115">4</span><span class="sxs-lookup"><span data-stu-id="aa479-115">4</span></span></p></td>
<td><p><span data-ttu-id="aa479-116">Связь существует в базе данных, содержащий два связанных таблиц</span><span class="sxs-lookup"><span data-stu-id="aa479-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa479-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="aa479-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="aa479-118">16777216</span><span class="sxs-lookup"><span data-stu-id="aa479-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="aa479-119">Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="aa479-119">Microsoft Access only.</span></span> <span data-ttu-id="aa479-120">В режиме конструктора отображение LEFT JOIN как тип связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa479-120">In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa479-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="aa479-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="aa479-122">33554432</span><span class="sxs-lookup"><span data-stu-id="aa479-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="aa479-123">Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="aa479-123">Microsoft Access only.</span></span> <span data-ttu-id="aa479-124">В режиме конструктора отображение RIGHT JOIN как тип связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa479-124">In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa479-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="aa479-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="aa479-126">1</span><span class="sxs-lookup"><span data-stu-id="aa479-126">1</span></span></p></td>
<td><p><span data-ttu-id="aa479-127">Двустороннее отношение</span><span class="sxs-lookup"><span data-stu-id="aa479-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa479-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="aa479-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="aa479-129">256</span><span class="sxs-lookup"><span data-stu-id="aa479-129">256</span></span></p></td>
<td><p><span data-ttu-id="aa479-130">Cascade обновлений</span><span class="sxs-lookup"><span data-stu-id="aa479-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

