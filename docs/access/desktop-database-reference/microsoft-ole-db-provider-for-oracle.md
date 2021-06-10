---
title: Поставщик Microsoft OLE DB для Oracle
TOCTitle: Microsoft OLE DB Provider for Oracle
ms:assetid: 97508e3f-077f-9b85-f4dd-8dd01a201aba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249674(v=office.15)
ms:contentKeyID: 48546465
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b9b506f40039ff91a6b1985606322fd86a9e7c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288934"
---
# <a name="microsoft-ole-db-provider-for-oracle"></a>Поставщик Microsoft OLE DB для Oracle

**Область применения**: Access 2013, Office 2013

В поставщик OLE DB для Oracle (Майкрософт) ADO можно получить доступ к базам данных Oracle.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к этому поставщику, установите *аргумент поставщика* свойства [ConnectionString:](connectionstring-property-ado.md)

```vb 
 
MSDAORA 
```

Чтение свойства [Provider](provider-property-ado.md) также вернет эту строку.

Если запрос на участие с набором ключей или динамическим курсором выполняется в базе данных Oracle, возникает ошибка. Oracle поддерживает только статичный курсор только для чтения.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
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
<td><p>Указывает поставщика OLE DB для Oracle.</p></td>
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
<td><p>Указывает пароль пользователя.</p></td>
</tr>
</tbody>
</table>


## <a name="provider-specific-connection-parameters"></a>Provider-Specific параметры подключения

Поставщик поддерживает несколько параметров подключения, определенных для поставщика, в дополнение к параметрам, определенным ADO. Как и в свойствах подключения ADO, эти свойства, определенные для поставщика, можно задать через коллекцию [свойств](properties-collection-ado.md) подключения или в **составе ConnectionString.** [](connection-object-ado.md)

Эти параметры полностью описаны в справочнике программиста OLE DB. (Индекс [динамического свойства ADO](ado-dynamic-property-index.md) обеспечивает перекрестную ссылку между этими именами параметров и соответствующими свойствами OLE DB.)

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
<td><p><strong>Ручка окна</strong></p></td>
<td><p>Указывает на ручку окна, которую нужно использовать для запроса дополнительных сведений.</p></td>
</tr>
<tr class="even">
<td><p><strong>Идентификатор locale</strong></p></td>
<td><p>Указывает уникальный 32-битный номер (например, 1033), который указывает предпочтения, связанные с языком пользователя. Эти параметры указывают форматирование дат и времени, сортировку элементов в алфавитном порядке, сравнение строк и так далее.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Службы OLE DB</strong></p></td>
<td><p>Указывает битмаску, которая указывает службы OLE DB, чтобы включить или отключить.</p></td>
</tr>
<tr class="even">
<td><p><strong>Prompt</strong></p></td>
<td><p>Указывает, следует ли подсказать пользователю во время подключения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Расширенные свойства</strong></p></td>
<td><p>Строка, содержащая сведения о расширенном подключении для конкретного поставщика. Используйте это свойство только для сведений о подключении, которые не могут быть описаны с помощью механизма свойств.</p></td>
</tr>
</tbody>
</table>

