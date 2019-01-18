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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704562"
---
# <a name="microsoft-ole-db-provider-for-odbc"></a>Поставщик Microsoft OLE DB для ODBC

**Применимо к**: Access 2013, Office 2013

Чтобы программист ADO или служб удаленных рабочих СТОЛОВ идеальном мире бы одно в каждом данных источника предоставляет интерфейс OLE DB, чтобы вызвать непосредственно в источник данных ADO. Несмотря на то, что все больше дополнительные базы данных поставщиков реализует интерфейсы OLE DB, некоторые источники данных не еще не представленных таким способом. Тем не менее практически все СУБД в настоящее время может осуществляться через ODBC.

Драйверы ODBC доступны для всех основных СУБД, в настоящее время, включая Microsoft SQL Server, Microsoft Access (базы данных Microsoft Jet) и Microsoft FoxPro, кроме базы данных сторонних продуктов, таких как Oracle.

Поставщик ODBC Microsoft, однако позволяет ADO для подключения к источникам данных ODBC. Поставщик свободных потоков и Юникод.

Поставщик поддерживает транзакции, несмотря на то, что разные ядра СУБД предлагают различные виды поддержки транзакций. Например Microsoft Access поддерживает до пяти уровней вложенных транзакций.

Поставщик по умолчанию для ADO и поддерживаются все зависящие от поставщика ADO свойства и методы.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Для подключения к данным поставщиком, задайте **поставщика =** аргумент свойства [ConnectionString](connectionstring-property-ado.md) для:

```sql 
 
MSDASQL 
```

Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.

## <a name="typical-connection-string"></a>Типичная строка подключения

— Это строка соединения для данного поставщика:

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
<th><p>Keyword</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Поставщик</strong></p></td>
<td><p>Задает поставщика OLE DB для ODBC.</p></td>
</tr>
<tr class="even">
<td><p><strong>УВЕДОМЛЕНИЯ О ДОСТАВКЕ</strong></p></td>
<td><p>Указывает имя источника данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UID</strong></p></td>
<td><p>Задает имя пользователя.</p></td>
</tr>
<tr class="even">
<td><p><strong>PWD</strong></p></td>
<td><p>Задает пароль пользователя.</p></td>
</tr>
<tr class="odd">
<td><p><strong>URL</strong>.</p></td>
<td><p>Задает URL-адрес файла или папки, опубликованной в веб-папку.</p></td>
</tr>
</tbody>
</table>


Так как это поставщика по умолчанию для ADO, если опустить **поставщика =** параметра в строке подключения ADO пытается установить подключение к данным поставщиком.

Поставщик не поддерживает параметры подключения в дополнение к определяемые ADO. Тем не менее Поставщик передает параметры соединения не ADO драйвера ODBC.

Так как можно опустить параметр **поставщика** , таким образом можно создать строку подключения ADO, идентичный строки подключения ODBC для одного источника данных. Используйте одинаковые имена параметров (**ДРАЙВЕРА =**, **базы данных =**, **уведомления о Доставке =** и так далее), значения и синтаксис, как вы бы при создании строки подключения ODBC. Можно подключить с и без имя источника данных (DSN) или FileDSN.

**Синтаксис с уведомления о Доставке или FileDSN:**

`"[Provider=MSDASQL;] { DSN=name | FileDSN=filename } ; [DATABASE=database;] UID=user; PWD=password"`

**Синтаксис без уведомления о Доставке (соединения):**

`"[Provider=MSDASQL;] DRIVER=driver; SERVER=server;DATABASE=database; UID=user; PWD=password"`

Если вы используете **уведомления о Доставке** или **FileDSN**, его необходимо определить через источники данных ODBC в панели управления Windows. В Microsoft Windows 2000 администратор ODBC находится в разделе Администрирование. В предыдущих версиях Windows значок администратор ODBC называется **32-разрядная версия ODBC** или просто **ODBC**.

В качестве альтернативы для установки **уведомления о Доставке**, можно указать драйвер ODBC (**ДРАЙВЕРА =**), например «SQL Server»; имя сервера (**SERVER =**); и имя базы данных (**базы данных =**).

Также можно указать имя учетной записи пользователя (**UID =**) и пароль для учетной записи пользователя (**PWD =**) в параметры, относящиеся к ODBC или в стандартный определенные ADO *пользователя* и *пароль* параметры.

