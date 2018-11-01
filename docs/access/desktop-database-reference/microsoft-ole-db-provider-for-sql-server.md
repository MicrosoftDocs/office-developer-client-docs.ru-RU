---
title: Поставщик Microsoft OLE DB для SQL Server
TOCTitle: Microsoft OLE DB Provider for SQL Server
ms:assetid: 0ffdea03-1a76-499b-f649-423f6b3c13d7
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248868(v=office.15)
ms:contentKeyID: 48543282
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c856b2ba8d39c9cfc03bdadd6250ee9411b9c9c8
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25883892"
---
# <a name="microsoft-ole-db-provider-for-sql-server"></a>Поставщик Microsoft OLE DB для SQL Server


**Применимо к**: Access 2013, Office 2013

Поставщик Microsoft OLE DB для SQL Server, SQLOLEDB, позволяет ADO для доступа к Microsoft SQL Server.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Для подключения к данным поставщиком аргументе *поставщика* свойство [ConnectionString](connectionstring-property-ado.md) для:

```sql 
 
SQLOLEDB 
```

Это значение может быть задана или ознакомьтесь с помощью свойства [поставщика](provider-property-ado.md) .

## <a name="typical-connection-string"></a>Типичная строка подключения

— Это строка соединения для данного поставщика:

```sql 
 
"Provider=SQLOLEDB;Data Source=serverName;" 
Initial Catalog=databaseName; 
User ID=userName;Password=userPassword;" 
```

Строка состоит из следующих ключевых слов:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Keyword</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Поставщик</strong></p></td>
<td><p>Задает поставщика OLE DB для SQL Server.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong> или <strong>сервера</strong></p></td>
<td><p>Указывает имя сервера.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Исходный каталог</strong> или <strong>База данных</strong></p></td>
<td><p>Указывает имя базы данных на сервере.</p></td>
</tr>
<tr class="even">
<td><p><strong>Идентификатор пользователя</strong> или <strong>ИД пользователя</strong></p></td>
<td><p>Задает имя пользователя (для проверки подлинности SQL Server).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Пароль</strong> или <strong>pwd</strong></p></td>
<td><p>Задает пароль пользователя (для проверки подлинности SQL Server).</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Параметры подключения от поставщика

Поставщик поддерживает несколько параметров подключения для конкретного поставщика дополнение к тем определяется ADO. Как и в случае с помощью свойства подключения ADO, эти свойства от поставщика можно задать с помощью коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или можно задать как часть **ConnectionString**.

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
<td><p>Указывает режим проверки подлинности пользователя. Это может быть значение <strong>Да</strong> или <strong>Нет</strong>. Значение по умолчанию — <strong>Нет</strong>. Если это свойство имеет значение <strong>Да</strong>, SQLOLEDB использует режим проверки подлинности Microsoft Windows NT для авторизации доступа пользователей к базе данных SQL Server, заданные значения свойств <strong>расположение</strong> и <a href="datasource-property-ado.md">источника данных</a> . Если задано значение <strong>No</strong>, SQLOLEDB использует смешанный режим для авторизации доступа пользователей к базе данных SQL Server. Имя пользователя SQL Server и пароль указанных в свойствах <strong>Идентификатор пользователя</strong> и <strong>пароль</strong> .</p></td>
</tr>
<tr class="even">
<td><p>Текущий язык</p></td>
<td><p>Указывает имя языка SQL Server. Определяет язык, используемый для выбора сообщения системы и форматирование. Язык должны быть установлены на SQL Server, в противном случае — открытие подключение завершится с ошибкой.</p></td>
</tr>
<tr class="odd">
<td><p>Адрес сети</p></td>
<td><p>Указывает адрес сети SQL Server, заданного в свойстве <strong>расположение</strong> .</p></td>
</tr>
<tr class="even">
<td><p>Сетевой библиотеки</p></td>
<td><p>Указывает имя библиотеки сети (библиотеки динамической компоновки), используемое для взаимодействия с SQL Server. Имя не должно содержать путь или расширение имени файла библиотеки DLL. Значение по умолчанию, предоставленные конфигурация клиента SQL Server.</p></td>
</tr>
<tr class="odd">
<td><p>Используйте процедуру для подготовки</p></td>
<td><p>Определяет, будет ли SQL Server создает временные хранимые процедуры, когда команды подготавливаются (свойством <strong>подготовленных</strong> ).</p></td>
</tr>
<tr class="even">
<td><p>Переводить Auto</p></td>
<td><p>Указывает необходимость преобразования символов OEM или ANSI. Это свойство может иметь значение <strong>True</strong> или <strong>False</strong>. Значение по умолчанию — <strong>True</strong>. Если этому свойству присвоено <strong>значение True</strong>, SQLOLEDB выполняет преобразование символов OEM или ANSI при строк символов нескольких байтов извлекается из или отправленные к серверу SQL Server. Если этому свойству присвоено <strong>значение False</strong>, затем SQLOLEDB не выполняет преобразование символов OEM или ANSI на символ нескольких байтов строковых данных.</p></td>
</tr>
<tr class="odd">
<td><p>Размер пакета</p></td>
<td><p>Указывает размер сетевого пакета в байтах. Значение свойства размера пакета должно быть от 512 до 32 767. Размер пакета сети SQLOLEDB по умолчанию — 4096.</p></td>
</tr>
<tr class="even">
<td><p>Имя приложения</p></td>
<td><p>Указывает имя клиентского приложения.</p></td>
</tr>
<tr class="odd">
<td><p>Идентификатор рабочей станции</p></td>
<td><p>Строка, идентифицирующая рабочей станции.</p></td>
</tr>
</tbody>
</table>


