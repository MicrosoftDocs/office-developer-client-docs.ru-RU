---
title: Поставщик Microsoft OLE DB для ODBC
TOCTitle: Microsoft OLE DB Provider for ODBC
ms:assetid: c507567e-5ad1-b32a-f6ad-5ba2c39aa4c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249964(v=office.15)
ms:contentKeyID: 48547602
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4f5ffae4880cadb90f47f1ac348ffc8b3ea58785
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288913"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a>Поставщик Microsoft OLE DB для ODBC

**Область применения**: Access 2013, Office 2013

Для программиста ADO или RDS идеальным был бы мир, в котором каждый источник данных предоставляет интерфейс OLE DB, чтобы ADO мог вызываться непосредственно в источник данных. Несмотря на то, что все больше поставщиков баз данных внедряют интерфейсы OLE DB, некоторые источники данных еще не открыты таким образом. Однако практически все системы DBMS, которые используются сегодня, можно получить доступ через ODBC.

Драйверы ODBC доступны для всех основных DBMS, которые используются сегодня, включая Microsoft SQL Server, Microsoft Access (двигатель базы данных Microsoft Jet) и Microsoft FoxPro, в дополнение к продуктам баз данных, не входим в microsoft, например Oracle.

Поставщик ODBC Майкрософт, однако, позволяет ADO подключаться к любому источнику данных ODBC. Поставщик имеет свободные потоки и включен Юникод.

Поставщик поддерживает транзакции, хотя различные двигатели DBMS предлагают различные типы поддержки транзакций. Например, Microsoft Access поддерживает вложенные транзакции глубиной до пяти уровней.

Это поставщик ADO по умолчанию, и все свойства и методы ADO, зависящие от поставщика, поддерживаются.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к этому поставщику, установите **аргумент Provider=** свойства [ConnectionString:](connectionstring-property-ado.md)

```sql 
 
MSDASQL 
```

Чтение свойства [Provider](provider-property-ado.md) также вернет эту строку.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
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
<td><p>Указывает поставщика OLE DB для ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>DSN</strong></p></td>
<td><p>Указывает имя источника данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UID</strong></p></td>
<td><p>Задает имя пользователя.</p></td>
</tr>
<tr class="even">
<td><p><strong>PWD</strong></p></td>
<td><p>Указывает пароль пользователя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>URL-адрес</strong></p></td>
<td><p>Указывает URL-адрес файла или каталога, опубликованный в веб-папке.</p></td>
</tr>
</tbody>
</table>


Так как это поставщик ADO по умолчанию, если вы не закроет параметр **Provider=** из строки подключения, ADO попытается установить подключение к этому поставщику.

Поставщик не поддерживает какие-либо конкретные параметры подключения в дополнение к параметрам, определенным ADO. Однако поставщик передает диспетчеру драйверов ODBC любые параметры подключения, не относясь к ADO.

Так как можно отменить параметр **Provider,** можно составить строку подключения ADO, идентичную строке подключения ODBC для того же источника данных. Используйте те же имена параметров **(DRIVER=**, **DATABASE=**, **DSN=** и так далее), значения и синтаксис, как при сочинении строки подключения ODBC. Вы можете подключиться к предварительному имени источника данных (DSN) или FileDSN или без него.

**Синтаксис с DSN или FileDSN:**

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

**Синтаксис без подключения к DSN (без DSN):**

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

Если вы используете **DSN** или **FileDSN,** его необходимо определить с помощью администратора источника данных ODBC в панели управления Windows. В Microsoft Windows 2000 г. Администратор ODBC находится под административными средствами. В предыдущих версиях Windows значок администратора ODBC называется **32-битным ODBC** или просто **ODBC**.

В качестве альтернативы настройке **DSN** можно указать драйвер ODBC **(DRIVER=),** например "SQL Server;" имя сервера **(SERVER=);** и имя базы данных **(DATABASE=**).

Вы также можете указать имя учетной записи пользователя **(UID=)** и пароль для учетной записи пользователя **(PWD=)**  в параметрах ODBC или в стандартных параметрах пользователя и пароля, определенных ADO. 

