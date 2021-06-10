---
title: Поставщик Microsoft OLE DB для SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c4faa664ed9001c1c06906f58c7d873faf75a5d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288892"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a>Поставщик Microsoft OLE DB для SQL Server


**Область применения**: Access 2013, Office 2013

Поставщик DB Microsoft OLE для SQL Server SQLOLEDB позволяет ADO получать доступ к Microsoft SQL Server.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к этому поставщику, установите аргумент *Поставщика* [свойству ConnectionString:](connectionstring-property-ado.md)

```sql 
 
SQLOLEDB 
```

Это значение также можно установить или прочитать с помощью свойства [Provider.](provider-property-ado.md)

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

Строка состоит из этих ключевых слов:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ключевое слово</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Поставщик</strong></p></td>
<td><p>Указывает поставщика OLE DB для SQL Server.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong> или <strong>сервер</strong></p></td>
<td><p>Указывает имя сервера.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Начальный каталог</strong> или <strong>база данных</strong></p></td>
<td><p>Указывает имя базы данных на сервере.</p></td>
</tr>
<tr class="even">
<td><p><strong>Пользовательский ID</strong> или <strong>uid</strong></p></td>
<td><p>Указывает имя пользователя (для SQL Server проверки подлинности).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Пароль</strong> или <strong>pwd</strong></p></td>
<td><p>Указывает пароль пользователя (для SQL Server проверки подлинности).</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Provider-Specific параметры подключения

Поставщик поддерживает несколько параметров подключения, определенных для поставщика, в дополнение к параметрам, определенным ADO. Как и в свойствах подключения ADO, эти свойства, определенные для поставщика, можно установить через коллекцию [свойств](properties-collection-ado.md) подключения или установить в составе **ConnectionString.** [](connection-object-ado.md)

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Trusted_Connection</p></td>
<td><p>Указывает режим проверки подлинности пользователей. Это может быть заданной <strong>для Да</strong> или <strong>Нет</strong>. По умолчанию выбрано <strong>Нет</strong>. Если это свойство задано <strong>да,</strong>то SQLOLEDB использует режим проверки подлинности microsoft Windows NT для авторизации доступа пользователей к базе данных SQL Server, указанной значениями свойств Location <strong>и</strong> <a href="datasource-property-ado.md">Datasource.</a> Если это свойство настроено на <strong>нет,</strong>SQLOLEDB использует смешанный режим для авторизации доступа пользователей к SQL Server базе данных. Код SQL Server и пароль указаны в <strong>свойствах User Id</strong> и <strong>Password.</strong></p></td>
</tr>
<tr class="even">
<td><p>Current Language</p></td>
<td><p>Указывает имя SQL Server языка. Определяет язык, используемый для выбора и форматирования системных сообщений. Язык должен быть установлен на SQL Server, в противном случае открытие подключения не удастся.</p></td>
</tr>
<tr class="odd">
<td><p>Сетевой адрес</p></td>
<td><p>Указывает сетевой адрес SQL Server, указанного <strong>свойством Location.</strong></p></td>
</tr>
<tr class="even">
<td><p>Библиотека сети</p></td>
<td><p>Указывает имя сетевой библиотеки (библиотеки динамических ссылок), используемой для связи с SQL Server. Имя не должно включать путь или расширение .dll файла. По умолчанию предоставляется конфигурация SQL Server клиента.</p></td>
</tr>
<tr class="odd">
<td><p>Использование процедуры подготовки</p></td>
<td><p>Определяет, создает ли SQL Server временные сохраненные процедуры при подготовке команд (по свойству <strong>Prepared).</strong></p></td>
</tr>
<tr class="even">
<td><p>Auto Translate</p></td>
<td><p>Указывает, преобразованы ли символы OEM/ANSI. Это свойство может быть заданной <strong>для True</strong> или <strong>False</strong>. Значение по умолчанию — <strong>True</strong>. Если это свойство настроено на <strong>True,</strong>то SQLOLEDB выполняет преобразование символов OEM/ANSI при извлечении или отправлении в SQL Server. Если это свойство настроено на <strong>False,</strong>SQLOLEDB не выполняет преобразование символов OEM/ANSI в данные строки многобайтных символов.</p></td>
</tr>
<tr class="odd">
<td><p>Размер пакета</p></td>
<td><p>Указывает размер сетевого пакета в bytes. Значение свойства размера пакета должно быть между 512 и 32767. Размер сетевого пакета SQLOLEDB по умолчанию — 4096.</p></td>
</tr>
<tr class="even">
<td><p>Имя приложения</p></td>
<td><p>Указывает имя приложения клиента.</p></td>
</tr>
<tr class="odd">
<td><p>ID рабочей станции</p></td>
<td><p>Строка, определяемая рабочей станции.</p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a>Использование командных объектов

