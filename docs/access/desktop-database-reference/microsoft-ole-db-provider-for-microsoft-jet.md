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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712843"
---
# <a name="microsoft-ole-db-provider-for-microsoft-jet"></a>Поставщик Microsoft OLE DB для Microsoft Jet

**Применимо к**: Access 2013, Office 2013

Поставщик OLE DB для Microsoft Jet позволяет ADO для доступа к базам данных Microsoft Jet.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Для подключения к данным поставщиком, задайте для свойства [ConnectionString](connectionstring-property-ado.md) для аргумента *поставщика* :

```vb 
 
Microsoft.Jet.OLEDB.4.0 
```

Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.

## <a name="typical-connection-string"></a>Типичная строка подключения

— Это строка соединения для данного поставщика:

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
<th><p>Keyword</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Поставщик</strong></p></td>
<td><p>Задает поставщика OLE DB для Microsoft Jet.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Указывает базу данных путь и имя файла (например, c:\Northwind.mdb).</p></td>
</tr>
<tr class="odd">
<td><p><strong>Идентификатор пользователя</strong></p></td>
<td><p>Задает имя пользователя. Если это ключевое слово не указан, строка, &quot;администратора&quot;, используемый по умолчанию.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Задает пароль пользователя. Если это ключевое слово не указан, пустая строка (&quot;&quot;), используемый по умолчанию.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Параметры подключения от поставщика

Поставщик OLE DB для Microsoft Jet поддерживает несколько динамические свойства от поставщика дополнение к тем определяется ADO. Как вместе с другими параметрами **подключения** могут устанавливаться с помощью **Свойства** коллекции объект **подключения** или в качестве части строки подключения.

