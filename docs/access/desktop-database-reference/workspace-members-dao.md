---
title: Workspace Members (DAO)
TOCTitle: Workspace Members
ms:assetid: 13ac7d41-1b25-20d2-5c85-0f21bfd38328
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845437(v=office.15)
ms:contentKeyID: 48543374
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 04dd82fcdb3bd9be0581ea5172429960769b31af
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483053"
---
# <a name="workspace-members-dao"></a>Workspace Members (DAO)


**Применимо к**: Access 2013 | Office 2013

Объект рабочей области определяет именованный сеанса для пользователя. Содержит open баз данных и предоставляет механизмы для одновременных операций и, в рабочих областях Microsoft Access безопасного поддержка рабочей группы.

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
<td><p>Начало новой транзакции. Чтение и запись <strong>базы данных</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-close-method-dao.md">Закрыть</a></strong></p></td>
<td><p>Закрытие открытых <strong>рабочей области</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-committrans-method-dao.md">CommitTrans</a></strong></p></td>
<td><p>Завершает текущий транзакций и сохраняет изменения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-createdatabase-method-dao.md">CreateDatabase</a></strong></p></td>
<td><p>Создает новый объект <strong><a href="database-object-dao.md">базы данных</a></strong> , сохраняет базы данных на диск и возвращает объект открыт <strong>базы данных</strong> (только для рабочих областей Microsoft Access).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-openconnection-method-dao.md">OpenConnection</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Открывает объект <strong><a href="connection-object-dao.md">подключения</a></strong> для источника данных ODBC (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-opendatabase-method-dao.md">OpenDatabase</a></strong></p></td>
<td><p>Открывает указанной базы данных в объекте <strong><a href="workspace-object-dao.md">рабочей области</a></strong> и возвращает ссылку на объект <strong><a href="database-object-dao.md">базы данных</a></strong> , который представляет его.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-rollback-method-dao.md">Откат</a></strong></p></td>
<td><p>Завершает текущий транзакцию и восстановление базы данных в объекте <strong>рабочей области</strong> для состояния, в котором они были на момент начала текущей транзакции.</p></td>
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
<td><p><strong><a href="workspace-connections-property-dao.md">Подключения</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>подключений</strong> , который представляет текущего подключения в указанной <strong>рабочей области</strong>. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-databases-property-dao.md">Базы данных</a></strong></p></td>
<td><p>Возвращает коллекцию <strong>баз данных</strong> , который представляет open баз данных в указанной <strong>рабочей области</strong>. Только для чтения.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-defaultcursordriver-property-dao.md">DefaultCursorDriver</a></strong></p></td>
<td><p></p>

> [!NOTE]
> <P>Рабочие области технология ODBCDirect не поддерживаются в Microsoft Access 2013. Использование ADO, если вы хотите получить доступ к внешним источникам данных без использования ядро базы данных Microsoft Access.</P>


<p>Задает или возвращает тип курсора драйвер, используемый для подключения, созданные методами <strong><a href="dbengine-openconnection-method-dao.md">OpenConnection</a></strong> или <strong><a href="dbengine-opendatabase-method-dao.md">OpenDatabase</a></strong> (только для рабочих областей технология ODBCDirect).</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-isolateodbctrans-property-dao.md">IsolateODBCTrans</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее, включены ли несколько transactiond, связанных с одной Microsoft Access базы данных подключен модуль источник данных ODBC изолированный (Microsoft Access рабочие области только).</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-logintimeout-property-dao.md">LoginTimeout</a></strong></p></td>
<td><p>Задает или возвращает число секунд, прежде чем возникает ошибка при попытке выполнить вход в базе данных ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-name-property-dao.md">Name</a></strong></p></td>
<td><p>Возвращает или задает имя указанного объекта. Чтение и запись <strong>строки</strong> Если объект не были добавлены в коллекцию. Только для чтения <strong>строка</strong> Если объект были добавлены в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><strong><a href="workspace-properties-property-dao.md">Свойства</a></strong></p></td>
<td><p>Возвращает коллекцию <strong><a href="properties-collection-dao.md">свойств</a></strong> для указанного объекта. Только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><strong><a href="workspace-type-property-dao.md">Тип</a></strong></p></td>
<td><p>Задает или возвращает значение, указывающее действующие типа или данных тип объекта. Только для чтения <strong>целое число</strong>.</p></td>
</tr>
</tbody>
</table>

