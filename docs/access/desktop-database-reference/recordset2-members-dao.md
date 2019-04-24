---
title: Элементы Recordset2 (DAO)
TOCTitle: Recordset2 Members
ms:assetid: 6ef57191-9da4-7904-d55c-60b59b895a50
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195572(v=office.15)
ms:contentKeyID: 48545523
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 29d1472e8cd02d8968ba84dbc1c1cf99be7ee858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307275"
---
# <a name="recordset2-members-dao"></a><span data-ttu-id="bae51-102">Элементы Recordset2 (DAO)</span><span class="sxs-lookup"><span data-stu-id="bae51-102">Recordset2 members (DAO)</span></span>


<span data-ttu-id="bae51-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="bae51-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bae51-104">Объект Recordset2 представляет записи в базовой таблице или записи, получаемые в результате выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="bae51-104">A Recordset2 object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="methods"></a><span data-ttu-id="bae51-105">Методы</span><span class="sxs-lookup"><span data-stu-id="bae51-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bae51-106">Имя</span><span class="sxs-lookup"><span data-stu-id="bae51-106">Name</span></span></p></th>
<th><p><span data-ttu-id="bae51-107">Описание</span><span class="sxs-lookup"><span data-stu-id="bae51-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bae51-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-108"><strong><a href="recordset2-addnew-method-dao.md">AddNew</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-109">Создает новую запись для обновляемого объекта <strong>Recordset2</strong> .</span><span class="sxs-lookup"><span data-stu-id="bae51-109">Creates a new record for an updatable <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-110"><strong><a href="recordset2-cancel-method-dao.md">Cancel</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-110"><strong><a href="recordset2-cancel-method-dao.md">Cancel</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-111"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bae51-111"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bae51-112">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bae51-112">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bae51-113">Отменяет выполнение ожидающего вызова асинхронного метода (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bae51-113">Cancels execution of a pending asynchronous method call (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-114"><strong><a href="recordset2-cancelupdate-method-dao.md">CancelUpdate</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-115">Отменяет любые незавершенные обновления для объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-115">Cancels any pending updates for a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-116"><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-116"><strong><a href="recordset2-clone-method-dao.md">Clone</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-117">Создает дубликат объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong> , ссылающегося на исходный объект <strong>Recordset2</strong> .</span><span class="sxs-lookup"><span data-stu-id="bae51-117">Creates a duplicate <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that refers to the original <strong>Recordset2</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-118"><strong><a href="recordset2-close-method-dao.md">Close</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-118"><strong><a href="recordset2-close-method-dao.md">Close</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-119">Закрывает открытый объект <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-119">Closes an open <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-120"><strong><a href="recordset2-copyquerydef-method-dao.md">CopyQueryDef</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-121">Возвращает объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong>, который является копией <strong>QueryDef</strong> и используется для создания объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong>, представленного заполнителем recordset (только для рабочие области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-121">Returns a <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object that is a copy of the <strong>QueryDef</strong> used to create the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object represented by the recordset placeholder (Microsoft Access workspaces only).</span></span> <span data-ttu-id="bae51-122">.</span><span class="sxs-lookup"><span data-stu-id="bae51-122"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-123"><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-123"><strong><a href="recordset2-delete-method-dao.md">Delete</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-124">Не поддерживается для объекта.</span><span class="sxs-lookup"><span data-stu-id="bae51-124">Not supported for this object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-125"><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-125"><strong><a href="recordset2-edit-method-dao.md">Edit</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-126">Копирует текущую запись с обновляемым объектом <strong><a href="recordset-object-dao.md">Recordset</a></strong> в буфер обмена для последующего редактирования.</span><span class="sxs-lookup"><span data-stu-id="bae51-126">Copies the current record from an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object to the copy buffer for subsequent editing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-127"><strong><a href="recordset2-fillcache-method-dao.md">FillCache</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-128">Заполняет полностью или частично локальный кэш для объекта <strong>Recordset</strong>, который содержит данные из источника ODBC, подключенного к ядру СУБД Microsoft Access (только для баз данных ODBC, подключенных к Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-128">Fills all or a part of a local cache for a <strong>Recordset</strong> object that contains data from a Microsoft Access database engine-connected ODBC data source (Microsoft Access database engine-connected ODBC databases only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-129"><strong><a href="recordset2-findfirst-method-dao.md">FindFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-130">Определяет положение первой записи в объекте <strong>Recordset</strong> типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-130">Locates the first record in a dynaset- or snapshot-type <strong>Recordset</strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-131"><strong><a href="recordset2-findlast-method-dao.md">FindLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-132">Определяет положение последней записи в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-132">Locates the last record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-133"><strong><a href="recordset2-findnext-method-dao.md">FindNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-134">Определяет положение следующей записи в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-134">Locates the next record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="bae51-135">.</span><span class="sxs-lookup"><span data-stu-id="bae51-135"></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-136"><strong><a href="recordset2-findprevious-method-dao.md">FindPrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-137">Определяет положение предыдущей записи в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-137">Locates the previous record in a dynaset- or snapshot-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object that satisfies the specified criteria and makes that record the current record (Microsoft Access workspaces only).</span></span> <span data-ttu-id="bae51-138">.</span><span class="sxs-lookup"><span data-stu-id="bae51-138"></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-139"><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-139"><strong><a href="recordset2-getrows-method-dao.md">GetRows</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-140">Извлекает несколько строк из объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-140">Retrieves multiple rows from a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-141"><strong><a href="recordset2-move-method-dao.md">Move</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-141"><strong><a href="recordset2-move-method-dao.md">Move</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-142">Перемещает положение текущей записью в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-142">Moves the position of the current record in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-143"><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-143"><strong><a href="recordset2-movefirst-method-dao.md">MoveFirst</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-144">Выполняет перемещение к первой записи в указанном объекте <strong>Recordset</strong> и делает запись текущей.</span><span class="sxs-lookup"><span data-stu-id="bae51-144">Moves to the first record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-145"><strong><a href="recordset2-movelast-method-dao.md">MoveLast</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-146">Выполняет перемещение к последней записи в указанном объекте <strong>Recordset</strong> и делает запись текущей.</span><span class="sxs-lookup"><span data-stu-id="bae51-146">Moves to the last record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-147"><strong><a href="recordset2-movenext-method-dao.md">MoveNext</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-148">Выполняет перемещение к последней записи в указанном объекте <strong>Recordset</strong> и делает запись текущей записью.</span><span class="sxs-lookup"><span data-stu-id="bae51-148">Moves to the next record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-149"><strong><a href="recordset2-moveprevious-method-dao.md">MovePrevious</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-150">Выполняет перемещение к предыдущей записи в указанном объекте <strong>Recordset</strong> и делает запись текущей.</span><span class="sxs-lookup"><span data-stu-id="bae51-150">Moves to the previous record in a specified <strong>Recordset</strong> object and make that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-151"><strong><a href="recordset2-nextrecordset-method-dao.md">NextRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-152"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bae51-152"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bae51-153">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bae51-153">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bae51-154">Получает следующий набор записей, при наличии, возвращаемый состоящим из нескольких частей запросом на выборку в вызове <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> и возвращает <strong>логическое</strong> значение, определяющее, находится ли одна или несколько дополнительных записей в состоянии ожидания (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bae51-154">Gets the next set of records, if any, returned by a multi-part select query in an <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> call, and returns a <strong>Boolean</strong> value indicating whether one or more additional records are pending (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-155"><strong><a href="recordset2-openrecordset-method-dao.md">OpenRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-156">Создает новый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> и добавляет его в коллекцию <strong>Recordsets</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-156">Creates a new <strong><a href="recordset-object-dao.md">Recordset</a></strong> object and appends it to the <strong>Recordsets</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-157"><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-157"><strong><a href="recordset2-requery-method-dao.md">Requery</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-158">Обновляет данные в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> с помощью повторного выполнения запроса, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="bae51-158">Updates the data in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-159"><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-159"><strong><a href="recordset2-seek-method-dao.md">Seek</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-160">Определяет положение записи в индексированном объекте<strong>Recordset</strong> табличного типа, которое отвечает заданным условиям для текущего индекса и превращает данную запись в текущую запись (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-160">Locates the record in an indexed table-type <strong>Recordset</strong> object that satisfies the specified criteria for the current index and makes that record the current record (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-161"><strong><a href="recordset2-update-method-dao.md">Update</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-162"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bae51-162"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bae51-163">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bae51-163">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bae51-164">Сохраняет содержимое буфера обмена в обновляемый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-164">Saves the contents of the copy buffer to an updatable <strong><a href="recordset-object-dao.md">Recordset</a></strong> object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="bae51-165">Свойства</span><span class="sxs-lookup"><span data-stu-id="bae51-165">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="bae51-166">Имя</span><span class="sxs-lookup"><span data-stu-id="bae51-166">Name</span></span></p></th>
<th><p><span data-ttu-id="bae51-167">Описание</span><span class="sxs-lookup"><span data-stu-id="bae51-167">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bae51-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-168"><strong><a href="recordset2-absoluteposition-property-dao.md">AbsolutePosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-169">Задает или возвращает номер относительной записи текущей записи объекта <strong>Recordset2</strong> .</span><span class="sxs-lookup"><span data-stu-id="bae51-169">Sets or returns the relative record number of a <strong>Recordset2</strong> object's current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-170"><strong><a href="recordset2-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-171"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bae51-171"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bae51-172">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bae51-172">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bae51-173">Возвращает количество записей, для которых не удалось выполнить последний пакет обновления (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bae51-173">Returns the number of records that did not complete the last batch update (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-174"><strong><a href="recordset2-batchcollisions-property-dao.md">BatchCollisions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-175"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bae51-175"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bae51-176">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bae51-176">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bae51-177">Возвращает массив закладок, указывающих на строки, которые вызывают конфликты при выполнении последнего пакета обновления (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bae51-177">Returns an array of bookmarks indicating the rows that generated collisions in the last batch update operation (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-178"><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-178"><strong><a href="recordset2-batchsize-property-dao.md">BatchSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-179"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bae51-179"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bae51-180">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bae51-180">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bae51-181">Задает или возвращает количество операторов, отправляемых на сервер в каждом пакете (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bae51-181">Sets or returns the number of statements sent back to the server in each batch (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-182"><strong><a href="recordset2-bof-property-dao.md">BOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-183">Возвращает значение, которое показывает, находится ли текущее положение записи курсора перед первой записью объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-183">Returns a value that indicates whether the current record position is before the first record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="bae51-184">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-184">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-185"><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-185"><strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-186">Задает или возвращает закладку, которая уникально определяет текущую запись в объекте <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-186">Sets or returns a bookmark that uniquely identifies the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-187"><strong><a href="recordset2-bookmarkable-property-dao.md">Bookmarkable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-188">Возвращает значение, которое указывает, поддерживает ли объект <strong>Recordset</strong> закладки, которые можно задать с помощью свойства <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-188">Returns a value that indicates whether a <strong>Recordset</strong> object supports bookmarks, which you can set by using the <strong><a href="recordset2-bookmark-property-dao.md">Bookmark</a></strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-189"><strong><a href="recordset2-cachesize-property-dao.md">CacheSize</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-190">Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально.</span><span class="sxs-lookup"><span data-stu-id="bae51-190">Sets or returns the number of records retrieved from an ODBC data source that will be cached locally.</span></span> <span data-ttu-id="bae51-191">Для чтения и записи, <strong>Long</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-191">Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-192"><strong><a href="recordset2-cachestart-property-dao.md">CacheStart</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-193">Задает или возвращает значение, которое определяет закладку первой записи в объекте Recordset типа dynaset, содержащих данные, локально кэшируемые из источника данных ODBC (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-193">Sets or returns a value that specifies the bookmark of the first record in a dynaset-type Recordset object containing data to be locally cached from an ODBC data source (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-194"><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-194"><strong><a href="recordset2-connection-property-dao.md">Connection</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-195">Возвращает объект <strong><a href="connection-object-dao.md">Connection</a></strong>, который соответствует базе данных.</span><span class="sxs-lookup"><span data-stu-id="bae51-195">Returns the <strong><a href="connection-object-dao.md">Connection</a></strong> object that corresponds to the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-196"><strong><a href="recordset2-datecreated-property-dao.md">DateCreated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-197">Возвращает дату и время создания базовой таблицы (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-197">Returns the date and time a base table was created (Microsoft Access workspaces only).</span></span> <span data-ttu-id="bae51-198">Только для чтения, <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-198">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-199"><strong><a href="recordset2-editmode-property-dao.md">EditMode</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-200">Возвращает значение, которое указывает состояние редактирования для текущей записи.</span><span class="sxs-lookup"><span data-stu-id="bae51-200">Returns a value that indicates the state of editing for the current record.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-201"><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-201"><strong><a href="recordset2-eof-property-dao.md">EOF</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-202">Возвращает значение, которое показывает, находится текущая запись после последней записи объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-202">Returns a value that indicates whether the current record position is after the last record in a <strong>Recordset</strong> object.</span></span> <span data-ttu-id="bae51-203">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-203">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-204"><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-204"><strong><a href="recordset2-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-205">Возвращает коллекцию <strong>Fields</strong>, которая представляет все объекты <strong>Field</strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="bae51-205">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object.</span></span> <span data-ttu-id="bae51-206">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bae51-206">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-207"><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-207"><strong><a href="recordset2-filter-property-dao.md">Filter</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-208">Задает или возвращает значение, определяющее записи, включаемые в открытом впоследствии объект <strong>Recordset</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-208">Sets or returns a value that determines the records included in a subsequently opened <strong>Recordset</strong> object (Microsoft Access workspaces only).</span></span> <span data-ttu-id="bae51-209">Для чтения и записи, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-209">Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-210"><strong><a href="recordset2-index-property-dao.md">Index</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-210"><strong><a href="recordset2-index-property-dao.md">Index</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-211">Задает или возвращает значение, которое указывает имя текущего объекта <strong><a href="index-object-dao.md">Index</a></strong> в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> табличного типа (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-211">Sets or returns a value that indicates the name of the current <strong><a href="index-object-dao.md">Index</a></strong> object in a table-type <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-212"><strong><a href="recordset2-lastmodified-property-dao.md">LastModified</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-213">Возвращает закладку, определяющую самую последнюю из добавленных или измененных записей.</span><span class="sxs-lookup"><span data-stu-id="bae51-213">Returns a ookmark indicating the most recently added or changed record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-214"><strong><a href="recordset2-lastupdated-property-dao.md">LastUpdated</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-215">Возвращает дату и время последнего изменения в базовой таблице.</span><span class="sxs-lookup"><span data-stu-id="bae51-215">Returns the date and time of the most recent change made to a base table.</span></span> <span data-ttu-id="bae51-216">Только для чтения, <strong>Variant</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-216">Read-only <strong>Variant</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-217"><strong><a href="recordset2-lockedits-property-dao.md">LockEdits</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-218">Задает или возвращает значение, определяющее тип блокировки, которая действует во время редактирования.</span><span class="sxs-lookup"><span data-stu-id="bae51-218">Sets or returns a value indicating the type of locking that is in effect while editing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-219"><strong><a href="recordset2-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-220">Возвращает имя указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="bae51-220">Returns the name of the specified object.</span></span> <span data-ttu-id="bae51-221">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-221">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-222"><strong><a href="recordset2-nomatch-property-dao.md">NoMatch</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-223">Указывает, была ли найдена конкретная запись с помощью метода <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> или одного из методов <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-223">Indicates whether a particular record was found by using the <strong><a href="recordset2-seek-method-dao.md">Seek</a></strong> method or one of the <strong><a href="recordset2-findfirst-method-dao.md">Find</a></strong> methods (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-224"><strong><a href="recordset2-parentrecordset-property-dao.md">ParentRecordset</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-225">Возвращает родительский <strong>набор записей</strong> указанного набора записей.</span><span class="sxs-lookup"><span data-stu-id="bae51-225">Returns the parent <strong>Recordset</strong> of the specified recordset.</span></span> <span data-ttu-id="bae51-226">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bae51-226">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-227"><strong><a href="recordset2-percentposition-property-dao.md">PercentPosition</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-228">Задает или возвращает значение, определяющее приблизительное место текущей записи в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> на основе процента записей в <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-228">Sets or returns a value indicating the approximate location of the current record in the <strong><a href="recordset-object-dao.md">Recordset</a></strong> object based on a percentage of the records in the <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-229"><strong><a href="recordset2-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-229"><strong><a href="recordset2-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-230">Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта.</span><span class="sxs-lookup"><span data-stu-id="bae51-230">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object.</span></span> <span data-ttu-id="bae51-231">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="bae51-231">Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-232"><strong><a href="recordset2-recordcount-property-dao.md">RecordCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-233">Возвращает число записей, доступных в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong>, или общее количество записей в <strong>Recordset</strong> табличного типа.</span><span class="sxs-lookup"><span data-stu-id="bae51-233">Returns the number of records accessed in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object, or the total number of records in a table-type <strong>Recordset</strong> object.</span></span> <span data-ttu-id="bae51-234">или объекте <strong><a href="tabledef-object-dao.md">TableDef</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-234">or <strong><a href="tabledef-object-dao.md">TableDef</a></strong> object.</span></span> <span data-ttu-id="bae51-235">Только для чтения, <strong>Long</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-235">Read-only <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-236"><strong><a href="recordset2-recordstatus-property-dao.md">RecordStatus</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-237"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bae51-237"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bae51-238">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bae51-238">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bae51-239">Возвращает значение, определяющее состояние обновления текущей записи, если она входит в пакет обновления (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bae51-239">Returns a value indicating the update status of the current record if it is part of a batch update (ODBCDirect workspaces only).</span></span> <span data-ttu-id="bae51-240">Только для чтения, <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-240">Read-only <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-241"><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-241"><strong><a href="recordset2-restartable-property-dao.md">Restartable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-242">Возвращает значение, которое указывает на то, поддерживает ли объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> метод <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong>, который повторно выполняет запрос, на котором основан объект <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-242">Returns a value that indicates whether a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object supports the <strong><a href="recordset2-requery-method-dao.md">Requery</a></strong> method, which re-executes the query on which the <strong>Recordset</strong> object is based.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-243"><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-243"><strong><a href="recordset2-sort-property-dao.md">Sort</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-244">Задает или возвращает порядок сортировки для записей в объекте <strong> <a href="recordset-object-dao.md">Recordset</a> </strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-244">Sets or returns the sort order for records in a <strong><a href="recordset-object-dao.md">Recordset</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-245"><strong><a href="recordset2-stillexecuting-property-dao.md">StillExecuting</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-246"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bae51-246"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bae51-247">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bae51-247">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bae51-248">Указывает на то, завершена или нет асинхронной операции (т. е метода, вызываемого с параметром <strong>dbRunAsync</strong>) (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bae51-248">Indicates whether or not an asynchronous operation (that is, a method called with the <strong>dbRunAsync</strong> option) has finished executing (ODBCDirect workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-249"><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-249"><strong><a href="recordset2-transactions-property-dao.md">Transactions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-250">Возвращает значение, которое указывает на то, поддерживает ли объект транзакций.</span><span class="sxs-lookup"><span data-stu-id="bae51-250">Returns a value that indicates whether an object supports transactions.</span></span> <span data-ttu-id="bae51-251">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-251">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-252"><strong><a href="recordset2-type-property-dao.md">Тип</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-252"><strong><a href="recordset2-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-253">Задает или возвращает значение, которое указывает операционный тип или тип данных объекта.</span><span class="sxs-lookup"><span data-stu-id="bae51-253">Sets or returns a value that indicates the operational type or data type of an object.</span></span> <span data-ttu-id="bae51-254">Только для чтения, <strong>Integer</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-254">Read-only <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-255"><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-255"><strong><a href="recordset2-updatable-property-dao.md">Updatable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-256">Возвращает значение, которое указывает на то, можно ли изменить DAO объект.</span><span class="sxs-lookup"><span data-stu-id="bae51-256">Returns a value that indicates whether you can change a DAO object.</span></span> <span data-ttu-id="bae51-257">Только для чтения, <strong>Boolean</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-257">Read-only <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-258"><strong><a href="recordset2-updateoptions-property-dao.md">UpdateOptions</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-259"><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013.</span><span class="sxs-lookup"><span data-stu-id="bae51-259"><strong>NOTE</strong>: ODBCDirect workspaces are not supported in Microsoft Access 2013.</span></span> <span data-ttu-id="bae51-260">Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="bae51-260">Use ADO if you want to access external data sources without using the Microsoft Access database engine.</span></span></p>
<p><span data-ttu-id="bae51-261">Задает или возвращает значение, которое указывает на то, как предложение WHERE создается для каждой записи во время обновления пакета, а также будет ли пакет обновления использовать оператор UPDATE или DELETE, за которым следует INSERT (только для рабочих областей ODBCDirect).</span><span class="sxs-lookup"><span data-stu-id="bae51-261">Sets or returns a value that indicates how the WHERE clause is constructed for each record during a batch update, and whether the batch update should use an UPDATE statement or a DELETE followed by an INSERT (ODBCDirect workspaces only).</span></span> <span data-ttu-id="bae51-262">Чтение и запись, <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-262">Read/write <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bae51-263"><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-263"><strong><a href="recordset2-validationrule-property-dao.md">ValidationRule</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-264">Задает или возвращает значение, которое проверяет данные в поле после его добавление или изменения в таблице (только для рабочих областей Microsoft Access). Чтение и запись, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-264">Sets or returns a value that validates the data in a field as it's changed or added to a table (Microsoft Access workspaces only).Read/write <strong>String</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bae51-265"><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></span><span class="sxs-lookup"><span data-stu-id="bae51-265"><strong><a href="recordset2-validationtext-property-dao.md">ValidationText</a></strong></span></span></p></td>
<td><p><span data-ttu-id="bae51-266">Задает или возвращает значение, определяющее текст сообщения, которое отображает ваше приложение, если значение объекта <strong>Field</strong> не удовлетворяют правилу проверки, задаваемому настройкой параметра <strong>ValidationRule</strong> (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="bae51-266">Sets or returns a value that specifies the text of the message that your application displays if the value of a <strong>Field</strong> object doesn't satisfy the validation rule specified by the <strong>ValidationRule</strong> property setting (Microsoft Access workspaces only).</span></span> <span data-ttu-id="bae51-267">Только для чтения, <strong>String</strong>.</span><span class="sxs-lookup"><span data-stu-id="bae51-267">Read-only <strong>String</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

