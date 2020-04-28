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
# <a name="ado-methods"></a>Методы ADO

**Область применения**: Access 2013, Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Метод</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Создает новую запись для обновляемого объекта <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Error</a></p></td>
<td><p>Добавляет объект в коллекцию. Если коллекция является <strong>полями</strong>, новый объект <strong>field</strong> можно создать перед добавлением в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>Добавляет данные в <strong>поле</strong>большого текста или двоичных данных или в объект <strong>Parameter</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans и RollbackTrans</a></p></td>
<td><p>Управляет обработкой транзакций в объекте <strong>Connection</strong> , как показано ниже.<br/><br/><strong>BeginTrans</strong> — начинает новую транзакцию.<br/><br/>
<strong>CommitTrans</strong> — сохраняет все изменения и завершает текущую транзакцию. Кроме того, может начаться новая транзакция.<br/><br/>
<strong>RollbackTrans</strong> — отменяет все изменения и завершает текущую транзакцию. Кроме того, может начаться новая транзакция.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Отмена</a></p></td>
<td><p>Отменяет выполнение ожидающего асинхронного вызова метода.</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Отменяет ожидающее пакетное обновление.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Отменяет любые изменения, внесенные в текущую или новую строку объекта <strong>Recordset</strong> , или коллекцию <strong>Fields</strong> объекта <strong>Record</strong> перед вызовом метода <strong>Update</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Clear</a></p></td>
<td><p>Удаляет все объекты <strong>Error</strong> из коллекции <strong>Errors</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Создает дубликат объекта <strong>Recordset</strong> из существующего объекта <strong>Recordset</strong> . При необходимости этот параметр указывает, что клон должен быть доступен только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Закрывает открытый объект и все зависимые объекты.</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>Сравнивает две закладки и возвращает сведения об их относительных значениях.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Копирует файл или каталог, а также его содержимое в другое расположение.</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Копирует указанное число символов или байтов (в зависимости от <strong>типа</strong>) в <strong>потоке</strong> в другой объект <strong>Stream</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>Создает новый объект <strong>Parameter</strong> с указанными свойствами.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Delete (Коллекция параметров ADO)</a></p></td>
<td><p>Удаляет объект из коллекции <strong>Parameters</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Delete (коллекция Fields в ADO)</a></p></td>
<td><p>Удаляет объект из коллекции <strong>Fields</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete (объект Recordset в ADO)</a></p></td>
<td><p>Удаляет текущую запись или группу записей.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Удаляет файл или каталог и все его подкаталоги.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Выполнение (команда ADO)</a></p></td>
<td><p>Выполняет запрос, инструкцию SQL или хранимую процедуру, указанную в свойстве <strong>CommandText</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Выполнение (подключение ADO)</a></p></td>
<td><p>Выполняет указанный запрос, инструкцию SQL, хранимую процедуру или текст, зависящий от поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Поиск</a></p></td>
<td><p>Выполняет поиск в <strong>наборе записей</strong> для строки, удовлетворяющей заданным условиям.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Удален</a></p></td>
<td><p>Принудительно применяет содержимое <strong>потока</strong> , оставшееся в БУФЕРе ADO, к базовому объекту, с которым связан <strong>поток</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Возвращает объект <strong>Recordset</strong> , строки которого представляют файлы и подкаталоги в каталоге, представленном этой <strong>записью</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>Возвращает значение ALL или часть содержимого большого текстового или двоичного <strong>объекта данных</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Получает несколько записей объекта <strong>Recordset</strong> в массив.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p>Возвращает объект <strong>Recordset</strong> в виде строки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Загружает содержимое существующего файла в <strong>поток</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Перемещает положение текущей записи в объекте <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext и MovePrevious</a></p></td>
<td><p>Перемещение к первой, последней, следующей или предыдущей записи в указанном объекте <strong>Recordset</strong> и делает эту запись текущей.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Перемещает файл или каталог вместе с его содержимым в другое расположение.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Очищает текущий объект <strong>Recordset</strong> и возвращает следующий <strong>набор записей</strong> путем перемещения по ряду команд.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Open (подключение ADO)</a></p></td>
<td><p>Открывает подключение к источнику данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Открыть (запись ADO)</a></p></td>
<td><p>Открывает существующий объект <strong>Record</strong> или создает новый файл или каталог.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Открыть (набор записей ADO)</a></p></td>
<td><p>Открывает курсор.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Открыть (поток ADO)</a></p></td>
<td><p>Открывает объект <strong>Stream</strong> для управления потоками двоичных или текстовых данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>Получает сведения о схеме базы данных от поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Чтение</a></p></td>
<td><p>Считывает заданное число байтов из объекта <strong>Stream</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Считывает заданное число символов из текстового объекта <strong>потока</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="refresh-method-ado.md">Refresh</a></p></td>
<td><p>Обновляет объекты в коллекции, чтобы отразить объекты, доступные поставщику и соответствующие объекты.</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Обновляет данные в объекте <strong>Recordset</strong> с помощью повторного выполнения запроса, на котором основан объект.</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Обновляет данные в текущем объекте <strong>Recordset</strong> или коллекции <strong>полей</strong> объекта <strong>Record</strong> из основной базы данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p>Сохраняет <strong>набор записей</strong> в объекте File или <strong>Stream</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Сохраняет двоичное содержимое <strong>потока</strong> в файл.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p>Выполняет поиск в индексе объекта <strong>Recordset</strong> , чтобы быстро найти строку, которая соответствует указанным значениям, и изменяет положение текущей строки на эту строку.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Задает позицию, которая является концом потока.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Пропускает одну строку целиком при чтении текстового потока.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Stat</a></p></td>
<td><p>Возвращает статистические сведения о открытом потоке.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Имеется</a></p></td>
<td><p>Определяет, поддерживает ли указанный объект <strong>Recordset</strong> определенный тип функциональных возможностей.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">обновление</a>.</p></td>
<td><p>Сохраняет все изменения, внесенные в текущую строку объекта <strong>Recordset</strong> , или коллекцию <strong>Fields</strong> объекта <strong>Record</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Записывает все ожидающие пакетные обновления на диск.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Записывает двоичные данные в объект <strong>Stream</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">Инструкция</a></p></td>
<td><p>Записывает указанную текстовую строку в объект <strong>Stream</strong> .</p></td>
</tr>
</tbody>
</table>

<br/>
