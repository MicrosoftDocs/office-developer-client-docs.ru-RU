---
title: Члены документа (DAO)
TOCTitle: Document Members
ms:assetid: 8de770e6-e4d1-372a-3ef8-8539c921b41f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197365(v=office.15)
ms:contentKeyID: 48546270
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d21151b2a30ec44b717031f2b0b8a8f506f22193
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930422"
---
# <a name="document-members-dao"></a><span data-ttu-id="b2e90-102">Члены документа (DAO)</span><span class="sxs-lookup"><span data-stu-id="b2e90-102">Document members (DAO)</span></span>


<span data-ttu-id="b2e90-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b2e90-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b2e90-104">Объект Document содержит сведения о один экземпляр объекта.</span><span class="sxs-lookup"><span data-stu-id="b2e90-104">A Document object includes information about one instance of an object.</span></span> <span data-ttu-id="b2e90-105">Объект может быть базы данных, сохраненные в таблице, запрос или связь (Microsoft Access базами данных, ядро только).</span><span class="sxs-lookup"><span data-stu-id="b2e90-105">The object can be a database, saved table, query, or relationship (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="b2e90-106">Методы</span><span class="sxs-lookup"><span data-stu-id="b2e90-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2e90-107">Имя</span><span class="sxs-lookup"><span data-stu-id="b2e90-107">Name</span></span></p></th>
<th><p><span data-ttu-id="b2e90-108">Описание</span><span class="sxs-lookup"><span data-stu-id="b2e90-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2e90-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="b2e90-109"><strong><a href="document-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b2e90-110">Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b2e90-110">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="b2e90-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="b2e90-111">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b2e90-112">Имя</span><span class="sxs-lookup"><span data-stu-id="b2e90-112">Name</span></span></p></th>
<th><p><span data-ttu-id="b2e90-113">Описание</span><span class="sxs-lookup"><span data-stu-id="b2e90-113">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b2e90-114"><strong><a href="document-container-property-dao.md">Контейнер</a></strong></span><span class="sxs-lookup"><span data-stu-id="b2e90-114"><strong><a href="document-container-property-dao.md">Container</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b2e90-115">Возвращает имя объекта <strong><a href="container-object-dao.md">контейнера</a></strong> , которому принадлежит объект <strong>Document</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b2e90-115">Returns the name of the <strong><a href="container-object-dao.md">Container</a></strong> object to which a <strong>Document</strong> object belongs (Microsoft Access workspaces only).</span></span> <span data-ttu-id="b2e90-116">.</span><span class="sxs-lookup"><span data-stu-id="b2e90-116"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2e90-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="b2e90-117"><strong><a href="document-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b2e90-118">Возвращает дату и время создания объекта.</span><span class="sxs-lookup"><span data-stu-id="b2e90-118">Returns the date and time that an object was created.</span></span> <span data-ttu-id="b2e90-119">Только для чтения <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2e90-119">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2e90-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="b2e90-120"><strong><a href="document-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b2e90-121">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="b2e90-121">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="b2e90-122">Только для чтения <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2e90-122">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b2e90-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="b2e90-123"><strong><a href="document-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b2e90-124">Возвращает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="b2e90-124">Returns the name of the specified object.</span></span> <span data-ttu-id="b2e90-125">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2e90-125">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b2e90-126"><strong><a href="document-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="b2e90-126"><strong><a href="document-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="b2e90-127">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="b2e90-127">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="b2e90-128">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b2e90-128">Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

