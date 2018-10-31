---
title: DBEngine Members (DAO)
TOCTitle: DBEngine Members
ms:assetid: 740b6a85-585f-0e1d-710b-84ba24825325
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195868(v=office.15)
ms:contentKeyID: 48545652
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7b534d4595bd003c76e756c44d6e88f53a725cc8
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25861787"
---
# <a name="dbengine-members-dao"></a>DBEngine Members (DAO)


**Применимо к**: Access 2013 | Office 2013

Объект DBEngine — это объект верхнего уровня в объектной модели DAO.

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
<td><p>Начало новой транзакции. Чтение и запись <strong>базы данных</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Завершает текущий транзакций и сохраняет изменения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-compactdatabase-method-dao.md">CompactDatabase</a></strong></p></td>
<td><p>Копирует и сжимает закрытой базы данных и позволяет изменить его версию, сортировки порядок и шифрования. (Microsoft Access рабочие области только). .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="database-object-dao.md">базы данных</a></strong> , сохраняет базы данных на диск и возвращает объект открыт <strong>базы данных</strong> (только для рабочих областей Microsoft Access). .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-createworkspace-method-dao.md">CreateWorkspace</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="workspace-object-dao.md">рабочей области</a></strong> .</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-idle-method-dao.md">Простоя</a></strong></p></td>
<td><p>Выполняется приостановка обработки данных, позволяя ядро базы данных Microsoft Access завершить все ожидающие задач, таких как оптимизации памяти или время ожидания страницы (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p></p>

> [!NOTE]
> Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.


<p>Открывает объект <strong><a href="connection-object-dao.md">подключения</a></strong> для источника данных ODBC (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Открывает указанной базы данных и возвращает ссылку на объект <strong><a href="database-object-dao.md">базы данных</a></strong> , который представляет его.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-registerdatabase-method-dao.md">RegisterDatabase</a></strong></p></td>
<td><p>Вводит сведения о подключении к источнику данных ODBC в реестре Windows. Драйвер ODBC требуются данные подключения при открытии источника данных во время сеанса.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-rollback-method-dao.md">Откат</a></strong></p></td>
<td><p>Завершает текущий транзакцию и восстановление базы данных в объекте <strong>рабочей области</strong> для состояния, в котором они были на момент начала текущей транзакции.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-setoption-method-dao.md">SetOption</a></strong></p></td>
<td><p>Временно переопределяет значения для клавиш ядра базы данных Microsoft Access в реестре Windows (только для рабочих областей Microsoft Access).</p></td>
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
<td><p>Задает пароль, используемый для создания <strong>рабочей области</strong> по умолчанию при ее инициализации. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-defaulttype-property-dao.md">DefaultType</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, какой тип рабочей области будет использоваться далее созданный объект <strong><a href="workspace-object-dao.md">рабочей области</a></strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-defaultuser-property-dao.md">DefaultUser</a></strong></p></td>
<td><p>Задает имя пользователя, используемое для создания <strong>рабочей области</strong> по умолчанию при ее инициализации. Для чтения и записи, <strong>String</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-errors-property-dao.md">Ошибки</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>ошибок</strong> , который содержит все хранимые объекты <strong>об ошибках</strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-inipath-property-dao.md">IniPath</a></strong></p></td>
<td><p>Задает или возвращает сведения о раздел реестра Windows, который содержит значения для ядро базы данных Microsoft Access (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Задает или возвращает число секунд, прежде чем возникает ошибка при попытке выполнить вход в базе данных ODBC.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="dbengine-version-property-dao.md">Версия</a></strong></p></td>
<td><p>Возвращает версию DAO в настоящее время используется. Только для чтения, <strong>String</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="dbengine-workspaces-property-dao.md">Рабочие области</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>рабочих областей</strong> , содержащий все объекты active, Показать <strong>рабочей области</strong> . Только для чтения.</p></td>
</tr>
</tbody>
</table>