Хотя **определение DSN** уже указывает базу данных, можно указать параметр базы данных в дополнение к   **DSN** для подключения к другой базе данных. Это хорошая идея, чтобы всегда включать *параметр* *базы данных* при использовании **DSN**. Это обеспечит подключение к соответствующей базе данных в том случае, если другой пользователь изменил параметр базы данных по умолчанию с момента последней проверки **определения DSN.**

## <a name="provider-specific-connection-properties"></a>Provider-Specific свойств подключения

Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **Connection.** В следующей таблице перечислены эти свойства с соответствующим именем свойства OLE DB в скобки.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Доступные процедуры<br />
(KAGPROP_ACCESSIBLEPROCEDURES)</p></td>
<td><p>Указывает, имеет ли пользователь доступ к сохраненным процедурам.</p></td>
</tr>
<tr class="even">
<td><p>Доступные таблицы<br />
(KAGPROP_ACCESSIBLETABLES)</p></td>
<td><p>Указывает, имеет ли пользователь разрешение на выполнение заявлений SELECT в таблицах баз данных.</p></td>
</tr>
<tr class="odd">
<td><p>Active Statements<br />
(KAGPROP_ACTIVESTATEMENTS)</p></td>
<td><p>Указывает количество обработок, которые драйвер ODBC может поддерживать в подключении.</p></td>
</tr>
<tr class="even">
<td><p>Имя драйвера<br />
(KAGPROP_DRIVERNAME)</p></td>
<td><p>Указывает имя файла драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Версия драйвера ODBC<br />
(KAGPROP_DRIVERODBCVER)</p></td>
<td><p>Указывает версию ODBC, поддерживаемую этим драйвером.</p></td>
</tr>
<tr class="even">
<td><p>Использование файлов<br />
(KAGPROP_FILEUSAGE)</p></td>
<td><p>Указывает, как драйвер обрабатывает файл в источнике данных; как таблица или каталог.</p></td>
</tr>
<tr class="odd">
<td><p>Как и предложение о побеге<br />
(KAGPROP_LIKEESCAPECLAUSE)</p></td>
<td><p>Указывает, поддерживает ли драйвер определение и использование символа побега для символа процента (%) и подчеркнуть символ (_) в предикате LIKE клаузула WHERE.</p></td>
</tr>
<tr class="even">
<td><p>Max Columns in Group By<br />
(KAGPROP_MAXCOLUMNSINGROUPBY)</p></td>
<td><p>Указывает максимальное количество столбцов, которые могут быть указаны в пункте GROUP BY в заявлении SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Столбцы Max в индексе<br />
(KAGPROP_MAXCOLUMNSININDEX)</p></td>
<td><p>Указывает максимальное количество столбцов, которые можно включить в индекс.</p></td>
</tr>
<tr class="even">
<td><p>Max Columns in Order By<br />
(KAGPROP_MAXCOLUMNSINORDERBY)</p></td>
<td><p>Указывает максимальное количество столбцов, которые могут быть указаны в пункте ORDER BY в заявлении SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Столбцы Max в Выберите<br />
(KAGPROP_MAXCOLUMNSINSELECT)</p></td>
<td><p>Указывает максимальное количество столбцов, которые могут быть указаны в части SELECT в заявлении SELECT.</p></td>
</tr>
<tr class="even">
<td><p>Столбцы Max в таблице<br />
(KAGPROP_MAXCOLUMNSINTABLE)</p></td>
<td><p>Указывает максимальное количество столбцов, разрешенных в таблице.</p></td>
</tr>
<tr class="odd">
<td><p>Числимые функции<br />
(KAGPROP_NUMERICFUNCTIONS)</p></td>
<td><p>Указывает, какие численные функции поддерживаются драйвером ODBC. Список имен функций и связанных значений, используемых в этой битмаске, см. в документации ODBC Appendix E: Scalar Functions.</p></td>
</tr>
<tr class="even">
<td><p>Внешние возможности окружных окружных окруж<br />
(KAGPROP_OJCAPABILITY)</p></td>
<td><p>Указывает типы ВНЕШНИХ ИОИ, поддерживаемые поставщиком.</p></td>
</tr>
<tr class="odd">
<td><p>Внешние присоединяется<br />
(KAGPROP_OUTERJOINS)</p></td>
<td><p>Указывает, поддерживает ли поставщик ВНЕШНИЕ JOINs.</p></td>
</tr>
<tr class="even">
<td><p>Специальные символы<br />
(KAGPROP_SPECIALCHARACTERS)</p></td>
<td><p>Указывает, какие символы имеют особое значение для драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Сохраненные процедуры<br />
(KAGPROP_PROCEDURES)</p></td>
<td><p>Указывает, доступны ли сохраненные процедуры для использования с этим драйвером ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Функции строки<br />
(KAGPROP_STRINGFUNCTIONS)</p></td>
<td><p>Указывает, какие функции строк поддерживаются драйвером ODBC. Список имен функций и связанных значений, используемых в этой битмаске, см. в документации ODBC Appendix E: Scalar Functions.</p></td>
</tr>
<tr class="odd">
<td><p>Функции системы<br />
(KAGPROP_SYSTEMFUNCTIONS)</p></td>
<td><p>Указывает, какие функции системы поддерживаются драйвером ODBC. Список имен функций и связанных значений, используемых в этой битмаске, см. в документации ODBC Appendix E: Scalar Functions.</p></td>
</tr>
<tr class="even">
<td><p>Функции времени и даты<br />
(KAGPROP_TIMEDATEFUNCTIONS)</p></td>
<td><p>Указывает, какие функции времени и даты поддерживаются драйвером ODBC. Список имен функций и связанных значений, используемых в этой битмаске, см. в документации ODBC Appendix E: Scalar Functions.</p></td>
</tr>
<tr class="odd">
<td><p>SQL Поддержка грамматики<br />
(KAGPROP_ODBCSQLCONFORMANCE)</p></td>
<td><p>Указывает грамматику SQL, поддерживаемую драйвером ODBC.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Provider-Specific Recordset и Command Properties

Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию **свойств** объектов **Recordset** и **Command.** В следующей таблице перечислены эти свойства с соответствующим именем свойства OLE DB в скобки.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства</p></th>
<th><p>Description</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Обновления на основе запроса/удаления/вставки<br />
(KAGPROP_QUERYBASEDUPDATES)</p></td>
<td><p>Указывает, можно ли выполнять обновления, удаления и вставки с помощью SQL запросов.</p></td>
</tr>
<tr class="even">
<td><p>Тип конвалюты ODBC<br />
(KAGPROP_CONCURRENCY)</p></td>
<td><p>Указывает метод, используемый для уменьшения потенциальных проблем, вызванных двумя пользователями, пытающихся одновременно получить доступ к данным из источника данных.</p></td>
</tr>
<tr class="odd">
<td><p>Доступность BLOB на Forward-Only курсоре<br />
(KAGPROP_BLOBSONFOCURSOR)</p></td>
<td><p>Указывает, можно ли получить доступ к полям <strong>BLOB</strong> при использовании курсора только для вперед.</p></td>
</tr>
<tr class="even">
<td><p>Включай SQL_FLOAT, SQL_DOUBLE и SQL_REAL в QBU WHERE clauses<br />
(KAGPROP_INCLUDENONEXACT)</p></td>
<td><p>Указывает, можно ли SQL_FLOAT, SQL_DOUBLE и SQL_REAL в положение QBU WHERE.</p></td>
</tr>
<tr class="odd">
<td><p>Положение в последней строке после вставки<br />
(KAGPROP_POSITIONONNEWROW)</p></td>
<td><p>Указывает, что после вставки новой записи в таблицу последняя строка в таблице будет приходить в текущем ряду.</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChangeExtInfo<br />
(KAGPROP_IROWSETCHANGEEXTINFO)</p></td>
<td><p>Указывает, предоставляет ли <strong>интерфейс IRowsetChange</strong> расширенную информационную поддержку.</p></td>
</tr>
<tr class="odd">
<td><p>Тип курсора ODBC<br />
(KAGPROP_CURSOR)</p></td>
<td><p>Указывает тип курсора, используемого в <strong>Recordset.</strong></p></td>
</tr>
<tr class="even">
<td><p>Создание rowset, который можно маршалить<br />
(KAGPROP_MARSHALLABLE)</p></td>
<td><p>Указывает, что драйвер ODBC создает набор записей, который можно</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Командный текст