SQLOLEDB принимает объединение ODBC, ANSI и SQL Server transact-SQL как допустимый синтаксис. Например, в следующем SQL для указания функции строки LCASE используется последовательность SQL ODBC:

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

LCASE возвращает строку символов, преобразуя все символы верхнего шкафа в их эквиваленты нижнего регистра. Функция строки SQL ANSI LOWER выполняет ту же операцию, поэтому следующее SQL является эквивалентом утверждения ANSI, представленного выше:

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

SQLOLEDB успешно обрабатывает форму заявления, если указана в виде текста для команды.

## <a name="stored-procedures"></a>Сохраненные процедуры

При выполнении SQL Server с помощью команды SQLOLEDB используйте последовательность побега процедуры ODBC в тексте команды. Затем SQLOLEDB использует механизм удаленного вызова процедуры SQL Server для оптимизации обработки команд. Например, следующим утверждением SQL ODBC является предпочтительный командный текст по форме Transact-SQL:

## <a name="odbc-sql"></a>ODBC SQL

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a>Transact-SQL

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a>Поведение наборов записей

SQLOLEDB не может использовать SQL Server курсоры для поддержки нескольких результатов, созданных многими командами. Если потребитель запрашивает набор записей, требующий SQL Server поддержки курсора, возникает ошибка, если используемый текст команды создает более одного наборов записей в результате.

Прокручиваемые записи SQLOLEDB поддерживаются SQL Server курсорами. SQL Server накладывает ограничения на курсоры, чувствительные к изменениям, внесенным другими пользователями базы данных. В частности, строки в некоторых курсорах невозможно заказать, и попытка создать набор записей с помощью команды, содержащей SQL ORDER BY, может привести к сбой.

## <a name="dynamic-properties"></a>Dynamic Properties

Поставщик microsoft OLE DB для SQL Server вставляет несколько динамических свойств в коллекцию **свойств** незапертых объектов [Connection,](connection-object-ado.md) [Recordset](recordset-object-ado.md)и [Command.](command-object-ado.md)

Следующие таблицы — это перекрестный индекс имен ADO и OLE DB для каждого динамического свойства. Ссылка программиста OLE DB относится к имени свойства ADO под термином "Описание". Дополнительные сведения об этих свойствах можно найти в справке программиста OLE DB. Поиск имени свойства OLE DB в Индексе или см. в приложении C: OLE DB Properties.

## <a name="connection-dynamic-properties"></a>Динамические свойства подключения

