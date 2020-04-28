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

Для программистов ADO или RDS лучше всего один, в котором каждый источник данных предоставляет интерфейс OLE DB, чтобы ADO мог напрямую вызывать источник данных. Несмотря на то, что дополнительные поставщики баз данных реализуют интерфейсы OLE DB, некоторые источники данных пока не предоставляются таким образом. Тем не менее, практически все используемые сегодня системы СУБД можно получить с помощью ODBC.

Драйверы ODBC доступны для всех основных СУБД, используемых в настоящее время, включая Microsoft SQL Server, Microsoft Access (ядро базы данных Microsoft Jet) и Microsoft FoxPro, в дополнение к продуктам баз данных, отличным от Майкрософт, например Oracle.

Тем не менее, поставщик Microsoft ODBC позволяет ADO подключаться к любому источнику данных ODBC. Поставщик доступен для бесплатных потоков и включен Юникод.

Поставщик поддерживает транзакции, хотя различные механизмы СУБД предоставляют различные типы поддержки транзакций. Например, Microsoft Access поддерживает вложенные транзакции вплоть до пяти уровней.

Это поставщик по умолчанию для ADO, а также поддерживаются все свойства и методы, зависящие от поставщика.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к поставщику, присвойте аргументу **provider =** свойства [ConnectionString](connectionstring-property-ado.md) значение:

```sql 
 
MSDASQL 
```

Считывание свойства [provider](provider-property-ado.md) также возвратит эту строку.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```sql 
 
"Provider=MSDASQL;DSN=dsnName;UID=userName;PWD=userPassword;" 
```

Строка состоит из следующих ключевых слов:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Ключевое слово</p></th>
<th><p>Описание</p></th>
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
<td><p><strong>URL</strong></p></td>
<td><p>Указывает URL-адрес файла или каталога, опубликованного в веб-папке.</p></td>
</tr>
</tbody>
</table>


Так как это поставщик по умолчанию для ADO, если вы опустите параметр **provider =** из строки подключения, ADO попытается установить подключение к этому поставщику.

Поставщик не поддерживает никакие особые параметры подключения, кроме тех, которые определены в ADO. Тем не менее, поставщик передаст параметры подключений, не являющихся ADO, в диспетчер драйверов ODBC.

Так как вы можете опустить параметр **provider** , вы можете создать строку подключения ADO, идентичную строке подключения ODBC для одного и того же источника данных. Используйте те же имена параметров (**Driver =**, **Database =**, **DSN =** и т. д.), значения и синтаксис, что и при создании строки подключения ODBC. Можно подключаться к предварительно заданному имени источника данных (DSN) или Филедсн без него.

**Синтаксис с именем DSN или Филедсн:**

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

**Синтаксис без имени DSN (подключение без DSN):**

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

Если вы используете **имя DSN** или **филедсн**, оно должно быть определено администратором источника данных ODBC в панели управления Windows. В Microsoft Windows 2000 администратор ODBC находится в разделе Администрирование. В предыдущих версиях Windows значок администратора ODBC называется **32-разрядным ODBC** или просто **ODBC**.

В качестве альтернативы для установки **DSN**можно указать драйвер ODBC (**Driver =**), например "SQL Server;" имя сервера (**Server =**); и имя базы данных (**Database =**).

Вы также можете указать имя учетной записи пользователя (**UID =**) и пароль для учетной записи пользователя (**PWD =**) в параметрах, ОТносящихся к ODBC, или в стандартных параметрах *пользователя* и *пароля* , определенных в ADO.

Несмотря на то, что определение **DSN** уже определяет *базу данных, можно указать параметр* *базы данных* в дополнение к **имени DSN** для подключения к другой базе данных. Рекомендуется *всегда включать параметр* *Database* при использовании **DSN**. Это обеспечит подключение к соответствующей базе данных в случае, если другой пользователь изменил параметр базы данных по умолчанию после последней проверки определения **DSN** .