В следующей таблице перечислены эти свойства имя соответствующего свойства OLE DB в скобки.

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
<td><p>Освобожденное место сумма Jet OLEDB:Compact<br />
(DBPROP_JETOLEDB_COMPACTFREESPACESIZE)</p></td>
<td><p>Указывает оценку дискового пространства, в байтах, который может быть восстановлена путем сжатие базы данных. Это значение допустимо только после установления подключения к базе данных.</p></td>
</tr>
<tr class="even">
<td><p>Элемент управления OLEDB:Connection Jet<br />
(DBPROP_JETOLEDB_CONNECTIONCONTROL)</p></td>
<td><p>Указывает, будет ли пользователи могут подключаться к базе данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: создание Системная база данных<br />
(DBPROP_JETOLEDB_CREATESYSTEMDATABASE)</p></td>
<td><p>Указывает, следует ли создавать Системная база данных при создании нового источника данных.</p></td>
</tr>
<tr class="even">
<td><p>Режим блокировки OLEDB:Database Jet<br />
(DBPROP_JETOLEDB_DATABASELOCKMODE)</p></td>
<td><p>Указывает режим блокировки для этой базы данных. Первый пользователю открывать базу данных определяет режим, используемый при открытом базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Пароль OLEDB:Database Jet<br />
(DBPROP_JETOLEDB_DATABASEPASSWORD)</p></td>
<td><p>Указывает пароль базы данных.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: не копировать языковой стандарт на компакт<br />
(DBPROP_JETOLEDB_COMPACT_DONTCOPYLOCALE)</p></td>
<td><p>Указывает, следует ли Jet скопировать сведения о языковом стандарте при сжатии базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: шифрование базы данных<br />
(DBPROP_JETOLEDB_ENCRYPTDATABASE)</p></td>
<td><p>Указывает, должен быть зашифрован сжатии баз данных. Если это свойство не задано, сжатии базы данных будет шифроваться, если также зашифрованные исходной базы данных.</p></td>
</tr>
<tr class="even">
<td><p>Тип OLEDB:Engine Jet<br />
(DBPROP_JETOLEDB_ENGINE)</p></td>
<td><p>Указывает, подсистема хранилища для доступа к текущей хранилищу данных.</p></td>
</tr>
<tr class="odd">
<td><p>Асинхронная задержка Jet OLEDB:Exclusive<br />
(DBPROP_JETOLEDB_EXCLUSIVEASYNCDELAY)</p></td>
<td><p>Указывает максимальную длину время в миллисекундах, которые Jet может отложить асинхронных операций записи на диск при открытии исключительно базы данных. Это свойство игнорируется, если <strong>Время ожидания транзакций OLEDB:Flush Jet</strong> не задано значение 0.</p></td>
</tr>
<tr class="even">
<td><p>Время ожидания транзакций OLEDB:Flush Jet<br />
(DBPROP_JETOLEDB_FLUSHTRANSACTIONTIMEOUT)</p></td>
<td><p>Указывает время ожидания до фактически записи данных, сохраненных в кэше для асинхронной записи на диск. Этот параметр переопределяет значения для <strong>Jet OLEDB: общих асинхронная задержка</strong> и <strong>Jet OLEDB:Exclusive асинхронная задержка</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: глобальные массовых операций<br />
(DBPROP_JETOLEDB_GLOBALBULKNOTRANSACTIONS)</p></td>
<td><p>Указывает, будет ли в рамках транзакции SQL массовых операций.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: глобальные частичное массового операций<br />
(DBPROP_JETOLEDB_GLOBALBULKPARTIAL)</p></td>
<td><p>Указывает пароль, используемый для открытия базы данных.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: неявных зафиксировать синхронизации<br />
(DBPROP_JETOLEDB_IMPLICITCOMMITSYNC)</p></td>
<td><p>Указывает, записываются ли изменения, внесенные в внутренних неявных транзакций в режиме синхронными и асинхронными.</p></td>
</tr>
<tr class="even">
<td><p>Задержка OLEDB:Lock Jet<br />
(DBPROP_JETOLEDB_LOCKDELAY)</p></td>
<td><p>Указывает время в миллисекундах ожидания запроса блокировки после Предыдущая попытка не удалось выполнить.</p></td>
</tr>
<tr class="odd">
<td><p>Повтор OLEDB:Lock Jet<br />
(DBPROP_JETOLEDB_LOCKRETRY)</p></td>
<td><p>Указывает, сколько раз при попытке доступа к заблокированной странице повторяется.</p></td>
</tr>
<tr class="even">
<td><p>Размер буфера OLEDB:Max Jet<br />
(DBPROP_JETOLEDB_MAXBUFFERSIZE)</p></td>
<td><p>Указывает максимальный объем памяти, в килобайтах Jet может использовать до начала записи изменений на диск.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Max блокировок в файл<br />
(DBPROP_JETOLEDB_MAXLOCKSPERFILE)</p></td>
<td><p>Указывает максимальное количество блокировок, которые Jet можно поместить в базе данных. Значение по умолчанию — 9500.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: новый пароль базы данных<br />
(DBPROP_JETOLEDB_NEWDATABASEPASSWORD)</p></td>
<td><p>Указывает новый пароль для этой базы данных. Старый пароль хранится в <strong>Jet OLEDB:Database пароль</strong>.</p></td>
</tr>
<tr class="odd">
<td><p>Время ожидания команды OLEDB:ODBC Jet<br />
(DBPROP_JETOLEDB_ODBCCOMMANDTIMEOUT)</p></td>
<td><p>Указывает, что количество миллисекунд до удаленный запрос ODBC с Jet будет времени ожидания.</p></td>
</tr>
<tr class="even">
<td><p>Блокировки OLEDB:Page Jet для блокировки таблицы<br />
(DBPROP_JETOLEDB_PAGELOCKSTOTABLELOCK)</p></td>
<td><p>Указывает, сколько страниц необходимо будут удалены в транзакции, прежде чем повышение уровня блокировки для блокировки таблицы. Если это значение равно 0, блокировки никогда не повышается.</p></td>
</tr>
<tr class="odd">
<td><p>Время ожидания OLEDB:Page Jet<br />
(DBPROP_JETOLEDB_PAGETIMEOUT)</p></td>
<td><p>Указывает количество миллисекунд ожидания Jet перед проверкой ли кэш устаревший с помощью файла базы данных.</p></td>
</tr>
<tr class="even">
<td><p>Страницы табличное Long Jet OLEDB:Recycle<br />
(DBPROP_JETOLEDB_RECYCLELONGVALUEPAGES)</p></td>
<td><p>Указывает, следует ли Jet пытаться агрессивное освобождение страниц больших двоичных ОБЪЕКТОВ, когда их освобождения.</p></td>
</tr>
<tr class="odd">
<td><p>Путь OLEDB:Registry Jet<br />
(DBPROP_JETOLEDB_REGPATH)</p></td>
<td><p>Указывает ключ реестра Windows, который содержит значения для базы данных Jet.</p></td>
</tr>
<tr class="even">
<td><p>Статистика ISAM OLEDB:Reset Jet<br />
(DBPROP_JETOLEDB_RESETISAMSTATS)</p></td>
<td><p>Указывает, должно ли схема <strong>набора записей</strong> DBSCHEMA_JETOLEDB_ISAMSTATS сбросить его счетчики производительности после возврата сведений о производительности.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: общих асинхронная задержка<br />
(DBPROP_JETOLEDB_SHAREDASYNCDELAY)</p></td>
<td><p>Указывает максимальное время в миллисекундах, Jet может отложить асинхронных операций записи на диск при открытии базы данных в режиме нескольких пользователей.</p></td>
</tr>
<tr class="even">
<td><p>База данных Microsoft Jet OLEDB: System<br />
(DBPROP_JETOLEDB_SYSDBPATH)</p></td>
<td><p>Указывает путь и имя файла для файла рабочей группы (системная база данных).</p></td>
</tr>
<tr class="odd">
<td><p>Режим фиксации OLEDB:Transaction Jet<br />
(DBPROP_JETOLEDB_TXNCOMMITMODE)</p></td>
<td><p>Указывает, является ли Jet записывает данные на диск синхронно или асинхронно при фиксации транзакции.</p></td>
</tr>
<tr class="even">
<td><p>Синхронизация зафиксировать OLEDB:User Jet<br />
(DBPROP_JETOLEDB_USERCOMMITSYNC)</p></td>
<td><p>Указывает, записываются ли изменения, внесенные в транзакции в режиме синхронными и асинхронными.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-recordset-and-command-properties"></a>Свойства команды и записей от поставщика

