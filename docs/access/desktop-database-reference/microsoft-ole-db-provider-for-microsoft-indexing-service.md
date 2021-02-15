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

Поставщик Microsoft OLE DB для службы индексации Майкрософт предоставляет программный доступ только для чтения к файловой системе и веб-данным, индексным службой Microsoft Indexing Service. Приложения ADO могут SQL запросы для получения сведений о содержимом и свойстве файла.

Поставщик имеет свободный поток и Юникод включен.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к этому поставщику, установите для **аргумента Provider=** свойство [ConnectionString:](connectionstring-property-ado.md)

```vb 
 
MSIDXS 
```

При [чтении свойства Provider](provider-property-ado.md) также будет возвращена эта строка.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```vb 
 
"Provider=MSIDXS;Data Source=myCatalog;Locale Identifier=nnnn;" 
```

Строка состоит из таких ключевых слов:

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
<td><p>Указывает поставщика OLE DB для службы индексации Майкрософт. Обычно это единственное ключевое слово, указанное в строке подключения.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Указывает имя каталога службы индексации. Если это ключевое слово не указано, используется системный каталог по умолчанию.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Код локального идентификатора</strong></p></td>
<td><p>Указывает уникальный 32-битный номер (например, 1033), который определяет параметры, связанные с языком пользователя. Эти параметры указывают, как форматированы даты и время, элементы отсортированы в алфавитном порядке, сравниваются строки и так далее. Если это ключевое слово не указано, используется идентификатор стандартного системного региональных стандарта.</p></td>
</tr>
</tbody>
</table>


## <a name="command-text"></a>Текст команды

Синтаксис SQL службы индексации состоит из расширений для заявления SQL-92 **SELECT** и его предложений **FROM** и **WHERE.** Результаты запроса возвращаются с помощью наборов строк OLE DB, которые могут быть потребляться ADO и управляться как [объекты Recordset.](recordset-object-ado.md)

Вы можете искать точные слова или фразы или использовать под шаблоны для поиска шаблонов или стеблей слов. Логика поиска может основываться на логических решениях, взвешеных терминах или близости к другим словам. Вы также можете искать по слову "свободный текст", который находит совпадения по значению, а не точным словам.

Поставщик не принимает хранимые вызовы процедур или простые имена таблиц (например, свойство [CommandType](commandtype-property-ado.md) всегда будет **adCmdText).**

## <a name="recordset-behavior"></a>Поведение наборов записей

В следующих таблицах фиксировать функции, доступные с **объектом Recordset,** открытым у этого поставщика. Доступен только тип статического курсора **(adOpenStatic).**

Для получения более подробных сведений о поведении **объекта Recordset** для конфигурации поставщика запустите метод [Supports](supports-method-ado.md) и нумеруйте коллекцию [свойств](properties-collection-ado.md) объекта **Recordset,** чтобы определить, присутствуют ли динамические свойства для конкретного поставщика.

Доступность стандартных свойств объекта **ADO Recordset:**

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
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="absoluteposition-property-ado.md">AbsolutePosition</a></p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="activeconnection-property-ado.md">ActiveConnection</a></p></td>
<td><p>read-only</p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">BOF</a></p></td>
<td><p>read-only</p></td>
</tr>
<tr class="odd">
<td><p><a href="bookmark-property-ado.md">Закладка</a>*</p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="cursorlocation-property-ado.md">CursorLocation</a></p></td>
<td><p>always <strong>adUseServer</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="cursortype-property-ado.md">CursorType</a></p></td>
<td><p>always <strong>adOpenStatic</strong></p></td>
</tr>
<tr class="odd">
<td><p><a href="editmode-property-ado.md">EditMode</a></p></td>
<td><p>always <strong>adEditNone</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>read-only</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Фильтр</a></p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="locktype-property-ado.md">LockType</a></p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="marshaloptions-property-ado.md">MarshalOptions</a></p></td>
<td><p>недоступен</p></td>
</tr>
<tr class="even">
<td><p><a href="maxrecords-property-ado.md">MaxRecords</a></p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="pagecount-property-ado.md">PageCount</a></p></td>
<td><p>read-only</p></td>
</tr>
<tr class="even">
<td><p><a href="pagesize-property-ado.md">PageSize</a></p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="recordcount-property-ado.md">RecordCount</a></p></td>
<td><p>read-only</p></td>
</tr>
<tr class="even">
<td><p><a href="source-property-ado-recordset.md">Source</a></p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="odd">
<td><p><a href="state-property-ado.md">State</a></p></td>
<td><p>read-only</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Состояние</a></p></td>
<td><p>read-only</p></td>
</tr>
</tbody>
</table>


\*Чтобы эта функция существовала в наборе **записей,** необходимо включить закладки у поставщика.

Доступность стандартных методов ADO **Recordset:**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Method</p></th>
<th><p>Доступно?</p></th>
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

Подробные сведения о реализации и функциональные сведения о поставщике Microsoft OLE DB для службы индексации Майкрософт можно получить в справочнике программиста Microsoft OLE DB.