Использование объекта [Command](command-object-ado.md) во многом зависит от источника данных и типа запроса или командного утверждения, которые он примет.

ODBC предоставляет определенный синтаксис для вызова сохраненных процедур. Для свойства  [CommandText](commandtext-property-ado.md)  объекта *CommandText аргумент CommandText* к [](connection-object-ado.md) методу Execute на объекте  Подключение или аргумент Source к методу Open на [объекте Recordset](recordset-object-ado.md) передается в строке с этим синтаксисом: 

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

**Каждый?** ссылается на объект в коллекции [Параметры.](parameters-collection-ado.md) Первый?  ссылки **Параметры**(0), далее **?** ссылки **Параметры**(1) и так далее.

Ссылки на параметры необязательны и зависят от структуры сохраненной процедуры. Если вы хотите вызвать сохраненную процедуру, которая не определяет параметры, строка будет выглядеть так:

`"{ call procedure }"`

Если у вас есть два параметра запроса, строка будет выглядеть так:

`"{ call procedure ( ?, ? ) }"`

Если сохраненная процедура возвращает значение, возвращаемая величина рассматривается как другой параметр. Если у вас нет параметров запроса, но у вас есть возвращаемая величина, строка будет выглядеть так:

`"{ ? = call procedure }"`

Наконец, если у вас есть значение возврата и два параметра запроса, строка будет выглядеть так:

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a>Поведение наборов записей

