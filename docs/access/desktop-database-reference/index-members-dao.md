---
title: Index members (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291798"
---
# <a name="index-members-dao"></a><span data-ttu-id="55a17-102">Index members (DAO)</span><span class="sxs-lookup"><span data-stu-id="55a17-102">Index members (DAO)</span></span>


<span data-ttu-id="55a17-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="55a17-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="55a17-104">Объекты индекса определяют порядок записей, доступных из таблиц баз данных, а также то, принимаются ли дублирующиеся записи, обеспечивая эффективный доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="55a17-104">Index objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data.</span></span> <span data-ttu-id="55a17-105">Для внешних баз данных объекты индекса описывают индексы, установленные для внешних таблиц (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55a17-105">For external databases, Index objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="55a17-106">Методы</span><span class="sxs-lookup"><span data-stu-id="55a17-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55a17-107">Имя</span><span class="sxs-lookup"><span data-stu-id="55a17-107">Name</span></span></p></th>
<th><p><span data-ttu-id="55a17-108">Описание</span><span class="sxs-lookup"><span data-stu-id="55a17-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55a17-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-110">Создает новый объект <strong><a href="field-object-dao.md">Field</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55a17-110">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55a17-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-112">Создает объект Property, определенный <strong><a href="property-object-dao.md">пользователем</a></strong> (только для рабочих пространств Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55a17-112">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="55a17-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="55a17-113">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="55a17-114">Имя</span><span class="sxs-lookup"><span data-stu-id="55a17-114">Name</span></span></p></th>
<th><p><span data-ttu-id="55a17-115">Описание</span><span class="sxs-lookup"><span data-stu-id="55a17-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55a17-116"><strong><a href="index-clustered-property-dao.md">Кластерная</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-117">Задает или возвращает значение, которое указывает, представляет ли объект <strong>Index</strong> кластерный индекс для таблицы (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55a17-117">Sets or returns a value that indicates whether an <strong>Index</strong> object represents a clustered index for a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="55a17-118">Для чтения и записи, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="55a17-118">Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55a17-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-120">Возвращает значение, которое указывает количество уникальных значений для объекта <strong><a href="index-object-dao.md">Index,</a></strong> включенных в связанную таблицу (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55a17-120">Returns a value that indicates the number of unique values for the <strong><a href="index-object-dao.md">Index</a></strong> object that are included in the associated table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55a17-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-122">Возвращает коллекцию <strong>Fields</strong>, которая представляет все объекты <strong>Field</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="55a17-122">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="55a17-123">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="55a17-123">Read/write.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55a17-124"><strong><a href="index-foreign-property-dao.md">Внешняя</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-125">Возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">Index</a></strong> внешние ключи в таблице (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55a17-125">Returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a foreign key in a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="55a17-126">.</span><span class="sxs-lookup"><span data-stu-id="55a17-126">.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55a17-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-128">Задает или возвращает значение, которое указывает, имеют ли записи с значениями NULL в полях индекса записи индекса (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55a17-128">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55a17-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-130">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="55a17-130">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="55a17-131">Строка <strong>чтения</strong> и записи, если объект не был appended к коллекции.</span><span class="sxs-lookup"><span data-stu-id="55a17-131">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="55a17-132">Строка только <strong>для</strong> чтения, если объект был appended к коллекции.</span><span class="sxs-lookup"><span data-stu-id="55a17-132">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55a17-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-134">Задает или возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">Index</a></strong> индекс индекса первичного ключа для таблицы (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55a17-134">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a primary key index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55a17-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-136">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="55a17-136">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="55a17-137">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="55a17-137">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55a17-138"><strong><a href="index-required-property-dao.md">Обязательно</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-138"><strong><a href="index-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-139">Задает или возвращает значение, которое указывает, требуется ли для объекта <strong><a href="field-object-dao.md">Field</a></strong> значение, не относящеся к NULL.</span><span class="sxs-lookup"><span data-stu-id="55a17-139">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55a17-140"><strong><a href="index-unique-property-dao.md">Уникальный</a></strong></span><span class="sxs-lookup"><span data-stu-id="55a17-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span></span></p></td>
<td><p><span data-ttu-id="55a17-141">Задает или возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">Index</a></strong> уникальный индекс (ключ) для таблицы (только для рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="55a17-141">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

