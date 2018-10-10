---
title: Property Members (DAO)
TOCTitle: Property Members
ms:assetid: 32658adb-f153-148d-a216-eb97b996579a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192303(v=office.15)
ms:contentKeyID: 48544076
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: fd6a24820e373c2b7ffcc1332f2fc5f9c2942481
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480583"
---
# <a name="property-members-dao"></a><span data-ttu-id="7a1e5-102">Property Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="7a1e5-102">Property Members (DAO)</span></span>


<span data-ttu-id="7a1e5-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="7a1e5-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7a1e5-104">Объект Property представляет характеристику встроенные или пользовательские объекта DAO.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-104">A Property object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="properties"></a><span data-ttu-id="7a1e5-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="7a1e5-105">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7a1e5-106">Имя</span><span class="sxs-lookup"><span data-stu-id="7a1e5-106">Name</span></span></p></th>
<th><p><span data-ttu-id="7a1e5-107">Описание</span><span class="sxs-lookup"><span data-stu-id="7a1e5-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7a1e5-108"><strong><a href="property-inherited-property-dao.md">Унаследованный</a></strong></span><span class="sxs-lookup"><span data-stu-id="7a1e5-108"><strong><a href="property-inherited-property-dao.md">Inherited</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e5-109">Возвращает значение, указывающее, является ли объект <strong><a href="property-object-dao.md">Свойства</a></strong> наследуется из базового объекта.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-109">Returns a value that indicates whether a <strong><a href="property-object-dao.md">Property</a></strong> object is inherited from an underlying object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a1e5-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="7a1e5-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e5-111">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-111">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="7a1e5-112">Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-112">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="7a1e5-113">Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-113">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a1e5-114"><strong><a href="property-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="7a1e5-114"><strong><a href="property-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e5-115">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-115">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="7a1e5-116">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-116">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7a1e5-117"><strong><a href="property-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="7a1e5-117"><strong><a href="property-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e5-118">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-118">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="7a1e5-119">Чтение и запись <strong>целое число</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-119">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7a1e5-120"><strong><a href="property-value-property-dao.md">Значение</a></strong></span><span class="sxs-lookup"><span data-stu-id="7a1e5-120"><strong><a href="property-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="7a1e5-121">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-121">Sets or returns the value of an object.</span></span> <span data-ttu-id="7a1e5-122">Чтение и запись <strong>типа Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="7a1e5-122">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

