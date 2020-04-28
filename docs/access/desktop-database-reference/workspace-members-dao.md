---
title: Участники рабочих областей (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8a2105c13f5f7ce9a75e7e18e20477d8b283543a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302596"
---
# <a name="workspace-members-dao"></a>Участники рабочих областей (DAO)


**Область применения**: Access 2013, Office 2013

Объект Workspace определяет именованный сеанс для пользователя. Он содержит открытые базы данных и предоставляет механизмы для одновременных транзакций и (в рабочих областях Microsoft Access) поддержку защищенной рабочей группы.

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
<td><p><strong><a href="workspace-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>Начинает новую транзакцию. Чтение и запись <strong>базы данных</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-close-method-dao.md">Close</a></strong></p></td>
<td><p>Закрывает открытую <strong>рабочую область</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Завершает текущую транзакцию и сохраняет изменения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="database-object-dao.md">Database</a></strong> , сохраняет базу данных на диске и возвращает открытый объект <strong>базы данных</strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Открывает объект <strong><a href="connection-object-dao.md">Connection</a></strong> в источнике данных ODBC (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Открывает указанную базу данных в объекте <strong> <a href="workspace-object-dao.md">Workspace</a> </strong> и возвращает ссылку на объект <strong> <a href="database-object-dao.md">Database</a> </strong>, который ее представляет.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-rollback-method-dao.md">Отката</a></strong></p></td>
<td><p>Завершает текущую транзакцию и восстанавливает базы данных в объекте <strong>Workspace</strong> в том состоянии, в котором они были в момент начала текущей транзакции.</p></td>
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
<td><p><strong><a href="workspace-connections-property-dao.md">Connections</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>Connections</strong> , представляющую текущие подключения в указанной <strong>рабочей области</strong>. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-databases-property-dao.md">Databases</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>баз данных</strong> , представляющую открытые базы данных в указанной <strong>рабочей области</strong>. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-defaultcursordriver-property-dao.md">дефаулткурсордривер</a></strong></p></td>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Задает или возвращает тип драйвера курсора, используемого в соединении, созданном методами <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> или <strong><a href="dbengine-opendatabase-method-dao.md">openDatabase</a></strong> (только для рабочих областей ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-isolateodbctrans-property-dao.md">исолатеодбктранс</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, изолированы ли множественные транзакции, использующие один и тот же источник данных ODBC, подключенный к ядру СУБД Microsoft Access (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Задает или возвращает число секунд до возникновения ошибки при попытке входа в базу данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. <strong>Строка</strong> для чтения и записи, если объект не был добавлен в коллекцию. <strong>Строка</strong> , доступная только для чтения, если объект добавлен в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-type-property-dao.md">Тип</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее операционный тип или тип данных объекта. Только для чтения, <strong>Integer</strong>.</p></td>
</tr>
</tbody>
</table>