## <a name="provider-specific-connection-properties"></a>Свойства подключения, зависящие от поставщика

Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **Connection** . В приведенной ниже таблице указаны эти свойства с соответствующим именем свойства OLE DB в круглых скобках.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Доступные процедуры<br />
(KAGPROP_ACCESSIBLEPROCEDURES)</p></td>
<td><p>Указывает, имеет ли пользователь доступ к хранимым процедурам.</p></td>
</tr>
<tr class="even">
<td><p>Доступные таблицы<br />
(KAGPROP_ACCESSIBLETABLES)</p></td>
<td><p>Указывает, имеет ли пользователь разрешение на выполнение операторов SELECT в таблицах базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Активные операторы<br />
(KAGPROP_ACTIVESTATEMENTS)</p></td>
<td><p>Указывает количество дескрипторов, которые драйвер ODBC может поддерживать для подключения.</p></td>
</tr>
<tr class="even">
<td><p>Имя драйвера<br />
(KAGPROP_DRIVERNAME)</p></td>
<td><p>Указывает имя файла драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Версия ODBC драйвера<br />
(KAGPROP_DRIVERODBCVER)</p></td>
<td><p>Указывает версию ODBC, поддерживаемую драйвером.</p></td>
</tr>
<tr class="even">
<td><p>Использование файла<br />
(KAGPROP_FILEUSAGE)</p></td>
<td><p>Указывает, как драйвер обрабатывает файл в источнике данных; как таблица или как каталог.</p></td>
</tr>
<tr class="odd">
<td><p>Как оператор escape<br />
(KAGPROP_LIKEESCAPECLAUSE)</p></td>
<td><p>Указывает, поддерживает ли драйвер определение и использование escape-символа для знака процента (%) и подчеркнуть символ (_) в предикате LIKE предложения WHERE.</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число столбцов в группе Group By<br />
(KAGPROP_MAXCOLUMNSINGROUPBY)</p></td>
<td><p>Указывает максимальное количество столбцов, которое может быть указано в предложении GROUP BY оператора SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число столбцов в индексе<br />
(KAGPROP_MAXCOLUMNSININDEX)</p></td>
<td><p>Указывает максимальное число столбцов, которые можно включить в индекс.</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число столбцов в упорядочении по<br />
(KAGPROP_MAXCOLUMNSINORDERBY)</p></td>
<td><p>Указывает максимальное количество столбцов, которое может быть указано в предложении ORDER BY оператора SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число столбцов в SELECT<br />
(KAGPROP_MAXCOLUMNSINSELECT)</p></td>
<td><p>Указывает максимальное количество столбцов, которое может быть указано в части SELECT оператора SELECT.</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число столбцов в таблице<br />
(KAGPROP_MAXCOLUMNSINTABLE)</p></td>
<td><p>Указывает максимальное допустимое количество столбцов в таблице.</p></td>
</tr>
<tr class="odd">
<td><p>Числовые функции<br />
(KAGPROP_NUMERICFUNCTIONS)</p></td>
<td><p>Указывает, какие числовые функции поддерживаются драйвером ODBC. Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Возможности внешнего соединения<br />
(KAGPROP_OJCAPABILITY)</p></td>
<td><p>Указывает типы внешних ОБЪЕДИНЕНий, поддерживаемые поставщиком.</p></td>
</tr>
<tr class="odd">
<td><p>Внешние соединения<br />
(KAGPROP_OUTERJOINS)</p></td>
<td><p>Указывает, поддерживает ли поставщик внешние соединения.</p></td>
</tr>
<tr class="even">
<td><p>Специальные символы<br />
(KAGPROP_SPECIALCHARACTERS)</p></td>
<td><p>Указывает, какие символы имеют особое значение для драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Хранимые процедуры<br />
(KAGPROP_PROCEDURES)</p></td>
<td><p>Указывает, доступны ли хранимые процедуры для использования с данным драйвером ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Строковые функции<br />
(KAGPROP_STRINGFUNCTIONS)</p></td>
<td><p>Указывает, какие строковые функции поддерживаются драйвером ODBC. Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Системные функции<br />
(KAGPROP_SYSTEMFUNCTIONS)</p></td>
<td><p>Указывает, какие системные функции поддерживаются драйвером ODBC. Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Функции времени и даты<br />
(KAGPROP_TIMEDATEFUNCTIONS)</p></td>
<td><p>Указывает, какие функции времени и даты поддерживаются драйвером ODBC. Список имен функций и соответствующих значений, используемых в этой битовой маске, приведен в разделе приложение E: скалярные функции в документации ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка грамматики SQL<br />
(KAGPROP_ODBCSQLCONFORMANCE)</p></td>
<td><p>Указывает грамматику SQL, поддерживаемую драйвером ODBC.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Специфические для поставщика наборы записей и свойства команд

Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию **свойств** объекта **Recordset** и **командных** объектов. В приведенной ниже таблице указаны эти свойства с соответствующим именем свойства OLE DB в круглых скобках.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя свойства</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Обновления, операции удаления и вставки на основе запросов<br />
(KAGPROP_QUERYBASEDUPDATES)</p></td>
<td><p>Указывает, можно ли выполнять операции обновления, удаления и вставки с помощью запросов SQL.</p></td>
</tr>
<tr class="even">
<td><p>Тип параллелизма ODBC<br />
(KAGPROP_CONCURRENCY)</p></td>
<td><p>Указывает метод, используемый для сокращения возможных проблем, вызванных двумя пользователями, пытающимися одновременно получить доступ к одним и тем же данным из источника данных.</p></td>
</tr>
<tr class="odd">
<td><p>Доступность BLOB-объектов для однонаправленного курсора<br />
(KAGPROP_BLOBSONFOCURSOR)</p></td>
<td><p>Указывает, можно ли получить доступ к <strong>полям</strong> BLOB при использовании однонаправленного курсора.</p></td>
</tr>
<tr class="even">
<td><p>Включает SQL_FLOAT, SQL_DOUBLE и SQL_REAL в КБУ, где предложения WHERE<br />
(KAGPROP_INCLUDENONEXACT)</p></td>
<td><p>Указывает, могут ли значения SQL_FLOAT, SQL_DOUBLE и SQL_REAL включаться в предложение WHERE КБУ.</p></td>
</tr>
<tr class="odd">
<td><p>Положение в последней строке после вставки<br />
(KAGPROP_POSITIONONNEWROW)</p></td>
<td><p>Указывает, что после вставки новой записи в таблицу текущая строка будет получена из последней строки таблицы.</p></td>
</tr>
<tr class="even">
<td><p>ировсетчанжеекстинфо<br />
(KAGPROP_IROWSETCHANGEEXTINFO)</p></td>
<td><p>Указывает, предоставляет ли интерфейс <strong>ировсетчанже</strong> расширенную поддержку информации.</p></td>
</tr>
<tr class="odd">
<td><p>Тип курсора ODBC<br />
(KAGPROP_CURSOR)</p></td>
<td><p>Указывает тип курсора, используемого в объекте <strong>Recordset</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Создание набора строк, который может быть маршалирован<br />
(KAGPROP_MARSHALLABLE)</p></td>
<td><p>Указывает, что драйвер ODBC создает объект Recordset, который может быть маршалирован</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Текст команды