Поставщик Jet также поддерживает несколько свойств **набора записей** и **команду** от поставщика. Эти свойства доступны и задается с помощью коллекции **свойств** объекта **команду** или **набора записей** . В таблице перечислены имя свойства ADO и OLE DB название в скобки.

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
<td><p>Транзакции OLEDB:Bulk Jet<br />
(DBPROP_JETOLEDB_BULKNOTRANSACTIONS)</p></td>
<td><p>Указывает, будет ли в рамках транзакции SQL массовых операций. Больших массовых операций может завершиться неудачно в рамках транзакции, из-за задержки ресурсов.</p></td>
</tr>
<tr class="even">
<td><p>Курсоры Fat OLEDB:Enable Jet<br />
(DBPROP_JETOLEDB_ENABLEFATCURSOR)</p></td>
<td><p>Указывает, следует ли Jet кэшировать несколько строк при заполнении набора записей для источников удаленной строки.</p></td>
</tr>
<tr class="odd">
<td><p>Размер кэша курсор OLEDB:Fat Jet<br />
(DBPROP_JETOLEDB_FATCURSORMAXROWS)</p></td>
<td><p>Указывает число строк, кэш при использовании кэширования строку хранения удаленных данных. Это значение используется только <strong>Fat курсоры Jet OLEDB:Enable</strong> имеет значение True.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: несогласованные<br />
(DBPROP_JETOLEDB_INCONSISTENT)</p></td>
<td><p>Указывает, разрешить ли результаты запроса несогласованных обновлений.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: блокировка степень детализации<br />
(DBPROP_JETOLEDB_LOCKGRANULARITY)</p></td>
<td><p>Указывает, открыт ли таблицы с помощью блокировка на уровне.</p></td>
</tr>
<tr class="even">
<td><p>Оператор к серверу OLEDB:ODBC Jet<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGH)</p></td>
<td><p>Указывает, что Jet должен передаваться текст SQL в объект <strong>команды</strong> для серверного компонента без изменений.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB:Partial массовых операций<br />
(DBPROP_JETOLEDB_BULKPARTIAL)</p></td>
<td><p>Задает поведение Jet при операции SQL DML с ошибкой.</p></td>
</tr>
<tr class="even">
<td><p>OLEDB:Pass Jet через массовых операций запросов<br />
(DBPROP_JETOLEDB_PASSTHROUGHBULKOP)</p></td>
<td><p>Указывает, запросов, которые не возвращает <strong>записей</strong> передаются ли изменена к источнику данных.</p></td>
</tr>
<tr class="odd">
<td><p>Строка подключения OLEDB:Pass Jet посредством запроса<br />
(DBPROP_JETOLEDB_ODBCPASSTHROUGHCONNECTSTRING)</p></td>
<td><p>Указывает Jet строку подключения, используемую для подключения к удаленному хранилищу. Это значение используется только <strong>Jet OLEDB:ODBC к серверу оператор</strong> имеет значение True.</p></td>
</tr>
<tr class="even">
<td><p>Jet OLEDB: хранимых запросов<br />
(DBPROP_JETOLEDB_STOREDQUERY)</p></td>
<td><p>Указывает, будет ли текст команды должны обрабатываются как сохраненного запроса вместо команды SQL.</p></td>
</tr>
<tr class="odd">
<td><p>Jet OLEDB: проверка правил набора<br />
(DBPROP_JETOLEDB_VALIDATEONSET)</p></td>
<td><p>Указывает, будет ли правила проверки Jet вычисляются при имеет значение столбца или изменения применяются к базе данных.</p></td>
</tr>
</tbody>
</table>


