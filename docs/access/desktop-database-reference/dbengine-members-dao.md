---
title: Участники DBEngine (DAO)
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
# <a name="dbengine-members-dao"></a>Участники DBEngine (DAO)


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
<td><p>Начинается новая транзакция. База данных чтения и <strong>записи</strong>.</p></td>
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
<td><p>Создает новый объект <strong><a href="database-object-dao.md">Database,</a></strong> сохраняет базу данных на диск и возвращает открытый объект <strong>Database</strong> (только рабочие пространства Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></p></td>
<td><p>Создает новый <strong><a href="workspace-object-dao.md">объект Workspace.</a></strong></p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-idle-method-dao.md">Idle</a></strong></p></td>
<td><p>Приостанавливать обработку данных, позволяя движку базы данных Microsoft Access выполнять любые ожидающие задачи, такие как оптимизация памяти или время ожидания страниц (только в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p>Одно из <strong><a href="workspacetypeenum-enumeration-dao.md">значений WorkspaceTypeEnum.</a></strong></p>
<td><p><strong>ПРИМЕЧАНИЕ</strong>: Рабочие области ODBCDirect не поддерживаются в Microsoft Access 2013. Используйте ADO, если вы хотите получить доступ к внешним источникам данных без использования ядра СУБД Microsoft Access.</p>
<p>Открывает объект <strong><a href="connection-object-dao.md">Connection</a></strong> в источнике данных ODBC (только в рабочей области ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Открывает указанную базу данных и возвращает ссылку на объект <strong><a href="database-object-dao.md">Database</a></strong>, который ее представляет.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></p></td>
<td><p>Вводит сведения о подключении для источника данных ODBC в Windows реестре. Драйверу ODBC необходимы сведения о подключении, когда источник данных ODBC открыт во время сеанса.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-rollback-method-dao.md">Откат</a></strong></p></td>
<td><p>Завершает текущую транзакцию и восстанавливает базы данных объекта <strong>Workspace</strong> до состояния, в который они были, когда началась текущая транзакция.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></p></td>
<td><p>Временно переопределяет значения для ключей двигателя базы данных Microsoft Access в реестре Windows (только в рабочей области Microsoft Access).</p></td>
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
<td><p>Задает пароль, используемый для создания рабочего <strong>пространства по</strong> умолчанию при инициализации. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></p></td>
<td><p>Задает или возвращает значение, которое указывает, какой тип рабочего пространства будет использоваться следующим созданным объектом <strong><a href="workspace-object-dao.md">Workspace.</a></strong></p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></p></td>
<td><p>Задает имя пользователя, используемого для создания рабочего <strong>пространства по</strong> умолчанию при инициализации. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-errors-property-dao.md">Ошибки</a></strong></p></td>
<td><p>Возвращает <strong>коллекцию ошибок,</strong> которая содержит все сохраненные объекты <strong>Ошибки</strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></p></td>
<td><p>Задает или возвращает сведения о ключе Windows реестра, который содержит значения для двигателя базы данных Microsoft Access (только в рабочей области Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Задает или возвращает количество секунд до возникновения ошибки при попытке войти в базу данных ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-properties-property-dao.md">Properties</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">Properties</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-version-property-dao.md">Версия</a></strong></p></td>
<td><p>Rreturns версия DAO в настоящее время используется. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-workspaces-property-dao.md">Workspaces</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>Workspaces,</strong> которая содержит все активные незагрузные объекты <strong>рабочей</strong> области. Только для чтения.</p></td>
</tr>
</tbody>
</table>

