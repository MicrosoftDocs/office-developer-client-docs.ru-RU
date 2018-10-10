---
title: Workspace Members (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04dd82fcdb3bd9be0581ea5172429960769b31af
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483053"
---
# <a name="workspace-members-dao"></a><span data-ttu-id="6314a-102">Workspace Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="6314a-102">Workspace Members (DAO)</span></span>


<span data-ttu-id="6314a-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6314a-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6314a-104">Объект рабочей области определяет именованный сеанса для пользователя.</span><span class="sxs-lookup"><span data-stu-id="6314a-104">A Workspace object defines a named session for a user.</span></span> <span data-ttu-id="6314a-105">Содержит open баз данных и предоставляет механизмы для одновременных операций и, в рабочих областях Microsoft Access безопасного поддержка рабочей группы.</span><span class="sxs-lookup"><span data-stu-id="6314a-105">It contains open databases and provides mechanisms for simultaneous transactions and, in Microsoft Access workspaces, secure workgroup support.</span></span>

## <a name="methods"></a><span data-ttu-id="6314a-106">Методы</span><span class="sxs-lookup"><span data-stu-id="6314a-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6314a-107">Имя</span><span class="sxs-lookup"><span data-stu-id="6314a-107">Name</span></span></p></th>
<th><p><span data-ttu-id="6314a-108">Описание</span><span class="sxs-lookup"><span data-stu-id="6314a-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6314a-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-109"><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-110">Начало новой транзакции.</span><span class="sxs-lookup"><span data-stu-id="6314a-110">Begins a new transaction.</span></span> <span data-ttu-id="6314a-111">Чтение и запись <strong>базы данных</strong>.</span><span class="sxs-lookup"><span data-stu-id="6314a-111">Read/write <strong>Database</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6314a-112"><strong><a href="workspace-close-method-dao.md">Закрыть</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-112"><strong><a href="workspace-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-113">Закрытие открытых <strong>рабочей области</strong>.</span><span class="sxs-lookup"><span data-stu-id="6314a-113">Closes an open <strong>Workspace</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6314a-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-114"><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-115">Завершает текущий транзакций и сохраняет изменения.</span><span class="sxs-lookup"><span data-stu-id="6314a-115">Ends the current transaction and saves the changes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6314a-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-116"><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-117">Создает новый объект <strong><a href="database-object-dao.md">базы данных</a></strong> , сохраняет базы данных на диск и возвращает объект открыт <strong>базы данных</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="6314a-117">Creates a new <strong><a href="database-object-dao.md">Database</a></strong> object, saves the database to disk, and returns an opened <strong>Database</strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6314a-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-118"><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="6314a-119">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="6314a-119">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="6314a-120">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6314a-120">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="6314a-121">Открывает объект <strong><a href="connection-object-dao.md">подключения</a></strong> для источника данных ODBC (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="6314a-121">Opens a <strong><a href="connection-object-dao.md">Connection</a></strong> object on an ODBC data source (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6314a-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-122"><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-123">Открывает указанной базы данных в объекте <strong><a href="workspace-object-dao.md">рабочей области</a></strong> и возвращает ссылку на объект <strong><a href="database-object-dao.md">базы данных</a></strong> , который представляет его.</span><span class="sxs-lookup"><span data-stu-id="6314a-123">Opens a specified database in a <strong><a href="workspace-object-dao.md">Workspace</a></strong> object and returns a reference to the <strong><a href="database-object-dao.md">Database</a></strong> object that represents it.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6314a-124"><strong><a href="workspace-rollback-method-dao.md">Откат</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-124"><strong><a href="workspace-rollback-method-dao.md">Rollback</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-125">Завершает текущий транзакцию и восстановление базы данных в объекте <strong>рабочей области</strong> для состояния, в котором они были на момент начала текущей транзакции.</span><span class="sxs-lookup"><span data-stu-id="6314a-125">Ends the current transaction and restores the databases in the <strong>Workspace</strong> object to the state they were in when the current transaction began.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="6314a-126">Свойства</span><span class="sxs-lookup"><span data-stu-id="6314a-126">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6314a-127">Имя</span><span class="sxs-lookup"><span data-stu-id="6314a-127">Name</span></span></p></th>
<th><p><span data-ttu-id="6314a-128">Описание</span><span class="sxs-lookup"><span data-stu-id="6314a-128">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6314a-129"><strong><a href="workspace-connections-property-dao.md">Подключения</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-129"><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-130">Возвращает коллекцию <strong>подключений</strong> , который представляет текущего подключения в указанной <strong>рабочей области</strong>.</span><span class="sxs-lookup"><span data-stu-id="6314a-130">Returns a <strong>Connections</strong> collection that represents the current connections in the specified <strong>Workspace</strong>.</span></span> <span data-ttu-id="6314a-131">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6314a-131">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6314a-132"><strong><a href="workspace-databases-property-dao.md">Базы данных</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-132"><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-133">Возвращает коллекцию <strong>баз данных</strong> , который представляет open баз данных в указанной <strong>рабочей области</strong>.</span><span class="sxs-lookup"><span data-stu-id="6314a-133">Returns a <strong>Databases</strong> collection that represents the open databases in the specified <strong>Workspace</strong>.</span></span> <span data-ttu-id="6314a-134">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6314a-134">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6314a-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-135"><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="6314a-136">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="6314a-136">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="6314a-137">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6314a-137">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="6314a-138">Задает или возвращает тип курсора драйвер, используемый для подключения, созданные методами <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> или <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="6314a-138">Sets or returns the type of cursor driver used on the connection created by the <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> or <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> methods (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6314a-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-139"><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-140">Задает или возвращает значение, указывающее, включены ли несколько transactiond, связанных с одной Microsoft Access базы данных подключен модуль источник данных ODBC изолированный (Microsoft Access рабочие области только).</span><span class="sxs-lookup"><span data-stu-id="6314a-140">Sets or returns a value that indicates whether multiple transactiond that involve the same Microsoft Access database engine-connected ODBC data source are isolated (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6314a-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-141"><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-142">Задает или возвращает число секунд, прежде чем возникает ошибка при попытке выполнить вход в базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="6314a-142">Sets or returns the number of seconds before an error occurs when you attempt to log on to an ODBC database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6314a-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-143"><strong><a href="workspace-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-144">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6314a-144">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="6314a-145">Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="6314a-145">Read/write <strong>String</strong> if the object has not been appended to a collection.</span></span> <span data-ttu-id="6314a-146">Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="6314a-146">Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6314a-147"><strong><a href="workspace-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-147"><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-148">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="6314a-148">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="6314a-149">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6314a-149">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6314a-150"><strong><a href="workspace-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="6314a-150"><strong><a href="workspace-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6314a-151">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="6314a-151">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="6314a-152">Только для чтения <strong>целое число</strong>.</span><span class="sxs-lookup"><span data-stu-id="6314a-152">Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