По умолчанию поставщик OLE DB для Microsoft Jet открывается в режиме чтения и записи баз данных Microsoft Jet. Чтобы открыть базу данных в режим только для чтения, присвойте свойству [режим](mode-property-ado.md) объекта ADO- **подключения** в **adModeRead**.

## <a name="command-object-usage"></a>Использование объекта команды

Текст команды в объекте [команда](command-object-ado.md) использует диалект Microsoft Jet SQL. Можно указать возвращающие строки запросов, запросов и имена таблиц в текст команды; Тем не менее хранимые процедуры не поддерживаются и не должен быть указан.

## <a name="recordset-behavior"></a>Поведение набора записей

Базы данных Microsoft Jet не поддерживает динамические курсоры. Таким образом поставщик OLE DB для Microsoft Jet не поддерживает тип **adLockDynamic** курсора. При запросе динамического курсора поставщик вернуть курсор набора ключей и сброс свойство [CursorType](cursortype-property-ado.md) указывает, что возвращаемые тип [набора записей](recordset-object-ado.md) . Затем, если запрашивается обновляемых **записей** (**LockType для** — **adLockOptimistic**, **adLockBatchOptimistic**или **adLockPessimistic**) также вернет курсор набора ключей и Сброс **CursorType** поставщика свойство.

## <a name="dynamic-properties"></a>Динамические свойства

Поставщик OLE DB для Microsoft Jet вставляет несколько динамических свойств в коллекцию **свойств** объектов неоткрытый [подключения](connection-object-ado.md), [записей](recordset-object-ado.md)и [команды](command-object-ado.md) .

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
<td><p>Модель потоков объекта источника данных</p></td>
<td><p>DBPROP_DSOTHREADMODEL</p></td>
</tr>
<tr class="even">
<td><p>Имя СУБД</p></td>
<td><p>DBPROP_DBMSNAME</p></td>
</tr>
<tr class="odd">
<td><p>Версия СУБД</p></td>
<td><p>DBPROP_DBMSVER</p></td>
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
<td><p>Уровни изоляции</p></td>
<td><p>DBPROP_SUPPORTEDTXNISOLEVELS</p></td>
</tr>
<tr class="even">
<td><p>Хранение изоляции</p></td>
<td><p>DBPROP_SUPPORTEDTXNISORETAIN</p></td>
</tr>
<tr class="odd">
<td><p>Идентификатор языка</p></td>
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
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
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
<td><p>Только для добавления строк</p></td>
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
<td><p>Кэш отложенной столбцов</p></td>
<td><p>DBPROP_CACHEDEFERRED</p></td>
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
<td><p>Столбец для записи</p></td>
<td><p>DBPROP_MAYWRITECOLUMN</p></td>
</tr>
<tr class="even">
<td><p>Отложите столбца</p></td>
<td><p>DBPROP_DEFERRED</p></td>
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
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
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
<td><p>Использование памяти</p></td>
<td><p>ОПРЕДЕЛЕН</p></td>
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
<td><p>Пропустить удаленных закладки</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="even">
<td><p>Строка строгого удостоверений</p></td>
<td><p>DBPROP_STRONGITDENTITY</p></td>
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
<td><p>Только для добавления строк</p></td>
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
<td><p>Права доступа столбца</p></td>
<td><p>DBPROP_COLUMNRESTRICT</p></td>
</tr>
<tr class="even">
<td><p>Столбец набор уведомлений</p></td>
<td><p>DBPROP_NOTIFYCOLUMNSET</p></td>
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
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILockBytes</p></td>
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
<td><p>Литерал закладки</p></td>
<td><p>DBPROP_LITERALBOOKMARKS</p></td>
</tr>
<tr class="even">
<td><p>Удостоверение литерала строки</p></td>
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
<td><p>Видны прочие изменения</p></td>
<td><p>DBPROP_OTHERUPDATEDELETE</p></td>
</tr>
<tr class="odd">
<td><p>Других пользователей вставки видимым</p></td>
<td><p>DBPROP_OTHERINSERT</p></td>
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
</tbody>
</table>


## <a name="see-also"></a>См. также

Сведения о реализации и функциональным сведения о поставщика OLE DB для Microsoft Jet обратитесь к поставщика OLE DB для Microsoft Jet документации в пакете SDK MDAC.

