---
title: Connection members (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 098f44d87390351c23e61000ecbe47eae35810ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295907"
---
# <a name="connection-members-dao"></a>Connection members (DAO)

**Область применения**: Access 2013, Office 2013

> [!NOTE]
> Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access. Объект Connection представляет подключение к базе данных ODBC (только для рабочей области ODBCDirect).
 
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
<td><p><strong><a href="connection-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p>Отменяет выполнение ожидающего вызова асинхронного метода (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-close-method-dao.md">Close</a></strong></p></td>
<td><p>Закрывает <strong>открытое</strong>подключение.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Выполняет запрос на изменение или запускает инструкцию SQL для указанного объекта.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="recordset-object-dao.md">Recordset</a></strong> и добавляет его в коллекцию <strong>Recordsets</strong>.</p></td>
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
<td><p><strong><a href="connection-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Задает или возвращает значение, которое предоставляет сведения об источнике открытого подключения. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-database-property-dao.md">Database</a></strong></p></td>
<td><p>Возвращает объект <strong><a href="database-object-dao.md">Database,</a></strong> соответствующий этому подключению (только для рабочей области ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-name-property-dao.md">Name</a></strong></p></td>
<td><p>Rreturns the name of a <strong><a href="connection-object-dao.md">Connection</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>Возвращает <strong>коллекцию QueryDefs,</strong> которая содержит все объекты <strong>QueryDef</strong> указанного подключения. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает количество секунд ожидания до возникновения ошибки времени ожидания при выполнении запроса в источнике данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Возвращает количество записей, затронутых последним вызовом метода <strong><a href="connection-execute-method-dao.md">Execute.</a></strong></p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-recordsets-property-dao.md">Recordsets</a></strong></p></td>
<td><p>Возвращает <strong>коллекцию Recordsets,</strong> которая содержит все открытые наборы записей для указанного подключения. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p>Указывает на то, завершена или нет асинхронной операции (т. е метода, вызываемого с параметром <strong>dbRunAsync</strong>) (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Возвращает значение, которое указывает на то, поддерживает ли объект транзакций. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает на то, можно ли изменить DAO объект. Boolean только <strong>для чтения.</strong> Только для чтения.</p></td>
</tr>
</tbody>
</table>