Хотя **уведомления о Доставке** определение уже указывает базу данных, можно задать *параметр *базы данных* , в дополнение к **уведомления о Доставке** для подключения в другую базу данных* . Рекомендуется всегда включать *параметр *базы данных* * при использовании **уведомления о Доставке**. Это обеспечит подключиться к базе соответствующих прав в случае, когда другой пользователь изменить параметр базы данных по умолчанию с момента последнего извлечения определения **уведомления о Доставке** .

## <a name="provider-specific-connection-properties"></a>Свойства подключения от поставщика

Поставщик OLE DB для ODBC добавляет несколько свойств в коллекцию [свойств](properties-collection-ado.md) объекта **подключения** . В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.

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
<td><p>Доступны процедуры<br />
(KAGPROP_ACCESSIBLEPROCEDURES)</p></td>
<td><p>Указывает, является ли пользователь имеет доступ к хранимые процедуры.</p></td>
</tr>
<tr class="even">
<td><p>Доступно таблиц<br />
(KAGPROP_ACCESSIBLETABLES)</p></td>
<td><p>Указывает, является ли пользователь имеет разрешения на выполнение инструкций SELECT таблиц базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Активные операторы<br />
(KAGPROP_ACTIVESTATEMENTS)</p></td>
<td><p>Указывает число дескрипторов, которые может поддерживать драйвера ODBC для подключения.</p></td>
</tr>
<tr class="even">
<td><p>Имя драйвера<br />
(KAGPROP_DRIVERNAME)</p></td>
<td><p>Указывает имя файла драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Версия драйвера ODBC<br />
(KAGPROP_DRIVERODBCVER)</p></td>
<td><p>Указывает версию, поддерживающего этот драйвер ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Использование файлов<br />
(KAGPROP_FILEUSAGE)</p></td>
<td><p>Указывает, как драйвер обрабатывает файл источника данных. как таблицы или как к каталогу.</p></td>
</tr>
<tr class="odd">
<td><p>Как предложение escape-последовательности<br />
(KAGPROP_LIKEESCAPECLAUSE)</p></td>
<td><p>Указывает предикат LIKE предложение WHERE ли драйвер поддерживается в определение и использование escape-символ знаком процента (%) и символ подчеркивания (_).</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число столбцов в группировать по<br />
(KAGPROP_MAXCOLUMNSINGROUPBY)</p></td>
<td><p>Указывает максимальное число столбцов, которые могут быть перечислены в предложении GROUP BY инструкции SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число столбцов в индексе<br />
(KAGPROP_MAXCOLUMNSININDEX)</p></td>
<td><p>Указывает максимальное число столбцов, которые можно включить в индекс.</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число столбцов в порядке<br />
(KAGPROP_MAXCOLUMNSINORDERBY)</p></td>
<td><p>Указывает максимальное число столбцов, которые могут быть перечислены в предложение ORDER BY инструкции SELECT.</p></td>
</tr>
<tr class="odd">
<td><p>Максимальное число столбцов в Выбор<br />
(KAGPROP_MAXCOLUMNSINSELECT)</p></td>
<td><p>Указывает максимальное число столбцов, которые могут быть перечислены в разделе SELECT инструкции SELECT.</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число столбцов в таблице<br />
(KAGPROP_MAXCOLUMNSINTABLE)</p></td>
<td><p>Указывает максимальное число столбцов в таблице.</p></td>
</tr>
<tr class="odd">
<td><p>Числовые функции<br />
(KAGPROP_NUMERICFUNCTIONS)</p></td>
<td><p>Указывает, какие числовые функции поддерживаются драйвер ODBC. Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Возможности внешнего соединения<br />
(KAGPROP_OJCAPABILITY)</p></td>
<td><p>Указывает типы ВНЕШНИЕ соединения, поддерживаемых поставщиком.</p></td>
</tr>
<tr class="odd">
<td><p>Внешние соединения<br />
(KAGPROP_OUTERJOINS)</p></td>
<td><p>Указывает, является ли поставщик поддерживает ВНЕШНИЕ соединения.</p></td>
</tr>
<tr class="even">
<td><p>Специальные символы<br />
(KAGPROP_SPECIALCHARACTERS)</p></td>
<td><p>Указывает, какие символы имеет особое значение для драйвера ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Хранимые процедуры<br />
(KAGPROP_PROCEDURES)</p></td>
<td><p>Указывает, доступны ли хранимые процедуры для использования с этой драйвер ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Строковые функции<br />
(KAGPROP_STRINGFUNCTIONS)</p></td>
<td><p>Указывает, какие функции string, поддерживаются драйвер ODBC. Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Системные функции<br />
(KAGPROP_SYSTEMFUNCTIONS)</p></td>
<td><p>Указывает, какие функции системы поддерживаются драйвер ODBC. Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</p></td>
</tr>
<tr class="even">
<td><p>Время и Дата функции<br />
(KAGPROP_TIMEDATEFUNCTIONS)</p></td>
<td><p>Указывает, какие функции даты и времени поддерживаются драйвер ODBC. Список имен функций и связанные значения, используемые в этом Битовая маска, см в приложении д: скалярные в документации по ODBC.</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка грамматики SQL<br />
(KAGPROP_ODBCSQLCONFORMANCE)</p></td>
<td><p>Указывает грамматику SQL, которая поддерживает драйвер ODBC.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Свойства команды и записей от поставщика

