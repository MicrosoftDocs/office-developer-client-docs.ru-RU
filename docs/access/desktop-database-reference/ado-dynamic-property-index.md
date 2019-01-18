---
title: Индекс динамических свойств ADO
TOCTitle: ADO dynamic property index
ms:assetid: 437beced-b97a-894d-b08f-4a322629a5a6
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249202(v=office.15)
ms:contentKeyID: 48544502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2bfe788923d623300edac28f0f27534b3ffd8b32
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28703554"
---
# <a name="ado-dynamic-property-index"></a>Индекс динамических свойств ADO

**Применимо к**: Access 2013, Office 2013

Поставщики данных, поставщиков услуг и компоненты службы можно добавить динамические свойства коллекции **свойств** объектов неоткрытый [подключения](connection-object-ado.md) и [набора записей](recordset-object-ado.md) . Данный поставщик также вставить дополнительные свойства при открытии эти объекты. В разделе [Свойства динамического ADO](ado-dynamic-properties.md) перечислены некоторые из этих свойств. Больше, указанных для конкретных поставщиков в разделе [Приложение а: поставщиков](appendix-a-providers.md) .

В таблице ниже приведен cross-index имен ADO и OLE DB для каждого стандартных OLE DB поставщика динамические свойства. Ваше поставщики могут добавлять несколько свойств, чем перечисленных здесь. Определенные сведения о динамических свойств от поставщика обратитесь к документации поставщика.

Справочник программиста OLE DB указано имя свойства ADO по слову «Описание». Дополнительные сведения об этих стандартных свойств можно найти в Справочник программиста OLE DB. Поиск имени свойства OLE DB в индексе или в следующих разделах:

- Приложение c. свойства OLE DB

- Поддерживаемые свойства службы курсора

- Поддерживаемые свойства поставщика службы сохранения

- Свойства Поддерживаемые OLE DB поставщика удаленного доступа

## <a name="remarks"></a>Замечания

Обратите внимание на номера, используемые в cross-index.

(1) это свойство соответствует флаг типа Boolean, указывающее, следует ли использовать данный интерфейс. Имя свойства в эквивалентный OLE DB отображается, если он существует.

(2) свойство «Bookmarkable» ADO создается внутренне для обратной совместимости и назначается свойству OLE DB DBPROP\_IROWSETLOCATE. Это то же свойство, которое соответствует свойству ADO IRowsetLocate.

(3) ADO имя свойства, «Скрытые столбцы», называется иначе, чем имя свойства OLE DB описания, «Count скрытые столбцы».

(4) для иерархические наборы записей ADO «Максимальное число строк» свойство получает применять на все дочерние элементы. В зависимости от того, в том порядке, в котором возвращенных строк может содержать все, некоторые или нет дочерних элементов для каждого родительского или потерянного дочерние элементы в наборе результатов. Таким образом после изменения формы иерархические наборы записей, идентификатор для каждого дочернего должен быть уникальным. В общем случае поставщика [Услуг формирования Microsoft данных для OLE DB (MSDATASHAPE)](microsoft-data-shaping-service-for-ole-db-ado-service-provider.md) не разрешает различие между свойства, которые могут наследоваться от родительского сайта и те, которые не могут быть унаследованы.

(5) не применяется.

**Динамические свойства подключения**

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
<td><p>Передайте с указанные методы</p></td>
<td><p>DBPROP_BYREFACCESSORS</p></td>
</tr>
<tr class="even">
<td><p>Password</p></td>
<td><p>DBPROP_AUTH_PASSWORD</p></td>
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


**Свойства динамической набора записей**

