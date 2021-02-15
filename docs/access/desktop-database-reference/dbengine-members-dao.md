---
title: Члены DBEngine (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 1128b27385ef9f8c898fb79d05ae28d596c4af6a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294283"
---
# <a name="dbengine-members-dao"></a>Члены DBEngine (DAO)


**Область применения**: Access 2013, Office 2013

Объект DBEngine — это объект верхнего уровня объектной модели DAO.

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
<td><p><strong><a href="dbengine-begintrans-method-dao.md">BeginTrans</a></strong></p></td>
<td><p>Начинает новую транзакцию. База данных для чтения и <strong>записи.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Завершает текущую транзакцию и сохраняет изменения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></p></td>
<td><p>Копирует и сжимает закрытую базу данных, предоставляя возможность изменить ее версию, порядок сортировки и шифрование. (Только для рабочих областей Microsoft Access.) .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="database-object-dao.md">Базы</a></strong> данных, сохраняет базу данных на диск и возвращает открытый объект <strong>базы</strong> данных (только для рабочих пространств Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="workspace-object-dao.md">Workspace.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-idle-method-dao.md">Бездействие</a></strong></p></td>
<td><p>Приостанавливать обработку данных, позволяя яд баз данных Microsoft Access выполнять любые ожидающие задачи, такие как оптимизация памяти или время ожидания страниц (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p>Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Открывает объект <strong><a href="connection-object-dao.md">Connection</a></strong> в источнике данных ODBC (только для рабочей области ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Открывает указанную базу данных и возвращает ссылку на объект <strong><a href="database-object-dao.md">Database</a></strong>, который ее представляет.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></p></td>
<td><p>Введите сведения о под соединении для источника данных ODBC в реестре Windows. Драйверу ODBC необходимы сведения о под подключениех при открытом источнике данных ODBC во время сеанса.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-rollback-method-dao.md">Откат</a></strong></p></td>
<td><p>Завершает текущую транзакцию и восстанавливает состояние баз данных в объекте <strong>Workspace</strong> в состоянии, в который они находились на момент начала текущей транзакции.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></p></td>
<td><p>Временно переопределяет значения ключей ядер ядер базы данных Microsoft Access в реестре Windows (только для рабочей области Microsoft Access).</p></td>
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
<td><p><strong><a href="dbengine-defaultpassword-property-dao.md">DefaultPassword</a></strong></p></td>
<td><p>Задает пароль, используемый для создания рабочей <strong>области по</strong> умолчанию при ее инициализации. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, какой тип рабочей области будет использоваться следующим созданным объектом <strong><a href="workspace-object-dao.md">Workspace.</a></strong></p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></p></td>
<td><p>Задает имя пользователя, используемого для создания рабочей <strong>области по</strong> умолчанию при ее инициализации. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-errors-property-dao.md">Ошибки</a></strong></p></td>
<td><p>Возвращает <strong>коллекцию Errors,</strong> которая содержит все сохраненные объекты <strong>Error</strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></p></td>
<td><p>Задает или возвращает сведения о ключе реестра Windows, который содержит значения для ядвижка базы данных Microsoft Access (только для рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Задает или возвращает время в секундах до возникновения ошибки при попытке входа в базу данных ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-version-property-dao.md">Версия</a></strong></p></td>
<td><p>Rreturns the version of DAO currently in use. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></p></td>
<td><p>Возвращает <strong>коллекцию Workspaces,</strong> которая содержит все активные незашифленные объекты <strong>рабочей</strong> области. Только для чтения.</p></td>
</tr>
</tbody>
</table>

