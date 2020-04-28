---
title: Элементы подключения (DAO)
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
# <a name="connection-members-dao"></a><span data-ttu-id="4cb67-102">Элементы подключения (DAO)</span><span class="sxs-lookup"><span data-stu-id="4cb67-102">Connection members (DAO)</span></span>

<span data-ttu-id="4cb67-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4cb67-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="4cb67-104">Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="4cb67-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="4cb67-105">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="4cb67-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span> <span data-ttu-id="4cb67-106">Объект Connection представляет подключение к базе данных ODBC (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="4cb67-106">A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>
 
## <a name="methods"></a><span data-ttu-id="4cb67-107">Методы</span><span class="sxs-lookup"><span data-stu-id="4cb67-107">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4cb67-108">Имя</span><span class="sxs-lookup"><span data-stu-id="4cb67-108">Name</span></span></p></th>
<th><p><span data-ttu-id="4cb67-109">Описание</span><span class="sxs-lookup"><span data-stu-id="4cb67-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cb67-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-111">Отменяет выполнение ожидающего вызова асинхронного метода (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="4cb67-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb67-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-113">Закрывает открытое <strong>Подключение</strong>.</span><span class="sxs-lookup"><span data-stu-id="4cb67-113">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cb67-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-115">Создает новый объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="4cb67-115">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb67-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-117">Выполняет запрос на изменение или запускает инструкцию SQL для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="4cb67-117">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cb67-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-119">Создает новый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> и добавляет его в коллекцию <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="4cb67-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="4cb67-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="4cb67-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4cb67-121">Имя</span><span class="sxs-lookup"><span data-stu-id="4cb67-121">Name</span></span></p></th>
<th><p><span data-ttu-id="4cb67-122">Описание</span><span class="sxs-lookup"><span data-stu-id="4cb67-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4cb67-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-124">Задает или возвращает значение, предоставляющее сведения об источнике открытого подключения.</span><span class="sxs-lookup"><span data-stu-id="4cb67-124">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="4cb67-125">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="4cb67-125">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb67-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-127">Возвращает объект <strong><a href="database-object-dao.md">базы данных</a></strong> , соответствующий этому подключению (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="4cb67-127">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cb67-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-129">Рретурнс имя <strong><a href="connection-object-dao.md">подключения</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="4cb67-129">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb67-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-131">Возвращает коллекцию <strong>QueryDef</strong> , содержащую все объекты <strong>QueryDef</strong> указанного подключения.</span><span class="sxs-lookup"><span data-stu-id="4cb67-131">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection.</span></span> <span data-ttu-id="4cb67-132">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4cb67-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cb67-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-134">Задает или возвращает значение, задающее время ожидания в секундах до возникновения ошибки времени ожидания при выполнении запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="4cb67-134">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb67-135"><strong><a href="connection-recordsaffected-property-dao.md">рекордсаффектед</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-136">Возвращает число записей, затронутых последним вызванным методом <strong><a href="connection-execute-method-dao.md">EXECUTE</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="4cb67-136">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cb67-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-138">Возвращает коллекцию <strong>Recordset</strong> , содержащую все открытые наборы записей в поле для указанного подключения.</span><span class="sxs-lookup"><span data-stu-id="4cb67-138">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection.</span></span> <span data-ttu-id="4cb67-139">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4cb67-139">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb67-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-141">Указывает на то, завершена или нет асинхронной операции (т. е метода, вызываемого с параметром <strong>dbRunAsync</strong>) (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="4cb67-141">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4cb67-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-143">Возвращает значение, которое указывает на то, поддерживает ли объект транзакций.</span><span class="sxs-lookup"><span data-stu-id="4cb67-143">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="4cb67-144">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="4cb67-144">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4cb67-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="4cb67-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="4cb67-146">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="4cb67-146">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="4cb67-147"><strong>Логическое значение</strong>, доступное только для чтения. Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="4cb67-147">Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