Способ использования объекта [Command](command-object-ado.md) во многом зависит от источника данных, а также от того, какой тип запроса или оператора команды будет принимать.

ODBC предоставляет специальный синтаксис для вызова хранимых процедур. Для свойства [CommandText](commandtext-property-ado.md) объекта **Command** , аргумент *CommandText* для метода **EXECUTE** объекта [Connection](connection-object-ado.md) или аргумента *Source* для метода **Open** объекта [Recordset](recordset-object-ado.md) , передается в строку с помощью следующего синтаксиса:

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

Каждый **из** них ссылается на объект в коллекции [Parameters](parameters-collection-ado.md) . Первый **?** **Параметры**References (0), следующие **?** ссылки на **Параметры**(1) и т. д.

Ссылки на параметры являются необязательными и зависят от структуры хранимой процедуры. Если вы хотите вызвать хранимую процедуру, которая не определяет параметры, строка будет выглядеть следующим образом:

`"{ call procedure }"`

Если у вас есть два параметра запроса, строка будет выглядеть следующим образом:

`"{ call procedure ( ?, ? ) }"`

Если хранимая процедура будет возвращать значение, возвращаемое значение будет считаться другим параметром. Если у вас нет параметров запроса, но у вас есть возвращаемое значение, строка будет выглядеть следующим образом:

`"{ ? = call procedure }"`

Наконец, если у вас есть возвращаемое значение и два параметра запроса, строка будет выглядеть следующим образом:

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a>Поведение набора записей

В следующих таблицах перечислены стандартные методы и свойства ADO, доступные для объекта **Recordset** , открытого с помощью этого поставщика.

Для получения более подробных сведений о поведении **набора записей** для конфигурации поставщика [запустите метод](supports-method-ado.md) Supports и перечислите коллекцию **свойств** объекта **Recordset** , чтобы определить, присутствуют ли динамические свойства, зависящие от поставщика.

Доступность стандартных свойств **записей** ADO:

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
<th><p>форвардонли</p></th>
<th><p>Динамическая группа</p></th>
<th><p>Keyset</p></th>
<th><p>Static</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>недоступно</p></td>
<td><p>недоступно</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>недоступно</p></td>
<td><p>недоступно</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>недоступно</p></td>
<td><p>недоступно</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="even">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>недоступен</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>недоступен</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><a href="status-property-ado-recordset.md">Состояние</a></p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
</tr>
</tbody>
</table>


Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) доступны только для записи при использовании ADO с поставщиком Microsoft OLE DB для ODBC версии 1,0.