Поставщик OLE DB для ODBC добавляет несколько свойств **Свойства** набора **записей** и **командных** объектов. В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.

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
<td><p>Запрос на основе обновления, удаления или вставки<br />
(KAGPROP_QUERYBASEDUPDATES)</p></td>
<td><p>Указывает, будет ли обновления, удаления и вставки можно выполнить с помощью SQL-запросов.</p></td>
</tr>
<tr class="even">
<td><p>Тип параллельного ODBC<br />
(KAGPROP_CONCURRENCY)</p></td>
<td><p>Метод, используемый для уменьшения потенциальных проблем, вызванных двух пользователей одновременно к той же информации из источника данных.</p></td>
</tr>
<tr class="odd">
<td><p>Специальные возможности больших двоичных ОБЪЕКТОВ на последовательный курсор<br />
(KAGPROP_BLOBSONFOCURSOR)</p></td>
<td><p>Указывает, будет ли при использовании последовательный курсор возможен больших двоичных ОБЪЕКТОВ <strong>полей</strong> .</p></td>
</tr>
<tr class="even">
<td><p>Включить в предложения QBU WHERE SQL_FLOAT, SQL_DOUBLE и SQL_REAL<br />
(KAGPROP_INCLUDENONEXACT)</p></td>
<td><p>Указывает, будет ли значения SQL_FLOAT, SQL_DOUBLE и SQL_REAL может быть включен в предложении QBU WHERE.</p></td>
</tr>
<tr class="odd">
<td><p>Положение в последней строке после вставки<br />
(KAGPROP_POSITIONONNEWROW)</p></td>
<td><p>Указывает, что после вставки новой записи в таблице последней строки в таблице должны быть поступают текущей строки.</p></td>
</tr>
<tr class="even">
<td><p>IRowsetChangeExtInfo<br />
(KAGPROP_IROWSETCHANGEEXTINFO)</p></td>
<td><p>Указывает, будет ли интерфейс <strong>IRowsetChange</strong> поддерживает расширенные сведения.</p></td>
</tr>
<tr class="odd">
<td><p>Тип курсора ODBC<br />
(KAGPROP_CURSOR)</p></td>
<td><p>Указывает тип курсора, используемого <strong>набора записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p>Создать набор строк, который может быть упакован<br />
(KAGPROP_MARSHALLABLE)</p></td>
<td><p>Указывает, что драйвер ODBC создает набор записей, который может быть упакован</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Текст команды

Как использовать объект [команды](command-object-ado.md) во многом зависит от источника данных и какой тип оператора запроса или команды будет принимать.

ODBC предоставляет определенный синтаксис для вызова хранимых процедур. Для свойства [CommandText](commandtext-property-ado.md) объекта **команды** *CommandText* аргумента метода **Execute** на объект [подключения](connection-object-ado.md) и *исходный* аргумент методу **Open** на [набора записей](recordset-object-ado.md) объект передает в строку с помощью следующего синтаксиса:

`"{ [ ? = ] call procedure [ ( ? [, ? [ ,  ]] ) ] }"`

Каждый **?** содержит ссылку на объект в коллекции [параметров](parameters-collection-ado.md) . Первый **?** ссылки на **Параметры**(0), Далее **?** Создание ссылки **Параметры**(1) и т. д.

