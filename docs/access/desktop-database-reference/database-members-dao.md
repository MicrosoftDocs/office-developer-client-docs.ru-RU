---
title: Элементы объекта Database (DAO)
TOCTitle: Database Members
ms:assetid: 68b0c069-8ed9-64dc-ea68-0d323e24c79c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195257(v=office.15)
ms:contentKeyID: 48545392
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d2254aeff94aeb2b8b078fc4f4cd4d3ef807e597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294927"
---
# <a name="database-members-dao"></a>Элементы объекта Database (DAO)


**Область применения**: Access 2013, Office 2013

Объект Database представляет открытую базу данных.

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
<td><p><strong><a href="database-close-method-dao.md">Close</a></strong></p></td>
<td><p>Закрывает открытую базу <strong>данных.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создает объект Property, определенный <strong><a href="property-object-dao.md">пользователем</a></strong> (только для рабочих пространств Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="relation-object-dao.md">Relation</a></strong> (только для рабочих пространств Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="tabledef-object-dao.md">TableDef</a></strong> (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Выполняет запрос на изменение или запускает инструкцию SQL для указанного объекта.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></p></td>
<td><p>Создает новую реплику из другой реплики базы данных (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-newpassword-method-dao.md">NewPassword</a></strong></p></td>
<td><p>Изменяет пароль существующей базы данных ястановки базы данных Microsoft Access (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> и добавляет его в коллекцию <strong>Recordsets</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></p></td>
<td><p>Синхронизирует все изменения в частичной реплике с полной репликой, очищает все записи в частичной реплике, а затем повторно наполнение частичной реплики на основе текущих фильтров реплики. (Только для баз данных ям баз данных Microsoft Access.)</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-synchronize-method-dao.md">Synchronize</a></strong></p></td>
<td><p>Синхронизирует две реплики. (Только для рабочих областей Microsoft Access.)</p></td>
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
<td><p><strong><a href="database-collatingorder-property-dao.md">CollatingOrder</a></strong></p></td>
<td><p>Возвращает значение, которое указывает последовательность порядка сортировки в тексте для сравнения строк или сортировки (только для рабочей области Microsoft Access). Только для чтения, <strong>Long</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Задает или возвращает значение, которое предоставляет сведения об источнике открытой базы данных. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-connection-property-dao.md">Connection</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Возвращает объект <strong><a href="connection-object-dao.md">Connection,</a></strong> соответствующий базе данных (только для рабочей области ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-containers-property-dao.md">Containers</a></strong></p></td>
<td><p>Возвращает <strong>коллекцию контейнеров,</strong> представляюную все объекты <strong>контейнера</strong> в засознаной базе данных. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></p></td>
<td><p>Задает или возвращает 16-byte-значение, которое уникальным образом идентифицирует master дизайна в наборе реплик (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает имя указанного объекта. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>Возвращает <strong>коллекцию QueryDefs,</strong> которая содержит все объекты <strong>QueryDef</strong> указанной базы данных. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает количество секунд ожидания до возникновения ошибки времени ожидания при выполнении запроса в источнике данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Возвращает количество записей, затронутых последним вызовом метода <strong><a href="connection-execute-method-dao.md">Execute.</a></strong></p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></p></td>
<td><p>Возвращает <strong>коллекцию Recordsets,</strong> которая содержит все открытые наборы записей в указанной базе данных. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-relations-property-dao.md">Relations</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>Relations,</strong> которая содержит все сохраненные объекты <strong>Relation</strong> для указанной базы данных. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-replicaid-property-dao.md">ReplicaID</a></strong></p></td>
<td><p>Возвращает 16-byte значение, уникальным образом идентифицирует реплику базы данных (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></p></td>
<td><p>Возвращает <strong>коллекцию TableDefs,</strong> которая содержит все объекты <strong>TableDef,</strong> хранимые в указанной базе данных. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Возвращает значение, которое указывает на то, поддерживает ли объект транзакций. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает на то, можно ли изменить DAO объект. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-version-property-dao.md">Версия</a></strong></p></td>
<td><p>В рабочей области Microsoft Access возвращается замещение ямы баз данных Microsoft Jet или Microsoft Access, которые создали базу данных. Только для чтения, <strong>String</strong>.</p></td>
</tr>
</tbody>
</table>

