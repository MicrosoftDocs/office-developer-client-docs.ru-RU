---
title: Участники подключения (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 098f44d87390351c23e61000ecbe47eae35810ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295907"
---
# <a name="connection-members-dao"></a><span data-ttu-id="88eee-102">Участники подключения (DAO)</span><span class="sxs-lookup"><span data-stu-id="88eee-102">Connection members (DAO)</span></span>

<span data-ttu-id="88eee-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="88eee-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="88eee-104">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="88eee-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="88eee-105">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="88eee-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span> <span data-ttu-id="88eee-106">Объект Connection представляет подключение к базе данных ODBC (только в рабочей области ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="88eee-106">A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>
 
## <a name="methods"></a><span data-ttu-id="88eee-107">Методы</span><span class="sxs-lookup"><span data-stu-id="88eee-107">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88eee-108">Имя</span><span class="sxs-lookup"><span data-stu-id="88eee-108">Name</span></span></p></th>
<th><p><span data-ttu-id="88eee-109">Описание</span><span class="sxs-lookup"><span data-stu-id="88eee-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88eee-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-111">Отменяет выполнение ожидающего вызова асинхронного метода (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="88eee-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88eee-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-113">Закрывает открытое <strong>подключение.</strong></span><span class="sxs-lookup"><span data-stu-id="88eee-113">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88eee-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-115">Создает новый объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="88eee-115">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88eee-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-117">Выполняет запрос на изменение или запускает инструкцию SQL для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="88eee-117">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88eee-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-119">Создает новый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> и добавляет его в коллекцию <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="88eee-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="88eee-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="88eee-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="88eee-121">Имя</span><span class="sxs-lookup"><span data-stu-id="88eee-121">Name</span></span></p></th>
<th><p><span data-ttu-id="88eee-122">Описание</span><span class="sxs-lookup"><span data-stu-id="88eee-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88eee-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-124">Задает или возвращает значение, которое предоставляет сведения об источнике открытого подключения.</span><span class="sxs-lookup"><span data-stu-id="88eee-124">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="88eee-125">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="88eee-125">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88eee-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-127">Возвращает объект <strong><a href="database-object-dao.md">Database,</a></strong> соответствующий этому подключению (только в рабочей области ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="88eee-127">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88eee-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-129">Rreturns имя <strong><a href="connection-object-dao.md">подключения</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="88eee-129">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88eee-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-131">Возвращает <strong>коллекцию QueryDefs,</strong> которая содержит все объекты <strong>QueryDef</strong> указанного подключения.</span><span class="sxs-lookup"><span data-stu-id="88eee-131">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection.</span></span> <span data-ttu-id="88eee-132">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="88eee-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88eee-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-134">Задает или возвращает значение, которое указывает количество секунд, которые необходимо ждать до возникновения ошибки при выполнении запроса в источнике данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="88eee-134">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88eee-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-136">Возвращает количество записей, затронутых самым недавно вызываемой методом <strong><a href="connection-execute-method-dao.md">Выполнения.</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-136">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88eee-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-138">Возвращает <strong>коллекцию Recordsets,</strong> которая содержит все открытые записи в указанном соединении.</span><span class="sxs-lookup"><span data-stu-id="88eee-138">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection.</span></span> <span data-ttu-id="88eee-139">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="88eee-139">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88eee-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-141">Указывает на то, завершена или нет асинхронной операции (т. е метода, вызываемого с параметром <strong>dbRunAsync</strong>) (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="88eee-141">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="88eee-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-143">Возвращает значение, которое указывает на то, поддерживает ли объект транзакций.</span><span class="sxs-lookup"><span data-stu-id="88eee-143">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="88eee-144">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="88eee-144">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88eee-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="88eee-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="88eee-146">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="88eee-146">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="88eee-147">Только для чтения <strong>Boolean</strong>. Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="88eee-147">Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

