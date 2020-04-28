---
title: Элементы индекса (DAO)
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
# <a name="index-members-dao"></a><span data-ttu-id="18d92-102">Элементы индекса (DAO)</span><span class="sxs-lookup"><span data-stu-id="18d92-102">Index members (DAO)</span></span>


<span data-ttu-id="18d92-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="18d92-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="18d92-104">Объект index указывает порядок записей, доступ к которым осуществляется из таблиц базы данных, а также сведения о том, принимаются ли повторяющиеся записи, что обеспечивает эффективный доступ к данным.</span><span class="sxs-lookup"><span data-stu-id="18d92-104">Index objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data.</span></span> <span data-ttu-id="18d92-105">Для внешних баз данных объекты index описывают индексы, установленные для внешних таблиц (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18d92-105">For external databases, Index objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="18d92-106">Методы</span><span class="sxs-lookup"><span data-stu-id="18d92-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18d92-107">Имя</span><span class="sxs-lookup"><span data-stu-id="18d92-107">Name</span></span></p></th>
<th><p><span data-ttu-id="18d92-108">Описание</span><span class="sxs-lookup"><span data-stu-id="18d92-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18d92-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-110">Создает новый объект <strong><a href="field-object-dao.md">Field</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18d92-110">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18d92-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-112">Создает новый объект определяемого пользователем <strong><a href="property-object-dao.md">Свойства</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18d92-112">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="18d92-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="18d92-113">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="18d92-114">Имя</span><span class="sxs-lookup"><span data-stu-id="18d92-114">Name</span></span></p></th>
<th><p><span data-ttu-id="18d92-115">Описание</span><span class="sxs-lookup"><span data-stu-id="18d92-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="18d92-116"><strong><a href="index-clustered-property-dao.md">Сгруппирован</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-117">Задает или возвращает значение, которое указывает, представляет ли объект <strong>index</strong> кластеризованный индекс для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18d92-117">Sets or returns a value that indicates whether an <strong>Index</strong> object represents a clustered index for a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="18d92-118">Для чтения и записи, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="18d92-118">Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18d92-119"><strong><a href="index-distinctcount-property-dao.md">дистинкткаунт</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-120">Возвращает значение, которое указывает количество уникальных значений для объекта <strong><a href="index-object-dao.md">index</a></strong> , включенных в связанную таблицу (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18d92-120">Returns a value that indicates the number of unique values for the <strong><a href="index-object-dao.md">Index</a></strong> object that are included in the associated table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d92-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-122">Возвращает коллекцию <strong>Fields</strong>, которая представляет все объекты <strong>Field</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="18d92-122">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="18d92-123">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="18d92-123">Read/write.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18d92-124"><strong><a href="index-foreign-property-dao.md">Правительства</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-125">Возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">index</a></strong> внешний ключ в таблице (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18d92-125">Returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a foreign key in a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="18d92-126">.</span><span class="sxs-lookup"><span data-stu-id="18d92-126">.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d92-127"><strong><a href="index-ignorenulls-property-dao.md">игноренуллс</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-128">Задает или возвращает значение, которое указывает, имеют ли записи индекса значения NULL в полях индекса (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18d92-128">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18d92-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-130">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="18d92-130">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="18d92-131"><strong>Строка</strong> для чтения и записи, если объект не был добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="18d92-131">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="18d92-132"><strong>Строка</strong> , доступная только для чтения, если объект добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="18d92-132">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d92-133"><strong><a href="index-primary-property-dao.md">Основной</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-134">Задает или возвращает значение, которое указывает, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> первичный индекс ключа для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18d92-134">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a primary key index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18d92-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-136">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="18d92-136">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="18d92-137">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="18d92-137">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="18d92-138"><strong><a href="index-required-property-dao.md">Обязательно</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-138"><strong><a href="index-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-139">Задает или возвращает значение, которое указывает, требуется ли для объекта <strong><a href="field-object-dao.md">field</a></strong> значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="18d92-139">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="18d92-140"><strong><a href="index-unique-property-dao.md">Уникальный</a></strong></span><span class="sxs-lookup"><span data-stu-id="18d92-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span></span></p></td>
<td><p><span data-ttu-id="18d92-141">Задает или возвращает значение, указывающее, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> уникальный (ключ) индекс для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="18d92-141">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

