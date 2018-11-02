---
title: Члены Recordset2 (DAO)
TOCTitle: Recordset2 Members
ms:assetid: 6ef57191-9da4-7904-d55c-60b59b895a50
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195572(v=office.15)
ms:contentKeyID: 48545523
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c68379b5672246f738bdecdb1e3a3bb32df2f1c4
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25921672"
---
# <a name="recordset2-members-dao"></a><span data-ttu-id="94b6c-102">Члены Recordset2 (DAO)</span><span class="sxs-lookup"><span data-stu-id="94b6c-102">Recordset2 members (DAO)</span></span>


<span data-ttu-id="94b6c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="94b6c-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="94b6c-104">Объект Recordset2 представляет записей в базовой таблице или записи, в результате выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="94b6c-104">A Recordset2 object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="94b6c-105">Методы</span><span class="sxs-lookup"><span data-stu-id="94b6c-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94b6c-106">Имя</span><span class="sxs-lookup"><span data-stu-id="94b6c-106">Name</span></span></p></th>
<th><p><span data-ttu-id="94b6c-107">Описание</span><span class="sxs-lookup"><span data-stu-id="94b6c-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-109">Создает новую запись для объекта обновляемых <strong>Recordset2</strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-109">Creates a new record for an updatable <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-110"><strong><a href="recordset2-cancel-method-dao.md">Отмена</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-110"><strong><a href="recordset2-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="94b6c-111">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="94b6c-111">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="94b6c-112">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94b6c-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="94b6c-113">Отменяет выполнение ожидающие асинхронного вызова метода (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="94b6c-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-115">Отменяет все ожидающие обновления для объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-116"><strong><a href="recordset2-clone-method-dao.md">Копия</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-116"><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-117">Создает объект повторяющихся <strong><a href="recordset-object-dao.md">записей</a></strong> , на который ссылается на исходный объект <strong>Recordset2</strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-118"><strong><a href="recordset2-close-method-dao.md">Закрыть</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-118"><strong><a href="recordset2-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-119">Закрытие открытых <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-121">Возвращает объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong> , являющееся копией <strong>QueryDef</strong> , используемый для создания объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> , представленного заполнитель набора записей (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="94b6c-122">.</span><span class="sxs-lookup"><span data-stu-id="94b6c-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-123"><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-123"><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-124">Не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="94b6c-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-125"><strong><a href="recordset2-edit-method-dao.md">Изменение</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-125"><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-126">Копирует текущей записи из обновляемый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> в буфер копирования для последующего редактирования.</span><span class="sxs-lookup"><span data-stu-id="94b6c-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-128">Заполняет все или часть из локального кэша для объекта <strong>набора записей</strong> , который содержит данные из Microsoft Access базы данных подключен модуль ODBC источника данных (Microsoft Access базы данных подключен модуль ODBC только баз данных).</span><span class="sxs-lookup"><span data-stu-id="94b6c-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-130">Поиск первой записи в объект <strong>набора записей</strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-132">Указывает расположение последние записи в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-134">Находит следующую запись в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-134">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="94b6c-135">.</span><span class="sxs-lookup"><span data-stu-id="94b6c-135"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-137">Указывает расположение предыдущей записи в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-137">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="94b6c-138">.</span><span class="sxs-lookup"><span data-stu-id="94b6c-138"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-139"><strong><a href="recordset2-getrows-method-dao.md">Получение строк</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-139"><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-140">Получает несколько строк из объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-141"><strong><a href="recordset2-move-method-dao.md">Перемещение</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-141"><strong><a href="recordset2-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-142">Перемещает положение текущей записи в объекте <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-143"><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-143"><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-144">Переход к первой записи в указанном объекте <strong>набора записей</strong> и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="94b6c-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-146">Переход к последней записи в указанный объект <strong>набора записей</strong> и сделать эту запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="94b6c-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-148">Переход к следующей записи в указанном объекте <strong>набора записей</strong> и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="94b6c-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-150">Переход к предыдущей записи в указанный <strong>набор записей</strong> объекта и убедитесь, что запись текущей записи.</span><span class="sxs-lookup"><span data-stu-id="94b6c-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="94b6c-152">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="94b6c-152">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="94b6c-153">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94b6c-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="94b6c-154">Получает следующего набора записей, если какие-либо, возвращаемых запросом составного select в вызове <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> и возвращает значение <strong>типа Boolean</strong> , указывающее, является ли один или несколько дополнительных записей ожидающие (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="94b6c-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-156">Создает новый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> и добавляет его в коллекцию <strong>наборов записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-157"><strong><a href="recordset2-requery-method-dao.md">Обновление</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-157"><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-158">Обновляет данные в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> , повторное выполнение запросов, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="94b6c-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-159"><strong><a href="recordset2-seek-method-dao.md">Поиск</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-159"><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-160">Указывает расположение записи в объекте <strong>набора записей</strong> индексированных тип таблицы, которая должна удовлетворять определенным условиям для текущего индекса и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="94b6c-162">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="94b6c-162">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="94b6c-163">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94b6c-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="94b6c-164">Сохранение содержимого буфера копирования обновляемый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="94b6c-165">Свойства</span><span class="sxs-lookup"><span data-stu-id="94b6c-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="94b6c-166">Имя</span><span class="sxs-lookup"><span data-stu-id="94b6c-166">Name</span></span></p></th>
<th><p><span data-ttu-id="94b6c-167">Описание</span><span class="sxs-lookup"><span data-stu-id="94b6c-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-169">Задает или возвращает относительный номер записи текущего объекта <strong>Recordset2</strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-169">Sets or returns the relative record number of a <strong>Recordset2</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="94b6c-171">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="94b6c-171">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="94b6c-172">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94b6c-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="94b6c-173">Возвращает число записей, которые не удалось завершить последнего обновления пакета (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="94b6c-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="94b6c-175">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="94b6c-175">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="94b6c-176">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94b6c-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="94b6c-177">Возвращает массив строк, которые созданы конфликтов в последнюю операцию обновления пакета (только для рабочих областей технология ODBCDirect), указывающее, закладок.</span><span class="sxs-lookup"><span data-stu-id="94b6c-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-178"><strong><a href="recordset2-batchsize-property-dao.md">Размер пакета</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-178"><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="94b6c-179">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="94b6c-179">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="94b6c-180">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94b6c-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="94b6c-181">Задает или возвращает число операторов, отправляемых на сервер в каждом пакете (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="94b6c-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-183">Возвращает значение, указывающее, является ли положение текущей записи перед первой записи в объекте <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-183">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="94b6c-184">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-184">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-185"><strong><a href="recordset2-bookmark-property-dao.md">Закладка</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-185"><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-186">Задает или возвращает закладки, который уникальным образом определяет текущую запись в объект <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-188">Возвращает значение, указывающее, поддерживает ли объект <strong>набора записей</strong> закладки, которые можно задать с помощью свойства <strong><a href="recordset2-bookmark-property-dao.md">Закладка</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-190">Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально.</span><span class="sxs-lookup"><span data-stu-id="94b6c-190">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="94b6c-191">Чтение и запись <strong>времени</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-191">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-193">Задает или возвращает значение, указывающее закладки для первой записи в объекте типа динамического набора записей, содержащий данные для локально кэшировать из источника данных ODBC (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-194"><strong><a href="recordset2-connection-property-dao.md">Подключение</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-194"><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-195">Возвращает объект <strong><a href="connection-object-dao.md">подключения</a></strong> , который соответствует в базу данных.</span><span class="sxs-lookup"><span data-stu-id="94b6c-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-197">Возвращает дату и время создания базовой таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-197">Returns the date and time a base table was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="94b6c-198">Только для чтения <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-198">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-200">Возвращает значение, указывающее состояние редактирования для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="94b6c-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-201"><strong><a href="recordset2-eof-property-dao.md">ФУНКЦИЯ EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-201"><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-202">Возвращает значение, указывающее, является ли положение текущей записи после последней записи в объекте <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-202">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="94b6c-203">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-203">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-204"><strong><a href="recordset2-fields-property-dao.md">Поля</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-204"><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-205">Возвращает коллекцию <strong>полей</strong> , представляющую все хранятся объекты <strong>поля</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="94b6c-205">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="94b6c-206">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="94b6c-206">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-207"><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-207"><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-208">Задает или возвращает значение, определяющее записей, включенных в последующем открытого объекта <strong>набора записей</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-208">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="94b6c-209">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-209">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-210"><strong><a href="recordset2-index-property-dao.md">Индекс</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-210"><strong><a href="recordset2-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-211">Задает или возвращает значение, указывающее имя текущего объекта <strong><a href="index-object-dao.md">индекса</a></strong> в таблице тип объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-213">Возвращает ookmark, указывающее наиболее недавно добавлены или изменены записи.</span><span class="sxs-lookup"><span data-stu-id="94b6c-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-215">Возвращает дату и время последнего изменения, внесенные базовая таблица.</span><span class="sxs-lookup"><span data-stu-id="94b6c-215">Returns the date and time of the most recent change made to a base table.</span></span> <span data-ttu-id="94b6c-216">Только для чтения <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-216">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-218">Задает или возвращает значение, указывающее тип блокировки, который фактически во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="94b6c-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-220">Возвращает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="94b6c-220">Returns the name of the specified object.</span></span> <span data-ttu-id="94b6c-221">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-221">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-223">Указывает, будет ли определенный запись найдена с помощью метода <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> или один из методов <strong><a href="recordset2-findfirst-method-dao.md">поиска</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-223">Indicates whether a particular record was found by using the <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-225">Возвращает родительский <strong>записей</strong> из указанного набора записей.</span><span class="sxs-lookup"><span data-stu-id="94b6c-225">Returns the parent <strong>Recordset</strong> of the specified recordset.</span></span> <span data-ttu-id="94b6c-226">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="94b6c-226">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-228">Задает или возвращает значение, указывающее, приблизительно, например расположение текущей записи в объекте <strong><a href="recordset-object-dao.md">набора записей</a></strong> на основе процента записей в <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-228">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-229"><strong><a href="recordset2-properties-property-dao.md">Свойства</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-229"><strong><a href="recordset2-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-230">Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="94b6c-230">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="94b6c-231">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="94b6c-231">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-233">Возвращает число записей в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> или общее число записей в таблице тип объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-233">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object.</span></span> <span data-ttu-id="94b6c-234">или <strong><a href="tabledef-object-dao.md">TableDef</a></strong> объект.</span><span class="sxs-lookup"><span data-stu-id="94b6c-234">or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object.</span></span> <span data-ttu-id="94b6c-235">Только для чтения <strong>времени</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-235">Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="94b6c-237">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="94b6c-237">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="94b6c-238">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94b6c-238">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="94b6c-239">Возвращает значение, указывающее состояние обновления текущую запись, если он является частью пакета обновления (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="94b6c-239">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only).</span></span> <span data-ttu-id="94b6c-240">Только для чтения <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-240">Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-241"><strong><a href="recordset2-restartable-property-dao.md">Перезапускаемое</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-241"><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-242">Возвращает значение, указывающее, поддерживает ли объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> метод <strong><a href="recordset2-requery-method-dao.md">повторный запрос</a></strong> , который повторно выполняет запрос, на котором основано объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="94b6c-242">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-243"><strong><a href="recordset2-sort-property-dao.md">Сортировка</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-243"><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-244">Задает или возвращает порядок сортировки для записей в объекте <strong><a href="recordset-object-dao.md">набора записей</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="94b6c-244">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="94b6c-246">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="94b6c-246">ODBCDirect workspaces are not supported in Microsoft Access 2013 .</span></span> <span data-ttu-id="94b6c-247">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94b6c-247">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="94b6c-248">Указывает, следует ли асинхронной операции (то есть, вызывается метод с параметром <strong>dbRunAsync</strong> ) завершено выполнение (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="94b6c-248">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-249"><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-249"><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-250">Возвращает значение, указывающее, поддерживает ли объект транзакции.</span><span class="sxs-lookup"><span data-stu-id="94b6c-250">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="94b6c-251">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-251">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-252"><strong><a href="recordset2-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-252"><strong><a href="recordset2-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-253">Задает или возвращает значение, указывающее действующие типа или данных тип объекта.</span><span class="sxs-lookup"><span data-stu-id="94b6c-253">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="94b6c-254">Только для чтения <strong>целое число</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-254">Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-255"><strong><a href="recordset2-updatable-property-dao.md">Обновляемые</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-255"><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-256">Возвращает значение, указывающее, является ли объект DAO можно изменить.</span><span class="sxs-lookup"><span data-stu-id="94b6c-256">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="94b6c-257">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-257">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p></p>

> [!NOTE]
> <P><span data-ttu-id="94b6c-259">Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="94b6c-259">ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="94b6c-260">Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="94b6c-260">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></P>


<p><span data-ttu-id="94b6c-261">Задает или возвращает значение, указывающее, как предложение WHERE создается для каждой записи во время обновления пакета и ли пакетного обновления следует использовать инструкции UPDATE или DELETE последующей вставкой (только для рабочих областей технология ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="94b6c-261">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only).</span></span> <span data-ttu-id="94b6c-262">Чтение и запись <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-262">Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="94b6c-263"><strong><a href="recordset2-validationrule-property-dao.md">Значение</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-263"><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-264">Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access). Чтение и запись <strong>строки</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-264">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="94b6c-265"><strong><a href="recordset2-validationtext-property-dao.md">Сообщение об ошибке</a></strong></span><span class="sxs-lookup"><span data-stu-id="94b6c-265"><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="94b6c-266">Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение <strong>поля</strong> объекта не удовлетворяют правило проверки, указанного идентификатором <strong>условие на значение</strong> свойства поля (только для рабочих областей Microsoft Access) .</span><span class="sxs-lookup"><span data-stu-id="94b6c-266">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="94b6c-267">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="94b6c-267">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

