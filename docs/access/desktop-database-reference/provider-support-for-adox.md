---
title: Поддержка поставщиков для ADOX
TOCTitle: Provider Support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b19d30f9b243629874f7219c5b23af895540eaa9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25881141"
---
# <a name="provider-support-for-adox"></a>Поддержка поставщиков для ADOX


**Применимо к**: Access 2013, Office 2013

Некоторые возможности ADOX не поддерживаются, в зависимости от поставщика данных OLE DB. ADOX полностью поддерживаются с помощью [Поставщика OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Неподдерживаемые функции с помощью [Поставщик Microsoft OLE DB для SQL Server](microsoft-ole-db-provider-for-sql-server.md), [Поставщик Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)или [Поставщик Microsoft OLE DB для Oracle](microsoft-ole-db-provider-for-oracle.md) , перечислены ниже. Другие поставщики OLE DB для Microsoft ADOX не поддерживается.

## <a name="microsoft-ole-db-provider-for-sql-server"></a>Поставщик Microsoft OLE DB для SQL Server

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект или семейства сайтов</p></th>
<th><p>Ограничение использования</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>каталога</strong></p></td>
<td><p>Метод <strong>Create</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>таблиц</strong></p></td>
<td><p>Свойства чтения/записи до создания объекта и только для чтения — это при обращении существующий объект.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекции <strong>представлений</strong></p></td>
<td><p><strong>Представления,</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p><strong>Процедуры</strong> семейства сайтов</p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>процедуры</strong></p></td>
<td><p>Свойство <strong>Command</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>ключей</strong></p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Пользователи</strong> семейства сайтов</p></td>
<td><p><strong>Пользователи</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Семейства сайтов <strong>групп</strong></p></td>
<td><p><strong>Группы</strong> не поддерживается.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a>Поставщик Microsoft OLE DB для ODBC

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект или семейства сайтов</p></th>
<th><p>Ограничение использования</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>каталога</strong></p></td>
<td><p>Метод <strong>Create</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>таблиц</strong></p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются. Свойства чтения/записи до создания объекта и только для чтения — это при обращении существующий объект.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Процедуры</strong> семейства сайтов</p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>процедуры</strong></p></td>
<td><p>Свойство <strong>Command</strong> не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекции <strong>индексов</strong></p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>ключей</strong></p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Пользователи</strong> семейства сайтов</p></td>
<td><p><strong>Пользователи</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Семейства сайтов <strong>групп</strong></p></td>
<td><p><strong>Группы</strong> не поддерживается.</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a>Поставщик Microsoft OLE DB для Oracle

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект или семейства сайтов</p></th>
<th><p>Ограничение использования</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>каталога</strong></p></td>
<td><p>Метод <strong>Create</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>таблиц</strong></p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются. Свойства чтения/записи до создания объекта и только для чтения — это при обращении существующий объект.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекции <strong>представлений</strong></p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p><strong>Просмотр</strong> объектов</p></td>
<td><p>Свойство <strong>Command</strong> не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>процедур</strong></p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>процедуры</strong></p></td>
<td><p>Свойство <strong>Command</strong> не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекции <strong>индексов</strong></p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>ключей</strong></p></td>
<td><p><strong>Добавление</strong> и <strong>Удаление</strong> методы не поддерживаются.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Пользователи</strong> семейства сайтов</p></td>
<td><p><strong>Пользователи</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Семейства сайтов <strong>групп</strong></p></td>
<td><p><strong>Группы</strong> не поддерживается.</p></td>
</tr>
</tbody>
</table>

