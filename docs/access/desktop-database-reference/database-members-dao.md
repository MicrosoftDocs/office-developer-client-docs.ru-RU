---
title: Элементы базы данных (DAO)
TOCTitle: Database Members
ms:assetid: 68b0c069-8ed9-64dc-ea68-0d323e24c79c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195257(v=office.15)
ms:contentKeyID: 48545392
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d2254aeff94aeb2b8b078fc4f4cd4d3ef807e597
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713053"
---
# <a name="database-members-dao"></a>Элементы базы данных (DAO)


**Применимо к**: Access 2013, Office 2013

Объект базы данных представляет базу данных.

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
<td><p><strong><a href="database-close-method-dao.md">Закрыть</a></strong></p></td>
<td><p>Закрывает открыть <strong>базу данных</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создание пользовательских <strong><a href="property-object-dao.md">свойств</a></strong> объекта (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-createrelation-method-dao.md">CreateRelation</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="relation-object-dao.md">связи</a></strong> (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-createtabledef-method-dao.md">CreateTableDef</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="tabledef-object-dao.md">TableDef</a></strong> (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Запуск запроса или выполняет инструкции SQL на указанный объект.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-makereplica-method-dao.md">MakeReplica</a></strong></p></td>
<td><p>Делает новой реплики из другой реплики базы данных (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-newpassword-method-dao.md">Новый_пароль</a></strong></p></td>
<td><p>Изменение пароля существующей базы данных ядра базы данных Microsoft Access (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> и добавляет его в коллекцию <strong>наборов записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-populatepartial-method-dao.md">PopulatePartial</a></strong></p></td>
<td><p>Синхронизирует все изменения в частичные реплики с полной реплики, очищает все записи в частичные реплики и затем повторно заполняется реплику на основе текущего фильтров реплики. (База данных ядра базы данных Microsoft Access только.).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-synchronize-method-dao.md">Синхронизация</a></strong></p></td>
<td><p>Синхронизирует две реплики. (Microsoft Access рабочие области только).</p></td>
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
<td><p>Возвращает значение, указывающее последовательность порядок сортировки в текст для сравнения строк или сортировка (только для рабочих областей Microsoft Access). Только для чтения <strong>времени</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Задает или возвращает значение, которое содержит сведения об источнике открыть базу данных. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-connection-property-dao.md">Connection</a></strong></p></td>
<td><p><strong>Примечание</strong>: технология ODBCDirect рабочие области, не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</p>
<p>Возвращает объект <strong><a href="connection-object-dao.md">подключения</a></strong> , соответствующий базе данных (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-containers-property-dao.md">Containers</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>контейнеров</strong> , представляющий все объекты <strong>контейнера</strong> в указанной базе данных. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-designmasterid-property-dao.md">DesignMasterID</a></strong></p></td>
<td><p>Задает или возвращает 16-битное значение, уникальным образом идентифицирующее репликой в наборе реплик (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает имя указанного объекта. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>QueryDefs</strong> , который содержит все объекты <strong>QueryDef</strong> с указанной базы данных. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-querytimeout-property-dao.md">QueryTimeout</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее количество секунд ожидания до возникновения ошибки времени ожидания при выполнении запроса на источник данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Возвращает число записей, влияет на недавно вызванного метода <strong><a href="connection-execute-method-dao.md">Execute</a></strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-recordsets-property-dao.md">Recordsets</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>наборов записей</strong> , который содержит все открытые наборы записей в указанной базы данных. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-relations-property-dao.md">Relations</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>отношений</strong> , который содержит все хранимые объекты <strong>отношения</strong> для указанной базы данных. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-replicaid-property-dao.md">ReplicaID</a></strong></p></td>
<td><p>Возвращает 16-битное значение, уникальным образом идентифицирующее реплики базы данных (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-tabledefs-property-dao.md">TableDefs</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>TableDefs</strong> , который содержит все объекты <strong>TableDef</strong> , хранящиеся в указанной базе данных. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Возвращает значение, указывающее, поддерживает ли объект транзакции. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="database-updatable-property-dao.md">Обновляемые</a></strong></p></td>
<td><p>Возвращает значение, указывающее, является ли объект DAO можно изменить. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="database-version-property-dao.md">Версия</a></strong></p></td>
<td><p>В рабочей области Microsoft Access возвращает vesion ядро базы данных Microsoft Access или Microsoft Jet созданной базе данных. Только для чтения, <strong>String</strong>.</p></td>
</tr>
</tbody>
</table>

