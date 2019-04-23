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

Чтобы подключиться к поставщику, присвойте аргументу *provider* свойства [ConnectionString](connectionstring-property-ado.md) значение:

```vb 
 
MSDAORA 
```

Считывание свойства [provider](provider-property-ado.md) также возвратит эту строку.

Если в базе данных Oracle выполняется запрос на присоединение с набором ключей или динамическим курсором, возникает ошибка. Oracle поддерживает только статический курсор только для чтения.

## <a name="typical-connection-string"></a>Типичная строка подключения

Типичная строка подключения для этого поставщика:

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
<th><p>Ключевое слово</p></th>
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
<td><p>Задает имя сервера.</p></td>
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


## <a name="provider-specific-connection-parameters"></a>Параметры подключения, зависящие от поставщика

Поставщик поддерживает несколько параметров подключения, относящихся к поставщику, помимо тех, которые определены в ADO. Как и в случае со свойствами подключения ADO, эти свойства, зависящие от поставщика, можно задать с помощью коллекции [свойств](properties-collection-ado.md) [подключения](connection-object-ado.md) или в качестве части **ConnectionString**.

Эти параметры полностью описаны в справочнике программиста OLE DB. ( [Индекс динамического свойства ADO](ado-dynamic-property-index.md) предоставляет перекрестные ссылки между именами этих параметров и СООТВЕТСТВУЮЩИМИ свойствами OLE DB.)

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
<td><p>Указывает дескриптор окна, используемый для вывода дополнительных сведений.</p></td>
</tr>
<tr class="even">
<td><p><strong>Идентификатор языкового стандарта</strong></p></td>
<td><p>Указывает уникальное 32-разрядное число (например, 1033), которое определяет параметры, связанные с языком пользователя. Эти установки указывают, как форматируется Дата и время, сортируются элементы в алфавитном порядке, сравниваются строки и т. д.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Службы OLE DB</strong></p></td>
<td><p>Указывает битовую маску, указывающую, какие службы OLE DB необходимо включить или отключить.</p></td>
</tr>
<tr class="even">
<td><p><strong>Prompt</strong></p></td>
<td><p>Указывает, следует ли запрашивать пользователя во время установки подключения.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Расширенные свойства</strong></p></td>
<td><p>Строка, содержащая сведения о расширенном подключении, зависящие от поставщика. Это свойство используется только для сведений о соединении с конкретным поставщиком, которые невозможно описать с помощью механизма свойств.</p></td>
</tr>
</tbody>
</table>

