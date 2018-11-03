---
title: Перечисление RelationAttributeEnum (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: edcf578780a2ffe1f384aeb590c6bea16ca9376f
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25945777"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="dcdfd-102">Перечисление RelationAttributeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="dcdfd-102">RelationAttributeEnum enumeration (DAO)</span></span>


<span data-ttu-id="dcdfd-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcdfd-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dcdfd-104">Используется со свойством **атрибуты** для определения атрибутов объекта **связи** .</span><span class="sxs-lookup"><span data-stu-id="dcdfd-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="dcdfd-105">Имя</span><span class="sxs-lookup"><span data-stu-id="dcdfd-105">Name</span></span></p></th>
<th><p><span data-ttu-id="dcdfd-106">Значение</span><span class="sxs-lookup"><span data-stu-id="dcdfd-106">Value</span></span></p></th>
<th><p><span data-ttu-id="dcdfd-107">Описание</span><span class="sxs-lookup"><span data-stu-id="dcdfd-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dcdfd-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="dcdfd-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-109">4096</span><span class="sxs-lookup"><span data-stu-id="dcdfd-109">4096</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-110">Удаление cascade</span><span class="sxs-lookup"><span data-stu-id="dcdfd-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcdfd-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="dcdfd-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-112">2</span><span class="sxs-lookup"><span data-stu-id="dcdfd-112">2</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-113">Отношение не применяется (не целостность данных)</span><span class="sxs-lookup"><span data-stu-id="dcdfd-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcdfd-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="dcdfd-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-115">4</span><span class="sxs-lookup"><span data-stu-id="dcdfd-115">4</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-116">Связь существует в базе данных, содержащий два связанных таблиц</span><span class="sxs-lookup"><span data-stu-id="dcdfd-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcdfd-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="dcdfd-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-118">16777216</span><span class="sxs-lookup"><span data-stu-id="dcdfd-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-119">Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-119">Microsoft Access only.</span></span> <span data-ttu-id="dcdfd-120">В режиме конструктора отображение LEFT JOIN как тип связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-120">In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcdfd-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="dcdfd-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-122">33554432</span><span class="sxs-lookup"><span data-stu-id="dcdfd-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-123">Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-123">Microsoft Access only.</span></span> <span data-ttu-id="dcdfd-124">В режиме конструктора отображение RIGHT JOIN как тип связи по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="dcdfd-124">In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dcdfd-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="dcdfd-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-126">1</span><span class="sxs-lookup"><span data-stu-id="dcdfd-126">1</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-127">Двустороннее отношение</span><span class="sxs-lookup"><span data-stu-id="dcdfd-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dcdfd-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="dcdfd-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-129">256</span><span class="sxs-lookup"><span data-stu-id="dcdfd-129">256</span></span></p></td>
<td><p><span data-ttu-id="dcdfd-130">Cascade обновлений</span><span class="sxs-lookup"><span data-stu-id="dcdfd-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