## <a name="command-object-usage"></a>Использование объекта команды

SQLOLEDB принимает сочетание ODBC, ANSI и Transact-SQL, относящиеся к SQL Server в качестве допустимого синтаксиса. К примеру следующей инструкции SQL использует escape-последовательности ODBC SQL для указания функция LCASE string:

```sql 
 
SELECT customerid={fn LCASE(CustomerID)} FROM Customers 
```

LCASE возвращает строку символов, преобразование все прописные буквы в нижнем регистре эквиваленты. Функция string ANSI SQL НИЖНЕМ выполняет одной и той же операции, поэтому следующей инструкции SQL — это эквивалентно оператор ODBC, представленному выше ANSI:

```sql
 
SELECT customerid=LOWER(CustomerID) FROM Customers 
```

SQLOLEDB успешно обрабатывает в любом из оператора, когда он указан как текст для команды.

## <a name="stored-procedures"></a>Хранимые процедуры

При выполнении SQL Server хранимой процедуры с помощью команды SQLOLEDB, используйте escape-последовательность вызовов ODBC процедуры в текст команды. SQLOLEDB затем использует механизм вызова удаленной процедуры из SQL Server для оптимизации обработки команд. К примеру следующей инструкции ODBC SQL окончена текст предпочитаемый команды формы Transact-SQL:

## <a name="odbc-sql"></a>ODBC SQL

```sql 
 
{call SalesByCategory('Produce', '1995')} 
```

## <a name="transact-sql"></a>Transact-SQL

```sql 
 
EXECUTE SalesByCategory 'Produce', '1995' 
```

## <a name="recordset-behavior"></a>Поведение набора записей

SQLOLEDB нельзя использовать курсоры SQL Server для поддержки нескольких результатов, созданных функцией многие команды. Потребитель запрашивает записей, требуя поддержки курсора SQL Server, если используется текст команды создает более чем одного набора записей в результате возникает ошибка.

Прокручиваемой наборов записей SQLOLEDB поддерживаемых курсоров SQL Server. SQL Server, задает ограничения на курсоров, зависит от изменения, внесенные другими пользователями базы данных. В частности строки в некоторые курсоры не могут быть упорядочены и попытка создания набора записей с помощью команды, содержащий предложение SQL ORDER BY может не работать.

## <a name="dynamic-properties"></a>Динамические свойства

Поставщик Microsoft OLE DB для SQL Server вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .

Следующие таблицы не cross-index имен ADO и OLE DB для каждого динамического свойства. Справочник программиста OLE DB указано имя свойства ADO по слову «Описание». Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB. Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.

## <a name="connection-dynamic-properties"></a>Динамические свойства подключения