Следующие свойства добавляются в коллекцию  Свойств объекта **Connection.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства ADO</p></th>
<th><p>Имя свойства OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Активные сеансы</p></td>
<td><p>DBPROP_ACTIVESESSIONS</p></td>
</tr>
<tr class="even">
<td><p>Asynchable Abort</p></td>
<td><p>DBPROP_ASYNCTXNABORT</p></td>
</tr>
<tr class="odd">
<td><p>Asynchable Commit</p></td>
<td><p>DBPROP_ASYNCTNXCOMMIT</p></td>
</tr>
<tr class="even">
<td><p>Уровни изоляции автокоммита</p></td>
<td><p>DBPROP_SESS_AUTOCOMMITISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Расположение каталога</p></td>
<td><p>DBPROP_CATALOGLOCATION</p></td>
</tr>
<tr class="even">
<td><p>Термин Каталог</p></td>
<td><p>DBPROP_CATALOGTERM</p></td>
</tr>
<tr class="odd">
<td><p>Определение столбцов</p></td>
<td><p>DBPROP_COLUMNDEFINITION</p></td>
</tr>
<tr class="even">
<td><p>Подключение Время от времени</p></td>
<td><p>DBPROP_INIT_TIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Текущий каталог</p></td>
<td><p>DBPROP_CURRENTCATALOG</p></td>
</tr>
<tr class="even">
<td><p>Источник данных</p></td>
<td><p>DBPROP_INIT_DATASOURCE</p></td>
</tr>
<tr class="odd">
<td><p>Имя источника данных</p></td>
<td><p>DBPROP_DATASOURCENAME</p></td>
</tr>
<tr class="even">
<td><p>Модель потоковой обработки объектов источника данных</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Имя DBMS</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="even">
<td><p>Версия DBMS</p></td>
<td><p>DBPROP_DBMSVER</p></td>
</tr>
<tr class="odd">
<td><p>Расширенные свойства</p></td>
<td><p>DBPROP_INIT_PROVIDERSTRING</p></td>
</tr>
<tr class="even">
<td><p>Поддержка GROUP BY</p></td>
<td><p>DBPROP_GROUPBY</p></td>
</tr>
<tr class="odd">
<td><p>Гетерогенная поддержка таблиц</p></td>
<td><p>DBPROP_HETEROGENEOUSTABLES</p></td>
</tr>
<tr class="even">
<td><p>Чувствительность к делу идентификатора</p></td>
<td><p>DBPROP_IDENTIFIERCASE</p></td>
</tr>
<tr class="odd">
<td><p>Начальный каталог</p></td>
<td><p>DBPROP_INIT_CATALOG</p></td>
</tr>
<tr class="even">
<td><p>Уровни изоляции</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Хранение изоляции</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="even">
<td><p>Идентификатор locale</p></td>
<td><p>DBPROP_INIT_LCID</p></td>
</tr>
<tr class="odd">
<td><p>Максимальный размер индекса</p></td>
<td><p>DBPROP_MAXINDEXSIZE</p></td>
</tr>
<tr class="even">
<td><p>Максимальный размер строки</p></td>
<td><p>DBPROP_MAXROWSIZE</p></td>
</tr>
<tr class="odd">
<td><p>Максимальный размер строки включает BLOB</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="even">
<td><p>Максимальные таблицы в SELECT</p></td>
<td><p>DBPROP_MAXTABLESINSELECT</p></td>
</tr>
<tr class="odd">
<td><p>Несколько наборов параметров</p></td>
<td><p>DBPROP_MULTIPLEPARAMSETS</p></td>
</tr>
<tr class="even">
<td><p>Несколько результатов</p></td>
<td><p>DBPROP_MULTIPLERESULTS</p></td>
</tr>
<tr class="odd">
<td><p>Несколько служба хранилища объектов</p></td>
<td><p>DBPROP_MULTIPLESTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Обновление с несколькими таблицами</p></td>
<td><p>DBPROP_MULTITABLEUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Порядок коллансирования NULL</p></td>
<td><p>DBPROP_NULLCOLLATION</p></td>
</tr>
<tr class="even">
<td><p>NULL Concatenation Behaviour</p></td>
<td><p>DBPROP_CONCATNULLBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Версия OLE DB</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="even">
<td><p>Поддержка объектов OLE</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка open Rowset</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="even">
<td><p>ORDER BY Columns in Select List</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="odd">
<td><p>Доступность параметров вывода</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="even">
<td><p>Pass By Ref Accessors</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Сохраняются сведения о безопасности</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="odd">
<td><p>Тип сохраняемого ID</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="even">
<td><p>Подготовка поведения прервать</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Подготовка поведения фиксации</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Термин процедуры</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="odd">
<td><p>Prompt</p></td>
<td><p>DBPROP_INIT_PROMPT</p></td>
</tr>
<tr class="even">
<td><p>Удобное имя поставщика</p></td>
<td><p>DBPROP_PROVIDERFRIENDLYNAME</p></td>
</tr>
<tr class="odd">
<td><p>Имя поставщика</p></td>
<td><p>DBPROP_PROVIDERFILENAME</p></td>
</tr>
<tr class="even">
<td><p>Версия поставщика</p></td>
<td><p>DBPROP_PROVIDERVER</p></td>
</tr>
<tr class="odd">
<td><p>Read-Only источник данных</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="even">
<td><p>Преобразования rowset в командной строке</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="odd">
<td><p>Термин Схемы</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="even">
<td><p>Использование схемы</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>SQL Поддержка</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="even">
<td><p>Структурированные служба хранилища</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка subquery</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="even">
<td><p>Термин Таблица</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="odd">
<td><p>DDL транзакций</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="even">
<td><p>Идентификатор пользователя</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="odd">
<td><p>имя пользователя;</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="even">
<td><p>Ручка окна</p></td>
<td><p>DBPROP_INIT_HWND</p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a>Динамические свойства Recordset

