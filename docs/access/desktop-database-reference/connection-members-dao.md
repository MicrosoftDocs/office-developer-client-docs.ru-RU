---
title: Connection Members (DAO)
TOCTitle: Connection Members
ms:assetid: 94fc60ee-b6f2-cf08-b008-ed51bf7e7f8c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197681(v=office.15)
ms:contentKeyID: 48546422
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 9d2c2af4dcf1cf8661d7cac170e8aa5b679ab083
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25886923"
---
# <a name="connection-members-dao"></a>Connection Members (DAO)

**Применимо к**: Access 2013, Office 2013

> [!NOTE]
> Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access. Объект подключения представляет подключение к базе данных ODBC (только для рабочих областей технология ODBCDirect).
 

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
<td><p><strong><a href="connection-cancel-method-dao.md">Отмена</a></strong></p></td>
<td><p></p>

<br/>


<p>Отменяет выполнение ожидающие асинхронного вызова метода (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-close-method-dao.md">Закрыть</a></strong></p></td>
<td><p>Закрывает открытое <strong>подключение</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-createquerydef-method-dao.md">CreateQueryDef</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="querydef-object-dao.md">QueryDef</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-execute-method-dao.md">Выполнение</a></strong></p></td>
<td><p>Запуск запроса или выполняет инструкции SQL на указанный объект.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="recordset-object-dao.md">набора записей</a></strong> и добавляет его в коллекцию <strong>наборов записей</strong> .</p></td>
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
<td><p><strong><a href="connection-connect-property-dao.md">Подключение</a></strong></p></td>
<td><p>Задает или возвращает значение, которое содержит сведения об источнике открытое подключение. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-database-property-dao.md">База данных</a></strong></p></td>
<td><p></p>

<br/>


<p>Возвращает объект <strong><a href="database-object-dao.md">базы данных</a></strong> , соответствующий для этого подключения (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает имя <strong><a href="connection-object-dao.md">подключения</a></strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-querydefs-property-dao.md">QueryDefs</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>QueryDefs</strong> , который содержит все объекты <strong>QueryDef</strong> указанного подключения. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-querytimeout-property-dao.md">QueryTimeout</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее количество секунд ожидания до возникновения ошибки времени ожидания при выполнении запроса на источник данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Возвращает число записей, влияет на недавно вызванного метода <strong><a href="connection-execute-method-dao.md">Execute</a></strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-recordsets-property-dao.md">Наборы записей</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>наборов записей</strong> , который содержит все открытые наборы записей в для указанного подключения. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p></p>

<br/>


<p>Указывает, следует ли асинхронной операции (то есть, вызывается метод с параметром <strong>dbRunAsync</strong> ) завершено выполнение (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="connection-transactions-property-dao.md">Transactions</a></strong></p></td>
<td><p>Возвращает значение, указывающее, поддерживает ли объект транзакции. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="connection-updatable-property-dao.md">Обновляемые</a></strong></p></td>
<td><p>Возвращает значение, указывающее, является ли объект DAO можно изменить. Только для чтения <strong>типа Boolean</strong>. Только для чтения.</p></td>
</tr>
</tbody>
</table>