Доступность стандартных методов **набора записей** ADO:

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
<th><p>Method</p></th>
<th><p>форвардонли</p></th>
<th><p>Динамическая группа</p></th>
<th><p>Keyset</p></th>
<th><p>Static</p></th>
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
<td><p><a href="delete-method-ado-recordset.md">удаление</a>;</p></td>
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
<td><p><a href="supports-method-ado.md">Имеется</a></p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">обновление</a>.</p></td>
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

## <a name="dynamic-properties"></a>Динамические свойства

Поставщик Microsoft OLE DB для ODBC вставляет несколько динамических свойств в коллекцию **свойств** неоткрытых [подключений](connection-object-ado.md), [наборов записей](recordset-object-ado.md)и [командных](command-object-ado.md) объектов.

В приведенных ниже таблицах указаны перекрестные индексы имен ADO и OLE DB для каждого динамического свойства. Справочник программиста OLE DB ссылается на имя свойства ADO по термину "Описание". Дополнительные сведения об этих свойствах можно найти в справочнике программиста по OLE DB. Выполните поиск по имени свойства OLE DB в индексе или в разделе приложение C: свойства OLE DB.

## <a name="connection-dynamic-properties"></a>Динамические свойства подключения

Следующие свойства добавляются в коллекцию **свойств** объекта **Connection** .

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
<td><p>Асинчабле Abort</p></td>
<td><p>DBPROP_ASYNCTXNABORT</p></td>
</tr>
<tr class="odd">
<td><p>Фиксация асинчабле</p></td>
<td><p>DBPROP_ASYNCTNXCOMMIT</p></td>
</tr>
<tr class="even">
<td><p>Уровни изоляции для автоматической фиксации</p></td>
<td><p>DBPROP_SESS_AUTOCOMMITISOLEVELS</p></td>
</tr>
<tr class="odd">
<td><p>Расположение каталога</p></td>
<td><p>DBPROP_CATALOGLOCATION</p></td>
</tr>
<tr class="even">
<td><p>Термин каталога</p></td>
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
<td><p>Модель потоков объектов источника данных</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Имя СУБД</p></td>
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
<td><p>ГРУППИРОВКа по поддержке</p></td>
<td><p>DBPROP_GROUPBY</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка гетерогенных таблиц</p></td>
<td><p>DBPROP_HETEROGENEOUSTABLES</p></td>
</tr>
<tr class="even">
<td><p>Чувствительность к регистру идентификаторов</p></td>
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
<td><p>Идентификатор языкового стандарта</p></td>
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
<td><p>Максимальный размер строки включает большой двоичный объект</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число таблиц в SELECT</p></td>
<td><p>DBPROP_MAXTABLESINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Режим</p></td>
<td><p>DBPROP_INIT_MODE</p></td>
</tr>
<tr class="odd">
<td><p>Наборы параметров с несколькими параметрами</p></td>
<td><p>DBPROP_MULTIPLEPARAMSETS</p></td>
</tr>
<tr class="even">
<td><p>Несколько результатов</p></td>
<td><p>DBPROP_MULTIPLERESULTS</p></td>
</tr>
<tr class="odd">
<td><p>Несколько объектов хранилища</p></td>
<td><p>DBPROP_MULTIPLESTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Обновление с несколькими таблицами</p></td>
<td><p>DBPROP_MULTITABLEUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Порядок сортировки NULL</p></td>
<td><p>DBPROP_NULLCOLLATION</p></td>
</tr>
<tr class="even">
<td><p>Поведение сцепления со значением NULL</p></td>
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
<td><p>Поддержка открытых наборов строк</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>УПОРЯДОЧЕНие по столбцам в списке выборки</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Доступность выходного параметра</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Передача по параметрам доступа ref</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Сохранение сведений о безопасности</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="even">
<td><p>Тип постоянного идентификатора</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Действие по подготовке к прерыванию</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Подготовка режима фиксации</p></td>
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
<td><p>Понятное имя поставщика</p></td>
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
<td><p>Источник данных, предназначенный только для чтения</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="odd">
<td><p>Преобразования наборов строк для команды</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>Термин схемы</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="odd">
<td><p>Использование схемы</p></td>
<td><p>DBPROP_SCHEMAUSAGE</p></td>
</tr>
<tr class="even">
<td><p>Поддержка SQL</p></td>
<td><p>DBPROP_SQLSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>Структурированное хранилище</p></td>
<td><p>DBPROP_STRUCTUREDSTORAGE</p></td>
</tr>
<tr class="even">
<td><p>Поддержка вложенных запросов</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="odd">
<td><p>Табличный термин</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="even">
<td><p>DDL транзакции</p></td>
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
<td><p>Дескриптор окна</p></td>
<td><p>DBPROP_INIT_HWND</p></td>
</tr>
</tbody>
</table>