В следующих таблицах перечислить стандартные методы и свойства ADO, доступные на **объекте Recordset,** открытом с помощью этого поставщика.

Дополнительные сведения о поведении **Recordset** для конфигурации поставщика запустите метод [Supports](supports-method-ado.md) и введите коллекцию **Свойств** в **наборе Recordset,** чтобы определить, присутствуют ли динамические свойства конкретного поставщика.

Доступность стандартных свойств ADO **Recordset:**

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Свойство</p></th>
<th><p>ForwardOnly</p></th>
<th><p>Динамический</p></th>
<th><p>Keyset</p></th>
<th><p>Статическое</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>недоступно</p></td>
<td><p>недоступно</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>недоступно</p></td>
<td><p>недоступно</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>недоступно</p></td>
<td><p>недоступно</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>недоступен</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>недоступен</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">Состояние</a></p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">Состояние</a></p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
<td><p>read-only</p></td>
</tr>
</tbody>
</table>


Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) являются только для записи, когда ADO используется с версией 1.0 поставщика DB Microsoft OLE для ODBC.

Доступность стандартных методов ADO **Recordset:**

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Метод</p></th>
<th><p>ForwardOnly</p></th>
<th><p>Динамический</p></th>
<th><p>Keyset</p></th>
<th><p>Статическое</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Отмена</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Нет</p></td>
<td><p>Нет</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>Нет</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>Нет</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a>*</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Нет</p></td>
<td><p>Нет</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Поддерживает</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Обновление</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
</tbody>
</table>


\*Не поддерживается для баз данных Microsoft Access.

## <a name="dynamic-properties"></a>Dynamic Properties

Поставщик DB Microsoft OLE для ODBC вставляет несколько динамических свойств в коллекцию **свойств** незапертых объектов [Connection,](connection-object-ado.md) [Recordset](recordset-object-ado.md)и [Command.](command-object-ado.md)

