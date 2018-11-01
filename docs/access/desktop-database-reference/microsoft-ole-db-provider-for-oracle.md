---
title: Поставщик Microsoft OLE DB для Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 7e473176ae6a34d04fc316a8d5075e414f6c8e98
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25868149"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a>Поставщик Microsoft OLE DB для Oracle

**Применимо к**: Access 2013, Office 2013

Поставщик Microsoft OLE DB для Oracle позволяет ADO для доступа к базам данных Oracle.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Для подключения к данным поставщиком, задайте для свойства [ConnectionString](connectionstring-property-ado.md) для аргумента *поставщика* :

```vb 
 
MSDAORA 
```

Чтение свойства [поставщика](provider-property-ado.md) будет возвращать также этой строки.

Запрос соединения с набором ключей или динамический курсор при выполнении в базе данных Oracle, возникает ошибка. Oracle поддерживает только статический курсор только для чтения.

## <a name="typical-connection-string"></a>Типичная строка подключения

— Это строка соединения для данного поставщика:

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
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
<td><p>Задает поставщика OLE DB для Oracle.</p></td>
</tr>
<tr class="even">
<td><p><strong>Источник данных</strong></p></td>
<td><p>Указывает имя сервера.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Идентификатор пользователя</strong></p></td>
<td><p>Задает имя пользователя.</p></td>
</tr>
<tr class="even">
<td><p><strong>Password</strong></p></td>
<td><p>Задает пароль пользователя.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Параметры подключения от поставщика

Поставщик поддерживает несколько параметров подключения для конкретного поставщика дополнение к тем определяется ADO. Как с помощью свойства подключения ADO, эти свойства от поставщика может быть задано посредством коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или как часть **ConnectionString**.

Эти параметры подробно описаны в Справочник программиста OLE DB. ( [Индекс динамические свойства ADO](ado-dynamic-property-index.md) предоставляет перекрестная ссылка между имена этих параметров и соответствующих свойств OLE DB).

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
<td><p><strong>Дескриптор окна</strong></p></td>
<td><p>Указывает дескриптор окна для использования запроса для получения дополнительных сведений.</p></td>
</tr>
<tr class="even">
<td><p><strong>Идентификатор языка</strong></p></td>
<td><p>Указывает уникальный 32-разрядная версия номер (например, 1033), который указывает параметры, связанные с языком пользователя. Эти параметры указывают способ форматирования даты и времени, элементы сортируются в алфавитном порядке, строк сравниваются и т. д.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Службы OLE DB</strong></p></td>
<td><p>Указывает битовую маску, которая определяет службы OLE DB для включения или отключения.</p></td>
</tr>
<tr class="even">
<td><p><strong>Запрос</strong></p></td>
<td><p>Указывает, следует ли запрашивать у пользователя при установке подключения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Расширенные свойства</strong></p></td>
<td><p>Строка, содержащая сведения о подключении к от поставщика, расширенная. Это свойство используется только для подключения к конкретному поставщику данных, которые не удается описано через механизм свойства.</p></td>
</tr>
</tbody>
</table>