## <a name="recordset-dynamic-properties"></a>Динамические свойства Recordset

Следующие свойства добавляются в коллекцию **свойств** объекта **Recordset** .

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
<td><p>Права на столбцы</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о наборе столбцов</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Откладывание обновлений объектов хранилища</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Извлечение назад</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Удержание строк</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>иакцессор</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>иколумнсинфо</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>иколумнсровсет</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>иконнектионпоинтконтаинер</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>иконверттипе</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Строки для мобильных устройств</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>ировсетчанже</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>ировсетидентити</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>ировсетинфо</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>ировсетлокате</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>ировсетресинч</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ировсетупдате</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>исекуентиалстреам</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>исуппортерроринфо</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Литеральные закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Идентификация строк литералов</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число открытых строк</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число ожидающих строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число строк</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Детализация уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Этапы уведомления</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Объекты, транзакционные</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Видны изменения</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Отображение собственных вставок</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Сохранение при прерывании</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Сохранение при фиксации</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Быстрый перезапуск</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Повторные события</p></td>
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
<td><p>Возврат ожидающих вставок</p></td>
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
<td><p>Уведомление о вставке строк</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Права на строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о повторной синхронизации строк</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Потоковая модель для строк</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене изменения строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о отмене удаления строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене вставки строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об обновлении строк</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об изменении положения при получении набора строк</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSISIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о выпуске набора строк</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Прокрутка назад</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Пропуск удаленных закладок</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="odd">
<td><p>Строгая идентификация строк</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Уникальные строки</p></td>
<td><p>DBPROP_UNIQUEROWS</p></td>
</tr>
<tr class="odd">
<td><p>Обновление</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Использование закладок</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="command-dynamic-properties"></a>Динамические свойства команд

Указанные ниже свойства добавляются в коллекцию **свойств** **командного** объекта.

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
<td><p>Права на столбцы</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о наборе столбцов</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="even">
<td><p>Откладывание обновлений объектов хранилища</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Извлечение назад</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Удержание строк</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>иакцессор</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="even">
<td><p>иколумнсинфо</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="odd">
<td><p>иколумнсровсет</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="even">
<td><p>иконнектионпоинтконтаинер</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="odd">
<td><p>иконверттипе</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="even">
<td><p>Строки для мобильных устройств</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="odd">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="even">
<td><p>ировсетчанже</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="odd">
<td><p>ировсетидентити</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="even">
<td><p>ировсетинфо</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="odd">
<td><p>ировсетлокате</p></td>
<td><p>DBPROP_IRowsetLocate</p></td>
</tr>
<tr class="even">
<td><p>ировсетресинч</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ировсетупдате</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="even">
<td><p>исекуентиалстреам</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="odd">
<td><p>исуппортерроринфо</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="even">
<td><p>Литеральные закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Идентификация строк литералов</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число открытых строк</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число ожидающих строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число строк</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Детализация уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Этапы уведомления</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Объекты, транзакционные</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Видны изменения</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Отображение собственных вставок</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Сохранение при прерывании</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Сохранение при фиксации</p></td>
<td><p>DBPROP_COMMITPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Быстрый перезапуск</p></td>
<td><p>DBPROP_QUICKRESTART</p></td>
</tr>
<tr class="odd">
<td><p>Повторные события</p></td>
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
<td><p>Возврат ожидающих вставок</p></td>
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
<td><p>Уведомление о вставке строк</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Права на строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о повторной синхронизации строк</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Потоковая модель для строк</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене изменения строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о отмене удаления строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об отмене вставки строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об обновлении строк</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об изменении положения при получении набора строк</p></td>
<td><p>DBPROP_NOTIFYROWSETFETCHPOSITIONCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о выпуске набора строк</p></td>
<td><p>DBPROP_NOTIFYROWSETRELEASE</p></td>
</tr>
<tr class="odd">
<td><p>Прокрутка назад</p></td>
<td><p>DBPROP_CANSCROLLBACKWARDS</p></td>
</tr>
<tr class="even">
<td><p>Пропуск удаленных закладок</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="odd">
<td><p>Строгая идентификация строк</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Обновление</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Использование закладок</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

Сведения о конкретных реализациях и функциональных сведениях о поставщике Microsoft OLE DB для ODBC можно найти в [руководстве программиста по OLE DB](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или посетить [Центр разработчиков платформы данных](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).

