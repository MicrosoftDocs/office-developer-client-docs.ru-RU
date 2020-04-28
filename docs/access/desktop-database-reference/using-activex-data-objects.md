---
title: Использование объектов данных ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access предоставляет три объектные модели, которые используются для создания, обслуживания и управления базами данных Access и связанных с ними данных с помощью Visual Basic.
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312742"
---
# <a name="use-activex-data-objects"></a>Использование объектов данных ActiveX

**Область применения**: Access 2013, Office 2013

Microsoft Access предоставляет три объектные модели, которые используются для создания, обслуживания и управления базами данных Access и связанных с ними данных с помощью Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Объекты данных Microsoft ActiveX (ADO)

ADO содержит объекты, необходимые для создания, обслуживания и удаления записей в заданном источнике данных.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO ext. для DDL и безопасности (ADOX)

ADOX предоставляет объекты языка определения данных (DDL), необходимые для создания новой базы данных и ее вложенных объектов в дополнение к объектам, необходимым для управления безопасностью.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Microsoft Jet и библиотека объектов репликации 2,5 (JRO)

Так как объекты ADO спроектированы для работы с множеством баз данных в дополнение к базам данных Microsoft Jet, функции, относящиеся к Jet, были разбиты на библиотеку JRO.

В следующей таблице перечислены функциональные возможности, предоставляемые в сравнении с DAO.

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
<th><p>функциональность.</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(Только для МДБС)</p></th>
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
<td><p>Изменение свойств запуска.</p></td>
<td><p>X</p></td>
<td><p>X * *</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Поддержка ANSI92 SQL. * * *</p></td>
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
<td><p>X</p></td>
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
<td><p>Создайте связи между таблицами.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение параметров безопасности.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Поддержка атрибута Compression для данных столбца.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение хранимых, базовых запросов или представлений SQL.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание постоянных запросов, доступных только с помощью кода.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Создание запросов, доступ к которым осуществляется с помощью контейнера базы данных, пользовательского интерфейса и кода.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Сжатие и кодирование базы данных.</p></td>
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
<td><p>Сделайте базу данных реплицируемой.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>Lingvo</p></td>
</tr>
<tr class="even">
<td><p>Сделайте реплики базы данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>Lingvo</p></td>
</tr>
<tr class="odd">
<td><p>Синхронизация реплик.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>Lingvo</p></td>
</tr>
<tr class="even">
<td><p>Изменение свойств базы данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание настраиваемых свойств базы данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение свойств столбца таблицы.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\*Доступно только при работе с базами данных Microsoft Access. В будущих версиях поставщика SQL эта функция может быть предоставлена в проектах Microsoft Access (ADP).

\*\*Доступно только при работе с проектами Access.

\*\*\*Несмотря на то, что ядро базы данных Access поддерживает некоторый ANSI 92 SQL, он пока не полностью совместим с ANSI92.

1 использует объект **Connection** для ссылки на базу данных.

2 использует объект **каталога** для ссылки на базу данных.

3 использует объект **реплики** для ссылки на базу данных.

4 использует объект **жетенгине** для ссылки на базу данных.


> [!NOTE]
> В отличие от DAO, объекты ADO и ADOX могут выполнять помеченные действия в базах данных, отличных от Jet, если поставщик этих баз данных поддерживает это действие.


