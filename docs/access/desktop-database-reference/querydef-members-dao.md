---
title: Элементы QueryDef (DAO)
TOCTitle: QueryDef Members
ms:assetid: 3f914d23-aa63-3ebd-1d86-4f53da71131b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192855(v=office.15)
ms:contentKeyID: 48544403
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 5b3afc134636d5621f38ece4530be5312e42bc74
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302984"
---
# <a name="querydef-members-dao"></a>Элементы QueryDef (DAO)


**Область применения**: Access 2013, Office 2013

Объект QueryDef — это сохраняемое определение запроса в базе данных ядра СУБД Microsoft Access.

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
<td><p><strong><a href="querydef-cancel-method-dao.md">Cancel</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Отменяет выполнение ожидающего вызова асинхронного метода (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-close-method-dao.md">Close</a></strong></p></td>
<td><p>Закрывает открытый <strong>queryDef</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-createproperty-method-dao.md">CreateProperty</a></strong></p></td>
<td><p>Создает новый объект Свойства, определенный <strong><a href="property-object-dao.md">пользователем</a></strong> (только рабочие пространства Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-execute-method-dao.md">Execute</a></strong></p></td>
<td><p>Выполняет инструкцию SQL для указанного объекта.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-openrecordset-method-dao.md">OpenRecordset</a></strong></p></td>
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
<td><p><strong><a href="querydef-cachesize-property-dao.md">CacheSize</a></strong></p></td>
<td><p>Задает или возвращает число записей, полученных из источника данных ODBC, который будет кэшироваться локально. Для чтения и записи, <strong>Long</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-connect-property-dao.md">Connect</a></strong></p></td>
<td><p>Задает или возвращает значение, которое предоставляет сведения об источнике базы данных, используемом в сквозной запрос. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-datecreated-property-dao.md">DateCreated</a></strong></p></td>
<td><p>Возвращает дату и время создания объекта (только в рабочей области Microsoft Access). Только для чтения, <strong>Variant</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-fields-property-dao.md">Fields</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="fields-collection-dao.md">Fields,</a></strong> которая представляет все сохраненные <strong><a href="field-object-dao.md">объекты Field</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-lastupdated-property-dao.md">LastUpdated</a></strong></p></td>
<td><p>Возвращает дату и время последнего изменения, выполненного в объекте. Только для чтения, <strong>Variant</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-maxrecords-property-dao.md">MaxRecords</a></strong></p></td>
<td><p>Задает или возвращает максимальное количество записей, возвращаемых из запроса к источнику данных ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-odbctimeout-property-dao.md">ODBCTimeout</a></strong></p></td>
<td><p>Указывает количество секунд, которые нужно ждать до возникновения ошибки ожидания при выполнении <strong><a href="querydef-object-dao.md">запроса в</a></strong> базе данных ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-parameters-property-dao.md">Parameters</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="parameters-collection-dao.md">Параметры,</a></strong> которая содержит все объекты <strong><a href="parameter-object-dao.md">Параметры</a></strong> указанного <strong>QueryDef.</strong> Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-prepare-property-dao.md">Подготовка</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Задает или возвращает значение, которое указывает, следует ли подготовить запрос на сервере в качестве временной процедуры хранения, используя функцию API <strong>SQLPrepare</strong> ODBC перед выполнением или только что выполненную с помощью функции <strong>API SQLExecDirect</strong> (только в рабочих пространствах ODBCDirect). Read/Write <strong><a href="querydefstateenum-enumeration-dao.md">QueryDefStateEnum</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-recordsaffected-property-dao.md">RecordsAffected</a></strong></p></td>
<td><p>Возвращает количество записей, затронутых самым недавно вызываемой методом <strong><a href="querydef-execute-method-dao.md">Выполнения.</a></strong></p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-returnsrecords-property-dao.md">ReturnsRecords</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, возвращает ли SQL-сквозной запрос во внешнюю базу данных записи (только в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-sql-property-dao.md">SQL</a></strong></p></td>
<td><p>Задает или возвращает инструкцию SQL, которая определяет запрос, выполняемый объектом <strong><a href="querydef-object-dao.md">QueryDef</a></strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-stillexecuting-property-dao.md">StillExecuting</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Указывает на то, завершена или нет асинхронной операции (т. е метода, вызываемого с параметром <a href="recordsetoptionenum-enumeration-dao.md">dbRunAsync</a>) (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="querydef-type-property-dao.md">Тип</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее операционный тип или тип данных объекта. Только для чтения<strong>в integer</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="querydef-updatable-property-dao.md">Updatable</a></strong></p></td>
<td><p>Возвращает значение, которое указывает на то, можно ли изменить DAO объект. Только для чтения, <strong>Boolean</strong>.</p></td>
</tr>
</tbody>
</table>

