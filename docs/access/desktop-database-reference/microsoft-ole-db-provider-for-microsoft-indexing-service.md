---
title: Microsoft OLE DB Provider for Microsoft Indexing Service
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 10af40231fc10e222f818896b3d65f44ac3d6d71
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481023"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a>Microsoft OLE DB Provider for Microsoft Indexing Service


**Применимо к**: Access 2013 | Office 2013

Поставщик Microsoft OLE DB для служб индексирования Microsoft предоставляет программный доступ только для чтения к файловой системе и данных веб-службой индексирования Microsoft. ADO приложений можно выполнять запросы SQL для извлечения сведений содержимое и файлы.

Поставщик свободных потоков и Юникод.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Для подключения к данным поставщиком, задайте **поставщика =** аргумент свойства [ConnectionString](connectionstring-property-ado.md) для:

```vb 
 
MSIDXS 
```

Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.

## <a name="typical-connection-string"></a>Типичная строка подключения

— Это строка соединения для данного поставщика:

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
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
<td><p>Задает поставщика OLE DB для службы индексирования. Обычно это единственный ключевого слова, указанного в строке подключения.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Задает имя каталога службы индексирования. Если это ключевое слово не указан, используется каталог системы по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Идентификатор языка</strong></p></td>
<td><p>Число уникальных 32-разрядная версия (например, 1033), который указывает параметры, связанные с языком пользователя. Эти параметры указывают способ форматирования даты и времени, элементы сортируются в алфавитном порядке, строк сравниваются и т. д. Если это ключевое слово не указан, используется идентификатор языкового стандарта системы по умолчанию.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Текст команды

Синтаксис запроса SQL службы индексирования состоит из расширения инструкции SQL-92 **ВЫБЕРИТЕ** и его **ОТПРАВИТЕЛЯ** и **ГДЕ** предложений. Результаты запроса возвращаются через строк OLE DB, который может использоваться с ADO и управлять как объекты [набора записей](recordset-object-ado.md) .

Поиск точного слова или фразы или использовать подстановочные знаки для поиска шаблонов или основам слов. Логика поиска может быть основана на логическое решения, Средневзвешенное термины или всего к другим слова. Также можно выполнить поиск по «бесплатную текст», который находит совпадений на основе значения, а не точное слова.

Поставщик не принимает вызовы хранимых процедур или простой таблице имен (например, для свойства [CommandType](commandtype-property-ado.md) всегда будет **adCmdText**).

## <a name="recordset-behavior"></a>Поведение набора записей

В следующей таблице перечислены функции, доступные с объектом **набора записей** , открытых с этим поставщиком. Доступен только тип статический курсор (**adOpenStatic**).

Для получения дополнительных сведений о поведении **набора записей** для вашей конфигурации поставщика, выполните метод [поддерживает](supports-method-ado.md) и перечисления коллекции [свойств](properties-collection-ado.md) **набора записей** для определения целесообразности поставщиком динамических свойства отсутствуют.

Доступность стандартными свойствами ADO **набора записей** :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Свойство</p></th>
<th><p>Availability</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="absolutepage-property-ado.md">AbsolutePage</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Закладка</a>*</p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>всегда <strong>adUseServer</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>всегда <strong>adOpenStatic</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>всегда <strong>как таковые</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">ФУНКЦИЯ EOF</a></p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType для</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>Недоступен</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Состояние</a></p></td>
<td><p>только для чтения</p></td>
</tr>
</tbody>
</table>


\*Закладки должна быть включена в поставщика в порядке для этой функции существует во **набора записей**.

Доступность стандартных способов ADO **набора записей** :

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Метод</p></th>
<th><p>Доступные?</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="cancel-method-ado.md">Отмена</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Копия</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Закрыть</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">Получение строк</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Перемещение</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Открытие</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="requery-method-ado.md">Обновление</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="supports-method-ado.md">Поддерживает</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="update-method-ado.md">обновление</a>.</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Нет</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

Сведения о реализации и функциональным сведения о поставщик Microsoft OLE DB для служб индексирования Microsoft обратитесь к Microsoft OLE DB Справочник программиста.