Ниже приведены перекрестные индексы имен ADO и OLE DB для каждого динамического свойства. Ссылка программиста OLE DB относится к имени свойства ADO по термину "Описание". Дополнительные сведения об этих свойствах можно найти в справке программиста OLE DB. Поиск имени свойства OLE DB в Индексе или см. в приложении C: OLE DB Properties.

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
<td><p>Расположение</p></td>
<td><p>DBPROP_INIT_LOCATION</p></td>
</tr>
<tr class="even">
<td><p>Максимальный размер индекса</p></td>
<td><p>DBPROP_MAXINDEXSIZE</p></td>
</tr>
<tr class="odd">
<td><p>Максимальный размер строки</p></td>
<td><p>DBPROP_MAXROWSIZE</p></td>
</tr>
<tr class="even">
<td><p>Максимальный размер строки включает BLOB</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="odd">
<td><p>Максимальные таблицы в SELECT</p></td>
<td><p>DBPROP_MAXTABLESINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Режим</p></td>
<td><p>DBPROP_INIT_MODE</p></td>
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
<td><p>Службы OLE DB</p></td>
<td><p>DBPROP_INIT_OLEDBSERVICES</p></td>
</tr>
<tr class="even">
<td><p>Версия OLE DB</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка объектов OLE</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Поддержка open Rowset</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>ORDER BY Columns in Select List</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Доступность параметров вывода</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Pass By Ref Accessors</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Сохраняются сведения о безопасности</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="even">
<td><p>Тип сохраняемого ID</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Подготовка поведения прервать</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Подготовка поведения фиксации</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Термин процедуры</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="even">
<td><p>Prompt</p></td>
<td><p>DBPROP_INIT_PROMPT</p></td>
</tr>
<tr class="odd">
<td><p>Удобное имя поставщика</p></td>
<td><p>DBPROP_PROVIDERFRIENDLYNAME</p></td>
</tr>
<tr class="even">
<td><p>Имя поставщика</p></td>
<td><p>DBPROP_PROVIDERFILENAME</p></td>
</tr>
<tr class="odd">
<td><p>Версия поставщика</p></td>
<td><p>DBPROP_PROVIDERVER</p></td>
</tr>
<tr class="even">
<td><p>Read-Only источник данных</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="odd">
<td><p>Преобразования rowset в командной строке</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>Термин Схемы</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="odd">
<td><p>Использование схемы</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="even">
<td><p>SQL Поддержка</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>Структурированные служба хранилища</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="even">
<td><p>Поддержка subquery</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="odd">
<td><p>Термин Таблица</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="even">
<td><p>DDL транзакций</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="odd">
<td><p>Идентификатор пользователя</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="even">
<td><p>имя пользователя;</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="odd">
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
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
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
<td><p>Максимальные открытые строки</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное количество ожидающих строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимальные строки</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Детализация уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Этапы уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Собственные изменения Видимые</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Собственные вставки Видимые</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Сохранение на abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Сохранение на коммит</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Быстрая перезагрузка</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>События для повторного антуламента</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Удаление удаленных строк</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Отчет о нескольких изменениях</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Возвращение ожидающих вставок</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об удалении строки</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о первом изменении строки</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о вставке строки</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Привилегии строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о повторной синхронизации строк</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Модель потоков строки</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об обновлении строки</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о выпуске Rowset</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Прокрутите назад</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
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
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
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
<td><p>Максимальные открытые строки</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное количество ожидающих строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимальные строки</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Детализация уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Этапы уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Objects Transacted</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Собственные изменения Видимые</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Собственные вставки Видимые</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Сохранение на abort</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Сохранение на коммит</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Быстрая перезагрузка</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>События для повторного антуламента</p></td>
<td><p>DBPROP_REENTRANTEVENTS</p></td>
</tr>
<tr class="even">
<td><p>Удаление удаленных строк</p></td>
<td><p>DBPROP_REMOVEDELETED</p></td>
</tr>
<tr class="odd">
<td><p>Отчет о нескольких изменениях</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Возвращение ожидающих вставок</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об удалении строки</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о первом изменении строки</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о вставке строки</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Привилегии строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о повторной синхронизации строк</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Модель потоков строки</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об обновлении строки</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Rowset Fetch Position Change Notification</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о выпуске Rowset</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Прокрутите назад</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Пропустить удаленные закладки</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="odd">
<td><p>Удостоверение Strong Row</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Updatability</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Использование закладок</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

Сведения о конкретной реализации и функциональных сведениях о поставщике DB Microsoft OLE для ODBC можно получить в руководстве программиста [OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или в Центре разработчиков [платформы данных.](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017)