Коллекция **Properties** объект **подключения** добавляются следующие свойства.

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
<td><p>Активных сеансов</p></td>
<td><p>DBPROP_ACTIVESESSIONS</p></td>
</tr>
<tr class="even">
<td><p>Прерывание Asynchable</p></td>
<td><p>DBPROP_ASYNCTXNABORT</p></td>
</tr>
<tr class="odd">
<td><p>Зафиксировать Asynchable</p></td>
<td><p>DBPROP_ASYNCTNXCOMMIT</p></td>
</tr>
<tr class="even">
<td><p>Уровни изоляции автоматической фиксации</p></td>
<td><p>DBPROP_SESS_AUTOCOMMITISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Расположение каталога</p></td>
<td><p>DBPROP_CATALOGLOCATION</p></td>
</tr>
<tr class="even">
<td><p>Каталог терминов</p></td>
<td><p>DBPROP_CATALOGTERM</p></td>
</tr>
<tr class="odd">
<td><p>Определение столбца</p></td>
<td><p>DBPROP_COLUMNDEFINITION</p></td>
</tr>
<tr class="even">
<td><p>Время ожидания подключения</p></td>
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
<td><p>Модель потоков объекта источника данных</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Имя СУБД</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="even">
<td><p>Версия СУБД</p></td>
<td><p>DBPROP_DBMSVER</p></td>
</tr>
<tr class="odd">
<td><p>Расширенные свойства</p></td>
<td><p>DBPROP_INIT_PROVIDERSTRING</p></td>
</tr>
<tr class="even">
<td><p>ГРУППИРОВКА по поддержке</p></td>
<td><p>DBPROP_GROUPBY</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка разнородных таблиц</p></td>
<td><p>DBPROP_HETEROGENEOUSTABLES</p></td>
</tr>
<tr class="even">
<td><p>Идентификатор регистра</p></td>
<td><p>DBPROP_IDENTIFIERCASE</p></td>
</tr>
<tr class="odd">
<td><p>Исходный каталог</p></td>
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
<td><p>Идентификатор языка</p></td>
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
<td><p>Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="even">
<td><p>Максимальная таблиц в Выбор</p></td>
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
<td><p>Несколько объектов хранения</p></td>
<td><p>DBPROP_MULTIPLESTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Обновление нескольких таблицы</p></td>
<td><p>DBPROP_MULTITABLEUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Порядок сортировки значений NULL</p></td>
<td><p>DBPROP_NULLCOLLATION</p></td>
</tr>
<tr class="even">
<td><p>Поведение NULL объединения</p></td>
<td><p>DBPROP_CONCATNULLBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Версия OLE DB</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="even">
<td><p>Поддержка OLE-объектов</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка открытых наборов строк</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="even">
<td><p>ORDER BY столбцы в списке Select</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="odd">
<td><p>Выходной параметр доступности</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="even">
<td><p>Передайте с указанные методы</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Пароль</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Сохранять сведения о безопасности</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="odd">
<td><p>Тип сохраняемого идентификатора</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="even">
<td><p>Подготовка поведение аварийное завершение</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Подготовка поведение выделения</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Процедура терминов</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="odd">
<td><p>Запрос</p></td>
<td><p>DBPROP_INIT_PROMPT</p></td>
</tr>
<tr class="even">
<td><p>Понятное имя поставщика</p></td>
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
<td><p>Источник данных только для чтения</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="even">
<td><p>Преобразование строк на команду</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="odd">
<td><p>Схема терминов</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="even">
<td><p>Об использовании схемы</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка SQL</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="even">
<td><p>Структурированное хранилище</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка вложенного запроса</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="even">
<td><p>В таблице терминов</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="odd">
<td><p>Транзакций DDL</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="even">
<td><p>Идентификатор пользователя</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="odd">
<td><p>Имя пользователя</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="even">
<td><p>Дескриптор окна</p></td>
<td><p>DBPROP_INIT_HWND</p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a>Свойства динамической набора записей

Следующие свойства добавляются в коллекцию **свойств** объекта **набора записей** .

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
<td><p>Блокировка объектов хранилища</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Тип закладки</p></td>
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
<td><p>Права доступа столбца</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Столбец набор уведомлений</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Время ожидания команды</p></td>
<td><p>DBPROP_COMMANDTIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Отложите столбца</p></td>
<td><p>DBPROP_DEFERRED</p></td>
</tr>
<tr class="even">
<td><p>Отложенное обновление объекта хранения</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Выборку</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Хранение строк</p></td>
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
<td><p>Немобильные строки</p></td>
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
<td><p>Литерал закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="even">
<td><p>Удостоверение литерала строки</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число открытых строк</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимум ожидающие строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число строк</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="even">
<td><p>Степень детализации уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="odd">
<td><p>Этапы уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="even">
<td><p>Объекты в транзакции</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="odd">
<td><p>Видны прочие изменения</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Других пользователей вставки видимым</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Видны собственные изменения</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Видны собственные операции вставки</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Сохранять при аварийном завершении</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Сохранять при фиксации</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Быстрый перезапуск</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="even">
<td><p>Повторные события</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="odd">
<td><p>Удаление удаленных строк</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="even">
<td><p>Сообщить о нескольких изменений</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>Вернуть ожидающие вставки</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="even">
<td><p>Удалить строку уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Строка первого уведомления об изменении</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Строка вставки уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Привилегии строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Уведомления о повторной синхронизации строки</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="odd">
<td><p>Строка, потоковой модели</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об изменении отмены строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Строка отмены Delete уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>Вставка отмены строки уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об обновлении строки</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об изменении положения строк выборки</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о выпуске набора строк</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="even">
<td><p>Прокрутка назад</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Серверный курсор</p></td>
<td><p>DBPROP_SERVERCURSOR</p></td>
</tr>
<tr class="even">
<td><p>Пропустить удаленных закладки</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="odd">
<td><p>Строка строгого удостоверений</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Уникальные строки</p></td>
<td><p>DBPROP_UNIQUEROWS</p></td>
</tr>
<tr class="odd">
<td><p>Возможности обновления</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Использование закладок</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a>Динамические свойства команды

