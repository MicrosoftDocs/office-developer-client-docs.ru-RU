---
title: Поставщик Microsoft OLE DB для Microsoft Jet
TOCTitle: Microsoft OLE DB Provider for Microsoft Jet
ms:assetid: 4a210d72-8c90-aa7c-4621-1a555a30a2d2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249228(v=office.15)
ms:contentKeyID: 48544660
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 9b4f1c46b390e1f059e57f3b7a70fc667da4b09b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288927"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a>Поставщик Microsoft OLE DB для Microsoft Jet

**Область применения**: Access 2013, Office 2013

Поставщик OLE DB для Microsoft Jet позволяет ADO получать доступ к базам данных Microsoft Jet.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к этому поставщику, установите *аргумент поставщика* свойства [ConnectionString:](connectionstring-property-ado.md)

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

Чтение свойства [Provider](provider-property-ado.md) также вернет эту строку.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
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
<td><p>Указывает поставщика OLE DB для Microsoft Jet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Указывает путь базы данных и имя файла (например, c:\Northwind.mdb).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Идентификатор пользователя</strong></p></td>
<td><p>Задает имя пользователя. Если это ключевое слово не указано, строка &quot; &quot; администратора используется по умолчанию.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Указывает пароль пользователя. Если это ключевое слово не указано, пустая строка (), &quot; &quot; используется по умолчанию.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Provider-Specific параметры подключения

Поставщик OLE DB для Microsoft Jet поддерживает несколько динамических свойств, определенных для конкретного поставщика, в дополнение к тем, которые определены ADO. Как и все другие параметры **Подключения,**  их можно установить с помощью коллекции **Свойств** объекта Подключения или в составе строки подключения.

