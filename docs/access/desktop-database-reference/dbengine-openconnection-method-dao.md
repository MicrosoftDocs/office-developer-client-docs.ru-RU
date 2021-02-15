---
title: Метод DBEngine.OpenConnection (DAO)
TOCTitle: OpenConnection Method
ms:assetid: 778a581f-be42-94ee-e5c6-4cbc1843450d
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196074(v=office.15)
ms:contentKeyID: 48545729
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053574
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 845c710954d83003f49a6cd9db21ae3f3bfab383
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294262"
---
# <a name="dbengineopenconnection-method-dao"></a>Метод DBEngine.OpenConnection (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*выражение .* OpenConnection(***Name***, ***Options***, ***ReadOnly***, ***Connect***)

*expression*: переменная, представляющая объект **DBEngine**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Строковое выражение. См. обсуждение в статье "Замечания".</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>задает различные параметры подключения, как указано в примечаиях. На основе этого значения диспетчер драйверов ODBC запросит у пользователя такие сведения о под подключением, как имя источника данных (DSN), имя пользователя и пароль.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Необязательно устанавливать.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Имеет значение <strong>True,</strong> если подключение должно быть открыто только для чтения, и <strong>False,</strong> если подключение должно быть открыто для чтения и записи (по умолчанию).</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Необязательно заполнять.</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строка подключения ODBC. См. <strong><a href="connection-connect-property-dao.md">свойство Connect</a></strong> для определенных элементов и синтаксиса этой строки. Предварительное &quot; ODBC; &quot; является обязательной.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Connection

## <a name="remarks"></a>Заметки

Используйте метод **OpenConnection,** чтобы установить подключение к источнику данных ODBC из рабочей области ODBCDirect. Метод **OpenConnection** похож, но не эквивалентен **Методу OpenDatabase.** Основное отличие заключается в **том, что OpenConnection** доступен только в рабочей области ODBCDirect.

Если в аргументе подключения указывается зарегистрированное имя источника данных ODBC (DSN), аргументом имени может быть любая допустимая строка, а также предоставляется свойство **Name** для объекта **Connection.** Если допустимое DSN не включено в аргумент подключения, имя должно ссылаться на допустимое DSN ODBC, которое также будет **свойством Name.** Если ни имя, ни подключение не содержат допустимое DSN, диспетчер драйверов ODBC можно настроить (с помощью аргумента параметров), чтобы задействовать у пользователя необходимые сведения о подключении. Затем DSN, предоставленное по запросу, предоставляет **свойство Name.**

Аргумент options определяет, следует ли и когда пользователю предложено установить подключение, а также следует ли открывать подключение асинхронно. Можно использовать одну из следующих констант.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbDriverNoPrompt</strong></p></td>
<td><p>Диспетчер драйверов ODBC использует строку подключения, предоставленную <em>в имени dbname</em> и <em>connect.</em> Если у вас недостаточно сведений, возникает ошибка во время запуска.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverPrompt</strong></p></td>
<td><p>В диспетчере драйверов ODBC отображается диалоговое окно "Источники данных <strong>ODBC",</strong> в котором отображаются все необходимые сведения, предоставленные в <em>имени dbname</em> или <em>connect.</em> Строка подключения состоит из DSN, выбранного пользователем через диалоговое окно, или, если пользователь не указывает DSN, используется DSN по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbDriverComplete</strong></p></td>
<td><p>Значение, используемое по умолчанию. Если аргумент <em>подключения</em> содержит все необходимые сведения для завершения подключения, диспетчер драйверов ODBC использует строку в <em>подключении.</em> В противном случае он будет вести себя так же, как при <strong>указании dbDriverPrompt.</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>dbDriverCompleteRequired</strong></p></td>
<td><p>Этот параметр работает так же, как <strong>и dbDriverComplete,</strong> за исключением того, что драйвер ODBC отключает запросы на все сведения, не необходимые для завершения подключения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Выполните метод асинхронно. Эта константа может использоваться с любыми другими <em>константами параметров.</em></p></td>
</tr>
</tbody>
</table>


**OpenConnection** возвращает объект **Connection,** содержащий сведения о подсети. Объект **Connection** похож на объект **[Database.](database-object-dao.md)** Основное отличие состоит в том, что объект **Database** обычно представляет базу данных, хотя его можно использовать для представления подключения к источнику данных ODBC из рабочей области Microsoft Access.

