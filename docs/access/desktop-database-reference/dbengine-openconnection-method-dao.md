---
title: Метод DBEngine. OpenConnection (DAO)
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
# <a name="dbengineopenconnection-method-dao"></a>Метод DBEngine. OpenConnection (DAO)

**Область применения**: Access 2013, Office 2013

## <a name="syntax"></a>Синтаксис

*Expression* . OpenConnection (***Name***, ***Options***, ***ReadOnly***, ***Connect***)

*Expression (выражение* ) Переменная, представляющая объект **DBEngine** .

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
<th><p>Обязательно/необязательно</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Name</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Строковое выражение. Просмотрите обсуждение в разделе Примечания.</p></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Задает различные параметры подключения, как указано в разделе "Примечания". На основе этого значения диспетчер драйверов ODBC запрашивает у пользователя сведения о подключении, такие как имя источника данных (DSN), имя пользователя и пароль.</p></td>
</tr>
<tr class="odd">
<td><p><em>ReadOnly</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p><strong>Имеет значение true</strong> , если подключение должно быть открыто только для чтения, и <strong>false</strong> , если подключение должно быть открыто для чтения и записи (по умолчанию).</p></td>
</tr>
<tr class="even">
<td><p><em>Connect</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строка подключения ODBC. Просмотрите свойство <strong><a href="connection-connect-property-dao.md">Connect</a></strong> для определенных элементов и синтаксиса этой строки. Префикс &quot;ODBC; &quot; является обязательным.</p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a>Возвращаемое значение

Connection

## <a name="remarks"></a>Замечания

Используйте метод **OpenConnection** , чтобы установить подключение к источнику данных ODBC из рабочей области ODBCDirect. Метод **OpenConnection** аналогичен, но не эквивалентен **openDatabase**. Основное отличие состоит в том, что **OpenConnection** доступно только в рабочей области ODBCDirect.

Если указать в аргументе Connect имя зарегистрированного источника данных ODBC (DSN), то аргумент name может быть любой допустимой строкой, а также будет предоставлять свойство **Name** для объекта **Connection** . Если допустимое имя DSN не включено в аргумент Connect, то имя должно ссылаться на допустимый DSN ODBC, которое также будет являться свойством **Name** . Если ни одно из этих имен и не содержит допустимое имя DSN, диспетчер драйверов ODBC можно настроить (с помощью аргумента Options), чтобы запросить у пользователя необходимые сведения о подключении. Имя источника данных, предоставляемое при высказке, предоставляет свойство **Name** .

Аргумент options определяет, когда и когда следует предлагать пользователю установить подключение, а также следует ли асинхронно открывать подключение. Можно использовать одну из следующих констант.

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
<td><p><strong>Дбдривернопромпт</strong></p></td>
<td><p>Диспетчер драйверов ODBC использует строку подключения, указанную в <em>dbname</em> и <em>Connect</em>. Если вы не выдаете достаточно сведений, возникает ошибка времени выполнения.</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбдриверпромпт</strong></p></td>
<td><p>Диспетчер драйверов ODBC отображает диалоговое окно <strong>Источники данных ODBC</strong> , в котором отображаются все релевантные сведения, предоставленные в <em>dbname</em> или <em>Connect</em>. Строка подключения состоит из имени источника данных, которое пользователь выбрал через диалоговые окна, или, если пользователь не указал значение DSN, используется DSN по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Дбдриверкомплете</strong></p></td>
<td><p>Значение, используемое по умолчанию. Если аргумент <em>Connect</em> включает все необходимые сведения для завершения подключения, диспетчер драйверов ODBC использует строку в разделе <em>Connect</em>. В противном случае он ведет себя так же, как и при указании <strong>дбдриверпромпт</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Дбдриверкомплетерекуиред</strong></p></td>
<td><p>Этот параметр имеет вид <strong>дбдриверкомплете</strong> , за исключением того, что в ДРАЙВЕРе ODBC отключается запрос для получения сведений, не необходимых для завершения подключения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbRunAsync</strong></p></td>
<td><p>Асинхронно выполняет метод. Эту константу можно использовать с любыми другими константами <em>Options</em> .</p></td>
</tr>
</tbody>
</table>


**OpenConnection** возвращает объект **Connection** , который содержит сведения о подключении. Объект **Connection** аналогичен объекту **[базы данных](database-object-dao.md)** . Основное различие состоит в том, что объект **базы данных** обычно представляет базу данных, хотя он может использоваться для представления подключения к источнику данных ODBC из рабочей области Microsoft Access.

