---
title: Объекты данных ActiveX (ADO) методы
TOCTitle: ADO Methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 6ef05e7f322b769102ce25aab7dfc26a75b0aa22
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879335"
---
# <a name="ado-methods"></a><span data-ttu-id="0f77b-102">Методы ADO</span><span class="sxs-lookup"><span data-stu-id="0f77b-102">ADO Methods</span></span>


<span data-ttu-id="0f77b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="0f77b-103">**Applies to**: Access 2013, Office 2013</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-104"><a href="addnew-method-ado.md">AddNew</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-104"><a href="addnew-method-ado.md">AddNew</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-105">Создает новую запись для обновляемых объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-105">Creates a new record for an updatable <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-106"><a href="append-method-ado.md">Добавление</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-106"><a href="append-method-ado.md">Append</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-107">Добавляет объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="0f77b-107">Appends an object to a collection.</span></span> <span data-ttu-id="0f77b-108">Если семейство <strong>полей</strong>, могут быть созданы новый объект <strong>поля</strong> перед добавлением в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="0f77b-108">If the collection is <strong>Fields</strong>, a new <strong>Field</strong> object may be created before it is appended to the collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-109"><a href="appendchunk-method-ado.md">AppendChunk</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-109"><a href="appendchunk-method-ado.md">AppendChunk</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-110">Добавляет данные большого текстового или двоичных данных <strong>поля</strong>или к объекту <strong>параметра</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-110">Appends data to a large text or binary data <strong>Field</strong>, or to a <strong>Parameter</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans CommitTrans и RollbackTrans</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-111"><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans, and RollbackTrans</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-112">Управляет транзакций обработка объект <strong>подключения</strong> следующим образом: <strong>BeginTrans</strong> — начало новой транзакции.</span><span class="sxs-lookup"><span data-stu-id="0f77b-112">Manages transaction processing within a <strong>Connection</strong> object as follows: <strong>BeginTrans</strong> — Begins a new transaction.</span></span><br /><span data-ttu-id="0f77b-113">
<strong>CommitTrans</strong> — сохраняет все изменения и заканчивающейся текущей операции.</span><span class="sxs-lookup"><span data-stu-id="0f77b-113">
<strong>CommitTrans</strong> — Saves any changes and ends the current transaction.</span></span> <span data-ttu-id="0f77b-114">Он также может начать новую операцию.</span><span class="sxs-lookup"><span data-stu-id="0f77b-114">It may also start a new transaction.</span></span><br /><span data-ttu-id="0f77b-115">
<strong>RollbackTrans</strong> — показано, как отменить все изменения и заканчивающейся текущей операции.</span><span class="sxs-lookup"><span data-stu-id="0f77b-115">
<strong>RollbackTrans</strong> — Cancels any changes and ends the current transaction.</span></span> <span data-ttu-id="0f77b-116">Он также может начать новую операцию.</span><span class="sxs-lookup"><span data-stu-id="0f77b-116">It may also start a new transaction.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-117"><a href="cancel-method-ado.md">Отмена</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-117"><a href="cancel-method-ado.md">Cancel</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-118">Отменяет выполнение ожидающих асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="0f77b-118">Cancels execution of a pending, asynchronous method call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-119"><a href="cancelbatch-method-ado.md">CancelBatch</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-120">Показано, как отменить ожидающие пакетного обновления.</span><span class="sxs-lookup"><span data-stu-id="0f77b-120">Cancels a pending batch update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-121"><a href="cancelupdate-method-ado.md">CancelUpdate</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-122">Отменяет все изменения, внесенные в строку текущей или новый объект <strong>набора записей</strong> или коллекции <strong>полей</strong> объекта <strong>записи</strong> , прежде чем вызывать метод <strong>Update</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-122">Cancels any changes made to the current or new row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object, before calling the <strong>Update</strong> method.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-123"><a href="clear-method-ado.md">Очистить</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-123"><a href="clear-method-ado.md">Clear</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-124">Удаляет все объекты <strong>ошибок</strong> из семейства <strong>Errors</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-124">Removes all the <strong>Error</strong> objects from the <strong>Errors</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-125"><a href="clone-method-ado.md">Копия</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-125"><a href="clone-method-ado.md">Clone</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-126">Создает объект повторяющихся <strong>записей</strong> из существующего объекта <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-126">Creates a duplicate <strong>Recordset</strong> object from an existing <strong>Recordset</strong> object.</span></span> <span data-ttu-id="0f77b-127">При необходимости указывает копию только для чтения.</span><span class="sxs-lookup"><span data-stu-id="0f77b-127">Optionally, specifies that the clone be read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-128"><a href="close-method-ado.md">Закрыть</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-128"><a href="close-method-ado.md">Close</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-129">Закрывает открытый объект и любые зависящие объекты.</span><span class="sxs-lookup"><span data-stu-id="0f77b-129">Closes an open object and any dependent objects.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-130"><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-131">Сравнение двух закладки и возвращает сведения об их значения.</span><span class="sxs-lookup"><span data-stu-id="0f77b-131">Compares two bookmarks and returns an indication of their relative values.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-132"><a href="copyrecord-method-ado.md">CopyRecord</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-132"><a href="copyrecord-method-ado.md">CopyRecord</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-133">Копирует файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="0f77b-133">Copies a file or directory, and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-134"><a href="copyto-method-ado.md">CopyTo</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-134"><a href="copyto-method-ado.md">CopyTo</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-135">Копирует указанного числа символов или байтов (в зависимости от <strong>типа</strong>) в <strong>потоке</strong> другой объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-135">Copies the specified number of characters or bytes (depending on <strong>Type</strong>) in the <strong>Stream</strong> to another <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-136"><a href="createparameter-method-ado.md">CreateParameter</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-136"><a href="createparameter-method-ado.md">CreateParameter</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-137">Создает новый объект <strong>параметр</strong> с указанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="0f77b-137">Creates a new <strong>Parameter</strong> object with the specified properties.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-138"><a href="delete-method-ado-parameters-collection.md">Удаление (коллекции параметров ADO)</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-138"><a href="delete-method-ado-parameters-collection.md">Delete (ADO Parameters Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-139">Удаляет объект из коллекции <strong>параметров</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-139">Deletes an object from the <strong>Parameters</strong> collection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-140"><a href="delete-method-ado-fields-collection.md">Удаление (коллекции полей ADO)</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-140"><a href="delete-method-ado-fields-collection.md">Delete (ADO Fields Collection)</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-141">Удаляет объект из коллекции <strong>полей</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-141">Deletes an object from the <strong>Fields</strong> collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-142"><a href="delete-method-ado-recordset.md">Удаление (записей ADO)</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-142"><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-143">Удаление текущей записи или группы записей.</span><span class="sxs-lookup"><span data-stu-id="0f77b-143">Deletes the current record or a group of records.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-144"><a href="deleterecord-method-ado.md">DeleteRecord</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-145">Удаляет файл или каталог и все его подкаталоги.</span><span class="sxs-lookup"><span data-stu-id="0f77b-145">Deletes a file or directory, and all its subdirectories.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Воспользуйтесь командой (ADO)</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-146"><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Execute (ADO Command)</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-147">Выполняет запрос, инструкции SQL или хранимую процедуру, указанных в свойстве <strong>CommandText</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-147">Executes the query, SQL statement, or stored procedure specified in the <strong>CommandText</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Выполнение (ADO-подключение)</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-148"><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Execute (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-149">Выполняет указанному запросу, оператор SQL, хранимую процедуру или текст от поставщика.</span><span class="sxs-lookup"><span data-stu-id="0f77b-149">Executes the specified query, SQL statement, stored procedure, or provider-specific text.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-150"><a href="find-method-ado.md">Найти</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-150"><a href="find-method-ado.md">Find</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-151">Выполняет поиск <strong>записей</strong> для строки, которая должна удовлетворять определенным условиям.</span><span class="sxs-lookup"><span data-stu-id="0f77b-151">Searches a <strong>Recordset</strong> for the row that satisfies the specified criteria.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-152"><a href="flush-method-ado.md">Очистка</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-152"><a href="flush-method-ado.md">Flush</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-153">Принудительно содержимое <strong>потока</strong> , оставшихся в буфер ADO для базового объекта, с которым связано <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-153">Forces the contents of the <strong>Stream</strong> remaining in the ADO buffer to the underlying object with which the <strong>Stream</strong> is associated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-154"><a href="getchildren-method-ado.md">GetChildren</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-154"><a href="getchildren-method-ado.md">GetChildren</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-155">Возвращает <strong>набор записей</strong> , строки представляют файлы и вложенные папки в каталоге, представленный этой <strong>записи</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f77b-155">Returns a <strong>Recordset</strong> whose rows represent the files and subdirectories in the directory represented by this <strong>Record</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-156"><a href="getchunk-method-ado.md">Методы GetChunk</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-156"><a href="getchunk-method-ado.md">GetChunk</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-157">Возвращает все или части, содержимое большого текстового или объекта <strong>поля</strong> двоичных данных.</span><span class="sxs-lookup"><span data-stu-id="0f77b-157">Returns all, or a portion of, the contents of a large text or binary data <strong>Field</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-158"><a href="getrows-method-ado.md">Получение строк</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-158"><a href="getrows-method-ado.md">GetRows</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-159">Извлекает нескольких записей объекта <strong>набора записей</strong> в массив.</span><span class="sxs-lookup"><span data-stu-id="0f77b-159">Retrieves multiple records of a <strong>Recordset</strong> object into an array.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-160"><a href="getstring-method-ado.md">GetString</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-160"><a href="getstring-method-ado.md">GetString</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-161">Возвращает <strong>набор записей</strong> в виде строки.</span><span class="sxs-lookup"><span data-stu-id="0f77b-161">Returns the <strong>Recordset</strong> as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-162"><a href="loadfromfile-method-ado.md">LoadFromFile</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-163">Загружает содержимое существующего файла в <strong>поток</strong>.</span><span class="sxs-lookup"><span data-stu-id="0f77b-163">Loads the contents of an existing file into a <strong>Stream</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-164"><a href="move-method-ado.md">Перемещение</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-164"><a href="move-method-ado.md">Move</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-165">Перемещает положение текущей записи в объекте <strong>набора записей</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-165">Moves the position of the current record in a <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext и MovePrevious</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-166"><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext, and MovePrevious</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-167">Перемещает имя, Фамилия следующий или предыдущий записи в указанном объекте <strong>набора записей</strong> и делает, запишите текущей записи.</span><span class="sxs-lookup"><span data-stu-id="0f77b-167">Moves to the first, last, next, or previous record in a specified <strong>Recordset</strong> object and makes that record the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-168"><a href="moverecord-method-ado.md">MoveRecord</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-168"><a href="moverecord-method-ado.md">MoveRecord</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-169">Перемещает файл или каталог и его содержимое в другое расположение.</span><span class="sxs-lookup"><span data-stu-id="0f77b-169">Moves a file, or a directory and its contents, to another location.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-170"><a href="nextrecordset-method-ado.md">NextRecordset</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-171">Удаляет текущий объект <strong>набора записей</strong> и возвращает следующего <strong>набора записей</strong> путем перемещения через последовательность команд.</span><span class="sxs-lookup"><span data-stu-id="0f77b-171">Clears the current <strong>Recordset</strong> object and returns the next <strong>Recordset</strong> by advancing through a series of commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-172"><a href="open-method-ado-connection.md">Откройте (ADO-подключение)</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-172"><a href="open-method-ado-connection.md">Open (ADO Connection)</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-173">Открывает подключение к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="0f77b-173">Opens a connection to a data source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-174"><a href="open-method-ado-record.md">Откройте (ADO запись)</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-174"><a href="open-method-ado-record.md">Open (ADO Record)</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-175">Открывает существующий объект <strong>записи</strong> или создает новый файл или каталог.</span><span class="sxs-lookup"><span data-stu-id="0f77b-175">Opens an existing <strong>Record</strong> object, or creates a new file or directory.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-176"><a href="open-method-ado-recordset.md">Откройте (записей ADO)</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-176"><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-177">Открывается курсор.</span><span class="sxs-lookup"><span data-stu-id="0f77b-177">Opens a cursor.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-178"><a href="open-method-ado-stream.md">Открыть (поток ADO)</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-178"><a href="open-method-ado-stream.md">Open (ADO Stream)</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-179">Открывает объект <strong>Stream</strong> для работы с потоки данных двоичный или текст.</span><span class="sxs-lookup"><span data-stu-id="0f77b-179">Opens a <strong>Stream</strong> object to manipulate streams of binary or text data.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-180"><a href="openschema-method-ado.md">OpenSchema</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-180"><a href="openschema-method-ado.md">OpenSchema</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-181">Получает сведения о схеме базы данных от поставщика.</span><span class="sxs-lookup"><span data-stu-id="0f77b-181">Obtains database schema information from the provider.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-182"><a href="read-method-ado.md">Read</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-182"><a href="read-method-ado.md">Read</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-183">Считывает указанное число байтов из объекта <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-183">Reads a specified number of bytes from a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-184"><a href="readtext-method-ado.md">ReadText</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-184"><a href="readtext-method-ado.md">ReadText</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-185">Считывает указанное количество символов из объекта <strong>потока</strong> текста.</span><span class="sxs-lookup"><span data-stu-id="0f77b-185">Reads a specified number of characters from a text <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-186"><a href="refresh-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-186"><a href="refresh-method-ado.md">Refresh</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-187">Обновление объектов в коллекции объектов, доступных из и относящиеся к поставщику.</span><span class="sxs-lookup"><span data-stu-id="0f77b-187">Updates the objects in a collection to reflect objects available from, and specific to, the provider.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-188"><a href="requery-method-ado.md">Обновление</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-188"><a href="requery-method-ado.md">Requery</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-189">Обновляет данные в объект <strong>набора записей</strong> , повторное выполнение запросов, на котором основан объект.</span><span class="sxs-lookup"><span data-stu-id="0f77b-189">Updates the data in a <strong>Recordset</strong> object by re-executing the query on which the object is based.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-190"><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-190"><a href="resync-method-ado.md">Resync</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-191">Обновляет данные в текущий объект <strong>набора записей</strong> или коллекции <strong>полей</strong> объекта <strong>записи</strong> из базы данных.</span><span class="sxs-lookup"><span data-stu-id="0f77b-191">Refreshes the data in the current <strong>Recordset</strong> object, or <strong>Fields</strong> collection of a <strong>Record</strong> object, from the underlying database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-192"><a href="save-method-ado.md">Save</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-192"><a href="save-method-ado.md">Save</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-193">Сохранение <strong>набора записей</strong> в файл или объект <strong>Stream</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-193">Saves the <strong>Recordset</strong> in a file or <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-194"><a href="savetofile-method-ado.md">SaveToFile</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-194"><a href="savetofile-method-ado.md">SaveToFile</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-195">Сохраняет двоичные содержимое <strong>потока</strong> в файл.</span><span class="sxs-lookup"><span data-stu-id="0f77b-195">Saves the binary contents of a <strong>Stream</strong> to a file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-196"><a href="seek-method-ado.md">Поиск</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-196"><a href="seek-method-ado.md">Seek</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-197">Выполняет поиск индекса <strong>набора записей</strong> для быстрого поиска строку, в которой совпадает с указанными значениями и изменяет текущее положение строки на эту строку.</span><span class="sxs-lookup"><span data-stu-id="0f77b-197">Searches the index of a <strong>Recordset</strong> to quickly locate the row that matches the specified values, and changes the current row position to that row.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-198"><a href="seteos-method-ado.md">SetEOS</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-198"><a href="seteos-method-ado.md">SetEOS</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-199">Задает позицию за конец потока.</span><span class="sxs-lookup"><span data-stu-id="0f77b-199">Sets the position that is the end of the stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-200"><a href="skipline-method-ado.md">SkipLine</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-200"><a href="skipline-method-ado.md">SkipLine</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-201">Пропускает одну всю строку при чтении текстовый поток.</span><span class="sxs-lookup"><span data-stu-id="0f77b-201">Skips one entire line when reading a text stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-202"><a href="stat-method-ado.md">Статистика</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-202"><a href="stat-method-ado.md">Stat</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-203">Получает статистические сведения об open потока.</span><span class="sxs-lookup"><span data-stu-id="0f77b-203">Gets statistical information about an open stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-204"><a href="supports-method-ado.md">Поддерживает</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-204"><a href="supports-method-ado.md">Supports</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-205">Определяет, поддерживает ли указанный объект <strong>набора записей</strong> определенного типа функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="0f77b-205">Determines whether a specified <strong>Recordset</strong> object supports a particular type of functionality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-206"><a href="update-method-ado.md">обновление</a>.</span><span class="sxs-lookup"><span data-stu-id="0f77b-206"><a href="update-method-ado.md">Update</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-207">Сохраняет все изменения, внесенные в текущей строки <strong>набора записей</strong> объекта или коллекции <strong>полей</strong> объекта <strong>записи</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-207">Saves any changes you make to the current row of a <strong>Recordset</strong> object, or the <strong>Fields</strong> collection of a <strong>Record</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-208"><a href="updatebatch-method-ado.md">UpdateBatch</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-209">Записывает все ожидающие пакета обновления на диск.</span><span class="sxs-lookup"><span data-stu-id="0f77b-209">Writes all pending batch updates to disk.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0f77b-210"><a href="write-method-ado.md">Write</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-210"><a href="write-method-ado.md">Write</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-211">Записывает двоичные данные в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-211">Writes binary data to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0f77b-212"><a href="writetext-method-ado.md">WriteText</a></span><span class="sxs-lookup"><span data-stu-id="0f77b-212"><a href="writetext-method-ado.md">WriteText</a></span></span></p></td>
<td><p><span data-ttu-id="0f77b-213">Записывает строку, указанный текст в объект <strong>потока</strong> .</span><span class="sxs-lookup"><span data-stu-id="0f77b-213">Writes a specified text string to a <strong>Stream</strong> object.</span></span></p></td>
</tr>
</tbody>
</table>

