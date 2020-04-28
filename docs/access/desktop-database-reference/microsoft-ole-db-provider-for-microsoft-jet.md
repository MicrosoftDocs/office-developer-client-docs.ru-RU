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

Чтобы подключиться к поставщику, присвойте аргументу *provider* свойства [ConnectionString](connectionstring-property-ado.md) значение:

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

Считывание свойства [provider](provider-property-ado.md) также возвратит эту строку.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```vb 
 
"Provider=Microsoft.Jet.OLEDB.4.0;Data Source=databaseName;User ID=userName;Password=userPassword;" 
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
<td><p>Указывает поставщика OLE DB для Microsoft Jet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Указывает путь к базе данных и имя файла (например, К:\норсвинд.МДБ).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Идентификатор пользователя</strong></p></td>
<td><p>Задает имя пользователя. Если это ключевое слово не указано, по умолчанию используется строка, &quot;admin&quot;.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Указывает пароль пользователя. Если это ключевое слово не указано, по умолчанию&quot;&quot;используется пустая строка ().</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Параметры подключения, зависящие от поставщика

Поставщик OLE DB для Microsoft Jet поддерживает несколько динамических свойств, относящихся к определенным поставщикам, в дополнение к тем, которые определены в ADO. Как и во всех остальных параметрах **подключения** , их можно задать с помощью коллекции **свойств** объекта **Connection** или в строке подключения.

В приведенной ниже таблице указаны эти свойства с соответствующим именем свойства OLE DB в круглых скобках.

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
<td><p>Jet OLEDB: сжатие освобожденного объема дискового пространства<br />
(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</p></td>
<td><p>Указывает оценку объема пространства в байтах, которое может быть восстановлено с помощью сжатия базы данных. Это значение является допустимым только после установки подключения к базе данных.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Управление подключением<br />
(DBPROP_JETOLEDB_CONNECTIONCONTROL)</p></td>
<td><p>Указывает, могут ли пользователи подключаться к базе данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Создание системной базы данных<br />
(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</p></td>
<td><p>Указывает, следует ли создавать системную базу данных при создании нового источника данных.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: режим блокировки базы данных<br />
(DBPROP_JETOLEDB_DATABASELOCKMODE)</p></td>
<td><p>Указывает режим блокировки для этой базы данных. Первый пользователь, который открывает базу данных, определяет режим, используемый при открытии базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: пароль базы данных<br />
(DBPROP_JETOLEDB_DATABASEPASSWORD)</p></td>
<td><p>Указывает пароль базы данных.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: не копировать языковой стандарт в Compact<br />
(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</p></td>
<td><p>Указывает, следует ли Jet копировать информацию о языковых стандартах при сжатии базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: шифрование базы данных<br />
(DBPROP_JETOLEDB_ENCRYPTDATABASE)</p></td>
<td><p>Указывает, следует ли шифровать сжатую базу данных. Если это свойство не задано, сжатая база данных будет зашифрована, если исходная база данных также была зашифрована.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: тип модуля<br />
(DBPROP_JETOLEDB_ENGINE)</p></td>
<td><p>Указывает подсистему хранилища, используемую для доступа к текущему хранилищу данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: исключительная асинхронная задержка<br />
(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</p></td>
<td><p>Указывает максимальное время (в миллисекундах), в течение которого Jet может задерживать асинхронные операции записи на диск, когда база данных открыта в монопольном режиме. Это свойство игнорируется, если <strong>Jet OLEDB: время ожидания транзакции на сброс</strong> устанавливается равным 0.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: время ожидания очистки транзакций<br />
(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</p></td>
<td><p>Указывает время ожидания, в течение которого данные, хранящиеся в кэше для асинхронной записи, фактически записываются на диск. Этот параметр переопределяет значения для <strong>Jet OLEDB: Общая асинхронная задержка</strong> и <strong>Jet OLEDB: исключительная асинхронная задержка</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: глобальные массовые транзакции<br />
(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</p></td>
<td><p>Указывает, являются ли транзакции массовых транзакций SQL транзакционными.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: глобальные частичные массовые операции<br />
(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</p></td>
<td><p>Указывает пароль, используемый для открытия базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Неявная синхронизация фиксации<br />
(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</p></td>
<td><p>Указывает, записываются ли изменения, внесенные во внутренние неявные транзакции, в синхронном или асинхронном режиме.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: задержка блокировки<br />
(DBPROP_JETOLEDB_LOCKDELAY)</p></td>
<td><p>Указывает время ожидания в миллисекундах перед попыткой получить блокировку после сбоя предыдущей попытки.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Блокировка повторных попыток<br />
(DBPROP_JETOLEDB_LOCKRETRY)</p></td>
<td><p>Указывает, сколько раз попытка доступа к заблокированной странице повторяется.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: максимальный размер буфера<br />
(DBPROP_JETOLEDB_MAXBUFFERSIZE)</p></td>
<td><p>Указывает максимальный объем памяти (в килобайтах), который может использоваться Jet перед запуском очистки изменений на диске.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: максимальное число блокировок на файл<br />
(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</p></td>
<td><p>Указывает максимальное число блокировок базы данных, которые Jet может разместить в базе данных. Значение по умолчанию — 9500.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: новый пароль базы данных<br />
(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</p></td>
<td><p>Указывает новый пароль, который необходимо задать для этой базы данных. Старый пароль хранится в <strong>Jet OLEDB: пароль базы данных</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: время ожидания команды ODBC<br />
(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</p></td>
<td><p>Указывает количество миллисекунд, по истечении которого удаленный запрос ODBC из Jet будет истечет.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Блокировка страниц для блокировки таблицы<br />
(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</p></td>
<td><p>Указывает, сколько страниц необходимо заблокировать в транзакции, прежде чем Jet пытается превратить блокировку в блокировку таблицы. Если это значение равно 0, блокировка никогда не будет повышена.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: время ожидания страницы<br />
(DBPROP_JETOLEDB_PAGETIMEOUT)</p></td>
<td><p>Указывает, что время ожидания Jet будет проверяться на наличие устаревших данных в файле базы данных в миллисекундах.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: повторное переработка страниц с длинными значениями<br />
(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</p></td>
<td><p>Указывает, следует ли использовать Jet для принудительного восстановления страниц BLOB при их освобождении.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: путь в реестре<br />
(DBPROP_JETOLEDB_REGPATH)</p></td>
<td><p>Указывает раздел реестра Windows, который содержит значения для ядра базы данных Jet.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Reset ISAM stats<br />
(DBPROP_JETOLEDB_RESETISAMSTATS)</p></td>
<td><p>Указывает, должен ли DBSCHEMA_JETOLEDB_ISAMSTATS <strong>набор записей</strong> схемы сбрасывать счетчики производительности после возврата сведений о производительности.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: асинхронная асинхронная задержка<br />
(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</p></td>
<td><p>Указывает максимальное время (в миллисекундах), в течение которого Jet может задерживать асинхронные операции записи на диск при открытии базы данных в режиме с несколькими пользователями.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: системная база данных<br />
(DBPROP_JETOLEDB_SYSDBPATH)</p></td>
<td><p>Указывает путь и имя файла для файла сведений о рабочей группе (системная база данных).</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: режим фиксации транзакции<br />
(DBPROP_JETOLEDB_TXNCOMMITMODE)</p></td>
<td><p>Указывает, записывает ли Jet данные на диск синхронно или асинхронно при фиксации транзакции.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: Синхронизация с сохранением пользователей<br />
(DBPROP_JETOLEDB_USERCOMMITSYNC)</p></td>
<td><p>Указывает, записываются ли изменения, внесенные в транзакции, в синхронном или асинхронном режиме.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Специфические для поставщика наборы записей и свойства команд

Поставщик Jet также поддерживает несколько специфических для конкретного поставщика **наборов записей** и свойств **команды** . Доступ к этим свойствам и их настройка осуществляется с помощью коллекции **свойств** объекта **Recordset** или объекта **Command** . В таблице перечислены имя свойства ADO и соответствующее имя свойства OLE DB в круглых скобках.

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
<td><p>Jet OLEDB: массовые транзакции<br />
(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</p></td>
<td><p>Указывает, являются ли массовые операции SQL транзакционными. Большие массовые операции могут привести к сбою в связи с задержками ресурсов.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: включение курсоров FAT<br />
(DBPROP_JETOLEDB_ENABLEFATCURSOR)</p></td>
<td><p>Указывает, должен ли Jet кэшировать несколько строк при заполнении набора записей для удаленных источников строк.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: размер кэша курсоров FAT<br />
(DBPROP_JETOLEDB_FATCURSORMAXROWS)</p></td>
<td><p>Указывает количество строк для кэширования при использовании кэширования строк удаленного хранилища данных. Это значение игнорируется, если <strong>Jet OLEDB: enable FAT Cursors</strong> имеет значение true.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: противоречивые<br />
(DBPROP_JETOLEDB_INCONSISTENT)</p></td>
<td><p>Указывает, разрешены ли в результатах запроса несогласованные обновления.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Гранулярность блокировок<br />
(DBPROP_JETOLEDB_LOCKGRANULARITY)</p></td>
<td><p>Указывает, открыта ли таблица с использованием блокировки на уровне строк.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: оператор сквозного ODBC<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</p></td>
<td><p>Указывает, что Jet должен передать текст SQL в объект <strong>Command</strong> обратно на сервер, не измененный.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: частичные массовые операции<br />
(DBPROP_JETOLEDB_BULKPARTIAL)</p></td>
<td><p>Указывает поведение Jet при отказе операций SQL DML.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: сквозная передача запроса массовой операции<br />
(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</p></td>
<td><p>Указывает, передаются ли запросы, не возвращающие объект <strong>Recordset</strong> , в источник данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: строка сквозного подключения запроса<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</p></td>
<td><p>Указывает строку подключения Jet, используемую для подключения к удаленному хранилищу данных. Это значение игнорируется, если <strong>Jet OLEDB: сквозной оператор ODBC</strong> имеет значение true.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: сохраненный запрос<br />
(DBPROP_JETOLEDB_STOREDQUERY)</p></td>
<td><p>Указывает, следует ли интерпретировать текст команды как хранимый запрос вместо команды SQL.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: Проверка правил для набора<br />
(DBPROP_JETOLEDB_VALIDATEONSET)</p></td>
<td><p>Указывает, оцениваются ли правила проверки Jet при задании данных столбцов или при фиксации изменений в базе данных.</p></td>
</tr>
</tbody>
</table>


По умолчанию поставщик OLE DB для Microsoft Jet открывает базы данных Microsoft Jet в режиме чтения и записи. Чтобы открыть базу данных в режиме только для чтения, задайте для свойства [mode](mode-property-ado.md) объекта **подключения** ADO значение **адмодереад**.

## <a name="command-object-usage"></a>Использование объекта Command

Текст команды в объекте [Command](command-object-ado.md) использует диалект Microsoft Jet SQL. Можно указать запросы, возвращающие строки, запросы на изменение и имена таблиц, в тексте команды; Однако хранимые процедуры не поддерживаются и не должны указываться.

## <a name="recordset-behavior"></a>Поведение набора записей

Ядро базы данных Microsoft Jet не поддерживает динамические курсоры. Таким образом, поставщик OLE DB для Microsoft Jet не поддерживает тип курсора **адлоккдинамик** . При запросе динамического курсора поставщик возвращает курсор KEYSET и сбрасывает свойство [CursorType](cursortype-property-ado.md) , чтобы указать тип возвращаемого [набора записей](recordset-object-ado.md) . Кроме того, если запрашивается обновляемый **набор записей** (**LockType** — **адлоккоптимистик**, **адлоккбатчоптимистик**или **адлоккпессимистик**), поставщик также возвращает курсор набора ключей и сбрасывает свойство **CursorType** .

## <a name="dynamic-properties"></a>Динамические свойства

Поставщик OLE DB для Microsoft Jet вставляет несколько динамических свойств в коллекцию **свойств** неоткрытых [подключений](connection-object-ado.md), [наборов записей](recordset-object-ado.md)и объектов [команд](command-object-ado.md) .

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
<td><p>Модель потоков объектов источника данных</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Имя СУБД</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="odd">
<td><p>Версия DBMS</p></td>
<td><p>DBPROP_DBMSVER</p></td>
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
<td><p>Уровни изоляции</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="even">
<td><p>Хранение изоляции</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="odd">
<td><p>Идентификатор языкового стандарта</p></td>
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
<td><p>Версия OLE DB</p></td>
<td><p>DBPROP_PROVIDEROLEDBVER</p></td>
</tr>
<tr class="even">
<td><p>Поддержка объектов OLE</p></td>
<td><p>DBPROP_OLEOBJECTS</p></td>
</tr>
<tr class="odd">
<td><p>Поддержка открытых наборов строк</p></td>
<td><p>DBPROP_OPENROWSETSUPPORT</p></td>
</tr>
<tr class="even">
<td><p>УПОРЯДОЧЕНие по столбцам в списке выборки</p></td>
<td><p>DBPROP_ORDERBYCOLUMNSINSELECT</p></td>
</tr>
<tr class="odd">
<td><p>Доступность выходного параметра</p></td>
<td><p>DBPROP_OUTPUTPARAMETERAVAILABILITY</p></td>
</tr>
<tr class="even">
<td><p>Передача по параметрам доступа ref</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="odd">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
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
<td><p>Набор строк только для добавления</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
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
<td><p>Упорядоченные закладки</p></td>
<td><p>DBPROP_ORDEREDBOOKMARKS</p></td>
</tr>
<tr class="odd">
<td><p>Кэширование отложенных столбцов</p></td>
<td><p>DBPROP_CACHEDEFERRED</p></td>
</tr>
<tr class="even">
<td><p>Изменение вставленных строк</p></td>
<td><p>DBPROP_CHANGEINSERTEDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Права на столбцы</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о наборе столбцов</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="odd">
<td><p>Столбец доступен для записи</p></td>
<td><p>DBPROP_MAYWRITECOLUMN</p></td>
</tr>
<tr class="even">
<td><p>Откладывание столбца</p></td>
<td><p>DBPROP_DEFERRED</p></td>
</tr>
<tr class="odd">
<td><p>Откладывание обновлений объектов хранилища</p></td>
<td><p>DBPROP_DELAYSTORAGEOBJECTS</p></td>
</tr>
<tr class="even">
<td><p>Извлечение назад</p></td>
<td><p>DBPROP_CANFETCHBACKWARDS</p></td>
</tr>
<tr class="odd">
<td><p>Удержание строк</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="even">
<td><p>иакцессор</p></td>
<td><p>DBPROP_IAccessor</p></td>
</tr>
<tr class="odd">
<td><p>иколумнсинфо</p></td>
<td><p>DBPROP_IColumnsInfo</p></td>
</tr>
<tr class="even">
<td><p>иколумнсровсет</p></td>
<td><p>DBPROP_IColumnsRowset</p></td>
</tr>
<tr class="odd">
<td><p>иконнектионпоинтконтаинер</p></td>
<td><p>DBPROP_IConnectionPointContainer</p></td>
</tr>
<tr class="even">
<td><p>иконверттипе</p></td>
<td><p>DBPROP_IConvertType</p></td>
</tr>
<tr class="odd">
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
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
<td><p>ировсетиндекс</p></td>
<td><p>DBPROP_IRowsetIndex</p></td>
</tr>
<tr class="odd">
<td><p>ировсетинфо</p></td>
<td><p>DBPROP_IRowsetInfo</p></td>
</tr>
<tr class="even">
<td><p>ировсетлокате</p></td>
<td><p>DBPROP_IRowsestLocate</p></td>
</tr>
<tr class="odd">
<td><p>ировсетресинч</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>ировсетскролл</p></td>
<td><p>DBPROP_IRowsetScroll</p></td>
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
<td><p>Содержим</p></td>
<td><p>DBPROP_IStorage</p></td>
</tr>
<tr class="even">
<td><p>IStream</p></td>
<td><p>DBPROP_IStream</p></td>
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
<td><p>Использование памяти</p></td>
<td><p>DBPROP_MEMORYUSAGE</p></td>
</tr>
<tr class="even">
<td><p>Детализация уведомлений</p></td>
<td><p>DBPROP_NOTIFICATIONGRANULARITY</p></td>
</tr>
<tr class="odd">
<td><p>Этапы уведомления</p></td>
<td><p>DBPROP_NOTIFICATIONPHASES</p></td>
</tr>
<tr class="even">
<td><p>Объекты, транзакционные</p></td>
<td><p>DBPROP_TRANSACTEDOBJECT</p></td>
</tr>
<tr class="odd">
<td><p>Видны другие изменения</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Видимые вставки других пользователей</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Видны изменения</p></td>
<td><p>DBPROP_OWNUPDATEDELETE</p></td>
</tr>
<tr class="even">
<td><p>Отображение собственных вставок</p></td>
<td><p>DBPROP_OWNINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Сохранение при прерывании</p></td>
<td><p>DBPROP_ABORTPRESERVE</p></td>
</tr>
<tr class="even">
<td><p>Сохранение при фиксации</p></td>
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
<td><p>Отчет о нескольких изменениях</p></td>
<td><p>DBPROP_REPORTMULTIPLECHANGES</p></td>
</tr>
<tr class="odd">
<td><p>Возврат ожидающих вставок</p></td>
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
<td><p>Уведомление о вставке строк</p></td>
<td><p>DBPROP_NOTIFYROWINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Права на строки</p></td>
<td><p>DBPROP_ROWRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о повторной синхронизации строк</p></td>
<td><p>DBPROP_NOTIFYROWRESYNCH</p></td>
</tr>
<tr class="odd">
<td><p>Потоковая модель для строк</p></td>
<td><p>DBPROP_ROWTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об отмене изменения строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOCHANGE</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление о отмене удаления строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDODELETE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об отмене вставки строки</p></td>
<td><p>DBPROP_NOTIFYROWUNDOINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Уведомление об обновлении строк</p></td>
<td><p>DBPROP_NOTIFYROWUPDATE</p></td>
</tr>
<tr class="even">
<td><p>Уведомление об изменении положения при получении набора строк</p></td>
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
<td><p>Пропуск удаленных закладок</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="even">
<td><p>Строгая идентификация строк</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
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
<td><p>Набор строк только для добавления</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
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
<td><p>Права на столбцы</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Уведомление о наборе столбцов</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
</tr>
<tr class="odd">
<td><p>Откладывание столбца</p></td>
<td><p>DBPROP_DEFERRED</p></td>
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
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
</tr>
<tr class="odd">
<td><p>Строки для мобильных устройств</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="even">
<td><p>IRowset</p></td>
<td><p>DBPROP_IRowset</p></td>
</tr>
<tr class="odd">
<td><p>ировсетчанже</p></td>
<td><p>DBPROP_IRowsetChange</p></td>
</tr>
<tr class="even">
<td><p>ировсетидентити</p></td>
<td><p>DBPROP_IRowsetIdentity</p></td>
</tr>
<tr class="odd">
<td><p>ировсетиндекс</p></td>
<td><p>DBPROP_IRowsetIndex</p></td>
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
<td><p>ировсетскролл</p></td>
<td><p>DBPROP_IRowsetScroll</p></td>
</tr>
<tr class="even">
<td><p>ировсетупдате</p></td>
<td><p>DBPROP_IRowsetUpdate</p></td>
</tr>
<tr class="odd">
<td><p>исекуентиалстреам</p></td>
<td><p>DBPROP_ISequentialStream</p></td>
</tr>
<tr class="even">
<td><p>Содержим</p></td>
<td><p>DBPROP_IStorage</p></td>
</tr>
<tr class="odd">
<td><p>IStream</p></td>
<td><p>DBPROP_IStream</p></td>
</tr>
<tr class="even">
<td><p>исуппортерроринфо</p></td>
<td><p>DBPROP_ISupportErrorInfo</p></td>
</tr>
<tr class="odd">
<td><p>Литеральные закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="even">
<td><p>Идентификация строк литералов</p></td>
<td><p>DBPROP_LITERALIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Режим блокировки</p></td>
<td><p>DBPROP_LOCKMODE</p></td>
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
<td><p>Видны другие изменения</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Видимые вставки других пользователей</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
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
<td><p>Данные сервера при вставке</p></td>
<td><p>DBPROP_SERVERDATAONINSERT</p></td>
</tr>
<tr class="odd">
<td><p>Пропуск удаленных закладок</p></td>
<td><p>DBPROP_BOOKMARKSKIP</p></td>
</tr>
<tr class="even">
<td><p>Строгая идентификация строк</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
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


## <a name="see-also"></a>См. также

Для получения подробных сведений о реализации и функциональных сведений о поставщике OLE DB для Microsoft Jet обратитесь к документации по поставщику OLE DB для Microsoft Jet в пакете MDAC SDK.

