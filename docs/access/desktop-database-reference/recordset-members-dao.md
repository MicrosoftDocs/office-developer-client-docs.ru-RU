---
title: Элементы Recordset (DAO)
TOCTitle: Recordset Members
ms:assetid: cfaae9ec-1b88-4285-1ebe-637564e99dc8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834683(v=office.15)
ms:contentKeyID: 48547815
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: c36187eef0b55681b2ba426d979f42ee8a6efea8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716784"
---
# <a name="recordset-members-dao"></a>Элементы Recordset (DAO)


**Область применения**: Access 2013, Office 2013

Объект Recordset представляет записи в базовой таблице или записи, получаемые в результате выполнения запросов.

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
<td><p>Создает новую запись для обновляемого объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Отменяет выполнение ожидающего вызова асинхронного метода (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cancelupdate-method-dao.md">CancelUpdate</a></strong></p></td>
<td><p>Отменяет любые незавершенные обновления для объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-clone-method-dao.md">Clone</a></strong></p></td>
<td><p>Создает дубликат объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong>, который ссылается на оригинальный объект <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-close-method-dao.md">Close</a></strong></p></td>
<td><p>Закрывает открытый объект <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-copyquerydef-method-dao.md">CopyQueryDef</a></strong></p></td>
<td><p>Возвращает объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong>, который является копией <strong>QueryDef</strong> и используется для создания объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong>, представленного заполнителем recordset (только для рабочие области Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-delete-method-dao.md">Delete</a></strong></p></td>
<td><p>Не поддерживается для объекта.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-edit-method-dao.md">Edit</a></strong></p></td>
<td><p>Копирует текущую запись с обновляемым объектом <strong><a href="recordset-object-dao.md">Recordset</a></strong> в буфер обмена для последующего редактирования.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-fillcache-method-dao.md">FillCache</a></strong></p></td>
<td><p>Заполняет полностью или частично локальный кэш для объекта <strong>Recordset</strong>, который содержит данные из источника ODBC, подключенного к ядру СУБД Microsoft Access (только для баз данных ODBC, подключенных к Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findfirst-method-dao.md">FindFirst</a></strong></p></td>
<td><p>Определяет положение первой записи в объекте <strong>Recordset</strong> типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findlast-method-dao.md">FindLast</a></strong></p></td>
<td><p>Определяет положение последней записи в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-findnext-method-dao.md">FindNext</a></strong></p></td>
<td><p>Определяет положение следующей записи в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-findprevious-method-dao.md">FindPrevious</a></strong></p></td>
<td><p>Определяет положение предыдущей записи в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> типа dynaset или мгновенный снимок, которая отвечает заданным условиям и превращает запись в текущую запись (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-getrows-method-dao.md">GetRows</a></strong></p></td>
<td><p>Извлекает несколько строк из объекта <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-move-method-dao.md">Move</a></strong></p></td>
<td><p>Перемещает положение текущей записью в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movefirst-method-dao.md">MoveFirst</a></strong></p></td>
<td><p>Выполняет перемещение к первой записи в указанном объекте <strong>Recordset</strong> и делает запись текущей.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-movelast-method-dao.md">MoveLast</a></strong></p></td>
<td><p>Выполняет перемещение к последней записи в указанном объекте <strong>Recordset</strong> и делает запись текущей.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-movenext-method-dao.md">MoveNext</a></strong></p></td>
<td><p>Выполняет перемещение к последней записи в указанном объекте <strong>Recordset</strong> и делает запись текущей записью.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-moveprevious-method-dao.md">MovePrevious</a></strong></p></td>
<td><p>Выполняет перемещение к предыдущей записи в указанном объекте <strong>Recordset</strong> и делает запись текущей.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-nextrecordset-method-dao.md">NextRecordset</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Получает следующий набор записей, при наличии, возвращаемый состоящим из нескольких частей запросом на выборку в вызове <strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong> и возвращает <strong>логическое</strong> значение, определяющее, находится ли одна или несколько дополнительных записей в состоянии ожидания (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> и добавляет его в коллекцию <strong>Recordsets</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-requery-method-dao.md">Requery</a></strong></p></td>
<td><p>Обновляет данные в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> с помощью повторного выполнения запроса, на котором основан объект.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-seek-method-dao.md">Seek</a></strong></p></td>
<td><p>Определяет положение записи в индексированном объекте<strong>Recordset</strong> табличного типа, которое отвечает заданным условиям для текущего индекса и превращает данную запись в текущую запись (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-update-method-dao.md">Update</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Сохраняет содержимое буфера обмена в обновляемый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
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
<td><p>Задает или возвращает относительный номер записи для текущей записи объекта <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchcollisioncount-property-dao.md">BatchCollisionCount</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает количество записей, для которых не удалось выполнить последний пакет обновления (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-batchcollisions-property-dao.md">BatchCollisions</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает массив закладок, указывающих на строки, которые вызывают конфликты при выполнении последнего пакета обновления (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-batchsize-property-dao.md">BatchSize</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Задает или возвращает количество операторов, отправляемых на сервер в каждом пакете (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bof-property-dao.md">BOF</a></strong></p></td>
<td><p>Возвращает значение, которое показывает, находится ли текущее положение записи курсора перед первой записью объекта <strong>Recordset</strong>. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong></p></td>
<td><p>Задает или возвращает закладку, которая уникально определяет текущую запись в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-bookmarkable-property-dao.md">Bookmarkable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает, поддерживает ли объект <strong>Recordset</strong> закладки, которые можно задать с помощью свойства <strong><a href="recordset-bookmark-property-dao.md">Bookmark</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально. Для чтения и записи, <strong>Long</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-cachestart-property-dao.md">CacheStart</a></strong></p></td>
<td><p>Задает или возвращает значение, которое определяет закладку первой записи в объекте Recordset типа dynaset, содержащих данные, локально кэшируемые из источника данных ODBC (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-connection-property-dao.md">Connection</a></strong></p></td>
<td><p>Возвращает объект <strong><a href="connection-object-dao.md">Connection</a></strong>, который соответствует базе данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Возвращает дату и время создания базовой таблицы (только для рабочих областей Microsoft Access). Только для чтения, <strong>Variant</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-editmode-property-dao.md">EditMode</a></strong></p></td>
<td><p>Возвращает значение, которое указывает состояние редактирования для текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-eof-property-dao.md">EOF</a></strong></p></td>
<td><p>Возвращает значение, которое показывает, находится текущая запись после последней записи объекта <strong>Recordset</strong>. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>Fields</strong>, которая представляет все объекты <strong>Field</strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-filter-property-dao.md">Filter</a></strong></p></td>
<td><p>Задает или возвращает значение, определяющее записи, включаемые в открытом впоследствии объект <strong>Recordset</strong> (только для рабочих областей Microsoft Access). Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-index-property-dao.md">Index</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает имя текущего объекта <strong><a href="index-object-dao.md">Index</a></strong> в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> табличного типа (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lastmodified-property-dao.md">LastModified</a></strong></p></td>
<td><p>Возвращает закладку, определяющую самую последнюю из добавленных или измененных записей.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Возвращает дату и время последнего изменения в базовой таблице. Только для чтения, <strong>Variant</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-lockedits-property-dao.md">LockEdits</a></strong></p></td>
<td><p>Задает или возвращает значение, определяющее тип блокировки, которая действует во время редактирования.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает имя указанного объекта. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-nomatch-property-dao.md">NoMatch</a></strong></p></td>
<td><p>Указывает, была ли найдена конкретная запись с помощью метода <strong><a href="recordset-seek-method-dao.md">Seek</a></strong> или одного из методов <strong><a href="recordset-findfirst-method-dao.md">Find</a></strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-percentposition-property-dao.md">PercentPosition</a></strong></p></td>
<td><p>Задает или возвращает значение, определяющее приблизительное место текущей записи в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong> на основе процента записей в <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-recordcount-property-dao.md">RecordCount</a></strong></p></td>
<td><p>Возвращает число записей, доступных в объекте <strong><a href="recordset-object-dao.md">Recordset</a></strong>, или общее количество записей в <strong>Recordset</strong> табличного типа. или объекте <strong><a href="tabledef-object-dao.md">TableDef</a></strong>. Только для чтения, <strong>Long</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-recordstatus-property-dao.md">RecordStatus</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает значение, определяющее состояние обновления текущей записи, если она входит в пакет обновления (только для рабочих областей ODBCDirect). Только для чтения, <strong><a href="recordstatusenum-enumeration-dao.md">RecordStatusEnum</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-restartable-property-dao.md">Restartable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает на то, поддерживает ли объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> метод <strong><a href="recordset-requery-method-dao.md">Requery</a></strong>, который повторно выполняет запрос, на котором основан объект <strong>Recordset</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-sort-property-dao.md">Sort</a></strong></p></td>
<td><p>Задает или возвращает порядок сортировки для записей в объекте <strong> <a href="recordset-object-dao.md">Recordset</a> </strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Указывает на то, завершена или нет асинхронной операции (т. е метода, вызываемого с параметром <strong>dbRunAsync</strong>) (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Возвращает значение, которое указывает на то, поддерживает ли объект транзакций. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Type</strong></p></td>
<td><p>Описание для этого элемента появится в итоговом выпуске Office 14.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает на то, можно ли изменить DAO объект. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-updateoptions-property-dao.md">UpdateOptions</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Задает или возвращает значение, которое указывает на то, как предложение WHERE создается для каждой записи во время обновления пакета, а также будет ли пакет обновления использовать оператор UPDATE или DELETE, за которым следует INSERT (только для рабочих областей ODBCDirect). Чтение и запись, <strong><a href="updatecriteriaenum-enumeration-dao.md">UpdateCriteriaEnum</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="recordset-validationrule-property-dao.md">ValidationRule</a></strong></p></td>
<td><p>Задает или возвращает значение, которое проверяет данные в поле после его добавление или изменения в таблице (только для рабочих областей Microsoft Access). Чтение и запись, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="recordset-validationtext-property-dao.md">ValidationText</a></strong></p></td>
<td><p>Задает или возвращает значение, определяющее текст сообщения, которое отображает ваше приложение, если значение объекта <strong>Field</strong> не удовлетворяют правилу проверки, задаваемому настройкой параметра <strong>ValidationRule</strong> (только для рабочих областей Microsoft Access). Только для чтения, <strong>String</strong>.</p></td>
</tr>
</tbody>
</table>

