---
title: Поставщик Microsoft OLE DB для службы Microsoft Active Directory
TOCTitle: Microsoft OLE DB Provider for Microsoft Active Directory Service
ms:assetid: 92d1c967-aa61-f3b5-1c0a-301ef236894c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249647(v=office.15)
ms:contentKeyID: 48546385
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23e1cab32fee6103a046219a7cda8c90f02d9f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288941"
---
# <a name="microsoft-ole-db-provider-for-microsoft-active-directory-service"></a>Поставщик Microsoft OLE DB для службы Microsoft Active Directory

**Область применения**: Access 2013, Office 2013

Поставщик служб Microsoft Active Directory Service Interfaces (ADSI) позволяет ADO подключаться к неоднородным службам каталогов с помощью ADSI. Это предоставляет приложениям ADO доступ только для чтения к службам каталогов Microsoft Windows NT 4.0 и Microsoft Windows 2000, а также к любым службам каталогов, совместимым с LDAP и Novell Directory Services. Сам ADSI основан на модели поставщика, поэтому если новый поставщик дает доступ к другому каталогу, приложение ADO сможет получить к нему доступ без проблем. Поставщик ADSI является бесплатным и включен юникодом.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к этому поставщику, установите **аргумент поставщика** свойства [ConnectionString:](connectionstring-property-ado.md)

```vb 
 
ADSDSOObject 
```

Чтение свойства [Provider](provider-property-ado.md) также вернет эту строку.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```vb 
 
"Provider=ADSDSOObject;User ID=userName;Password=userPassword;" 
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
<td><p>Указывает поставщика OLE DB для службы Microsoft Active Directory.</p></td>
</tr>
<tr class="even">
<td><p><strong>Идентификатор пользователя</strong></p></td>
<td><p>Задает имя пользователя. Если это ключевое слово пропущено, используется текущий логотип.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Password</strong></p></td>
<td><p>Указывает пароль пользователя. Если это ключевое слово пропущено, используется текущий логотип.</p></td>
</tr>
</tbody>
</table>


**Командный текст**

Текстовая строка из четырех команд распознается поставщиком в следующем синтаксисе:

`"Root; Filter; Attributes[; Scope]"`

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>Root</em></p></td>
<td><p>Указывает объект <strong>ADsPath,</strong> с которого следует начать поиск (то есть корень поиска).</p></td>
</tr>
<tr class="even">
<td><p><em>Filter</em></p></td>
<td><p>Указывает фильтр поиска в формате RFC 1960.</p></td>
</tr>
<tr class="odd">
<td><p><em>Attributes</em></p></td>
<td><p>Указывает список атрибутов, возвращаемого с запятой.</p></td>
</tr>
<tr class="even">
<td><p><em>Scope</em></p></td>
<td><p>Необязательный параметр. <strong>Строка,</strong> которая указывает область поиска. Может быть одним из следующих: Base — поиск только базового объекта (корень поиска).<br />
OneLevel — поиск только одного уровня.<br />
Subtree — поиск всего подтрия.</p></td>
</tr>
</tbody>
</table>


Пример.

```vb 
 
"<LDAP://DC=ArcadiaBay,DC=COM>;(objectClass=*);sn, givenName; subtree" 
```

Поставщик также поддерживает SQL SELECT для командного текста. Пример.

```vb 
 
"SELECT title, telephoneNumber From 'LDAP://DC=Microsoft, DC=COM' WHERE 
objectClass='user' AND objectCategory='Person'" 
```

Поставщик не принимает сохраненные вызовы процедур или простые имена таблиц (например, свойство [CommandType](commandtype-property-ado.md) всегда **будет adCmdText).** Дополнительные описания текстовых элементов команд см. в документации по интерфейсам службы Active Directory.

## <a name="recordset-behavior"></a>Поведение наборов записей

В следующих таблицах перечислить функции, доступные на [объекте Recordset,](recordset-object-ado.md) открытом с помощью этого поставщика. Доступен только тип статического курсора **(adOpenStatic).**

Дополнительные сведения о поведении **Recordset** для конфигурации поставщика запустите метод [Supports](supports-method-ado.md) и введите коллекцию [Свойств](properties-collection-ado.md) в **наборе Recordset,** чтобы определить, присутствуют ли динамические свойства конкретного поставщика.

Доступность стандартных свойств ADO **Recordset:**

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
<td><p><a href="bookmark-property-ado.md">Bookmark</a></p></td>
<td><p>чтение и написание</p></td>
</tr>
<tr class="even">
<td><p><a href="cachesize-property-ado.md">CacheSize</a></p></td>
<td><p>чтение и написание</p></td>
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
<td><p>всегда <strong>adEditNone</strong></p></td>
</tr>
<tr class="even">
<td><p><a href="bof-eof-properties-ado.md">EOF</a></p></td>
<td><p>read-only</p></td>
</tr>
<tr class="odd">
<td><p><a href="filter-property-ado.md">Filter</a></p></td>
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
<td><p><a href="state-property-ado.md">Состояние</a></p></td>
<td><p>read-only</p></td>
</tr>
<tr class="even">
<td><p><a href="status-property-ado-recordset.md">Состояние</a></p></td>
<td><p>read-only</p></td>
</tr>
</tbody>
</table>


Доступность стандартных методов ADO **Recordset:**

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Метод</p></th>
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
<td><p>Нет</p></td>
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
<td><p><a href="delete-method-ado-recordset.md">Delete</a></p></td>
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
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveLast</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveNext</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-recordset.md">Open</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Requery</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Resync</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Поддерживает</a></p></td>
<td><p>Да</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">Обновление</a></p></td>
<td><p>Нет</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Нет</p></td>
</tr>
</tbody>
</table>

