---
title: Index Members (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 18f885dadb5ef86f78ed0a19ca9b2a5feb424b34
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483175"
---
# <a name="index-members-dao"></a><span data-ttu-id="6b3df-102">Index Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="6b3df-102">Index Members (DAO)</span></span>


<span data-ttu-id="6b3df-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6b3df-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6b3df-104">Объекты индекса указать порядок записей, доступного из таблицы базы данных и принимаются ли повторяющихся записей, предоставляя эффективного доступа к данным.</span><span class="sxs-lookup"><span data-stu-id="6b3df-104">Index objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data.</span></span> <span data-ttu-id="6b3df-105">Для внешних баз данных объекты индекса описывают индексов, установленных для внешних таблиц (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b3df-105">For external databases, Index objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="6b3df-106">Методы</span><span class="sxs-lookup"><span data-stu-id="6b3df-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b3df-107">Имя</span><span class="sxs-lookup"><span data-stu-id="6b3df-107">Name</span></span></p></th>
<th><p><span data-ttu-id="6b3df-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6b3df-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b3df-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-110">Создает новый объект <strong><a href="field-object-dao.md">поля</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b3df-110">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b3df-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-112">Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b3df-112">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="6b3df-113">Свойства</span><span class="sxs-lookup"><span data-stu-id="6b3df-113">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6b3df-114">Имя</span><span class="sxs-lookup"><span data-stu-id="6b3df-114">Name</span></span></p></th>
<th><p><span data-ttu-id="6b3df-115">Описание</span><span class="sxs-lookup"><span data-stu-id="6b3df-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b3df-116"><strong><a href="index-clustered-property-dao.md">Кластерные</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-117">Задает или возвращает значение, указывающее, представляет ли объект <strong>индекса</strong> кластеризованных индекса для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b3df-117">Sets or returns a value that indicates whether an <strong>Index</strong> object represents a clustered index for a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6b3df-118">Для чтения и записи, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="6b3df-118">Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b3df-119"><strong><a href="index-distinctcount-property-dao.md">Число различных значений</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-120">Возвращает значение, указывающее количество уникальных значений для объекта <strong><a href="index-object-dao.md">индекса</a></strong> , содержащихся в связанной таблице (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b3df-120">Returns a value that indicates the number of unique values for the <strong><a href="index-object-dao.md">Index</a></strong> object that are included in the associated table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b3df-121"><strong><a href="index-fields-property-dao.md">Поля</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-122">Возвращает коллекцию <strong>полей</strong> , представляющую все хранятся объекты <strong>поля</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6b3df-122">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="6b3df-123">Для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="6b3df-123">Read/write.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b3df-124"><strong><a href="index-foreign-property-dao.md">Внешний</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-125">Возвращает значение, указывающее, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> внешний ключ в таблице (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b3df-125">Returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a foreign key in a table (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6b3df-126">.</span><span class="sxs-lookup"><span data-stu-id="6b3df-126"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b3df-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-128">Задает или возвращает значение, указывающее, имеют ли записи, для которых значения Null в полях индекса записи индекса (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b3df-128">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b3df-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-130">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6b3df-130">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="6b3df-131">Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="6b3df-131">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="6b3df-132">Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="6b3df-132">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b3df-133"><strong><a href="index-primary-property-dao.md">Основной</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-134">Задает или возвращает значение, указывающее, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> индекс первичного ключа для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b3df-134">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a primary key index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b3df-135"><strong><a href="index-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-136">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6b3df-136">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="6b3df-137">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6b3df-137">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b3df-138"><strong><a href="index-required-property-dao.md">Обязательный</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-138"><strong><a href="index-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-139">Задает или возвращает значение, которое указывает, требуется ли объект <strong><a href="field-object-dao.md">поля</a></strong> ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="6b3df-139">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b3df-140"><strong><a href="index-unique-property-dao.md">Уникальный</a></strong></span><span class="sxs-lookup"><span data-stu-id="6b3df-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6b3df-141">Задает или возвращает значение, указывающее, представляет ли объект <strong><a href="index-object-dao.md">индекса</a></strong> уникальный индекс (основные) для таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6b3df-141">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

