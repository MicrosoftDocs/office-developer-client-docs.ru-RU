---
title: Использование объектов данных ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access предоставляет три объектных моделей для использования в создании, обслуживания и управления баз данных Access и их данных, связанных с использованием Visual Basic.
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719227"
---
# <a name="use-activex-data-objects"></a>Использование объектов данных ActiveX

**Применимо к**: Access 2013, Office 2013

Microsoft Access предоставляет три объектных моделей для использования в создании, обслуживания и управления баз данных Access и их данных, связанных с использованием Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data Objects (ADO)

ADO содержит объекты, необходимые для создания, обслуживания и удаления записей в заданном источнике данных.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Внешний Microsoft ADO для DDL и безопасности (ADOX)

ADOX предоставляет язык описания данных (DDL) объекты, необходимые для создания новой базы данных и ее вложенные объекты, помимо объекты, необходимые для управления безопасностью.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Библиотека Microsoft Jet и репликации объектов 2.5 (JRO)

Так как объекты ADO были предназначена для работы с использованием многих баз данных, кроме баз данных Microsoft Jet, функциональные возможности, относящиеся к Jet был разбиваются на библиотеку JRO.

В следующей таблице перечислены функциональные возможности, предоставляемые каждым по сравнению с DAO.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Функциональность</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(MDB)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Создание наборов записей.</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение параметров запуска.</p></td>
<td><p>X</p></td>
<td><p>X **</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Поддержка ANSI92 SQL.* **</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Создание таблиц.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание новой базы данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение свойств существующей таблицы.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание связи между таблицами.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение параметров безопасности.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Поддержка сжатия для столбца данных.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Измените хранимые, основные запросы SQL или представления.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создайте постоянные запросов, которые доступны только с помощью кода.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Создание запросов через контейнер базы данных и пользовательского интерфейса и кода.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Сжать/шифрование базы данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Обновление кэша.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Сделать реплицированной базы данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Сделайте репликами баз данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Синхронизации реплик.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Изменение свойств базы данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание настраиваемой базы данных свойств.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение свойств столбца в таблице.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\*Доступно только при работе с базами данных Microsoft Access. В будущих версиях поставщика SQL можно указать эту функцию в проектах Microsoft Access (файлы с расширением ADP).

\*\*Доступно только при работе с проектами Access.

\*\*\*Несмотря на то, что ядро СУБД Access поддерживают некоторые ANSI SQL-92, она еще не полностью спецификации ANSI92.

1 объект использует **подключение** к базе данных ссылок.

Объект 2 использует **каталога** для базы данных ссылок.

3 объект использует **реплику** базы данных ссылок.

4 использует **JetEngine** объект базы данных ссылок.


> [!NOTE]
> В отличие от DAO ADO и ADOX объекты можно выполнить помеченные действия в базах данных, отличный от Jet до тех пор, пока поставщик для этих баз данных поддерживает это действие.


