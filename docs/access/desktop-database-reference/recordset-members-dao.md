---
title: Recordset Members (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d0bf59a8be000d01dc6f514112265b640384e549
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869381"
---
# <a name="recordset-members-dao"></a>Recordset Members (DAO)


**Применимо к**: Access 2013, Office 2013

Объект набора записей представляет записей в базовой таблице или записей, в результате выполнения запроса.

## <a name="methods"></a>Методы

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset-addnew-method-dao.md">AddNew</a></strong></p></td>
<td><p>Создает новую запись для обновляемых объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cancel-method-dao.md">Отмена</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Отменяет выполнение ожидающие асинхронного вызова метода (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></p></td>
<td><p>Отменяет все ожидающие обновления для объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-clone-method-dao.md">Копия</a></strong></p></td>
<td><p>Создает объект повторяющихся <strong><a href="recordset-object-dao.md">записей</a></strong> , на который ссылается на исходный объект <strong>набора записей</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-close-method-dao.md">Закрыть</a></strong></p></td>
<td><p>Закрытие открытых <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></p></td>
<td><p>Возвращает объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong> , являющееся копией <strong>QueryDef</strong> , используемый для создания объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> , представленного заполнитель набора записей (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></p></td>
<td><p>Не поддерживается для этого объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-edit-method-dao.md">Изменение</a></strong></p></td>
<td><p>Копирует текущей записи из обновляемый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> в буфер копирования для последующего редактирования.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></p></td>
<td><p>Заполняет все или часть из локального кэша для объекта <strong>набора записей</strong> , который содержит данные из Microsoft Access базы данных подключен модуль ODBC источника данных (Microsoft Access базы данных подключен модуль ODBC только баз данных).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></p></td>
<td><p>Поиск первой записи в объект <strong>набора записей</strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></p></td>
<td><p>Указывает расположение последние записи в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></p></td>
<td><p>Находит следующую запись в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></p></td>
<td><p>Указывает расположение предыдущей записи в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> добавляющий или моментальных снимков, которая должна удовлетворять определенным условиям и делает, запишите текущей записи (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-getrows-method-dao.md">Получение строк</a></strong></p></td>
<td><p>Получает несколько строк из объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-move-method-dao.md">Перемещение</a></strong></p></td>
<td><p>Перемещает положение текущей записи в объекте <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></p></td>
<td><p>Переход к первой записи в указанном объекте <strong>набора записей</strong> и убедитесь, что запись текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></p></td>
<td><p>Переход к последней записи в указанный объект <strong>набора записей</strong> и сделать эту запись текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></p></td>
<td><p>Переход к следующей записи в указанном объекте <strong>набора записей</strong> и убедитесь, что запись текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></p></td>
<td><p>Переход к предыдущей записи в указанный <strong>набор записей</strong> объекта и убедитесь, что запись текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Получает следующего набора записей, если какие-либо, возвращаемых запросом составного select в вызове <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> и возвращает значение <strong>типа Boolean</strong> , указывающее, является ли один или несколько дополнительных записей ожидающие (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> и добавляет его в коллекцию <strong>наборов записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-requery-method-dao.md">Обновление</a></strong></p></td>
<td><p>Обновляет данные в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> , повторное выполнение запросов, на котором основан объект.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-seek-method-dao.md">Поиск</a></strong></p></td>
<td><p>Указывает расположение записи в объекте <strong>набора записей</strong> индексированных тип таблицы, которая должна удовлетворять определенным условиям для текущего индекса и делает, запишите текущей записи (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-update-method-dao.md">Update</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Сохранение содержимого буфера копирования обновляемый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a>Свойства

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong><a href="recordset-absoluteposition-property-dao.md">AbsolutePosition</a></strong></p></td>
<td><p>Задает или возвращает относительный номер записи текущего объекта <strong>набора записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Возвращает число записей, которые не удалось завершить последнего обновления пакета (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Возвращает массив строк, которые созданы конфликтов в последнюю операцию обновления пакета (только для рабочих областей технология ODBCDirect), указывающее, закладок.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchsize-property-dao.md">Размер пакета</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Задает или возвращает число операторов, отправляемых на сервер в каждом пакете (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></p></td>
<td><p>Возвращает значение, указывающее, является ли положение текущей записи перед первой записи в объекте <strong>набора записей</strong> . Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-bookmark-property-dao.md">Закладка</a></strong></p></td>
<td><p>Задает или возвращает закладки, который уникальным образом определяет текущую запись в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></p></td>
<td><p>Возвращает значение, указывающее, поддерживает ли объект <strong>набора записей</strong> закладки, которые можно задать с помощью свойства <strong><a href="recordset-bookmark-property-dao.md">Закладка</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Задает или возвращает число записей, полученных из источника данных ODBC, которые будут кэшированы локально. Чтение и запись <strong>времени</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее закладки для первой записи в объекте типа динамического набора записей, содержащий данные для локально кэшировать из источника данных ODBC (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-connection-property-dao.md">Подключение</a></strong></p></td>
<td><p>Возвращает объект <strong><a href="connection-object-dao.md">подключения</a></strong> , который соответствует в базу данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Возвращает дату и время создания базовой таблицы (только для рабочих областей Microsoft Access). Только для чтения <strong>Variant</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></p></td>
<td><p>Возвращает значение, указывающее состояние редактирования для текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-eof-property-dao.md">ФУНКЦИЯ EOF</a></strong></p></td>
<td><p>Возвращает значение, указывающее, является ли положение текущей записи после последней записи в объекте <strong>набора записей</strong> . Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-fields-property-dao.md">Поля</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>полей</strong> , представляющую все хранятся объекты <strong>поля</strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></p></td>
<td><p>Задает или возвращает значение, определяющее записей, включенных в последующем открытого объекта <strong>набора записей</strong> (только для рабочих областей Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-index-property-dao.md">Индекс</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее имя текущего объекта <strong><a href="index-object-dao.md">индекса</a></strong> в таблице тип объекта <strong><a href="recordset-object-dao.md">набора записей</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></p></td>
<td><p>Возвращает ookmark, указывающее наиболее недавно добавлены или изменены записи.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Возвращает дату и время последнего изменения, внесенные базовая таблица. Только для чтения <strong>Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее тип блокировки, который фактически во время редактирования.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает имя указанного объекта. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></p></td>
<td><p>Указывает, будет ли определенный запись найдена с помощью метода <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> или один из методов <strong><a href="recordset-findfirst-method-dao.md">поиска</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, приблизительно, например расположение текущей записи в объекте <strong><a href="recordset-object-dao.md">набора записей</a></strong> на основе процента записей в <strong>набора записей</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Возвращает число записей в объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> или общее число записей в таблице тип объекта <strong>набора записей</strong> . или <strong><a href="tabledef-object-dao.md">TableDef</a></strong> объект. Только для чтения <strong>времени</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Возвращает значение, указывающее состояние обновления текущую запись, если он является частью пакета обновления (только для рабочих областей технология ODBCDirect). Только для чтения <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-restartable-property-dao.md">Перезапускаемое</a></strong></p></td>
<td><p>Возвращает значение, указывающее, поддерживает ли объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> метод <strong><a href="recordset-requery-method-dao.md">повторный запрос</a></strong> , который повторно выполняет запрос, на котором основано объекта <strong>набора записей</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-sort-property-dao.md">Сортировка</a></strong></p></td>
<td><p>Задает или возвращает порядок сортировки для записей в объекте <strong><a href="recordset-object-dao.md">набора записей</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Указывает, следует ли асинхронной операции (то есть, вызывается метод с параметром <strong>dbRunAsync</strong> ) завершено выполнение (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Возвращает значение, указывающее, поддерживает ли объект транзакции. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Тип</strong></p></td>
<td><p>Описание для данного члена будет отображаться в окончательной версии Office 14.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-updatable-property-dao.md">Обновляемые</a></strong></p></td>
<td><p>Возвращает значение, указывающее, является ли объект DAO можно изменить. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Задает или возвращает значение, указывающее, как предложение WHERE создается для каждой записи во время обновления пакета и ли пакетного обновления следует использовать инструкции UPDATE или DELETE последующей вставкой (только для рабочих областей технология ODBCDirect). Чтение и запись <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-validationrule-property-dao.md">Значение</a></strong></p></td>
<td><p>Задает или возвращает значение, которое проверяет данные в поля, как она изменен или добавлен в таблицу (только для рабочих областей Microsoft Access). Чтение и запись <strong>строки</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-validationtext-property-dao.md">Сообщение об ошибке</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, текст сообщения, приложение, если значение <strong>поля</strong> объекта не удовлетворяют правило проверки, указанного идентификатором <strong>условие на значение</strong> свойства поля (только для рабочих областей Microsoft Access) . Только для чтения, <strong>String</strong>.</p></td>
</tr>
</tbody>
</table>

