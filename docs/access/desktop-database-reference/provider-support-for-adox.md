---
title: Provider Support for ADOX
TOCTitle: Provider Support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3d55ae14d124bfad7f8abbfcf3d94398ea92d792
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482932"
---
# <a name="provider-support-for-adox"></a>Provider Support for ADOX


**Применимо к**: Access 2013 | Office 2013

Некоторые возможности ADOX не поддерживаются, в зависимости от поставщика данных OLE DB. ADOX полностью поддерживаются с помощью [Поставщика OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Неподдерживаемые функции с помощью [Поставщик Microsoft OLE DB для SQL Server](microsoft-ole-db-provider-for-sql-server.md), [Поставщик Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)или [Поставщик Microsoft OLE DB для Oracle](microsoft-ole-db-provider-for-oracle.md) , перечислены ниже. Другие поставщики OLE DB для Microsoft ADOX не поддерживается.

## <a name="microsoft-ole-db-provider-for-sql-server"></a>Microsoft OLE DB Provider for SQL Server

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


## <a name="microsoft-ole-db-provider-for-odbc"></a>Microsoft OLE DB Provider for ODBC

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


## <a name="microsoft-ole-db-provider-for-oracle"></a>Microsoft OLE DB Provider for Oracle

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