Параметр ссылки являются необязательными и зависят от структуры хранимую процедуру. Если вы хотите вызвать хранимую процедуру, определяющий без параметров, строка будет выглядеть следующим образом:

`"{ call procedure }"`

Если у вас есть два параметра запроса, строка будет выглядеть следующим образом:

`"{ call procedure ( ?, ? ) }"`

Если хранимая процедура возвращает значение, возвращаемое значение обрабатывается как еще один параметр. Если у вас нет параметров запроса, но возвращаемое значение, строка будет выглядеть следующим образом:

`"{ ? = call procedure }"`

И, наконец Если у вас есть возвращаемое значение и два параметра запроса, строка будет выглядеть следующим образом:

`"{ ? = call procedure ( ?, ? ) }"`

## <a name="recordset-behavior"></a>Поведение набора записей

В следующих таблицах перечислены стандартные ADO методы и свойства, доступные для объекта **набора записей** , открытых с этим поставщиком.

Для получения дополнительных сведений о поведении **набора записей** для вашей конфигурации поставщика, выполните метод [поддерживает](supports-method-ado.md) и перечисления коллекции **свойств** **набора записей** для определения целесообразности поставщиком динамических свойства отсутствуют.

Доступность стандартными свойствами ADO **набора записей** :

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
<th><p>Динамическая группа</p></th>
<th><p>Набор ключей</p></th>
<th><p>Статическое</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>Недоступен</p></td>
<td><p>Недоступен</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>Недоступен</p></td>
<td><p>Недоступен</p></td>
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
<td><p>Недоступен</p></td>
<td><p>Недоступен</p></td>
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
<td><p><a href="filter-property-ado.md">Фильтр</a></p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="locktype-property-ado.md">LockType для</a></p></td>
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
<td><p>Недоступен</p></td>
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
<td><p>Недоступен</p></td>
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
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
<td><p>только для чтения</p></td>
</tr>
</tbody>
</table>


Свойства [AbsolutePosition](absoluteposition-property-ado.md) и [AbsolutePage](absolutepage-property-ado.md) доступны только для записи при использовании ADO с версии 1.0 поставщик Microsoft OLE DB для ODBC.

Доступность стандартных способов ADO **набора записей** :

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
<th><p>ForwardOnly</p></th>
<th><p>Динамическая группа</p></th>
<th><p>Набор ключей</p></th>
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
<td><p><a href="delete-method-ado-recordset.md">удаление</a>;</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">Получение строк</a></p></td>
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
<td><p><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></p></td>
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

Поставщик Microsoft OLE DB для ODBC вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .

