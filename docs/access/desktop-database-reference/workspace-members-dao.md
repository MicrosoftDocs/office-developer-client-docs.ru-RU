---
title: Участники рабочих областей (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a2105c13f5f7ce9a75e7e18e20477d8b283543a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302596"
---
# <a name="workspace-members-dao"></a><span data-ttu-id="2e082-102">Участники рабочих областей (DAO)</span><span class="sxs-lookup"><span data-stu-id="2e082-102">Workspace members (DAO)</span></span>


<span data-ttu-id="2e082-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2e082-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2e082-104">Объект Workspace определяет именованный сеанс для пользователя.</span><span class="sxs-lookup"><span data-stu-id="2e082-104">A Workspace object defines a named session for a user.</span></span> <span data-ttu-id="2e082-105">Он содержит открытые базы данных и предоставляет механизмы для одновременных транзакций и (в рабочих областях Microsoft Access) поддержку защищенной рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="2e082-105">It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="methods"></a><span data-ttu-id="2e082-106">Методы</span><span class="sxs-lookup"><span data-stu-id="2e082-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e082-107">Имя</span><span class="sxs-lookup"><span data-stu-id="2e082-107">Name</span></span></p></th>
<th><p><span data-ttu-id="2e082-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2e082-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e082-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-110">Начинает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="2e082-110">Begins a new transaction.</span></span> <span data-ttu-id="2e082-111">Чтение и запись <strong>базы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e082-111">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e082-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-113">Закрывает открытую <strong>рабочую область</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e082-113">Closes an open <strong>Workspace</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e082-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-115">Завершает текущую транзакцию и сохраняет изменения.</span><span class="sxs-lookup"><span data-stu-id="2e082-115">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e082-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-117">Создает новый объект <strong><a href="database-object-dao.md">Database</a></strong> , сохраняет базу данных на диске и возвращает открытый объект <strong>базы данных</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2e082-117">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e082-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-119"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2e082-119"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2e082-120">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2e082-120">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2e082-121">Открывает объект <strong><a href="connection-object-dao.md">Connection</a></strong> в источнике данных ODBC (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="2e082-121">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e082-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-123">Открывает указанную базу данных в объекте <strong> <a href="workspace-object-dao.md">Workspace</a> </strong> и возвращает ссылку на объект <strong> <a href="database-object-dao.md">Database</a> </strong>, который ее представляет.</span><span class="sxs-lookup"><span data-stu-id="2e082-123">Opens a specified database in a <strong><a href="workspace-object-dao.md">Workspace</a></strong> object and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e082-124"><strong><a href="workspace-rollback-method-dao.md">Отката</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-125">Завершает текущую транзакцию и восстанавливает базы данных в объекте <strong>Workspace</strong> в том состоянии, в котором они были в момент начала текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="2e082-125">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="2e082-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="2e082-126">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2e082-127">Имя</span><span class="sxs-lookup"><span data-stu-id="2e082-127">Name</span></span></p></th>
<th><p><span data-ttu-id="2e082-128">Описание</span><span class="sxs-lookup"><span data-stu-id="2e082-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2e082-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-130">Возвращает коллекцию <strong>Connections</strong> , представляющую текущие подключения в указанной <strong>рабочей области</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e082-130">Returns a <strong>Connections</strong> collection that represents the current connections in the specified <strong>Workspace</strong>.</span></span> <span data-ttu-id="2e082-131">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2e082-131">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e082-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-133">Возвращает коллекцию <strong>баз данных</strong> , представляющую открытые базы данных в указанной <strong>рабочей области</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e082-133">Returns a <strong>Databases</strong> collection that represents the open databases in the specified <strong>Workspace</strong>.</span></span> <span data-ttu-id="2e082-134">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2e082-134">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e082-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">дефаулткурсордривер</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-136"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="2e082-136"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="2e082-137">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="2e082-137">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="2e082-138">Задает или возвращает тип драйвера курсора, используемого в соединении, созданном методами <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> или <strong><a href="dbengine-opendatabase-method-dao.md">openDatabase</a></strong> (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="2e082-138">Sets or returns the type of cursor driver used on the connection created by the <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> or <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> methods (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e082-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">исолатеодбктранс</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-140">Задает или возвращает значение, указывающее, изолированы ли множественные транзакции, использующие один и тот же источник данных ODBC, подключенный к ядру СУБД Microsoft Access (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="2e082-140">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e082-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-142">Задает или возвращает число секунд до возникновения ошибки при попытке входа в базу данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="2e082-142">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e082-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-144">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="2e082-144">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="2e082-145"><strong>Строка</strong> для чтения и записи, если объект не был добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="2e082-145">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="2e082-146"><strong>Строка</strong> , доступная только для чтения, если объект добавлен в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="2e082-146">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2e082-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-148">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="2e082-148">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="2e082-149">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="2e082-149">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2e082-150"><strong><a href="workspace-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="2e082-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="2e082-151">Задает или возвращает значение, указывающее операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="2e082-151">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="2e082-152">Только для чтения, <strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="2e082-152">Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

