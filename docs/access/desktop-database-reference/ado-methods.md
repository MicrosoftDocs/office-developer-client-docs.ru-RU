---
title: Методы ActiveX Data Objects (ADO)
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3649a7146c0d6ab70bc5f785404f03269df1540b
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910805"
---
# <a name="ado-methods"></a><span data-ttu-id="15a0c-102">Методы ADO</span><span class="sxs-lookup"><span data-stu-id="15a0c-102">ADO methods</span></span>

<span data-ttu-id="15a0c-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="15a0c-103">**Applies to**: Access 2013, Office 2013</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th><span data-ttu-id="15a0c-104">Метод</span><span class="sxs-lookup"><span data-stu-id="15a0c-104">Method</span></span></th>
<th><span data-ttu-id="15a0c-105">Описание</span><span class="sxs-lookup"><span data-stu-id="15a0c-105">Description</span></span></th>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-106"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-106"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-107">Создает новую запись для обновляемых объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-107">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-108"><a href="append-method-ado.md">Добавление</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-108"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-109">Добавляет объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="15a0c-109">Appends an object to a collection.</span></span> <span data-ttu-id="15a0c-110">Если семейство <strong>полей</strong>, могут быть созданы новый объект <strong>поля</strong> перед добавлением в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="15a0c-110">If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-111"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-112">Добавляет данные большого текстового или двоичных данных <strong>поля</strong>или к объекту <strong>параметра</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-112">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans CommitTrans и RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-113"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-114">Управляет транзакций обработка объект <strong>подключения</strong> следующим образом:</span><span class="sxs-lookup"><span data-stu-id="15a0c-114">Manages transaction processing within a <strong>Connection</strong> object as follows:</span></span><br/><br/><span data-ttu-id="15a0c-115"><strong>BeginTrans</strong> — начало новой транзакции.</span><span class="sxs-lookup"><span data-stu-id="15a0c-115"><strong>BeginTrans</strong> — Begins a new transaction.</span></span><br/><br/><span data-ttu-id="15a0c-116">
<strong>CommitTrans</strong> — сохраняет все изменения и заканчивающейся текущей операции.</span><span class="sxs-lookup"><span data-stu-id="15a0c-116">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction.</span></span> <span data-ttu-id="15a0c-117">Он также может начать новую операцию.</span><span class="sxs-lookup"><span data-stu-id="15a0c-117">It may also start a new transaction.</span></span><br/><br/><span data-ttu-id="15a0c-118">
<strong>RollbackTrans</strong> — показано, как отменить все изменения и заканчивающейся текущей операции.</span><span class="sxs-lookup"><span data-stu-id="15a0c-118">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="15a0c-119">Он также может начать новую операцию.</span><span class="sxs-lookup"><span data-stu-id="15a0c-119">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-120"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-120"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-121">Отменяет выполнение ожидающих асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="15a0c-121">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-122"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-123">Показано, как отменить ожидающие пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="15a0c-123">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-124"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-125">Отменяет все изменения, внесенные в строку текущей или новый объект <strong>набора записей</strong> или коллекции <strong>полей</strong> объекта <strong>записи</strong> , прежде чем вызывать метод <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-125">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-126"><a href="clear-method-ado.md">Очистить</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-126"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-127">Удаляет все объекты <strong>ошибок</strong> из семейства <strong>Errors</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-127">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-128"><a href="clone-method-ado.md">Копия</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-128"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-129">Создает объект повторяющихся <strong>записей</strong> из существующего объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-129">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object.</span></span> <span data-ttu-id="15a0c-130">При необходимости указывает копию только для чтения.</span><span class="sxs-lookup"><span data-stu-id="15a0c-130">Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-131"><a href="close-method-ado.md">Закрыть</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-131"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-132">Закрывает открытый объект и любые зависящие объекты.</span><span class="sxs-lookup"><span data-stu-id="15a0c-132">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-133"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-134">Сравнение двух закладки и возвращает сведения об их значения.</span><span class="sxs-lookup"><span data-stu-id="15a0c-134">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-135"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-136">Копирует файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="15a0c-136">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-137"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-137"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-138">Копирует указанного числа символов или байтов (в зависимости от <strong>типа</strong>) в <strong>потоке</strong> другой объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-138">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-139"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-139"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-140">Создает новый объект <strong>параметр</strong> с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="15a0c-140">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-141"><a href="delete-method-ado-parameters-collection.md">Удаление (коллекции параметров ADO)</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-141"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-142">Удаляет объект из коллекции <strong>параметров</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-142">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-143"><a href="delete-method-ado-fields-collection.md">Удаление (коллекции полей ADO)</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-143"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-144">Удаляет объект из коллекции <strong>полей</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-144">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-145"><a href="delete-method-ado-recordset.md">Удаление (записей ADO)</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-145"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-146">Удаление текущей записи или группы записей.</span><span class="sxs-lookup"><span data-stu-id="15a0c-146">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-147"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-148">Удаляет файл или каталог и все его подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="15a0c-148">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-149"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Воспользуйтесь командой (ADO)</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-149"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-150">Выполняет запрос, инструкции SQL или хранимую процедуру, указанных в свойстве <strong>CommandText</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-150">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-151"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Выполнение (ADO-подключение)</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-151"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-152">Выполняет указанному запросу, оператор SQL, хранимую процедуру или текст от поставщика.</span><span class="sxs-lookup"><span data-stu-id="15a0c-152">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-153"><a href="find-method-ado.md">Найти</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-153"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-154">Выполняет поиск <strong>записей</strong> для строки, которая должна удовлетворять определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="15a0c-154">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-155"><a href="flush-method-ado.md">Очистка</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-155"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-156">Принудительно содержимое <strong>потока</strong> , оставшихся в буфер ADO для базового объекта, с которым связано <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-156">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-157"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-157"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-158">Возвращает <strong>набор записей</strong> , строки представляют файлы и вложенные папки в каталоге, представленный этой <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="15a0c-158">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-159"><a href="getchunk-method-ado.md">Методы GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-159"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-160">Возвращает все или части, содержимое большого текстового или объекта <strong>поля</strong> двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="15a0c-160">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-161"><a href="getrows-method-ado.md">Получение строк</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-161"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-162">Извлекает нескольких записей объекта <strong>набора записей</strong> в массив.</span><span class="sxs-lookup"><span data-stu-id="15a0c-162">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-163"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-163"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-164">Возвращает <strong>набор записей</strong> в виде строки.</span><span class="sxs-lookup"><span data-stu-id="15a0c-164">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-165"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-166">Загружает содержимое существующего файла в <strong>поток</strong>.</span><span class="sxs-lookup"><span data-stu-id="15a0c-166">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-167"><a href="move-method-ado.md">Перемещение</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-167"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-168">Перемещает положение текущей записи в объекте <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-168">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext и MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-169"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-170">Перемещает имя, Фамилия следующий или предыдущий записи в указанном объекте <strong>набора записей</strong> и делает, запишите текущей записи.</span><span class="sxs-lookup"><span data-stu-id="15a0c-170">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-171"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-171"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-172">Перемещает файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="15a0c-172">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-173"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-174">Удаляет текущий объект <strong>набора записей</strong> и возвращает следующего <strong>набора записей</strong> путем перемещения через последовательность команд.</span><span class="sxs-lookup"><span data-stu-id="15a0c-174">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-175"><a href="open-method-ado-connection.md">Откройте (ADO-подключение)</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-175"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-176">Открывает подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="15a0c-176">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-177"><a href="open-method-ado-record.md">Откройте (ADO запись)</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-177"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-178">Открывает существующий объект <strong>записи</strong> или создает новый файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="15a0c-178">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-179"><a href="open-method-ado-recordset.md">Откройте (записей ADO)</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-179"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-180">Открывается курсор.</span><span class="sxs-lookup"><span data-stu-id="15a0c-180">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-181"><a href="open-method-ado-stream.md">Открыть (поток ADO)</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-181"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-182">Открывает объект <strong>Stream</strong> для работы с потоки данных двоичный или текст.</span><span class="sxs-lookup"><span data-stu-id="15a0c-182">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-183"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-183"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-184">Получает сведения о схеме базы данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="15a0c-184">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-185"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-185"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-186">Считывает указанное число байтов из объекта <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-186">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-187"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-187"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-188">Считывает указанное количество символов из объекта <strong>потока</strong> текста.</span><span class="sxs-lookup"><span data-stu-id="15a0c-188">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-189"><a href="refresh-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-189"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-190">Обновление объектов в коллекции объектов, доступных из и относящиеся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="15a0c-190">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-191"><a href="requery-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-191"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-192">Обновляет данные в объект <strong>набора записей</strong> , повторное выполнение запросов, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="15a0c-192">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-193"><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-193"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-194">Обновляет данные в текущий объект <strong>набора записей</strong> или коллекции <strong>полей</strong> объекта <strong>записи</strong> из базы данных.</span><span class="sxs-lookup"><span data-stu-id="15a0c-194">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-195"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-195"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-196">Сохранение <strong>набора записей</strong> в файл или объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-196">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-197"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-197"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-198">Сохраняет двоичные содержимое <strong>потока</strong> в файл.</span><span class="sxs-lookup"><span data-stu-id="15a0c-198">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-199"><a href="seek-method-ado.md">Поиск</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-199"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-200">Выполняет поиск индекса <strong>набора записей</strong> для быстрого поиска строку, в которой совпадает с указанными значениями и изменяет текущее положение строки на эту строку.</span><span class="sxs-lookup"><span data-stu-id="15a0c-200">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-201"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-201"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-202">Задает позицию за конец потока.</span><span class="sxs-lookup"><span data-stu-id="15a0c-202">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-203"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-203"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-204">Пропускает одну всю строку при чтении текстовый поток.</span><span class="sxs-lookup"><span data-stu-id="15a0c-204">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-205"><a href="stat-method-ado.md">Статистика</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-205"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-206">Получает статистические сведения об open потока.</span><span class="sxs-lookup"><span data-stu-id="15a0c-206">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-207"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-207"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-208">Определяет, поддерживает ли указанный объект <strong>набора записей</strong> определенного типа функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="15a0c-208">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-209"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="15a0c-209"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-210">Сохраняет все изменения, внесенные в текущей строки <strong>набора записей</strong> объекта или коллекции <strong>полей</strong> объекта <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-210">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-211"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-212">Записывает все ожидающие пакета обновления на диск.</span><span class="sxs-lookup"><span data-stu-id="15a0c-212">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15a0c-213"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-213"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-214">Записывает двоичные данные в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-214">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15a0c-215"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="15a0c-215"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="15a0c-216">Записывает строку, указанный текст в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="15a0c-216">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>