В таблицах ниже — это cross-index имен ADO и OLE DB для каждого динамического свойства. Справочник программиста OLE DB указано имя свойства ADO по слову «Описание». Дополнительные сведения об этих свойств можно найти в Справочник программиста OLE DB. Поиск имени свойства OLE DB в индексе или просмотреть приложение C: OLE DB свойства.

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
<td><p>Location</p></td>
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
<td><p>Максимальный размер строки включает в себя больших двоичных ОБЪЕКТОВ</p></td>
<td><p>DBPROP_MAXROWSIZEINCLUDESBLOB</p></td>
</tr>
<tr class="odd">
<td><p>Максимальная таблиц в Выбор</p></td>
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
<td><p>Службы OLE DB</p></td>
<td><p>DBPROP_INIT_OLEDBSERVICES, УСТАНОВИТЬ</p></td>
</tr>
<tr class="even">
<td><p>Версия OLE DB</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка OLE-объектов</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Поддержка открытых наборов строк</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="odd">
<td><p>ORDER BY столбцы в списке Select</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="even">
<td><p>Выходной параметр доступности</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
</tr>
<tr class="even">
<td><p>Передайте с указанные методы</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Сохранять сведения о безопасности</p></td>
<td><p>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</p></td>
</tr>
<tr class="even">
<td><p>Тип сохраняемого идентификатора</p></td>
<td><p>DBPROP_PERSISTENTIDTYPE</p></td>
</tr>
<tr class="odd">
<td><p>Подготовка поведение аварийное завершение</p></td>
<td><p>DBPROP_PREPAREABORTBEHAVIOR</p></td>
</tr>
<tr class="even">
<td><p>Подготовка поведение выделения</p></td>
<td><p>DBPROP_PREPARECOMMITBEHAVIOR</p></td>
</tr>
<tr class="odd">
<td><p>Процедура терминов</p></td>
<td><p>DBPROP_PROCEDURETERM</p></td>
</tr>
<tr class="even">
<td><p>Запрос</p></td>
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
<td><p>Источник данных только для чтения</p></td>
<td><p>DBPROP_DATASOURCEREADONLY</p></td>
</tr>
<tr class="odd">
<td><p>Преобразование строк на команду</p></td>
<td><p>DBPROP_ROWSETCONVERSIONSONCOMMAND</p></td>
</tr>
<tr class="even">
<td><p>Схема терминов</p></td>
<td><p>DBPROP_SCHEMATERM</p></td>
</tr>
<tr class="odd">
<td><p>Об использовании схемы</p></td>
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
<td><p>Поддержка вложенного запроса</p></td>
<td><p>DBPROP_SUBQUERIES</p></td>
</tr>
<tr class="odd">
<td><p>В таблице терминов</p></td>
<td><p>DBPROP_TABLETERM</p></td>
</tr>
<tr class="even">
<td><p>Транзакций DDL</p></td>
<td><p>DBPROP_SUPPORTEDTXNDDL</p></td>
</tr>
<tr class="odd">
<td><p>Идентификатор пользователя</p></td>
<td><p>DBPROP_AUTH_USERID</p></td>
</tr>
<tr class="even">
<td><p>Имя пользователя</p></td>
<td><p>DBPROP_USERNAME</p></td>
</tr>
<tr class="odd">
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
<td><p>Литерал закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Удостоверение литерала строки</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число открытых строк</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимум ожидающие строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число строк</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Степень детализации уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Этапы уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Объекты в транзакции</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Видны собственные изменения</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Видны собственные операции вставки</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Сохранять при аварийном завершении</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Сохранять при фиксации</p></td>
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
<td><p>Сообщить о нескольких изменений</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Вернуть ожидающие вставки</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Удалить строку уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Строка первого уведомления об изменении</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Строка вставки уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Привилегии строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомления о повторной синхронизации строки</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Строка, потоковой модели</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об изменении отмены строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Строка отмены Delete уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Вставка отмены строки уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об обновлении строки</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об изменении положения строк выборки</p></td>
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
<td><p>Литерал закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Удостоверение литерала строки</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число открытых строк</p></td>
<td><p>DBPROP_MAXOPENROWS</p></td>
</tr>
<tr class="odd">
<td><p>Максимум ожидающие строк</p></td>
<td><p>DBPROP_MAXPENDINGROWS</p></td>
</tr>
<tr class="even">
<td><p>Максимальное число строк</p></td>
<td><p>DBPROP_MAXROWS</p></td>
</tr>
<tr class="odd">
<td><p>Степень детализации уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="even">
<td><p>Этапы уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="odd">
<td><p>Объекты в транзакции</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="even">
<td><p>Видны собственные изменения</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Видны собственные операции вставки</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="even">
<td><p>Сохранять при аварийном завершении</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="odd">
<td><p>Сохранять при фиксации</p></td>
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
<td><p>Сообщить о нескольких изменений</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="even">
<td><p>Вернуть ожидающие вставки</p></td>
<td><p>DBPROP_RETURNPENDINGINSERTS</p></td>
</tr>
<tr class="odd">
<td><p>Удалить строку уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWDELETE</p></td>
</tr>
<tr class="even">
<td><p>Строка первого уведомления об изменении</p></td>
<td><p>DBPROP_NOTIFYROWFIRSTCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Строка вставки уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="even">
<td><p>Привилегии строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомления о повторной синхронизации строки</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="even">
<td><p>Строка, потоковой модели</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об изменении отмены строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="even">
<td><p>Строка отмены Delete уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="odd">
<td><p>Вставка отмены строки уведомлений</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об обновлении строки</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об изменении положения строк выборки</p></td>
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
<td><p>Пропустить удаленных закладки</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="odd">
<td><p>Строка строгого удостоверений</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="even">
<td><p>Возможности обновления</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="odd">
<td><p>Использование закладок</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

Для получения дополнительных сведений о реализации и функциональным сведения о поставщик Microsoft OLE DB для ODBC обратитесь к [OLE DB Руководство программиста](https://docs.microsoft.com/previous-versions/windows/desktop/ms713643(v=vs.85)) или посетите [Центр разработчиков данных платформы](https://docs.microsoft.com/sql/connect/sql-data-developer?view=sql-server-2017).