Следующие свойства добавляются в коллекцию **свойств** объекта **команды** .

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
<td><p>Блокировка объектов хранилища</p></td>
<td><p>DBPROP_BLOCKINGSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Тип закладки</p></td>
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
<td><p>Права доступа столбца</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Столбец набор уведомлений</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="odd">
<td><p>Тип контента</p></td>
<td><p>SSPROP_STREAM_CONTENTTYPE</p></td>
</tr>
<tr class="even">
<td><p>Автоматическая выборка курсора</p></td>
<td><p>SSPROP_CURSORAUTOFETCH</p></td>
</tr>
<tr class="odd">
<td><p>Отложите столбца</p></td>
<td><p>DBPROP_DEFERRED</p></td>
</tr>
<tr class="even">
<td><p>Отложите Подготовка</p></td>
<td><p>SSPROP_DEFERPREPARE</p></td>
</tr>
<tr class="odd">
<td><p>Отложенное обновление объекта хранения</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Выборку</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Хранение строк</p></td>
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
<td><p>Немобильные строки</p></td>
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
<td><p>Литерал закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Удостоверение литерала строки</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Режим блокировки</p></td>
<td><p>DBPROP_LOCKMODE</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число открытых строк</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимум ожидающие строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число строк</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="even">
<td><p>Степень детализации уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="odd">
<td><p>Этапы уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="even">
<td><p>Объекты в транзакции</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="odd">
<td><p>Видны прочие изменения</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Других пользователей вставки видимым</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Свойство кодировки выходных данных</p></td>
<td><p>DBPROP_OUTPUTENCODING</p></td>
</tr>
<tr class="even">
<td><p>Свойство потока выходных данных</p></td>
<td><p>DBPROP_OUTPUTSTREAM</p></td>
</tr>
<tr class="odd">
<td><p>Видны собственные изменения</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Видны собственные операции вставки</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Сохранять при аварийном завершении</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Сохранять при фиксации</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Быстрый перезапуск</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="even">
<td><p>Повторные события</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="odd">
<td><p>Удаление удаленных строк</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="even">
<td><p>Сообщить о нескольких изменений</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>Вернуть ожидающие вставки</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="even">
<td><p>Удалить строку уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Строка первого уведомления об изменении</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Строка вставки уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Привилегии строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Уведомления о повторной синхронизации строки</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="odd">
<td><p>Строка, потоковой модели</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об изменении отмены строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Строка отмены Delete уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>Вставка отмены строки уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об обновлении строки</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об изменении положения строк выборки</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о выпуске набора строк</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="even">
<td><p>Прокрутка назад</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Серверный курсор</p></td>
<td><p>DBPROP_SERVERCURSOR</p></td>
</tr>
<tr class="even">
<td><p>Вставка данных сервера</p></td>
<td><p>DBPROP_SERVERDATAONINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Пропустить удаленных закладки</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="even">
<td><p>Строка строгого удостоверений</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Возможности обновления</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Использование закладок</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Корневой XML</p></td>
<td><p>SSPROP_STREAM_XMLROOT</p></td>
</tr>
<tr class="even">
<td><p>XSL</p></td>
<td><p>SSPROP_STREAM_XSL</p></td>
</tr>
</tbody>
</table>


Сведения о реализации и функциональным сведений о Microsoft SQL Server поставщик OLE DB можно найти поставщика OLE DB для документации по SQL Server в разделе OLE DB MDAC SDK.

