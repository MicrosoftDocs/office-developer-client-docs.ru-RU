---
title: ActiveX Свойства объектов данных (ADO)
TOCTitle: ADO properties
ms:assetid: 04f08f22-6327-c603-229e-d06a9f1c0d83
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248809(v=office.15)
ms:contentKeyID: 48543020
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a0efb40d1b5e4c5d675d8add7cdb7a05760578a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283235"
---
# <a name="ado-properties"></a>Свойства ADO

**Область применения**: Access 2013, Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Свойство</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>Указывает, на какой странице находится текущая запись.</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>Указывает расположение текущей записи объекта <strong>Recordset.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="activecommand-property-ado.md">ActiveCommand</a></p></td>
<td><p>Указывает объект <strong>Command,</strong> создав связанный <strong>объект Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>Указывает, к каков <strong>объекту Подключение,</strong> которому в настоящее время принадлежит <strong>объект Command,</strong> <strong>Recordset</strong>или <strong>Record.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="actualsize-property-ado.md">ActualSize</a></p></td>
<td><p>Указывает фактическую длину значения поля.</p></td>
</tr>
<tr class="even">
<td><p><a href="attributes-property-ado.md">Attributes</a></p></td>
<td><p>Указывает одну или несколько характеристик объекта.</p></td>
</tr>
<tr class="odd">
<td><p><a href="bof-eof-properties-ado.md">BOF и EOF</a></p></td>
<td><p><strong>BOF</strong> — указывает, что текущая позиция записи находится перед первой записью в <strong>объекте Recordset.</strong> <strong>EOF</strong> — указывает, что текущая позиция записи находится после последней записи в <strong>объекте Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>Указывает закладки, которые однозначно идентифицируют текущую запись в объекте <strong>Recordset</strong> или устанавливают текущую запись в объекте <strong>Recordset</strong> к записи, определенной допустимой закладкой.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>Указывает количество записей из объекта <strong>Recordset,</strong> кэшироваться локально в памяти.</p></td>
</tr>
<tr class="even">
<td><p><a href="chapter-property-ado.md">Глава</a></p></td>
<td><p>Получает или задает объект OLE DB <strong>Chapter</strong> из/на <strong>объект ADORecordsetConstruction.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="charset-property-ado.md">CharSet</a></p></td>
<td><p>Указывает набор символов, в который должно быть переведено содержимое <strong>текстового</strong> потока.</p></td>
</tr>
<tr class="even">
<td><p><a href="commandtext-property-ado.md">CommandText</a></p></td>
<td><p>Указывает текст команды, которая будет выдана поставщику.</p></td>
</tr>
<tr class="odd">
<td><p><a href="commandtimeout-property-ado.md">CommandTimeout</a></p></td>
<td><p>Указывает, как долго ждать при выполнении команды перед прекращением попытки и созданием ошибки.</p></td>
</tr>
<tr class="even">
<td><p><a href="commandtype-property-ado.md">CommandType</a></p></td>
<td><p>Указывает тип объекта <strong>Command.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="connectionstring-property-ado.md">Свойство ConnectionString</a></p></td>
<td><p>Указывает сведения, используемые для установления подключения к источнику данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="connectiontimeout-property-ado.md">ConnectionTimeout</a></p></td>
<td><p>Указывает, как долго ждать при создании подключения перед прекращением попытки и созданием ошибки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="count-property-ado.md">Count</a></p></td>
<td><p>Указывает количество объектов в коллекции.</p></td>
</tr>
<tr class="even">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>Указывает расположение службы курсоров.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>Указывает тип курсора, используемого в <strong>объекте Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="datamember-property-ado.md">DataMember</a></p></td>
<td><p>Указывает имя участника данных, который будет извлечен из объекта, на который ссылается свойство <strong>DataSource.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="datasource-property-ado.md">DataSource</a></p></td>
<td><p>Указывает объект, содержащий данные, которые будут представлены в качестве <strong>объекта Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="defaultdatabase-property-ado.md">DefaultDatabase</a></p></td>
<td><p>Указывает базу данных по умолчанию для объекта <strong>Подключения.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="definedsize-property-ado.md">DefinedSize</a></p></td>
<td><p>Указывает емкость данных объекта <strong>Field.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="description-property-ado.md">Описание</a></p></td>
<td><p>Описывает объект <strong>Error.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="direction-property-ado.md">Направление</a></p></td>
<td><p>Указывает, является ли <strong>параметр</strong> входным параметром, выходным параметром или и тем, и другим, или параметром является возвращаемая величина из сохраненной процедуры.</p></td>
</tr>
<tr class="even">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>Указывает состояние редактирования текущей записи.</p></td>
</tr>
<tr class="odd">
<td><p><a href="eos-property-ado.md">EOS</a></p></td>
<td><p>Указывает, находится ли текущая позиция в конце потока.</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>Указывает фильтр для данных в <strong>Наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="helpcontext-helpfile-properties-ado.md">HelpContext и HelpFile</a></p></td>
<td><p>Указывает файл справки и тему, связанную с <strong>объектом Error.</strong> <strong>HelpContextID</strong> — возвращает контекстный ID в качестве значения <strong>Long</strong> для темы в файле справки. <strong>HelpFile</strong> — возвращает значение <strong>String,</strong> которое оценивается в полностью разрешенный путь к файлу справки.</p></td>
</tr>
<tr class="even">
<td><p><a href="index-property-ado.md">Index</a></p></td>
<td><p>Указывает имя индекса, который в настоящее время действует для <strong>объекта Recordset.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="isolationlevel-property-ado.md">IsolationLevel</a></p></td>
<td><p>Указывает уровень изоляции для объекта <strong>Подключения.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="item-property-ado.md">Элемент</a></p></td>
<td><p>Указывает определенный член коллекции по имени или порядковому номеру.</p></td>
</tr>
<tr class="odd">
<td><p><a href="lineseparator-property-ado.md">LineSeparator</a></p></td>
<td><p>Указывает двоичный символ, который будет использоваться в качестве сепаратора строки в текстовых <strong>объектах Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>Указывает тип блокировок, размещенных на записях во время редактирования.</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>Указывает, какие записи должны быть маршалией обратно на сервер.</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>Указывает максимальное количество записей, которые возвращаются в <strong>набор записей</strong> из запроса.</p></td>
</tr>
<tr class="odd">
<td><p><a href="mode-property-ado.md">Mode</a></p></td>
<td><p>Указывает доступные разрешения на изменение данных в <strong>объекте Подключение,</strong> <strong>Запись</strong>или <strong>Поток.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="name-property-ado.md">Имя</a></p></td>
<td><p>Указывает имя объекта.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nativeerror-property-ado.md">NativeError</a></p></td>
<td><p>Указывает код ошибки для определенного поставщика для данного объекта <strong>Error.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="number-property-ado.md">Number</a></p></td>
<td><p>Указывает номер, который однозначно идентифицирует объект <strong>Error.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="numericscale-property-ado.md">NumericScale</a></p></td>
<td><p>Указывает масштаб числовые значения в <strong>объекте Параметр</strong> или <strong>Поле.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="originalvalue-property-ado.md">OriginalValue</a></p></td>
<td><p>Указывает значение <strong>поля,</strong> которое существовало в записи до внесения каких-либо изменений.</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>Указывает, сколько страниц данных содержит объект <strong>Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>Указывает количество записей, составляющих одну страницу <strong>в Наборе записей.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="parentrow-property-ado.md">ParentRow</a></p></td>
<td><p>Задает контейнер объекта OLE DB <strong>Row</strong> на объект <strong>ADORecordConstruction,</strong> чтобы родитель строки превратился в объект записи <strong>ADO.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="parenturl-property-ado.md">ParentURL</a></p></td>
<td><p>Указывает абсолютную строку URL-адреса, которая указывает на родительную <strong>запись</strong> текущего объекта <strong>Record.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="position-property-ado.md">Position</a></p></td>
<td><p>Указывает текущее положение в <strong>объекте Stream.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="precision-property-ado.md">Точность</a></p></td>
<td><p>Указывает степень точности числимых значений в объекте <strong>Parameter</strong> или числовые объекты <strong>Field.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="prepared-property-ado.md">Подготовлено</a></p></td>
<td><p>Указывает, следует ли сохранять скомпилировали версию команды перед выполнением.</p></td>
</tr>
<tr class="even">
<td><p><a href="provider-property-ado.md">Поставщик</a></p></td>
<td><p>Указывает имя поставщика для объекта <strong>Подключения.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>Указывает количество записей в <strong>объекте Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="recordtype-property-ado.md">RecordType</a></p></td>
<td><p>Указывает тип объекта <strong>Запись.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="row-property-ado.md">Row</a></p></td>
<td><p>Получает или задает объект OLE DB <strong>Row</strong> из/на <strong>объект ADORecordConstruction.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="rowposition-property-ado.md">RowPosition</a></p></td>
<td><p>Получает или задает объект OLE DB <strong>RowPosition</strong> из/на <strong>объект ADORecordsetConstruction.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="rowset-property-ado.md">Rowset</a></p></td>
<td><p>Получает или задает объект OLE DB <strong>Rowset</strong> из/на <strong>объект ADORecordsetConstruction.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="size-property-ado.md">Размер</a></p></td>
<td><p>Указывает максимальный размер в bytes или characters объекта <strong>Parameter.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="https://docs.microsoft.com/office/vba/access/concepts/miscellaneous/size-property-ado-stream">Размер (ADO Stream)</a></p></td>
<td><p>Указывает общий размер потока в количестве bytes.</p></td>
</tr>
<tr class="even">
<td><p><a href="sort-property-ado.md">Sort</a></p></td>
<td><p>Указывает одно или несколько имен полей, на которых <strong>сортироваться Набор</strong> записей, и отсортировали ли каждое поле в порядке по возрастанию или убыванию.</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-error.md">Источник (ошибка ADO)</a></p></td>
<td><p>Указывает имя объекта или приложения, которые изначально создали ошибку.</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-record.md">Source (ADO Record)</a></p></td>
<td><p>Указывает сущность, представленную объектом <strong>Record.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">Source (ADO Recordset)</a></p></td>
<td><p>Указывает источник данных в <strong>объекте Recordset</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="sqlstate-property-ado.md">SQLState</a></p></td>
<td><p>Указывает состояние SQL для данного объекта <strong>Error.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">Состояние</a></p></td>
<td><p>Указывает для всех применимых объектов, открытое или закрытое состояние объекта. Указывает для всех применимых объектов, исполняющих асинхронный метод, независимо от того, является ли текущее состояние объекта подключением, выполнением или искомой</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-field.md">Состояние (поле ADO)</a></p></td>
<td><p>Указывает состояние объекта <strong>Field.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">Status (ADO Recordset)</a></p></td>
<td><p>Указывает состояние текущей записи в отношении пакетных обновлений или других массовых операций.</p></td>
</tr>
<tr class="even">
<td><p><a href="stayinsync-property-ado.md">StayInSync</a></p></td>
<td><p>Указывает, изменяется ли <strong></strong> ссылка на логичные записи детей (то есть главу) <em></em>при изменениях позиции родительской строки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="type-property-ado.md">Тип</a></p></td>
<td><p>Указывает тип или тип данных объекта <strong>Параметр,</strong> <strong>Поле</strong>или <strong>Свойство.</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="type-property-ado-stream.md">Тип (ADO Stream)</a></p></td>
<td><p>Указывает тип данных, содержащихся в <strong>Потоке</strong> (двоичный или текстовый).</p></td>
</tr>
<tr class="odd">
<td><p><a href="underlyingvalue-property-ado.md">UnderlyingValue</a></p></td>
<td><p>Указывает текущее значение объекта <strong>Field</strong> в базе данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="value-property-ado.md">Значение</a></p></td>
<td><p>Указывает значение, назначенное <strong>объекту Field,</strong> <strong>Parameter</strong>или <strong>Property.</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="version-property-ado.md">Версия</a></p></td>
<td><p>Указывает номер версии ADO.</p></td>
</tr>
</tbody>
</table>

<br/>
