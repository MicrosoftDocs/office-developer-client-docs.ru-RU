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

Поставщик Microsoft OLE DB для Oracle позволяет ADO получать доступ к базам данных Oracle.

## <a name="connection-string-parameters"></a>Параметры строки подключения

Чтобы подключиться к этому поставщику, установите для аргумента *Provider* свойства [ConnectionString:](connectionstring-property-ado.md)

```vb 
 
MSDAORA 
```

При [чтении свойства Provider](provider-property-ado.md) также будет возвращена эта строка.

Если в базе данных Oracle выполняется запрос на присоединить с набором ключей или динамическим курсором, возникает ошибка. Oracle поддерживает только статический курсор только для чтения.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

```vb 
 
"Provider=MSDAORA;Data Source=serverName;User ID=userName; Password=userPassword;" 
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


## <a name="provider-specific-connection-parameters"></a>Provider-Specific connection parameters

Поставщик поддерживает несколько параметров подключения для конкретного поставщика в дополнение к параметрам, определенным aDO. Как и в свойствах подключения ADO, эти свойства для конкретного поставщика можно установить с помощью коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или в составе **ConnectionString.**

Эти параметры полностью описаны в справочнике программиста OLE DB. (Индекс [динамического свойства ADO](ado-dynamic-property-index.md) предоставляет перекрестную ссылку между этими именами параметров и соответствующими свойствами OLE DB.)

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
<td><p><strong>Окне Окне</strong></p></td>
<td><p>Указывает окне, который будет использовать для запроса дополнительных сведений.</p></td>
</tr>
<tr class="even">
<td><p><strong>Код локального идентификатора</strong></p></td>
<td><p>Указывает уникальный 32-битный номер (например, 1033), который указывает параметры, связанные с языком пользователя. Эти параметры указывают, как форматированы даты и время, элементы отсортированы в алфавитном порядке, сравниваются строки и так далее.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Службы OLE DB</strong></p></td>
<td><p>Указывает битовуюmask, которая указывает службы OLE DB, которые необходимо включить или отключить.</p></td>
</tr>
<tr class="even">
<td><p><strong>Prompt</strong></p></td>
<td><p>Указывает, следует ли затметь пользователя во время подключения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Расширенные свойства</strong></p></td>
<td><p>Строка, содержащая сведения о расширенных подключениях, относящаяся к конкретному поставщику. Используйте это свойство только для сведений о под подключениех для конкретного поставщика, которые не могут быть описаны с помощью механизма свойств.</p></td>
</tr>
</tbody>
</table>

