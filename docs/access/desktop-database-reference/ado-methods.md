---
title: ActiveX data Objects (ADO) methods
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3169b7eaab6ad290bfc385881f5de69edc80111f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283284"
---
# <a name="ado-methods"></a><span data-ttu-id="e7bd2-102">Методы ADO</span><span class="sxs-lookup"><span data-stu-id="e7bd2-102">ADO methods</span></span>

<span data-ttu-id="e7bd2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e7bd2-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="e7bd2-104">Метод</span><span class="sxs-lookup"><span data-stu-id="e7bd2-104">Method</span></span></th>
<th><span data-ttu-id="e7bd2-105">Описание</span><span class="sxs-lookup"><span data-stu-id="e7bd2-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-106"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-106"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-107">Создает новую запись для обновляемого объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-107">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-108"><a href="append-method-ado.md">Append</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-108"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-109">Привносимый объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-109">Appends an object to a collection.</span></span> <span data-ttu-id="e7bd2-110">Если коллекция является <strong>Fields,</strong> <strong>перед</strong> его приложением в коллекцию может быть создан новый объект Field.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-110">If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans и RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-114">Управляет обработкой транзакций в <strong>объекте Connection</strong> следующим образом:</span><span class="sxs-lookup"><span data-stu-id="e7bd2-114">Manages transaction processing within a <strong>Connection</strong> object as follows:</span></span><br/><br/><span data-ttu-id="e7bd2-115"><strong>BeginTrans</strong> — начинает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-115"><strong>BeginTrans</strong> — Begins a new transaction.</span></span><br/><br/><span data-ttu-id="e7bd2-116">
<strong>CommitTrans</strong> — сохраняет все изменения и завершает текущую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-116">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction.</span></span> <span data-ttu-id="e7bd2-117">Он также может запустить новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-117">It may also start a new transaction.</span></span><br/><br/><span data-ttu-id="e7bd2-118">
<strong>RollbackTrans</strong> — отменяет все изменения и завершает текущую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-118">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="e7bd2-119">Он также может запустить новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-119">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-120"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-120"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-121">Отменяет выполнение ожидающих вызовов асинхронного метода.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-121">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-123">Отменяет ожидающих пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-123">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-125">Отменяет все изменения, внесенные в текущую или новую строку объекта <strong>Recordset</strong> или коллекцию <strong>Fields</strong> объекта <strong>Record,</strong> перед вызовом <strong>метода Update.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-125">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-126"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-126"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-127">Удаляет все объекты <strong>Error</strong> из коллекции <strong>Errors.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-127">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-128"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-128"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-129">Создает дубликат <strong>объекта Recordset</strong> из существующего <strong>объекта Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-129">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object.</span></span> <span data-ttu-id="e7bd2-130">При желании указывает, что клон должен быть только для чтения.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-130">Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-131"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-131"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-132">Закрывает открытый объект и все зависимые объекты.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-132">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-134">Сравнивает две закладки и возвращает индикатор их относительных значений.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-134">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-136">Копирует файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-136">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-137"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-137"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-138">Копирует указанное количество символов или ветвей (в зависимости от <strong>типа)</strong> <strong>в потоке</strong> в другой <strong>объект Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-138">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-139"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-139"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-140">Создает новый объект <strong>Parameter</strong> с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-140">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-142">Удаляет объект из коллекции <strong>Parameters.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-142">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-144">Удаляет объект из коллекции <strong>Fields.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-144">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-146">Удаляет текущую запись или группу записей.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-146">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-148">Удаляет файл или каталог и все его подкадиректоры.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-148">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-150">Выполняет запрос, SQL или хранимую процедуру, указанную в свойстве <strong>CommandText.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-152">Выполняет указанный запрос, SQL оператор, хранимую процедуру или текст для конкретного поставщика.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-153"><a href="find-method-ado.md">Поиск</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-153"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-154">Выполняет поиск <strong>в наборе</strong> записей строки, которая соответствует указанным условиям.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-154">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-155"><a href="flush-method-ado.md">Flush</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-155"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-156">Привнося содержимое потока, <strong>оставшегося</strong> в буфере ADO, к основному объекту, с которым связан <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-156">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-157"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-157"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-158">Возвращает набор <strong>записей,</strong> строки которого представляют файлы и подкадиректоры в каталоге, представленном этой <strong>записью.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-158">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-159"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-159"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-160">Возвращает все или часть содержимого большого текста или двоичного объекта <strong>field.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-160">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-161"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-161"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-162">Извлекает несколько записей объекта <strong>Recordset</strong> в массив.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-162">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-163"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-163"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-164">Возвращает набор <strong>записей в</strong> качестве строки.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-164">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-166">Загружает содержимое существующего файла в <strong>поток.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-166">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-167"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-167"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-168">Перемещает положение текущей записи в объекте <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-168">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext и MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-170">Перемещается к первой, последней, следующей или предыдущей записи в указанном объекте <strong>Recordset</strong> и делает запись текущей.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-170">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-171"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-171"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-172">Перемещает файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-172">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-174">Очищает текущий <strong>объект Recordset</strong> и возвращает следующий набор <strong>записей</strong> путем надвигания с помощью ряда команд.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-174">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-176">Открывает подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-176">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-178">Открывает существующий <strong>объект Record</strong> или создает новый файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-178">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-180">Открывает курсор.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-180">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-182">Открывает объект <strong>Stream</strong> для управления потоками двоичных или текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-182">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-183"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-183"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-184">Получает сведения о схеме базы данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-184">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-185"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-185"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-186">Считывает указанное количество ветвей из объекта <strong>Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-186">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-187"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-187"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-188">Считывая указанное количество символов из объекта <strong>Text Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-188">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-189"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-189"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-190">Обновляет объекты в коллекции, чтобы отразить объекты, доступные поставщику и относяющиеся к конкретному поставщику.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-190">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-191"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-191"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-192">Обновляет данные в объекте <strong>Recordset</strong> с помощью повторного выполнения запроса, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-192">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-193"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-193"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-194">Обновляет данные в текущем объекте <strong>Recordset</strong> или коллекции <strong>Fields</strong> объекта <strong>Record</strong> из базы данных.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-194">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-195"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-195"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-196">Сохраняет набор <strong>записей в</strong> файле или <strong>объекте Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-196">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-197"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-197"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-198">Сохраняет двоичное содержимое <strong>Stream</strong> в файл.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-198">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-199"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-199"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-200">Выполняет поиск в индексе наборов <strong>записей,</strong> чтобы быстро найти строку, которая соответствует указанным значениям, и изменяет текущую позицию строки на эту строку.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-200">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-201"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-201"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-202">Задает положение, которое является окончанием потока.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-202">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-203"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-203"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-204">Пропускает всю строку при чтении текстового потока.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-204">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-205"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-205"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-206">Получает статистическую информацию об открытом потоке.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-206">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-207"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-207"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-208">Определяет, поддерживает ли указанный <strong>объект Recordset</strong> определенный тип функций.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-208">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-209"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-209"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-210">Сохраняет все изменения, внесенные в текущую строку объекта <strong>Recordset</strong> или коллекцию <strong>Fields</strong> объекта <strong>Record.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-210">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-212">Записывает все ожидающих пакетных обновлений на диск.</span><span class="sxs-lookup"><span data-stu-id="e7bd2-212">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7bd2-213"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-213"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-214">Записывает двоичные данные в <strong>объект Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-214">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7bd2-215"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="e7bd2-215"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="e7bd2-216">Записывает указанную текстовую строку в <strong>объект Stream.</strong></span><span class="sxs-lookup"><span data-stu-id="e7bd2-216">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
