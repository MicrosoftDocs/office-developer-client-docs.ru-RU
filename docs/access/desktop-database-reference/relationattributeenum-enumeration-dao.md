---
title: Переопределение RelationAttributeEnum (DAO)
TOCTitle: RelationAttributeEnum Enumeration
ms:assetid: ce8d0696-66d7-052f-1313-64baee3442ed
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834499(v=office.15)
ms:contentKeyID: 48547787
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dbb8ca2e1a63154f17bd814a26fe79ed405765cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306981"
---
# <a name="relationattributeenum-enumeration-dao"></a><span data-ttu-id="b8b83-102">Переопределение RelationAttributeEnum (DAO)</span><span class="sxs-lookup"><span data-stu-id="b8b83-102">RelationAttributeEnum enumeration (DAO)</span></span>


<span data-ttu-id="b8b83-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b8b83-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b8b83-104">Используется с **свойством Атрибуты** для определения атрибутов объекта **Relation.**</span><span class="sxs-lookup"><span data-stu-id="b8b83-104">Used with the **Attributes** property to determine attributes of a **Relation** object.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b8b83-105">Имя</span><span class="sxs-lookup"><span data-stu-id="b8b83-105">Name</span></span></p></th>
<th><p><span data-ttu-id="b8b83-106">Значение</span><span class="sxs-lookup"><span data-stu-id="b8b83-106">Value</span></span></p></th>
<th><p><span data-ttu-id="b8b83-107">Описание</span><span class="sxs-lookup"><span data-stu-id="b8b83-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8b83-108">dbRelationDeleteCascade</span><span class="sxs-lookup"><span data-stu-id="b8b83-108">dbRelationDeleteCascade</span></span></p></td>
<td><p><span data-ttu-id="b8b83-109">4096</span><span class="sxs-lookup"><span data-stu-id="b8b83-109">4096</span></span></p></td>
<td><p><span data-ttu-id="b8b83-110">Каскад удалений</span><span class="sxs-lookup"><span data-stu-id="b8b83-110">Deletions cascade</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b83-111">dbRelationDontEnforce</span><span class="sxs-lookup"><span data-stu-id="b8b83-111">dbRelationDontEnforce</span></span></p></td>
<td><p><span data-ttu-id="b8b83-112">2</span><span class="sxs-lookup"><span data-stu-id="b8b83-112">2</span></span></p></td>
<td><p><span data-ttu-id="b8b83-113">Отношение, не принудительное (без целостности ссылок)</span><span class="sxs-lookup"><span data-stu-id="b8b83-113">Relationship not enforced (no referential integrity)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b83-114">dbRelationInherited</span><span class="sxs-lookup"><span data-stu-id="b8b83-114">dbRelationInherited</span></span></p></td>
<td><p><span data-ttu-id="b8b83-115">4 </span><span class="sxs-lookup"><span data-stu-id="b8b83-115">4</span></span></p></td>
<td><p><span data-ttu-id="b8b83-116">Связь существует в базе данных, содержащей две связанные таблицы</span><span class="sxs-lookup"><span data-stu-id="b8b83-116">Relationship exists in the database containing the two linked tables</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b83-117">dbRelationLeft</span><span class="sxs-lookup"><span data-stu-id="b8b83-117">dbRelationLeft</span></span></p></td>
<td><p><span data-ttu-id="b8b83-118">16777216</span><span class="sxs-lookup"><span data-stu-id="b8b83-118">16777216</span></span></p></td>
<td><p><span data-ttu-id="b8b83-119">Только Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b8b83-119">Microsoft Access only.</span></span> <span data-ttu-id="b8b83-120">В представлении Design отобразить ЛЕВЫЙ JOIN в виде типа присоединиться по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b8b83-120">In Design view, display a LEFT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b83-121">dbRelationRight</span><span class="sxs-lookup"><span data-stu-id="b8b83-121">dbRelationRight</span></span></p></td>
<td><p><span data-ttu-id="b8b83-122">33554432</span><span class="sxs-lookup"><span data-stu-id="b8b83-122">33554432</span></span></p></td>
<td><p><span data-ttu-id="b8b83-123">Только Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="b8b83-123">Microsoft Access only.</span></span> <span data-ttu-id="b8b83-124">В представлении Design отобразить RIGHT JOIN в качестве типа присоединиться по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b8b83-124">In Design view, display a RIGHT JOIN as the default join type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8b83-125">dbRelationUnique</span><span class="sxs-lookup"><span data-stu-id="b8b83-125">dbRelationUnique</span></span></p></td>
<td><p><span data-ttu-id="b8b83-126">1</span><span class="sxs-lookup"><span data-stu-id="b8b83-126">1</span></span></p></td>
<td><p><span data-ttu-id="b8b83-127">Отношение один к одному</span><span class="sxs-lookup"><span data-stu-id="b8b83-127">One-to-one relationship</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8b83-128">dbRelationUpdateCascade</span><span class="sxs-lookup"><span data-stu-id="b8b83-128">dbRelationUpdateCascade</span></span></p></td>
<td><p><span data-ttu-id="b8b83-129">256</span><span class="sxs-lookup"><span data-stu-id="b8b83-129">256</span></span></p></td>
<td><p><span data-ttu-id="b8b83-130">Каскад обновлений</span><span class="sxs-lookup"><span data-stu-id="b8b83-130">Updates cascade</span></span></p></td>
</tr>
</tbody>
</table>