В следующей таблице перечислены эти свойства с соответствующим именем свойства OLE DB в скобки.

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
<td><p>Jet OLEDB:Compact Reclaimed Space Amount<br />
(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</p></td>
<td><p>Указывает оценку количества пространства в bytes, которое можно восстановить, уплотнив базу данных. Это значение допустимо только после подключения к базе данных.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Connection Control<br />
(DBPROP_JETOLEDB_CONNECTIONCONTROL)</p></td>
<td><p>Указывает, могут ли пользователи подключаться к базе данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Create System Database<br />
(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</p></td>
<td><p>Указывает, следует ли создавать системную базу данных при создании нового источника данных.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Database Locking Mode<br />
(DBPROP_JETOLEDB_DATABASELOCKMODE)</p></td>
<td><p>Указывает режим блокировки для этой базы данных. Первый пользователь, открывая базу данных, определяет режим, используемый во время открытия базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Пароль jet OLEDB:Database<br />
(DBPROP_JETOLEDB_DATABASEPASSWORD)</p></td>
<td><p>Указывает пароль базы данных.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Don't Copy Locale on Compact<br />
(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</p></td>
<td><p>Указывает, следует ли jet скопировать сведения о локальном уровне при сжатии базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Encrypt Database<br />
(DBPROP_JETOLEDB_ENCRYPTDATABASE)</p></td>
<td><p>Указывает, следует ли шифровать сжатую базу данных. Если это свойство не установлено, сжатая база данных будет зашифрована, если оригинальная база данных также была зашифрована.</p></td>
</tr>
<tr class="even">
<td><p>Тип двигателя OLEDB:Engine<br />
(DBPROP_JETOLEDB_ENGINE)</p></td>
<td><p>Указывает двигатель хранения, используемый для доступа к текущему хранилище данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Exclusive Async Delay<br />
(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</p></td>
<td><p>Указывает максимальное время, в миллисекунд, что Jet может задерживать асинхронные записи на диск, когда база данных открыта исключительно. Это свойство игнорируется, если только время времени транзакции <strong>jet OLEDB:Flush</strong> не установлено до 0.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Flush Transaction Timeout<br />
(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</p></td>
<td><p>Указывает время ожидания, прежде чем данные, хранимые в кэше для асинхронной записи, фактически будут записаны на диск. Этот параметр переопределяет значения для <strong>jet OLEDB:Shared Async Delay</strong> и <strong>Jet OLEDB:Exclusive Async Delay</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Global Bulk Transactions<br />
(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</p></td>
<td><p>Указывает, SQL транзакции.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Global Partial Bulk Ops<br />
(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</p></td>
<td><p>Указывает пароль, используемый для открытия базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Синхронизация фиксации Jet OLEDB:Implicit<br />
(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</p></td>
<td><p>Указывает, пишутся ли изменения во внутренних неявных транзакциях в синхронном или асинхронном режиме.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Lock Delay<br />
(DBPROP_JETOLEDB_LOCKDELAY)</p></td>
<td><p>Указывает количество миллисекунд, которые следует ждать перед попыткой получить блокировку после сбой предыдущей попытки.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Lock Retry<br />
(DBPROP_JETOLEDB_LOCKRETRY)</p></td>
<td><p>Указывает, сколько раз повторяется попытка доступа к заблокированной странице.</p></td>
</tr>
<tr class="even">
<td><p>Размер буфера Jet OLEDB:Max<br />
(DBPROP_JETOLEDB_MAXBUFFERSIZE)</p></td>
<td><p>Указывает максимальное количество памяти в килобайтах, которые Jet может использовать до начала очистки изменений на диске.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Max Locks Per File<br />
(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</p></td>
<td><p>Указывает максимальное количество блокировок, которые Jet может разместить в базе данных. Значение по умолчанию — 9500.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Новый пароль базы данных<br />
(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</p></td>
<td><p>Указывает новый пароль, заданной для этой базы данных. Старый пароль хранится в <strong>jet OLEDB:Database Password</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:ODBC Командный выход<br />
(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</p></td>
<td><p>Указывает количество миллисекунд перед удаленным запросом ODBC от Jet.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Page Locks to Table Lock<br />
(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</p></td>
<td><p>Указывает, сколько страниц необходимо заблокировать в транзакции перед попыткой Jet продвинуть блокировку в блокировку таблицы. Если это значение 0, блокировка никогда не будет повышена.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Page Timeout<br />
(DBPROP_JETOLEDB_PAGETIMEOUT)</p></td>
<td><p>Указывает количество миллисекунд Jet, которые будут ждать, прежде чем проверять, устарел ли кэш с файлом базы данных.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Recycle Long-Valued Pages<br />
(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</p></td>
<td><p>Указывает, следует ли jet агрессивно пытаться вернуть страницы BLOB при их освобождении.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Registry Path<br />
(DBPROP_JETOLEDB_REGPATH)</p></td>
<td><p>Указывает ключ Windows реестра, содержащий значения для двигателя базы данных Jet.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Reset ISAM Stats<br />
(DBPROP_JETOLEDB_RESETISAMSTATS)</p></td>
<td><p>Указывает, следует ли <strong></strong> DBSCHEMA_JETOLEDB_ISAMSTATS сбросить счетчики производительности после возврата сведений о производительности.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Shared Async Delay<br />
(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</p></td>
<td><p>Указывает максимальное количество времени, в миллисекунде Jet может задерживать асинхронные записи на диск, когда база данных открывается в много пользователя режиме.</p></td>
</tr>
<tr class="even">
<td><p>База данных Jet OLEDB:System<br />
(DBPROP_JETOLEDB_SYSDBPATH)</p></td>
<td><p>Указывает путь и имя файла для информационного файла workgroup (база данных системы).</p></td>
</tr>
<tr class="odd">
<td><p>Режим фиксации транзакций Jet OLEDB:Transaction<br />
(DBPROP_JETOLEDB_TXNCOMMITMODE)</p></td>
<td><p>Указывает, синхронно или асинхронно ли Jet записывает данные на диск при совершении транзакции.</p></td>
</tr>
<tr class="even">
<td><p>Синхронизация фиксации jet OLEDB:User<br />
(DBPROP_JETOLEDB_USERCOMMITSYNC)</p></td>
<td><p>Указывает, пишутся ли изменения в транзакциях в синхронном или асинхронном режиме.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Provider-Specific Recordset и Command Properties

Поставщик Jet также поддерживает несколько свойств **Recordset** и **Command,** определенных для поставщика. Доступ к этим свойствам устанавливается в коллекции **Свойств** объекта **Recordset** или **Command.** В таблице перечислены имя свойства ADO и соответствующее имя свойства OLE DB в скобки.

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
<td><p>Jet OLEDB:Bulk Transactions<br />
(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</p></td>
<td><p>Указывает, SQL ли массовые операции. Крупные массовые операции могут привести к сбойу при переносе из-за задержек ресурсов.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Enable Fat Cursors<br />
(DBPROP_JETOLEDB_ENABLEFATCURSOR)</p></td>
<td><p>Указывает, должен ли Jet кэшировать несколько строк при заполнении наборов записей для удаленных источников строк.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Fat Cursor Cache Size<br />
(DBPROP_JETOLEDB_FATCURSORMAXROWS)</p></td>
<td><p>Указывает количество строк кэша при использовании удаленного кэша строк хранения данных. Это значение игнорируется, если <strong>jet OLEDB:Enable Fat Cursors</strong> is True.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Inconsistent<br />
(DBPROP_JETOLEDB_INCONSISTENT)</p></td>
<td><p>Указывает, позволяют ли результаты запроса несогласованные обновления.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Locking Granularity<br />
(DBPROP_JETOLEDB_LOCKGRANULARITY)</p></td>
<td><p>Указывает, открыта ли таблица с помощью блокировки на уровне строки.</p></td>
</tr>
<tr class="even">
<td><p>Заявление jet OLEDB:ODBC Pass-Through<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</p></td>
<td><p>Указывает, что Jet должен передать SQL в <strong>объекте Command</strong> на задний конец безальтераторно.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Partial Bulk Ops<br />
(DBPROP_JETOLEDB_BULKPARTIAL)</p></td>
<td><p>Указывает поведение Jet при сбой SQL DML.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB:Pass Through Query Bulk-Op<br />
(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</p></td>
<td><p>Указывает, передаются ли запросы, которые не возвращают <strong>набор записей,</strong> в источник данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Pass Through Query Подключение String<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</p></td>
<td><p>Указывает строку jet connect, используемую для подключения к удаленному хранилище данных. Это значение игнорируется, если <strong>заявление jet OLEDB:ODBC Pass-Through является</strong> true.</p></td>
</tr>
<tr class="even">
<td><p>Запрос JET OLEDB:Stored<br />
(DBPROP_JETOLEDB_STOREDQUERY)</p></td>
<td><p>Указывает, следует ли интерпретировать текст команды как сохраненный запрос, а не SQL команду.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Проверка правил в наборе<br />
(DBPROP_JETOLEDB_VALIDATEONSET)</p></td>
<td><p>Указывает, оцениваются ли правила проверки jet при наборе данных столбцов или при внесении изменений в базу данных.</p></td>
</tr>
</tbody>
</table>


По умолчанию поставщик OLE DB для Microsoft Jet открывает базы данных Microsoft Jet в режиме чтения и записи. Чтобы открыть базу данных в режиме только для чтения, установите свойство [Mode](mode-property-ado.md) на объекте ADO **Connection** **adModeRead.**

## <a name="command-object-usage"></a>Использование командных объектов

Командный текст в [объекте Command](command-object-ado.md) использует диалект Microsoft Jet SQL. В тексте команды можно указать запросы, запросы действий и имена таблиц, возвращающие строки; однако сохраненные процедуры не поддерживаются и не должны быть указаны.

## <a name="recordset-behavior"></a>Поведение наборов записей

Двигатель базы данных Microsoft Jet не поддерживает динамические курсоры. Поэтому поставщик OLE DB для Microsoft Jet не поддерживает тип **курсора adLockDynamic.** Когда запрашивается динамический курсор, поставщик возвращает курсор наборов ключей и сбрасывает свойство [CursorType,](cursortype-property-ado.md) чтобы указать тип возвращенного [recordset.](recordset-object-ado.md) Кроме того, если запрашивается updatable **Recordset** **(LockType** является **adLockOptimistic,** **adLockBatchOptimistic** или **adLockPessimistic),** поставщик также возвращает курсор наборов ключей и сбрасывает свойство **CursorType.**

## <a name="dynamic-properties"></a>Dynamic Properties

Поставщик OLE DB для Microsoft Jet вставляет несколько динамических свойств в коллекцию **свойств** незапертых объектов [Connection,](connection-object-ado.md) [Recordset](recordset-object-ado.md)и [Command.](command-object-ado.md)

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
<td><p>Текущий каталог</p></td>
<td><p>DBPROP_CURRENTCATALOG</p></td>
</tr>
<tr class="odd">
<td><p>Источник данных</p></td>
<td><p>DBPROP_INIT_DATASOURCE</p></td>
</tr>
<tr class="even">
<td><p>Имя источника данных</p></td>
<td><p>DBPROP_DATASOURCENAME</p></td>
</tr>
<tr class="odd">
<td><p>Модель потоковой обработки объектов источника данных</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Имя DBMS</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="odd">
<td><p>Версия DBMS</p></td>
<td><p>DBPROP_DBMSVER</p></td>
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
<td><p>Уровни изоляции</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="even">
<td><p>Хранение изоляции</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="odd">
<td><p>Идентификатор locale</p></td>
<td><p>DBPROP_INIT_LCID</p></td>
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
<td><p>Append-Only Rowset</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
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
<td><p>Закладки заказать</p></td>
<td><p>DBPROP_ORDEREDBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Отложенные столбцы кэша</p></td>
<td><p>DBPROP_CACHEDEFERRED</p></td>
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
<td><p>Колонка Writable</p></td>
<td><p>DBPROP_MAYWRITECOLUMN</p></td>
</tr>
<tr class="even">
<td><p>Столбец Отсрочка</p></td>
<td><p>DBPROP_DEFERRED</p></td>
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
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
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
<td><p>IRowsetIndex</p></td>
<td><p>DBPROP_IRowsetIndex</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="even">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IRowsestLocate</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetResynch</p></td>
<td><p></p></td>
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
<td><p>IStorage</p></td>
<td><p>DBPROP_IStorage</p></td>
</tr>
<tr class="even">
<td><p>IStream</p></td>
<td><p>DBPROP_IStream</p></td>
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
<td><p>Использование памяти</p></td>
<td><p>DBPROP_MEMORYUSAGE</p></td>
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
<td><p>Пропустить удаленные закладки</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="even">
<td><p>Удостоверение Strong Row</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
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
<td><p>Append-Only Rowset</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
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
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
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
<td><p>IRowsetIndex</p></td>
<td><p>DBPROP_IRowsetIndex</p></td>
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
<td><p>IStorage</p></td>
<td><p>DBPROP_IStorage</p></td>
</tr>
<tr class="odd">
<td><p>IStream</p></td>
<td><p>DBPROP_IStream</p></td>
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
<td><p>Режим блокировки</p></td>
<td><p>DBPROP_LOCKMODE</p></td>
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
<td><p>Видимые изменения других</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Видимые вставки других</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
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
</tbody>
</table>


## <a name="see-also"></a>См. также

Для получения конкретных сведений о реализации и функциональных сведений о поставщике OLE DB для Microsoft Jet обратитесь к поставщику OLE DB для документации Microsoft Jet в SDK MDAC.