Обратите внимание, что **Динамические свойства** объекта **набора записей** выйдет из области действия (становятся недоступными) при закрытии **набора записей** .

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
<td><p>IAccessor</p></td>
<td><p>DBPROP_IACCESSOR (1)</p></td>
</tr>
<tr class="even">
<td><p>IChapteredRowset</p></td>
<td><p>(1)</p></td>
</tr>
<tr class="odd">
<td><p>IColumnsInfo</p></td>
<td><p>DBPROP_ICOLUMNSINFO (1)</p></td>
</tr>
<tr class="even">
<td><p>IColumnsRowset</p></td>
<td><p>DBPROP_ICOLUMNSROWSET (1)</p></td>
</tr>
<tr class="odd">
<td><p>IConnectionPointContainer</p></td>
<td><p>DBPROP_ICONNECTIONPOINTCONTAINER (1)</p></td>
</tr>
<tr class="even">
<td><p>IConvertType</p></td>
<td><p>(1)</p></td>
</tr>
<tr class="odd">
<td><p>ILockBytes</p></td>
<td><p>DBPROP_ILOCKBYTES (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowset</p></td>
<td><p>DBPROP_IROWSET (1)</p></td>
</tr>
<tr class="odd">
<td><p>IDBAsynchStatus</p></td>
<td><p>DBPROP_IDBASYNCHSTATUS (1)</p></td>
</tr>
<tr class="even">
<td><p>IParentRowset</p></td>
<td><p>(1)</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetChange</p></td>
<td><p>DBPROP_IROWSETCHANGE (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetExactScroll</p></td>
<td><p>(1)</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetFind</p></td>
<td><p>DBPROP_IROWSETFIND (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetIdentity</p></td>
<td><p>DBPROP_IROWSETIDENTITY (1)</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetInfo</p></td>
<td><p>DBPROP_IROWSETINFO (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetLocate</p></td>
<td><p>DBPROP_IROWSETLOCATE (1)</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetRefresh</p></td>
<td><p>DBPROP_IROWSETREFRESH (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetResynch</p></td>
<td><p>(1)</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetScroll</p></td>
<td><p>DBPROP_IROWSETSCROLL (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetUpdate</p></td>
<td><p>DBPROP_IROWSETUPDATE (1)</p></td>
</tr>
<tr class="odd">
<td><p>IRowsetView</p></td>
<td><p>DBPROP_IROWSETVIEW (1)</p></td>
</tr>
<tr class="even">
<td><p>IRowsetIndex</p></td>
<td><p>DBPROP_IROWSETINDEX (1)</p></td>
</tr>
<tr class="odd">
<td><p>ISequentialStream</p></td>
<td><p>DBPROP_ISEQUENTIALSTREAM (1)</p></td>
</tr>
<tr class="even">
<td><p>IStorage</p></td>
<td><p>DBPROP_ISTORAGE (1)</p></td>
</tr>
<tr class="odd">
<td><p>IStream</p></td>
<td><p>DBPROP_ISTREAM (1)</p></td>
</tr>
<tr class="even">
<td><p>ISupportErrorInfo</p></td>
<td><p>DBPROP_ISUPPORTERRORINFO (1)</p></td>
</tr>
<tr class="odd">
<td><p>Порядок доступа</p></td>
<td><p>DBPROP_ACCESSORDER</p></td>
</tr>
<tr class="even">
<td><p>Только для добавления строк</p></td>
<td><p>DBPROP_APPENDONLY</p></td>
</tr>
<tr class="odd">
<td><p>Обработка асинхронных строк</p></td>
<td><p>DBPROP_ROWSET_ASYNCH</p></td>
</tr>
<tr class="even">
<td><p>Автоматическое обновление ссылок</p></td>
<td><p>DBPROP_ADC_AUTORECALC</p></td>
</tr>
<tr class="odd">
<td><p>Размер выборки фона</p></td>
<td><p>DBPROP_ASYNCHFETCHSIZE</p></td>
</tr>
<tr class="even">
<td><p>Приоритет потока фона</p></td>
<td><p>DBPROP_ASYNCHTHREADPRIORITY</p></td>
</tr>
<tr class="odd">
<td><p>Размер пакета</p></td>
<td><p>DBPROP_ADC_BATCHSIZE</p></td>
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
<td><p>DBPROP_IROWSETLOCATE (2)</p></td>
</tr>
<tr class="odd">
<td><p>Упорядоченные закладки</p></td>
<td><p>DBPROP_ORDEREDBOOKMARKS</p></td>
</tr>
<tr class="even">
<td><p>Кэш дочерних строк</p></td>
<td><p>DBPROP_ADC_CACHECHILDROWS</p></td>
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
<td><p>Время ожидания команды</p></td>
<td><p>DBPROP_COMMANDTIMEOUT</p></td>
</tr>
<tr class="odd">
<td><p>Версия модуля текущей позиции</p></td>
<td><p>DBPROP_ADC_CEVER</p></td>
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
<td><p>Операции фильтрации</p></td>
<td><p>DBPROP_FILTERCOMPAREOPS</p></td>
</tr>
<tr class="even">
<td><p>Найдите операций</p></td>
<td><p>DBPROP_FINDCOMPAREOPS</p></td>
</tr>
<tr class="odd">
<td><p>Скрытые столбцы (количество)</p></td>
<td><p>DBPROP_HIDDENCOLUMNS (3)</p></td>
</tr>
<tr class="even">
<td><p>Хранение строк</p></td>
<td><p>DBPROP_CANHOLDROWS</p></td>
</tr>
<tr class="odd">
<td><p>Немобильные строки</p></td>
<td><p>DBPROP_IMMOBILEROWS</p></td>
</tr>
<tr class="even">
<td><p>Размер начальной выборки</p></td>
<td><p>DBPROP_ASYNCHPREFETCHSIZE</p></td>
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
<td><p>Обслуживание изменений состояния</p></td>
<td><p>DBPROP_ADC_MAINTAINCHANGESTATUS</p></td>
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
<td><p>DBPROP_MAXROWS (4)</p></td>
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
<td><p>Private1</p></td>
<td><p>(5)</p></td>
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
<td><p>Изменить форму имя</p></td>
<td><p>DBPROP_ADC_RESHAPENAME</p></td>
</tr>
<tr class="odd">
<td><p>Команда синхронизации</p></td>
<td><p>DBPROP_ADC_CUSTOMRESYNCH</p></td>
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
<td><p>Серверный курсор</p></td>
<td><p>DBPROP_SERVERCURSOR</p></td>
</tr>
<tr class="odd">
<td><p>Пропустить удаленных закладки</p></td>
<td><p>DBPROP_BOOKMARKSKIPPED</p></td>
</tr>
<tr class="even">
<td><p>Строка строгого удостоверений</p></td>
<td><p>DBPROP_STRONGIDENTITY</p></td>
</tr>
<tr class="odd">
<td><p>Уникальный каталога</p></td>
<td><p>DBPROP_ADC_UNIQUECATALOG</p></td>
</tr>
<tr class="even">
<td><p>Уникальные строки</p></td>
<td><p>DBPROP_UNIQUEROWS</p></td>
</tr>
<tr class="odd">
<td><p>Уникальный схемы</p></td>
<td><p>DBPROP_ADC_UNIQUESCHEMA</p></td>
</tr>
<tr class="even">
<td><p>Уникальная таблица</p></td>
<td><p>DBPROP_ADC_UNIQUETABLE</p></td>
</tr>
<tr class="odd">
<td><p>Возможности обновления</p></td>
<td><p>DBPROP_UPDATABILITY</p></td>
</tr>
<tr class="even">
<td><p>Обновление критериев</p></td>
<td><p>DBPROP_ADC_UPDATECRITERIA</p></td>
</tr>
<tr class="odd">
<td><p>Обновление повторной синхронизации</p></td>
<td><p>DBPROP_ADC_UPDATERESYNC</p></td>
</tr>
<tr class="even">
<td><p>Использование закладок</p></td>
<td><p>DBPROP_BOOKMARKS</p></td>
</tr>
</tbody>
</table>

