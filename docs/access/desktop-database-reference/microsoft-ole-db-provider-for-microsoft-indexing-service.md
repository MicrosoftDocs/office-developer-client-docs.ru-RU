---
title: Поставщик Microsoft OLE DB для службы индексирования (Майкрософт)
TOCTitle: Microsoft OLE DB Provider for Microsoft Indexing Service
ms:assetid: 01c2e75c-950a-dd8a-2b20-bbd916315ec5
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248786(v=office.15)
ms:contentKeyID: 48542942
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ba27bfdf6cc1317b441e626c61784e2c50b589f1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288920"
---
# <a name="microsoft-ole-db-provider-for-microsoft-indexing-service"></a>Поставщик Microsoft OLE DB для службы индексирования (Майкрософт)


**Область применения**: Access 2013, Office 2013

Поставщик Microsoft OLE DB для Microsoft Indexing Service предоставляет программный доступ только для чтения к файловой системе и веб-данным, индексируемым службой индексирования Microsoft. Приложения ADO могут выдать запросы SQL для получения сведений о содержимом и свойствах файлов.

Поставщик доступен для бесплатных потоков и включен Юникод.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к поставщику, присвойте аргументу **provider =** свойство [ConnectionString](connectionstring-property-ado.md) значение:

```vb 
 
MSIDXS 
```

Считывание свойства [provider](provider-property-ado.md) также возвратит эту строку.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

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
<th><p>Ключевое слово</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Поставщик</strong></p></td>
<td><p>Указывает поставщика OLE DB для службы индексирования (Майкрософт). Как правило, это единственное ключевое слово, указанное в строке подключения.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Указывает имя каталога службы индексирования. Если это ключевое слово не задано, используется системный каталог по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Идентификатор языкового стандарта</strong></p></td>
<td><p>Задает уникальное 32-разрядное число (например, 1033), которое определяет параметры, связанные с языком пользователя. Эти установки указывают, как форматируется Дата и время, сортируются элементы в алфавитном порядке, сравниваются строки и т. д. Если это ключевое слово не задано, используется идентификатор языка системы по умолчанию.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Текст команды

Синтаксис запроса SQL службы индексирования состоит из расширений для оператора **SELECT** sql – 92 и предложений **from** и **WHERE** . Результаты запроса возвращаются с помощью наборов строк OLE DB, которые могут обрабатываться ADO и обрабатываться как объекты [Recordset](recordset-object-ado.md) .

Можно искать точные слова или фразы или использовать подстановочные знаки для поиска шаблонов или основных фрагментов слов. Логика поиска может основываться на логических решениях, взвешенных терминах или сходстве с другими словами. Вы также можете выполнять поиск по слову "свободный текст", который находит совпадения, в зависимости от значения, а не точных слов.

Поставщик не принимает вызовы хранимых процедур или простые имена таблиц (например, свойство [CommandType](commandtype-property-ado.md) всегда будет **адкмдтекст**).

## <a name="recordset-behavior"></a>Поведение набора записей

В следующих таблицах перечислены возможности, доступные при использовании объекта **Recordset** , открытого с помощью этого поставщика. Доступен только статический тип курсора (**адопенстатик**).

Для получения более подробных сведений о поведении **набора записей** для конфигурации поставщика [](supports-method-ado.md) запустите метод Supports и перечислите коллекцию [свойств](properties-collection-ado.md) объекта **Recordset** , чтобы определить, зависит ли от поставщика динамический имеются свойства.

Доступность стандартных свойств **записей** ADO:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Свойство</p></th>
<th><p>Доступность</p></th>
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
<td><p>всегда <strong>адусесервер</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>всегда <strong>адопенстатик</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>всегда <strong>адедитноне</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>только для чтения</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>чтение и запись</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>недоступно</p></td>
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
<td><p><a href="status-property-ado-recordset.md">Status</a></p></td>
<td><p>только для чтения</p></td>
</tr>
</tbody>
</table>


\*Для того чтобы эта функция существовала в **наборе записей**, в поставщике должны быть включены закладки.

Доступность стандартных методов **набора записей** ADO:

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Метод</p></th>
<th><p>Доступность?</p></th>
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
<td><p><a href="clone-method-ado.md">Clone</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Close</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">удаление</a>;</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="getrows-method-ado.md">GetRows</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="move-method-ado.md">Move</a></p></td>
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
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="supports-method-ado.md">Имеется</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="update-method-ado.md">обновление</a>;</p></td>
<td><p>Нет</p></td>
</tr>
<tr class="odd">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Нет</p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>См. также

Для получения подробных сведений о реализации и функциональных сведений о поставщике Microsoft OLE DB для Microsoft Indexing Service обратитесь к справочным материалам программиста Microsoft OLE DB.

