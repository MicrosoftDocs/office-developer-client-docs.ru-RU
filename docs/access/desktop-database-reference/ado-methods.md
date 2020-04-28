---
title: Методы объектов данных ActiveX (ADO)
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
# <a name="ado-methods"></a><span data-ttu-id="9ef61-102">Методы ADO</span><span class="sxs-lookup"><span data-stu-id="9ef61-102">ADO methods</span></span>

<span data-ttu-id="9ef61-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9ef61-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="9ef61-104">Метод</span><span class="sxs-lookup"><span data-stu-id="9ef61-104">Method</span></span></th>
<th><span data-ttu-id="9ef61-105">Описание</span><span class="sxs-lookup"><span data-stu-id="9ef61-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-106"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-106"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-107">Создает новую запись для обновляемого объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="9ef61-107">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-108"><a href="append-method-ado.md">Error</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-108"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-109">Добавляет объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="9ef61-109">Appends an object to a collection.</span></span> <span data-ttu-id="9ef61-110">Если коллекция является <strong>полями</strong>, новый объект <strong>field</strong> можно создать перед добавлением в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="9ef61-110">If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-112">Добавляет данные в <strong>поле</strong>большого текста или двоичных данных или в объект <strong>Parameter</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans и RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-114">Управляет обработкой транзакций в объекте <strong>Connection</strong> , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="9ef61-114">Manages transaction processing within a <strong>Connection</strong> object as follows:</span></span><br/><br/><span data-ttu-id="9ef61-115"><strong>BeginTrans</strong> — начинает новую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="9ef61-115"><strong>BeginTrans</strong> — Begins a new transaction.</span></span><br/><br/><span data-ttu-id="9ef61-116">
<strong>CommitTrans</strong> — сохраняет все изменения и завершает текущую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="9ef61-116">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction.</span></span> <span data-ttu-id="9ef61-117">Кроме того, может начаться новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="9ef61-117">It may also start a new transaction.</span></span><br/><br/><span data-ttu-id="9ef61-118">
<strong>RollbackTrans</strong> — отменяет все изменения и завершает текущую транзакцию.</span><span class="sxs-lookup"><span data-stu-id="9ef61-118">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="9ef61-119">Кроме того, может начаться новая транзакция.</span><span class="sxs-lookup"><span data-stu-id="9ef61-119">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-120"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-120"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-121">Отменяет выполнение ожидающего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="9ef61-121">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-123">Отменяет ожидающее пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="9ef61-123">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-125">Отменяет любые изменения, внесенные в текущую или новую строку объекта <strong>Recordset</strong> , или коллекцию <strong>Fields</strong> объекта <strong>Record</strong> перед вызовом метода <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-125">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-126"><a href="clear-method-ado.md">Clear</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-126"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-127">Удаляет все объекты <strong>Error</strong> из коллекции <strong>Errors</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-127">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-128"><a href="clone-method-ado.md">Clone</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-128"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-129">Создает дубликат объекта <strong>Recordset</strong> из существующего объекта <strong>Recordset</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-129">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object.</span></span> <span data-ttu-id="9ef61-130">При необходимости этот параметр указывает, что клон должен быть доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="9ef61-130">Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-131"><a href="close-method-ado.md">Close</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-131"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-132">Закрывает открытый объект и все зависимые объекты.</span><span class="sxs-lookup"><span data-stu-id="9ef61-132">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-134">Сравнивает две закладки и возвращает сведения об их относительных значениях.</span><span class="sxs-lookup"><span data-stu-id="9ef61-134">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-136">Копирует файл или каталог, а также его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="9ef61-136">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-137"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-137"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-138">Копирует указанное число символов или байтов (в зависимости от <strong>типа</strong>) в <strong>потоке</strong> в другой объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-138">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-139"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-139"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-140">Создает новый объект <strong>Parameter</strong> с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="9ef61-140">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-141"><a href="delete-method-ado-parameters-collection.md">Delete (Коллекция параметров ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-142">Удаляет объект из коллекции <strong>Parameters</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-142">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-143"><a href="delete-method-ado-fields-collection.md">Delete (коллекция Fields в ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-144">Удаляет объект из коллекции <strong>Fields</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-144">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-145"><a href="delete-method-ado-recordset.md">Delete (объект Recordset в ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-146">Удаляет текущую запись или группу записей.</span><span class="sxs-lookup"><span data-stu-id="9ef61-146">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-148">Удаляет файл или каталог и все его подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="9ef61-148">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Выполнение (команда ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-149"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-150">Выполняет запрос, инструкцию SQL или хранимую процедуру, указанную в свойстве <strong>CommandText</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Выполнение (подключение ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-151"><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-152">Выполняет указанный запрос, инструкцию SQL, хранимую процедуру или текст, зависящий от поставщика.</span><span class="sxs-lookup"><span data-stu-id="9ef61-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-153"><a href="find-method-ado.md">Поиск</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-153"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-154">Выполняет поиск в <strong>наборе записей</strong> для строки, удовлетворяющей заданным условиям.</span><span class="sxs-lookup"><span data-stu-id="9ef61-154">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-155"><a href="flush-method-ado.md">Удален</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-155"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-156">Принудительно применяет содержимое <strong>потока</strong> , оставшееся в БУФЕРе ADO, к базовому объекту, с которым связан <strong>поток</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-156">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-157"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-157"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-158">Возвращает объект <strong>Recordset</strong> , строки которого представляют файлы и подкаталоги в каталоге, представленном этой <strong>записью</strong>.</span><span class="sxs-lookup"><span data-stu-id="9ef61-158">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-159"><a href="getchunk-method-ado.md">GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-159"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-160">Возвращает значение ALL или часть содержимого большого текстового или двоичного <strong>объекта данных</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-160">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-161"><a href="getrows-method-ado.md">GetRows</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-161"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-162">Получает несколько записей объекта <strong>Recordset</strong> в массив.</span><span class="sxs-lookup"><span data-stu-id="9ef61-162">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-163"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-163"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-164">Возвращает объект <strong>Recordset</strong> в виде строки.</span><span class="sxs-lookup"><span data-stu-id="9ef61-164">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-166">Загружает содержимое существующего файла в <strong>поток</strong>.</span><span class="sxs-lookup"><span data-stu-id="9ef61-166">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-167"><a href="move-method-ado.md">Move</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-167"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-168">Перемещает положение текущей записи в объекте <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="9ef61-168">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext и MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-170">Перемещение к первой, последней, следующей или предыдущей записи в указанном объекте <strong>Recordset</strong> и делает эту запись текущей.</span><span class="sxs-lookup"><span data-stu-id="9ef61-170">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-171"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-171"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-172">Перемещает файл или каталог вместе с его содержимым в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="9ef61-172">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-174">Очищает текущий объект <strong>Recordset</strong> и возвращает следующий <strong>набор записей</strong> путем перемещения по ряду команд.</span><span class="sxs-lookup"><span data-stu-id="9ef61-174">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-175"><a href="open-method-ado-connection.md">Open (подключение ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-176">Открывает подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="9ef61-176">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-177"><a href="open-method-ado-record.md">Открыть (запись ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-178">Открывает существующий объект <strong>Record</strong> или создает новый файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="9ef61-178">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-179"><a href="open-method-ado-recordset.md">Открыть (набор записей ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-180">Открывает курсор.</span><span class="sxs-lookup"><span data-stu-id="9ef61-180">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-181"><a href="open-method-ado-stream.md">Открыть (поток ADO)</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-182">Открывает объект <strong>Stream</strong> для управления потоками двоичных или текстовых данных.</span><span class="sxs-lookup"><span data-stu-id="9ef61-182">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-183"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-183"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-184">Получает сведения о схеме базы данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="9ef61-184">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-185"><a href="read-method-ado.md">Чтение</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-185"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-186">Считывает заданное число байтов из объекта <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-186">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-187"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-187"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-188">Считывает заданное число символов из текстового объекта <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-188">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-189"><a href="refresh-method-ado.md">Refresh</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-189"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-190">Обновляет объекты в коллекции, чтобы отразить объекты, доступные поставщику и соответствующие объекты.</span><span class="sxs-lookup"><span data-stu-id="9ef61-190">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-191"><a href="requery-method-ado.md">Requery</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-191"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-192">Обновляет данные в объекте <strong>Recordset</strong> с помощью повторного выполнения запроса, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="9ef61-192">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-193"><a href="resync-method-ado.md">Resync</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-193"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-194">Обновляет данные в текущем объекте <strong>Recordset</strong> или коллекции <strong>полей</strong> объекта <strong>Record</strong> из основной базы данных.</span><span class="sxs-lookup"><span data-stu-id="9ef61-194">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-195"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-195"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-196">Сохраняет <strong>набор записей</strong> в объекте File или <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-196">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-197"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-197"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-198">Сохраняет двоичное содержимое <strong>потока</strong> в файл.</span><span class="sxs-lookup"><span data-stu-id="9ef61-198">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-199"><a href="seek-method-ado.md">Seek</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-199"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-200">Выполняет поиск в индексе объекта <strong>Recordset</strong> , чтобы быстро найти строку, которая соответствует указанным значениям, и изменяет положение текущей строки на эту строку.</span><span class="sxs-lookup"><span data-stu-id="9ef61-200">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-201"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-201"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-202">Задает позицию, которая является концом потока.</span><span class="sxs-lookup"><span data-stu-id="9ef61-202">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-203"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-203"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-204">Пропускает одну строку целиком при чтении текстового потока.</span><span class="sxs-lookup"><span data-stu-id="9ef61-204">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-205"><a href="stat-method-ado.md">Stat</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-205"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-206">Возвращает статистические сведения о открытом потоке.</span><span class="sxs-lookup"><span data-stu-id="9ef61-206">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-207"><a href="supports-method-ado.md">Имеется</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-207"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-208">Определяет, поддерживает ли указанный объект <strong>Recordset</strong> определенный тип функциональных возможностей.</span><span class="sxs-lookup"><span data-stu-id="9ef61-208">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-209"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="9ef61-209"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-210">Сохраняет все изменения, внесенные в текущую строку объекта <strong>Recordset</strong> , или коллекцию <strong>Fields</strong> объекта <strong>Record</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-210">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-212">Записывает все ожидающие пакетные обновления на диск.</span><span class="sxs-lookup"><span data-stu-id="9ef61-212">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9ef61-213"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-213"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-214">Записывает двоичные данные в объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-214">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9ef61-215"><a href="writetext-method-ado.md">Инструкция</a></span><span class="sxs-lookup"><span data-stu-id="9ef61-215"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="9ef61-216">Записывает указанную текстовую строку в объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="9ef61-216">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>
