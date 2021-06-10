---
title: ActiveX Методы объектов данных (ADO)
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
<td><p><a href="append-method-ado.md">Приложение</a></p></td>
<td><p>Придает объект коллекции. Если коллекция <strong>полей,</strong>новый <strong>объект Field</strong> может быть создан, прежде чем он будет придан в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>Придает данные большому текстовом или двоичному <strong>поле</strong>данных или <strong>объекту Parameter.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans, CommitTrans и RollbackTrans</a></p></td>
<td><p>Управление обработкой транзакций в <strong>объекте Подключения</strong> следующим образом:<br/><br/><strong>BeginTrans</strong> — начинается новая транзакция.<br/><br/>
<strong>CommitTrans</strong> — сохраняет все изменения и завершает текущую транзакцию. Кроме того, может начаться новая транзакция.<br/><br/>
<strong>RollbackTrans</strong> — отменяет изменения и завершает текущую транзакцию. Кроме того, может начаться новая транзакция.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Отмена</a></p></td>
<td><p>Отменяет выполнение ожидаемого асинхронного вызова метода.</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Отмена ожидающих пакетных обновлений.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Отменяет изменения, внесенные в текущую или новую строку объекта <strong>Recordset</strong> или коллекцию <strong>Полей</strong> объекта <strong>Record,</strong> перед вызовом метода <strong>Update.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Clear</a></p></td>
<td><p>Удаляет все <strong>объекты Error</strong> из коллекции <strong>Errors.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Создает дубликат <strong>объекта Recordset</strong> из существующего объекта <strong>Recordset.</strong> Необязательно указывает, что клон должен быть только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Закрывает открытый объект и все зависимые объекты.</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>Сравнивает две закладки и возвращает указание их относительных значений.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Копирует файл или каталог и его содержимое в другое расположение.</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Копирует указанное количество символов или bytes (в зависимости от <strong>типа)</strong>в <strong>потоке</strong> на другой <strong>объект Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>Создает новый объект <strong>Parameter</strong> с указанными свойствами.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Удаление (коллекция параметров ADO)</a></p></td>
<td><p>Удаляет объект из коллекции <strong>Параметры.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Удаление (коллекция полей ADO)</a></p></td>
<td><p>Удаляет объект из коллекции <strong>Fields.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete (ADO Recordset)</a></p></td>
<td><p>Удаляет текущую запись или группу записей.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Удаляет файл или каталог и все его подтеки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-command">Выполнение (команда ADO)</a></p></td>
<td><p>Выполняет запрос, SQL или сохраненную процедуру, указанную в <strong>свойстве CommandText.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/execute-method-ado-connection">Выполнение (подключение ADO)</a></p></td>
<td><p>Выполняет указанный запрос, SQL, сохраненную процедуру или текст, определенный поставщику.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Find</a></p></td>
<td><p>Поиск <strong>наборов записей</strong> для строки, удовлетворяемой указанным критериям.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Флеш</a></p></td>
<td><p>Привнося содержимое <strong>потока,</strong> оставшегося в буфере ADO, к основному объекту, с которым связан <strong>поток.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Возвращает набор <strong>recordset,</strong> строки которого представляют файлы и подтеки в каталоге, представленном этой <strong>записью.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">GetChunk</a></p></td>
<td><p>Возвращает все или часть содержимого большого объекта поля текстовых или двоичных <strong>данных.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Извлекает несколько записей объекта <strong>Recordset</strong> в массив.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p>Возвращает набор <strong>записей в</strong> качестве строки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Загружает содержимое существующего файла в <strong>поток.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Перемещает положение текущей записи в объекте <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext и MovePrevious</a></p></td>
<td><p>Перемещается к первой, последней, следующей или предыдущей записи в указанном объекте <strong>Recordset</strong> и записи текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Перемещает файл или каталог и его содержимое в другое расположение.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Очищает текущий объект <strong>Recordset</strong> и возвращает следующий <strong>набор записей,</strong> продвигаясь по ряду команд.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Open (ADO Connection)</a></p></td>
<td><p>Открывает подключение к источнику данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Open (ADO Record)</a></p></td>
<td><p>Открывает <strong>существующий объект Record</strong> или создает новый файл или каталог.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Open (ADO Recordset)</a></p></td>
<td><p>Открывает курсор.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Open (ADO Stream)</a></p></td>
<td><p>Открывает объект <strong>Stream</strong> для управления потоками двоичных или текстовых данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>Получает сведения о схеме баз данных от поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Считывает определенное количество bytes с объекта <strong>Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Читает определенное количество символов из объекта text <strong>Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="refresh-method-ado.md">Refresh</a></p></td>
<td><p>Обновляет объекты в коллекции, чтобы отражать объекты, доступные поставщику, и определенные для него.</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Обновляет данные в объекте <strong>Recordset</strong> с помощью повторного выполнения запроса, на котором основан объект.</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Обновляет данные в текущем объекте <strong>Recordset</strong> или <strong>полей</strong> объекта <strong>Record</strong> из баз данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p>Сохраняет набор <strong>записей в</strong> файле или <strong>объекте Stream.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Сохраняет двоичное содержимое <strong>потока в</strong> файл.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Seek</a></p></td>
<td><p>Выполняется поиск индекса <strong>наборов записей,</strong> чтобы быстро найти строку, которая соответствует указанным значениям, и изменить текущее положение строки в этой строке.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Задает позицию, которая является конечным потоком.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Пропускает всю строку при чтении текстового потока.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Stat</a></p></td>
<td><p>Получает статистическую информацию об открытом потоке.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Поддерживает</a></p></td>
<td><p>Определяет, поддерживает ли указанный <strong>объект Recordset</strong> определенный тип функций.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Обновление</a></p></td>
<td><p>Сохраняет все изменения, внесенные в текущую строку объекта <strong>Recordset</strong> или коллекцию <strong>Полей</strong> объекта <strong>Record.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Записывает все ожидающих пакетных обновлений на диск.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Записывает двоичные данные на <strong>объект Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Записывает указанную текстовую строку на <strong>объект Stream.</strong></p></td>
</tr>
</tbody>
</table>

<br/>