Следующие свойства добавляются в коллекцию Свойств  объекта **Recordset.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства ADO</p></th>
<th><p>Имя свойства OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Порядок доступа</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Блокировка служба хранилища объектов</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Тип закладок</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="even">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="odd">
<td><p>Изменение вставленных строк</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="even">
<td><p>Привилегии столбца</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о наборе столбцов</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Командный выход</p></td>
<td><p>DBPROP_COMMANDTIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Столбец Отсрочка</p></td>
<td><p>DBPROP_DEFERRED</p></td>
</tr>
<tr class="even">
<td><p>Задержка служба хранилища обновлений объектов</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Строки удержания</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsestLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>IRowsetScroll</p></td>
<td><p>DBPROP_IRowsetScroll</p></td>
</tr>
<tr class="even">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="odd">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="even">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="odd">
<td><p>Буквальные закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="even">
<td><p>Удостоверение буквальных строк</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Максимальные открытые строки</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимальное количество ожидающих строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимальные строки</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="even">
<td><p>Детализация уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="odd">
<td><p>Этапы уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="even">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="odd">
<td><p>Видимые изменения других</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Видимые вставки других</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Собственные изменения Видимые</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Собственные вставки Видимые</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Сохранение на abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Сохранение на коммит</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Быстрая перезагрузка</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="even">
<td><p>События для повторного антуламента</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="odd">
<td><p>Удаление удаленных строк</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="even">
<td><p>Отчет о нескольких изменениях</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>Возвращение ожидающих вставок</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об удалении строки</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о первом изменении строки</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о вставке строки</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Привилегии строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о повторной синхронизации строк</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="odd">
<td><p>Модель потоков строки</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об обновлении строки</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о выпуске Rowset</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="even">
<td><p>Прокрутите назад</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Курсор сервера</p></td>
<td><p>DBPROP_SERVERCURSOR</p></td>
</tr>
<tr class="even">
<td><p>Пропустить удаленные закладки</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="odd">
<td><p>Удостоверение Strong Row</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Уникальные строки</p></td>
<td><p>DBPROP_UNIQUEROWS</p></td>
</tr>
<tr class="odd">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Использование закладок</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a>Командные динамические свойства

