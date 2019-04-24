---
title: Элементы QueryDef (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b3afc134636d5621f38ece4530be5312e42bc74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302984"
---
# <a name="querydef-members-dao"></a><span data-ttu-id="0ea68-102">Элементы QueryDef (DAO)</span><span class="sxs-lookup"><span data-stu-id="0ea68-102">QueryDef members (DAO)</span></span>


<span data-ttu-id="0ea68-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0ea68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="0ea68-104">Объект QueryDef это хранимое определение запроса в базе данных ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0ea68-104">A QueryDef object is a stored definition of a query in a Microsoft Access database engine database.</span></span>

## <a name="methods"></a><span data-ttu-id="0ea68-105">Методы</span><span class="sxs-lookup"><span data-stu-id="0ea68-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ea68-106">Имя</span><span class="sxs-lookup"><span data-stu-id="0ea68-106">Name</span></span></p></th>
<th><p><span data-ttu-id="0ea68-107">Описание</span><span class="sxs-lookup"><span data-stu-id="0ea68-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-108"><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-108"><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-109"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="0ea68-109"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0ea68-110">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0ea68-110">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="0ea68-111">Отменяет выполнение ожидающего вызова асинхронного метода (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="0ea68-111">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-112"><strong><a href="querydef-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-112"><strong><a href="querydef-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-113">ЗаКрывает открытый объект <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-113">Closes an open <strong>QueryDef</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-114"><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-115">Создает новый объект определяемого пользователем <strong><a href="property-object-dao.md">Свойства</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0ea68-115">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-116"><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-116"><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-117">Выполняет инструкцию SQL для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="0ea68-117">Executes an SQL statement on the specified object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-118"><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-119">Создает новый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> и добавляет его в коллекцию <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-119">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="0ea68-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="0ea68-120">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0ea68-121">Имя</span><span class="sxs-lookup"><span data-stu-id="0ea68-121">Name</span></span></p></th>
<th><p><span data-ttu-id="0ea68-122">Описание</span><span class="sxs-lookup"><span data-stu-id="0ea68-122">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-123"><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-124">Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально.</span><span class="sxs-lookup"><span data-stu-id="0ea68-124">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="0ea68-125">Для чтения и записи, <strong>Long</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-125">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-126"><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-127">Задает или возвращает значение, которое предоставляет сведения об источнике базы данных, используемой в запросе к серверу.</span><span class="sxs-lookup"><span data-stu-id="0ea68-127">Sets or returns a value that provides information about the source of database used in a pass-through query.</span></span> <span data-ttu-id="0ea68-128">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-128">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-129"><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-130">Возвращает дату и время создания объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0ea68-130">Returns the date and time that an object was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="0ea68-131">Только для чтения, <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-131">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-132"><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-133">Возвращает коллекцию <strong><a href="fields-collection-dao.md">Fields</a></strong> , которая представляет все сохраненные объекты <strong><a href="field-object-dao.md">field</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="0ea68-133">Returns a <strong><a href="fields-collection-dao.md">Fields</a></strong> collection that represents all stored <strong><a href="field-object-dao.md">Field</a></strong> objects for the specified object.</span></span> <span data-ttu-id="0ea68-134">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0ea68-134">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-135"><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-136">Возвращает дату и время последнего изменения, внесенного в объект.</span><span class="sxs-lookup"><span data-stu-id="0ea68-136">Returns the date and time of the most recent change made to an object.</span></span> <span data-ttu-id="0ea68-137">Только для чтения, <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-137">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-138"><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-139">Задает или возвращает максимальное число записей, возвращаемых из запроса к источнику данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="0ea68-139">Sets or returns the maximum number of records to return from a query against an ODBC data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-140"><strong><a href="querydef-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-141">Возвращает или задает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="0ea68-141">Returns or sets the name of the specified object.</span></span> <span data-ttu-id="0ea68-142">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-142">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-143"><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-144">Указывает время ожидания (в секундах) до возникновения ошибки времени ожидания при выполнении объекта <strong><a href="querydef-object-dao.md">QueryDef</a></strong> в базе данных ODBC.</span><span class="sxs-lookup"><span data-stu-id="0ea68-144">Indicates the number of seconds to wait before a timeout error occurs when a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> is executed on an ODBC database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-145"><strong><a href="querydef-parameters-property-dao.md">Параметры</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-145"><strong><a href="querydef-parameters-property-dao.md">Parameters</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-146">Возвращает коллекцию <strong><a href="parameters-collection-dao.md">Parameters</a></strong> , содержащую все объекты <strong><a href="parameter-object-dao.md">параметров</a></strong> указанного объекта <strong>QueryDef</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-146">Returns a <strong><a href="parameters-collection-dao.md">Parameters</a></strong> collection that contains all of the <strong><a href="parameter-object-dao.md">Parameter</a></strong> objects of the specified <strong>QueryDef</strong>.</span></span> <span data-ttu-id="0ea68-147">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0ea68-147">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-148"><strong><a href="querydef-prepare-property-dao.md">Подготовка</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-148"><strong><a href="querydef-prepare-property-dao.md">Prepare</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-149"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="0ea68-149"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0ea68-150">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0ea68-150">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="0ea68-151">Задает или возвращает значение, которое указывает, следует ли подготовить запрос на сервере в качестве временной хранимой процедуры, с помощью функции ODBC <strong>склпрепаре</strong> API, перед выполнением или только после выполнения с помощью функции ODBC <strong>склексекдирект</strong> API ( Только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="0ea68-151">Sets or returns a value that indicates whether the query should be prepared on the server as a temporary stored procedure, using the ODBC <strong>SQLPrepare</strong> API function, prior to execution, or just executed using the ODBC <strong>SQLExecDirect</strong> API function (ODBCDirect workspaces only).</span></span> <span data-ttu-id="0ea68-152">Чтение и запись <strong><a href="querydefstateenum-enumeration-dao.md">куеридефстатинум</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-152">Read/Write <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-153"><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-153"><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-154">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="0ea68-154">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="0ea68-155">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0ea68-155">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-156"><strong><a href="querydef-recordsaffected-property-dao.md">Рекордсаффектед</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-156"><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-157">Возвращает число записей, затронутых последним вызванным методом <strong><a href="querydef-execute-method-dao.md">EXECUTE</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="0ea68-157">Returns the number of records affected by the most recently invoked <strong><a href="querydef-execute-method-dao.md">Execute</a></strong> method.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-158"><strong><a href="querydef-returnsrecords-property-dao.md">Записей</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-158"><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-159">Задает или возвращает значение, указывающее, возвращает ли запрос к серверу SQL Server только записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="0ea68-159">Sets or returns a value that indicates whether an SQL pass-through query to an external database returns records (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-160"><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-161">Задает или возвращает инструкцию SQL, определяющую запрос, выполняемый объектом <strong><a href="querydef-object-dao.md">QueryDef</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="0ea68-161">Sets or returns the SQL statement that defines the query executed by a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-162"><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-163"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="0ea68-163"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="0ea68-164">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="0ea68-164">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="0ea68-165">Указывает на то, завершена или нет асинхронной операции (т. е метода, вызываемого с параметром <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a>) (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="0ea68-165">Indicates whether or not an asynchronous operation (that is, a method called with the <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0ea68-166"><strong><a href="querydef-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-166"><strong><a href="querydef-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-167">Задает или возвращает значение, которое указывает операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="0ea68-167">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="0ea68-168"><strong>Целое число</strong>, доступное только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0ea68-168">Read-only<strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0ea68-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="0ea68-169"><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="0ea68-170">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="0ea68-170">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="0ea68-171">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="0ea68-171">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

