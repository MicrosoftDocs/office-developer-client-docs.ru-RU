---
title: Элементы подключения (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: f8127109834a617e86116a81731d964181c1bdf2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25930597"
---
# <a name="connection-members-dao"></a><span data-ttu-id="6c0ed-102">Элементы подключения (DAO)</span><span class="sxs-lookup"><span data-stu-id="6c0ed-102">Connection members (DAO)</span></span>

<span data-ttu-id="6c0ed-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6c0ed-103">**Applies to**: Access 2013, Office 2013</span></span>

> [!NOTE]
> <span data-ttu-id="6c0ed-104">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-104">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="6c0ed-105">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-105">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span> <span data-ttu-id="6c0ed-106">Объект подключения представляет подключение к базе данных ODBC (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="6c0ed-106">A Connection object represents a connection to an ODBC database (ODBCDirect workspaces only).</span></span>
 

## <a name="methods"></a><span data-ttu-id="6c0ed-107">Методы</span><span class="sxs-lookup"><span data-stu-id="6c0ed-107">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c0ed-108">Имя</span><span class="sxs-lookup"><span data-stu-id="6c0ed-108">Name</span></span></p></th>
<th><p><span data-ttu-id="6c0ed-109">Описание</span><span class="sxs-lookup"><span data-stu-id="6c0ed-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c0ed-110"><strong><a href="connection-cancel-method-dao.md">Отмена</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-110"><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

<br/>


<p><span data-ttu-id="6c0ed-111">Отменяет выполнение ожидающие асинхронного вызова метода (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="6c0ed-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0ed-112"><strong><a href="connection-close-method-dao.md">Закрыть</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-112"><strong><a href="connection-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-113">Закрывает открытое <strong>подключение</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-113">Closes an open <strong>Connection</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c0ed-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-114"><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-115">Создает новый объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="6c0ed-115">Creates a new <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0ed-116"><strong><a href="connection-execute-method-dao.md">Выполнение</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-116"><strong><a href="connection-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-117">Запуск запроса или выполняет инструкции SQL на указанный объект.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-117">Runs an action query or executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c0ed-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-118"><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-119">Создает новый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> и добавляет его в коллекцию <strong>наборов записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="6c0ed-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="6c0ed-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="6c0ed-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6c0ed-121">Имя</span><span class="sxs-lookup"><span data-stu-id="6c0ed-121">Name</span></span></p></th>
<th><p><span data-ttu-id="6c0ed-122">Описание</span><span class="sxs-lookup"><span data-stu-id="6c0ed-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6c0ed-123"><strong><a href="connection-connect-property-dao.md">Подключение</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-123"><strong><a href="connection-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-124">Задает или возвращает значение, которое содержит сведения об источнике открытое подключение.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-124">Sets or returns a value that provides information about the source of an open connection.</span></span> <span data-ttu-id="6c0ed-125">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-125">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0ed-126"><strong><a href="connection-database-property-dao.md">База данных</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-126"><strong><a href="connection-database-property-dao.md">Database</a></strong></span></span></p></td>
<td><p></p>

<br/>


<p><span data-ttu-id="6c0ed-127">Возвращает объект <strong><a href="database-object-dao.md">базы данных</a></strong> , соответствующий для этого подключения (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="6c0ed-127">Returns the <strong><a href="database-object-dao.md">Database</a></strong> object that corresponds to this connection (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c0ed-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-128"><strong><a href="connection-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-129">Возвращает имя <strong><a href="connection-object-dao.md">подключения</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-129">Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0ed-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-130"><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-131">Возвращает коллекцию <strong>QueryDefs</strong> , который содержит все объекты <strong>QueryDef</strong> указанного подключения.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-131">Returns a <strong>QueryDefs</strong> collection that contains all of the <strong>QueryDef</strong> objects of the specified connection.</span></span> <span data-ttu-id="6c0ed-132">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-132">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c0ed-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-133"><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-134">Задает или возвращает значение, указывающее количество секунд ожидания до возникновения ошибки времени ожидания при выполнении запроса на источник данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-134">Sets or returns a value that specifies the number of seconds to wait before a timeout error occurs when a query is executed on an ODBC data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0ed-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-135"><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-136">Возвращает число записей, влияет на недавно вызванного метода <strong><a href="connection-execute-method-dao.md">Execute</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="6c0ed-136">Returns the number of records affected by the most recently invoked <strong><a href="connection-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c0ed-137"><strong><a href="connection-recordsets-property-dao.md">Наборы записей</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-137"><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-138">Возвращает коллекцию <strong>наборов записей</strong> , который содержит все открытые наборы записей в для указанного подключения.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-138">Returns a <strong>Recordsets</strong> collection that contains all of the open recordsets in the for the specified connection.</span></span> <span data-ttu-id="6c0ed-139">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-139">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0ed-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-140"><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

<br/>


<p><span data-ttu-id="6c0ed-141">Указывает, следует ли асинхронной операции (то есть, вызывается метод с параметром <strong>dbRunAsync</strong> ) завершено выполнение (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="6c0ed-141">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6c0ed-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-142"><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-143">Возвращает значение, указывающее, поддерживает ли объект транзакции.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-143">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="6c0ed-144">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-144">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6c0ed-145"><strong><a href="connection-updatable-property-dao.md">Обновляемые</a></strong></span><span class="sxs-lookup"><span data-stu-id="6c0ed-145"><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="6c0ed-146">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-146">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="6c0ed-147">Только для чтения <strong>типа Boolean</strong>. Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6c0ed-147">Read-only <strong>Boolean</strong>.Read-only.</span></span></p></td>
</tr>
</tbody>
</table>

