---
title: Элементы Property (DAO)
TOCTitle: Property Members
ms:assetid: 32658adb-f153-148d-a216-eb97b996579a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192303(v=office.15)
ms:contentKeyID: 48544076
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe60c12a85eff0dd8f796f9affeef71979dac580
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301213"
---
# <a name="property-members-dao"></a><span data-ttu-id="f118d-102">Элементы Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="f118d-102">Property members (DAO)</span></span>


<span data-ttu-id="f118d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f118d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f118d-104">Объект Property представляет встроенную или определяемую пользователем характеристику объекта DAO.</span><span class="sxs-lookup"><span data-stu-id="f118d-104">A Property object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="properties"></a><span data-ttu-id="f118d-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="f118d-105">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f118d-106">Имя</span><span class="sxs-lookup"><span data-stu-id="f118d-106">Name</span></span></p></th>
<th><p><span data-ttu-id="f118d-107">Описание</span><span class="sxs-lookup"><span data-stu-id="f118d-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f118d-108"><strong><a href="property-inherited-property-dao.md">Унаследованные</a></strong></span><span class="sxs-lookup"><span data-stu-id="f118d-108"><strong><a href="property-inherited-property-dao.md">Inherited</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f118d-109">Возвращает значение, которое указывает, наследуется ли объект <strong><a href="property-object-dao.md">Свойства</a></strong> из базового объекта.</span><span class="sxs-lookup"><span data-stu-id="f118d-109">Returns a value that indicates whether a <strong><a href="property-object-dao.md">Property</a></strong> object is inherited from an underlying object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f118d-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="f118d-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f118d-111">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="f118d-111">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="f118d-112"><strong>Строка</strong> для чтения и записи, если объект не был добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f118d-112">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="f118d-113"><strong>Строка</strong> , доступная только для чтения, если объект добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f118d-113">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f118d-114"><strong><a href="property-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="f118d-114"><strong><a href="property-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f118d-115">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="f118d-115">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="f118d-116">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f118d-116">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f118d-117"><strong><a href="property-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="f118d-117"><strong><a href="property-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f118d-118">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="f118d-118">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="f118d-119">Для чтения и записи, <strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="f118d-119">Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f118d-120"><strong><a href="property-value-property-dao.md">Значение</a></strong></span><span class="sxs-lookup"><span data-stu-id="f118d-120"><strong><a href="property-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f118d-121">Задает или возвращает значение объекта.</span><span class="sxs-lookup"><span data-stu-id="f118d-121">Sets or returns the value of an object.</span></span> <span data-ttu-id="f118d-122">Для чтения и записи, <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="f118d-122">Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

