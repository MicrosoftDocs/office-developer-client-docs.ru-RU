---
title: QueryDef Members (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 357e419f27efdcc7b6b46004cd340c100114a72a
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480968"
---
# <a name="querydef-members-dao"></a><span data-ttu-id="0cb0c-102">QueryDef Members (DAO)</span><span class="sxs-lookup"><span data-stu-id="0cb0c-102">QueryDef Members (DAO)</span></span>


<span data-ttu-id="0cb0c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="0cb0c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="0cb0c-104">Объект QueryDef — сохраненных определение запроса в базе данных ядра базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-104">A QueryDef object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="methods"></a><span data-ttu-id="0cb0c-105">Методы</span><span class="sxs-lookup"><span data-stu-id="0cb0c-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0cb0c-106">Имя</span><span class="sxs-lookup"><span data-stu-id="0cb0c-106">Name</span></span></p></th>
<th><p><span data-ttu-id="0cb0c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0cb0c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-108"><strong><a href="querydef-cancel-method-dao.md">Отмена</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-108"><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="0cb0c-109">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-109">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0cb0c-110">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-110">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="0cb0c-111">Отменяет выполнение ожидающие асинхронного вызова метода (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="0cb0c-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-112"><strong><a href="querydef-close-method-dao.md">Закрыть</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-112"><strong><a href="querydef-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-113">Закрытие открытых <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-113">Closes an open <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-115">Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0cb0c-115">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-116"><strong><a href="querydef-execute-method-dao.md">Выполнение</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-116"><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-117">Выполняет инструкции SQL на указанный объект.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-117">Executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-119">Создает новый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> и добавляет его в коллекцию <strong>наборов записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="0cb0c-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="0cb0c-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="0cb0c-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0cb0c-121">Имя</span><span class="sxs-lookup"><span data-stu-id="0cb0c-121">Name</span></span></p></th>
<th><p><span data-ttu-id="0cb0c-122">Описание</span><span class="sxs-lookup"><span data-stu-id="0cb0c-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-124">Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-124">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="0cb0c-125">Чтение и запись <strong>времени</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-125">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-126"><strong><a href="querydef-connect-property-dao.md">Подключение</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-127">Задает или возвращает значение, которое содержит сведения об источнике базы данных, используемой в запросе к серверу.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-127">Sets or returns a value that provides information about the source of database used in a pass-through query.</span></span> <span data-ttu-id="0cb0c-128">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-128">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-130">Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0cb0c-130">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="0cb0c-131">Только для чтения <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-131">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-132"><strong><a href="querydef-fields-property-dao.md">Поля</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-133">Возвращает коллекцию <strong><a href="fields-collection-dao.md">полей</a></strong> , представляющую все хранятся объекты <strong><a href="field-object-dao.md">поля</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-133">Returns a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection that represents all stored <strong><a href="field-object-dao.md">Field</a></strong> objects for the specified object.</span></span> <span data-ttu-id="0cb0c-134">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-134">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-136">Возвращает дату и время последнего изменения, внесенные в объект.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-136">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="0cb0c-137">Только для чтения <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-137">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-139">Задает или возвращает максимальное число записей для возврата из запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-139">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-141">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-141">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="0cb0c-142">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-142">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-143"><strong><a href="querydef-odbctimeout-property-dao.md">Время ожидания ODBC</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-144">Указывает количество секунд до ошибку времени ожидания происходит, когда <strong><a href="querydef-object-dao.md">QueryDef</a></strong> выполняется в базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-144">Indicates the number of seconds to wait before a timeout error occurs when a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> is executed on an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-145"><strong><a href="querydef-parameters-property-dao.md">Параметры</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-145"><strong><a href="querydef-parameters-property-dao.md">Parameters</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-146">Возвращает коллекцию <strong><a href="parameters-collection-dao.md">параметров</a></strong> , который содержит все объекты <strong><a href="parameter-object-dao.md">параметров</a></strong> из указанного <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-146">Returns a <strong><a href="parameters-collection-dao.md">Parameters</a></strong> collection that contains all of the <strong><a href="parameter-object-dao.md">Parameter</a></strong> objects of the specified <strong>QueryDef</strong>.</span></span> <span data-ttu-id="0cb0c-147">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-147">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-148"><strong><a href="querydef-prepare-property-dao.md">Подготовка</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="0cb0c-149">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-149">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0cb0c-150">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-150">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="0cb0c-151">Задает или возвращает значение, указывающее, следует подготовить на сервере как временной хранимой процедуры с помощью функции ODBC <strong>SQLPrepare</strong> API, прежде чем начать выполнение, запрос или просто выполняется с помощью (функция ODBC <strong>SQLExecDirect</strong> API Технология ODBCDirect рабочие области только).</span><span class="sxs-lookup"><span data-stu-id="0cb0c-151">Sets or returns a value that indicates whether the query should be prepared on the server as a temporary stored procedure, using the ODBC <strong>SQLPrepare</strong> API function, prior to execution, or just executed using the ODBC <strong>SQLExecDirect</strong> API function (ODBCDirect workspaces only).</span></span> <span data-ttu-id="0cb0c-152">Чтение и запись <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-152">Read/Write <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-153"><strong><a href="querydef-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-153"><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-154">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-154">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="0cb0c-155">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-155">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-157">Возвращает число записей, влияет на недавно вызванного метода <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="0cb0c-157">Returns the number of records affected by the most recently invoked <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-159">Задает или возвращает значение, указывающее, возвращает ли запрос к серверу к внешней базе данных записей (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0cb0c-159">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-161">Задает или возвращает SQL, который определяет запрос, выполняемый с помощью объекта <strong><a href="querydef-object-dao.md">QueryDef</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="0cb0c-161">Sets or returns the SQL statement that defines the query executed by a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="0cb0c-163">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-163">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0cb0c-164">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-164">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="0cb0c-165">Указывает, следует ли асинхронной операции (то есть, вызывается метод с параметром <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a> ) завершено выполнение (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="0cb0c-165">Indicates whether or not an asynchronous operation (that is, a method called with the <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0cb0c-166"><strong><a href="querydef-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-166"><strong><a href="querydef-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-167">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-167">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="0cb0c-168">Только для чтения<strong>целое число</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-168">Read-only<strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0cb0c-169"><strong><a href="querydef-updatable-property-dao.md">Обновляемые</a></strong></span><span class="sxs-lookup"><span data-stu-id="0cb0c-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0cb0c-170">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-170">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="0cb0c-171">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="0cb0c-171">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