Следующие свойства добавляются в коллекцию **Свойств** объекта **Command.**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства ADO</p></th>
<th><p>Имя свойства OLE DB</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Порядок доступа</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Базовый путь</p></td>
<td><p>SSPROP_STREAM_BASEPATH</p></td>
</tr>
<tr class="odd">
<td><p>Блокировка служба хранилища объектов</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Тип закладок</p></td>
<td><p>DBPROP_BOOKMARKTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Bookmarkable</p></td>
<td><p>DBPROP_IROWSETLOCATE</p></td>
</tr>
<tr class="even">
<td><p>Изменение вставленных строк</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Привилегии столбца</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о наборе столбцов</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="odd">
<td><p>Тип контента</p></td>
<td><p>SSPROP_STREAM_CONTENTTYPE</p></td>
</tr>
<tr class="even">
<td><p>Автоматическое извлечение cursor</p></td>
<td><p>SSPROP_CURSORAUTOFETCH</p></td>
</tr>
<tr class="odd">
<td><p>Столбец Отсрочка</p></td>
<td><p>DBPROP_DEFERRED</p></td>
</tr>
<tr class="even">
<td><p>Отсрочка подготовки</p></td>
<td><p>SSPROP_DEFERPREPARE</p></td>
</tr>
<tr class="odd">
<td><p>Задержка служба хранилища обновлений объектов</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Fetch Backwards</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Строки удержания</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="even">
<td><p>IAccessor</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="even">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="odd">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="even">
<td><p>IConvertType</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="odd">
<td><p>Immobile Rows</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="even">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="even">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="even">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetResynch</p></td>
<td><p>DBPROP_IRowsetResynch</p></td>
</tr>
<tr class="even">
<td><p>IRowsetScroll</p></td>
<td><p>DBPROP_IRowsetScroll</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Буквальные закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Удостоверение буквальных строк</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Режим блокировки</p></td>
<td><p>DBPROP_LOCKMODE</p></td>
</tr>
<tr class="odd">
<td><p>Максимальные открытые строки</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимальное количество ожидающих строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимальные строки</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="even">
<td><p>Детализация уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="odd">
<td><p>Этапы уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="even">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="odd">
<td><p>Видимые изменения других</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Видимые вставки других</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Свойство коди-ния выходных данных</p></td>
<td><p>DBPROP_OUTPUTENCODING</p></td>
</tr>
<tr class="even">
<td><p>Свойство Поток выходных данных</p></td>
<td><p>DBPROP_OUTPUTSTREAM</p></td>
</tr>
<tr class="odd">
<td><p>Собственные изменения Видимые</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Собственные вставки Видимые</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Сохранение на abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Сохранение на коммит</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Быстрая перезагрузка</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="even">
<td><p>События для повторного антуламента</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="odd">
<td><p>Удаление удаленных строк</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="even">
<td><p>Отчет о нескольких изменениях</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>Возвращение ожидающих вставок</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об удалении строки</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о первом изменении строки</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о вставке строки</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Привилегии строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о повторной синхронизации строк</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="odd">
<td><p>Модель потоков строки</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об обновлении строки</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="even">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о выпуске Rowset</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="even">
<td><p>Прокрутите назад</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Курсор сервера</p></td>
<td><p>DBPROP_SERVERCURSOR</p></td>
</tr>
<tr class="even">
<td><p>Данные сервера на вставке</p></td>
<td><p>DBPROP_SERVERDATAONINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Пропустить удаленные закладки</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="even">
<td><p>Удостоверение Strong Row</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Использование закладок</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Корень XML</p></td>
<td><p>SSPROP_STREAM_XMLROOT</p></td>
</tr>
<tr class="even">
<td><p>XSL</p></td>
<td><p>SSPROP_STREAM_XSL</p></td>
</tr>
</tbody>
</table>


Подробные сведения о реализации и функциональные сведения о поставщике Microsoft SQL Server OLE DB обратитесь к поставщику OLE DB для SQL Server документации в разделе OLE DB SDK MDAC.

