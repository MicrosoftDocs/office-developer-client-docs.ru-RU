---
title: Члены набора записей (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 70593fdcab32602ba6b0e4597368f64371d8f116
ms.sourcegitcommit: 38d0db57580cc5f4a0231c27b1643f8db5431ca3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25937367"
---
# <a name="recordset-members-dao"></a><span data-ttu-id="3ec26-102">Члены набора записей (DAO)</span><span class="sxs-lookup"><span data-stu-id="3ec26-102">Recordset members (DAO)</span></span>


<span data-ttu-id="3ec26-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3ec26-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3ec26-104">Объект набора записей представляет записей в базовой таблице или записей, в результате выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="3ec26-104">A Recordset object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="3ec26-105">Методы</span><span class="sxs-lookup"><span data-stu-id="3ec26-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ec26-106">Имя</span><span class="sxs-lookup"><span data-stu-id="3ec26-106">Name</span></span></p></th>
<th><p><span data-ttu-id="3ec26-107">Описание</span><span class="sxs-lookup"><span data-stu-id="3ec26-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-108"><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-108"><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-109">Создает новую запись для обновляемых объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-109">Creates a new record for an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-110"><strong><a href="recordset-cancel-method-dao.md">Отмена</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-110"><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="3ec26-111">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec26-111">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3ec26-112">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ec26-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="3ec26-113">Отменяет выполнение ожидающие асинхронного вызова метода (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3ec26-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-114"><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-115">Отменяет все ожидающие обновления для объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-116"><strong><a href="recordset-clone-method-dao.md">Копия</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-116"><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-117">Создает объект повторяющихся <strong><a href="recordset-object-dao.md">записей</a></strong> , на который ссылается на исходный объект <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-118"><strong><a href="recordset-close-method-dao.md">Закрыть</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-118"><strong><a href="recordset-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-119">Закрытие открытых <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-120"><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-120"><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-121">Возвращает объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong> , являющееся копией <strong>QueryDef</strong> , используемый для создания объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> , представленного заполнитель набора записей (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3ec26-122">.</span><span class="sxs-lookup"><span data-stu-id="3ec26-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-123"><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-124">Не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="3ec26-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-125"><strong><a href="recordset-edit-method-dao.md">Изменение</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-125"><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-126">Копирует текущей записи из обновляемый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> в буфер копирования для последующего редактирования.</span><span class="sxs-lookup"><span data-stu-id="3ec26-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-127"><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-128">Заполняет все или часть из локального кэша для объекта <strong>набора записей</strong> , который содержит данные из Microsoft Access базы данных подключен модуль ODBC источника данных (Microsoft Access базы данных подключен модуль ODBC только баз данных).</span><span class="sxs-lookup"><span data-stu-id="3ec26-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-129"><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-130">Поиск первой записи в объект <strong>набора записей</strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-131"><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-132">Указывает расположение последние записи в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-133"><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-134">Находит следующую запись в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-134">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3ec26-135">.</span><span class="sxs-lookup"><span data-stu-id="3ec26-135"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-136"><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-137">Указывает расположение предыдущей записи в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-137">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3ec26-138">.</span><span class="sxs-lookup"><span data-stu-id="3ec26-138"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-139"><strong><a href="recordset-getrows-method-dao.md">Получение строк</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-139"><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-140">Получает несколько строк из объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-141"><strong><a href="recordset-move-method-dao.md">Перемещение</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-141"><strong><a href="recordset-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-142">Перемещает положение текущей записи в объекте <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-143"><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-143"><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-144">Переход к первой записи в указанном объекте <strong>набора записей</strong> и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3ec26-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-145"><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-146">Переход к последней записи в указанный объект <strong>набора записей</strong> и сделать эту запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3ec26-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-147"><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-147"><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-148">Переход к следующей записи в указанном объекте <strong>набора записей</strong> и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3ec26-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-149"><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-149"><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-150">Переход к предыдущей записи в указанный <strong>набор записей</strong> объекта и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3ec26-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-151"><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-151"><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="3ec26-152">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec26-152">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3ec26-153">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ec26-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="3ec26-154">Получает следующего набора записей, если какие-либо, возвращаемых запросом составного select в вызове <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> и возвращает значение <strong>типа Boolean</strong> , указывающее, является ли один или несколько дополнительных записей ожидающие (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3ec26-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-155"><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-156">Создает новый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> и добавляет его в коллекцию <strong>наборов записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-157"><strong><a href="recordset-requery-method-dao.md">Обновление</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-157"><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-158">Обновляет данные в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> , повторное выполнение запросов, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="3ec26-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-159"><strong><a href="recordset-seek-method-dao.md">Поиск</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-159"><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-160">Указывает расположение записи в объекте <strong>набора записей</strong> индексированных тип таблицы, которая должна удовлетворять определенным условиям для текущего индекса и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-161"><strong><a href="recordset-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="3ec26-162">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec26-162">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3ec26-163">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ec26-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="3ec26-164">Сохранение содержимого буфера копирования обновляемый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="3ec26-165">Свойства</span><span class="sxs-lookup"><span data-stu-id="3ec26-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3ec26-166">Имя</span><span class="sxs-lookup"><span data-stu-id="3ec26-166">Name</span></span></p></th>
<th><p><span data-ttu-id="3ec26-167">Описание</span><span class="sxs-lookup"><span data-stu-id="3ec26-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-168"><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-168"><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-169">Задает или возвращает относительный номер записи текущего объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-169">Sets or returns the relative record number of a <strong>Recordset</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-170"><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-170"><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="3ec26-171">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec26-171">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3ec26-172">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ec26-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="3ec26-173">Возвращает число записей, которые не удалось завершить последнего обновления пакета (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3ec26-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-174"><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-174"><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="3ec26-175">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec26-175">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3ec26-176">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ec26-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="3ec26-177">Возвращает массив строк, которые созданы конфликтов в последнюю операцию обновления пакета (только для рабочих областей технология ODBCDirect), указывающее, закладок.</span><span class="sxs-lookup"><span data-stu-id="3ec26-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-178"><strong><a href="recordset-batchsize-property-dao.md">Размер пакета</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-178"><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="3ec26-179">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec26-179">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3ec26-180">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ec26-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="3ec26-181">Задает или возвращает число операторов, отправляемых на сервер в каждом пакете (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3ec26-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-182"><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-183">Возвращает значение, указывающее, является ли положение текущей записи перед первой записи в объекте <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-183">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="3ec26-184">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-184">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-185"><strong><a href="recordset-bookmark-property-dao.md">Закладка</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-185"><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-186">Задает или возвращает закладки, который уникальным образом определяет текущую запись в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-187"><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-188">Возвращает значение, указывающее, поддерживает ли объект <strong>набора записей</strong> закладки, которые можно задать с помощью свойства <strong><a href="recordset-bookmark-property-dao.md">Закладка</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-189"><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-189"><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-190">Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально.</span><span class="sxs-lookup"><span data-stu-id="3ec26-190">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="3ec26-191">Чтение и запись <strong>времени</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-191">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-192"><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-192"><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-193">Задает или возвращает значение, указывающее закладки для первой записи в объекте типа динамического набора записей, содержащий данные для локально кэшировать из источника данных ODBC (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-194"><strong><a href="recordset-connection-property-dao.md">Подключение</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-194"><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-195">Возвращает объект <strong><a href="connection-object-dao.md">подключения</a></strong> , который соответствует в базу данных.</span><span class="sxs-lookup"><span data-stu-id="3ec26-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-196"><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-197">Возвращает дату и время создания базовой таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-197">Returns the date and time a base table was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3ec26-198">Только для чтения <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-198">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-199"><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-199"><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-200">Возвращает значение, указывающее состояние редактирования для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="3ec26-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-201"><strong><a href="recordset-eof-property-dao.md">ФУНКЦИЯ EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-201"><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-202">Возвращает значение, указывающее, является ли положение текущей записи после последней записи в объекте <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-202">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="3ec26-203">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-203">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-204"><strong><a href="recordset-fields-property-dao.md">Поля</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-204"><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-205">Возвращает коллекцию <strong>полей</strong> , представляющую все хранятся объекты <strong>поля</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="3ec26-205">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="3ec26-206">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3ec26-206">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-207"><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-208">Задает или возвращает значение, определяющее записей, включенных в последующем открытого объекта <strong>набора записей</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-208">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3ec26-209">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-209">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-210"><strong><a href="recordset-index-property-dao.md">Индекс</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-210"><strong><a href="recordset-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-211">Задает или возвращает значение, указывающее имя текущего объекта <strong><a href="index-object-dao.md">индекса</a></strong> в таблице тип объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-212"><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-212"><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-213">Возвращает ookmark, указывающее наиболее недавно добавлены или изменены записи.</span><span class="sxs-lookup"><span data-stu-id="3ec26-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-214"><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-214"><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-215">Возвращает дату и время последнего изменения, внесенные базовая таблица.</span><span class="sxs-lookup"><span data-stu-id="3ec26-215">Returns the date and time of the most recent change made to a base table.</span></span> <span data-ttu-id="3ec26-216">Только для чтения <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-216">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-217"><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-217"><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-218">Задает или возвращает значение, указывающее тип блокировки, который фактически во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="3ec26-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-219"><strong><a href="recordset-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-220">Возвращает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="3ec26-220">Returns the name of the specified object.</span></span> <span data-ttu-id="3ec26-221">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-221">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-222"><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-222"><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-223">Указывает, будет ли определенный запись найдена с помощью метода <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> или один из методов <strong><a href="recordset-findfirst-method-dao.md">поиска</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-223">Indicates whether a particular record was found by using the <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-224"><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-224"><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-225">Задает или возвращает значение, указывающее, приблизительно, например расположение текущей записи в объекте <strong><a href="recordset-object-dao.md">набора записей</a></strong> на основе процента записей в <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-225">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-226"><strong><a href="recordset-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-226"><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-227">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="3ec26-227">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="3ec26-228">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3ec26-228">Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-229"><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-230">Возвращает число записей в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> или общее число записей в таблице тип объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-230">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object.</span></span> <span data-ttu-id="3ec26-231">или <strong><a href="tabledef-object-dao.md">TableDef</a></strong> объект.</span><span class="sxs-lookup"><span data-stu-id="3ec26-231">or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object.</span></span> <span data-ttu-id="3ec26-232">Только для чтения <strong>времени</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-232">Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-233"><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-233"><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="3ec26-234">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec26-234">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3ec26-235">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ec26-235">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="3ec26-236">Возвращает значение, указывающее состояние обновления текущую запись, если он является частью пакета обновления (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3ec26-236">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only).</span></span> <span data-ttu-id="3ec26-237">Только для чтения <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-237">Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-238"><strong><a href="recordset-restartable-property-dao.md">Перезапускаемое</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-238"><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-239">Возвращает значение, указывающее, поддерживает ли объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> метод <strong><a href="recordset-requery-method-dao.md">повторный запрос</a></strong> , который повторно выполняет запрос, на котором основано объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="3ec26-239">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-240"><strong><a href="recordset-sort-property-dao.md">Сортировка</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-240"><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-241">Задает или возвращает порядок сортировки для записей в объекте <strong><a href="recordset-object-dao.md">набора записей</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="3ec26-241">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-242"><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-242"><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="3ec26-243">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec26-243">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3ec26-244">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ec26-244">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="3ec26-245">Указывает, следует ли асинхронной операции (то есть, вызывается метод с параметром <strong>dbRunAsync</strong> ) завершено выполнение (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3ec26-245">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-246"><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-247">Возвращает значение, указывающее, поддерживает ли объект транзакции.</span><span class="sxs-lookup"><span data-stu-id="3ec26-247">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="3ec26-248">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-248">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-249"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-249"><strong>Type</strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-250">Описание для данного члена будет отображаться в окончательной версии Office 14.</span><span class="sxs-lookup"><span data-stu-id="3ec26-250">The description for this member will appear in the final release of Office 14.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-251"><strong><a href="recordset-updatable-property-dao.md">Обновляемые</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-251"><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-252">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="3ec26-252">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="3ec26-253">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-253">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-254"><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <span data-ttu-id="3ec26-255">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="3ec26-255">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="3ec26-256">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="3ec26-256">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span>


<p><span data-ttu-id="3ec26-257">Задает или возвращает значение, указывающее, как предложение WHERE создается для каждой записи во время обновления пакета и ли пакетного обновления следует использовать инструкции UPDATE или DELETE последующей вставкой (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="3ec26-257">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only).</span></span> <span data-ttu-id="3ec26-258">Чтение и запись <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-258">Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3ec26-259"><strong><a href="recordset-validationrule-property-dao.md">Значение</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-259"><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-260">Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access). Чтение и запись <strong>строки</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-260">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3ec26-261"><strong><a href="recordset-validationtext-property-dao.md">Сообщение об ошибке</a></strong></span><span class="sxs-lookup"><span data-stu-id="3ec26-261"><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="3ec26-262">Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение <strong>поля</strong> объекта не удовлетворяют правило проверки, указанного идентификатором <strong>условие на значение</strong> свойства поля (только для рабочих областей Microsoft Access) .</span><span class="sxs-lookup"><span data-stu-id="3ec26-262">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="3ec26-263">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="3ec26-263">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

