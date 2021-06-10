---
title: Элементы TableDef (DAO)
TOCTitle: TableDef Members
ms:assetid: bc55315e-bafe-d89e-ad31-fd4c9bb6486e
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822714(v=office.15)
ms:contentKeyID: 48547408
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ff9f6841b50b70f8846c829f0ee7b911c84c0e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314905"
---
# <a name="tabledef-members-dao"></a><span data-ttu-id="6f0bf-102">Элементы TableDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="6f0bf-102">TableDef members (DAO)</span></span>


<span data-ttu-id="6f0bf-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6f0bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f0bf-104">Объект TableDef представляет сохраненное определение основной или связанной таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-104">A TableDef object represents the stored definition of a base table or a linked table (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="6f0bf-105">Методы</span><span class="sxs-lookup"><span data-stu-id="6f0bf-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f0bf-106">Имя</span><span class="sxs-lookup"><span data-stu-id="6f0bf-106">Name</span></span></p></th>
<th><p><span data-ttu-id="6f0bf-107">Описание</span><span class="sxs-lookup"><span data-stu-id="6f0bf-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-108"><strong><a href="tabledef-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-108"><strong><a href="tabledef-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-109">Создает новый объект <strong><a href="field-object-dao.md">Field</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-109">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6f0bf-110">.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-110">.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0bf-111"><strong><a href="tabledef-createindex-method-dao.md">CreateIndex</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-111"><strong><a href="tabledef-createindex-method-dao.md">CreateIndex</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-112">Создает новый объект <strong><a href="index-object-dao.md">Index</a></strong> (только рабочие пространства Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-112">Creates a new <strong><a href="index-object-dao.md">Index</a></strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6f0bf-113">.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-113">.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-114"><strong><a href="tabledef-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-114"><strong><a href="tabledef-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-115">Создает новый объект Свойства, определенный <strong><a href="property-object-dao.md">пользователем</a></strong> (только рабочие пространства Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-115">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0bf-116"><strong><a href="tabledef-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-116"><strong><a href="tabledef-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-117">Создает новый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> и добавляет его в коллекцию <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-117">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-118"><strong><a href="tabledef-refreshlink-method-dao.md">RefreshLink</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-118"><strong><a href="tabledef-refreshlink-method-dao.md">RefreshLink</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-119">Обновляет сведения о подключении для связанной таблицы (только для рабочего пространства Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-119">Updates the connection information for a linked table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="6f0bf-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="6f0bf-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f0bf-121">Имя</span><span class="sxs-lookup"><span data-stu-id="6f0bf-121">Name</span></span></p></th>
<th><p><span data-ttu-id="6f0bf-122">Описание</span><span class="sxs-lookup"><span data-stu-id="6f0bf-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-123"><strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-123"><strong><a href="tabledef-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-124">Задает или возвращает значение, которое указывает одну или несколько характеристик объекта <strong>TableDef.</strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-124">Sets or returns a value that indicates one or more characteristics of a <strong>TableDef</strong> object.</span></span> <span data-ttu-id="6f0bf-125">Для чтения и записи, <strong>Long</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-125">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0bf-126"><strong><a href="tabledef-conflicttable-property-dao.md">ConflictTable</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-126"><strong><a href="tabledef-conflicttable-property-dao.md">ConflictTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-127">Возвращает имя таблицы конфликтов, содержащей записи баз данных, которые конфликтовали во время синхронизации двух реплик (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-127">Returns the name of a conflict table containing the database records that conflicted during the synchronization of two replicas (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6f0bf-128">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-128">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-129"><strong><a href="tabledef-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-129"><strong><a href="tabledef-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-130">Задает или возвращает значение, которое содержит сведения о связанной таблице.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-130">Sets or returns a value that provides information about a linked table.</span></span> <span data-ttu-id="6f0bf-131">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-131">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0bf-132"><strong><a href="tabledef-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-132"><strong><a href="tabledef-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-133">Возвращает дату и время создания объекта (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-133">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6f0bf-134">Только для чтения, <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-134">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-135"><strong><a href="tabledef-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-135"><strong><a href="tabledef-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-136">Возвращает коллекцию <strong>Fields</strong>, которая представляет все объекты <strong>Field</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-136">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="6f0bf-137">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-137">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0bf-138"><strong><a href="tabledef-indexes-property-dao.md">Indexes</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-138"><strong><a href="tabledef-indexes-property-dao.md">Indexes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-139">Возвращает <strong>коллекцию Indexes,</strong> которая содержит все сохраненные объекты <strong>Index</strong> для указанной таблицы.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-139">Returns an <strong>Indexes</strong> collection that contains all of the stored <strong>Index</strong> objects for the specified table.</span></span> <span data-ttu-id="6f0bf-140">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-140">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-141"><strong><a href="tabledef-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-141"><strong><a href="tabledef-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-142">Возвращает дату и время последнего изменения, выполненного в объекте.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-142">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="6f0bf-143">Только для чтения, <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-143">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0bf-144"><strong><a href="tabledef-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-144"><strong><a href="tabledef-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-145">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-145">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="6f0bf-146">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-146">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-147"><strong><a href="tabledef-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-147"><strong><a href="tabledef-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-148">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-148">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="6f0bf-149">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-149">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0bf-150"><strong><a href="tabledef-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-150"><strong><a href="tabledef-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-151">Возвращает общее количество записей в <strong><a href="tabledef-object-dao.md">объекте TableDef.</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-151">Returns the total number of records in a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object.</span></span> <span data-ttu-id="6f0bf-152">Только для чтения, <strong>Long</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-152">Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-153"><strong><a href="tabledef-replicafilter-property-dao.md">ReplicaFilter</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-153"><strong><a href="tabledef-replicafilter-property-dao.md">ReplicaFilter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-154">Задает или возвращает значение объекта <strong><a href="tabledef-object-dao.md">TableDef</a></strong> в частичной реплике, которая указывает, какой подмножество записей реплицируется в эту таблицу из полной реплики.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-154">Sets or returns a value on a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object within a partial replica that indicates which subset of records is replicated to that table from a full replica.</span></span> <span data-ttu-id="6f0bf-155">(Только для рабочих областей Microsoft Access.)</span><span class="sxs-lookup"><span data-stu-id="6f0bf-155">(Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0bf-156"><strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-156"><strong><a href="tabledef-sourcetablename-property-dao.md">SourceTableName</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-157">Задает или возвращает значение, которое указывает имя связанной таблицы или имя базовой таблицы (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-157">Sets or returns a value that specifies the name of a linked table or the name of a base table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-158"><strong><a href="tabledef-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-158"><strong><a href="tabledef-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-159">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-159">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="6f0bf-160">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-160">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f0bf-161"><strong><a href="tabledef-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-161"><strong><a href="tabledef-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-162">Задает или возвращает значение, которое проверяет данные в поле после его добавление или изменения в таблице (только для рабочих областей Microsoft Access). Чтение и запись, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-162">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f0bf-163"><strong><a href="tabledef-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="6f0bf-163"><strong><a href="tabledef-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6f0bf-164">Задает или возвращает значение, определяющее текст сообщения, которое отображает ваше приложение, если значение объекта <strong>Field</strong> не удовлетворяют правилу проверки, задаваемому настройкой параметра <strong>ValidationRule</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6f0bf-164">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="6f0bf-165">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="6f0bf-165">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

