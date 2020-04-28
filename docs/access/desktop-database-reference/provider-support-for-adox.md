---
title: Поддержка поставщиков для ADOX
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a92ffe9b4b713518330d9dbfd9979d904a5abe8e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301101"
---
# <a name="provider-support-for-adox"></a>Поддержка поставщиков для ADOX


**Область применения**: Access 2013, Office 2013

Некоторые функции ADOX не поддерживаются в зависимости от поставщика данных OLE DB. ADOX полностью поддерживается [поставщиком OLE DB для Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md). Ниже перечислены неподдерживаемые возможности [поставщика Microsoft OLE DB для SQL Server](microsoft-ole-db-provider-for-sql-server.md), [поставщика Microsoft OLE DB для ODBC](microsoft-ole-db-provider-for-odbc.md)или [поставщика Microsoft OLE DB для Oracle](microsoft-ole-db-provider-for-oracle.md) . ADOX не поддерживается какими-либо другими поставщиками Microsoft OLE DB.

## <a name="microsoft-ole-db-provider-for-sql-server"></a>Поставщик Microsoft OLE DB для SQL Server

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Объект или коллекция</p></th>
<th><p>Ограничение использования</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>Catalog</strong></p></td>
<td><p>Метод <strong>CREATE</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>Tables</strong></p></td>
<td><p>Свойства доступны для чтения и записи перед созданием объекта и доступны только для чтения при обращении к существующему объекту.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекция <strong>views</strong></p></td>
<td><p><strong>Представления</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>процедур</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>PROCEDURE</strong></p></td>
<td><p>Свойство <strong>Command</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>Keys</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекция <strong>Users</strong></p></td>
<td><p><strong>Пользователи</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>Groups</strong></p></td>
<td><p><strong>Группы</strong> не поддерживаются.</p></td>
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
<th><p>Объект или коллекция</p></th>
<th><p>Ограничение использования</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>Catalog</strong></p></td>
<td><p>Метод <strong>CREATE</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>Tables</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются. Свойства доступны для чтения и записи перед созданием объекта и доступны только для чтения при обращении к существующему объекту.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекция <strong>процедур</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>PROCEDURE</strong></p></td>
<td><p>Свойство <strong>Command</strong> не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекция <strong>indexes</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>Keys</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекция <strong>Users</strong></p></td>
<td><p><strong>Пользователи</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>Groups</strong></p></td>
<td><p><strong>Группы</strong> не поддерживаются.</p></td>
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
<th><p>Объект или коллекция</p></th>
<th><p>Ограничение использования</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Объект <strong>Catalog</strong></p></td>
<td><p>Метод <strong>CREATE</strong> не поддерживается.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>Tables</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются. Свойства доступны для чтения и записи перед созданием объекта и доступны только для чтения при обращении к существующему объекту.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекция <strong>views</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>View</strong></p></td>
<td><p>Свойство <strong>Command</strong> не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p>Объект <strong>процедур</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Объект <strong>PROCEDURE</strong></p></td>
<td><p>Свойство <strong>Command</strong> не поддерживается.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекция <strong>indexes</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>Keys</strong></p></td>
<td><p>Методы <strong>append</strong> и <strong>Delete</strong> не поддерживаются.</p></td>
</tr>
<tr class="odd">
<td><p>Коллекция <strong>Users</strong></p></td>
<td><p><strong>Пользователи</strong> не поддерживаются.</p></td>
</tr>
<tr class="even">
<td><p>Коллекция <strong>Groups</strong></p></td>
<td><p><strong>Группы</strong> не поддерживаются.</p></td>
</tr>
</tbody>
</table>

