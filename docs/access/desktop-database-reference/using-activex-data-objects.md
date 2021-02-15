---
title: Использование объектов данных ActiveX
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access предоставляет три объектные модели, которые можно использовать при создании, обслуживании и управлении базами данных Access и связанными с ними данными с помощью Visual Basic.
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

Microsoft Access предоставляет три объектные модели, которые можно использовать при создании, обслуживании и управлении базами данных Access и связанными с ними данными с помощью Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data Objects (ADO)

ADO содержит объекты, необходимые для создания, обслуживания и удаления записей в заданный datasource.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO ext. for DDL and security (ADOX)

ADOX предоставляет объекты языка определения данных (DDL), необходимые для создания новой базы данных и ее содержащихся объектов в дополнение к объектам, необходимым для управления безопасностью.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Библиотека Объектов Microsoft Jet и объектов репликации 2.5 (JRO)

Поскольку объекты ADO были разработаны для работы со многими базами данных в дополнение к базам данных Microsoft Jet, функциональные возможности, специфифиченные для Jet, были разбиты на библиотеку JRO.

В следующей таблице перечислены функции, предоставляемые по сравнению с DAO.

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
(Только MDB)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Создание записей.</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение свойств запуска.</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Поддержка anSI92 SQL.***</p></td>
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
<td><p>Создайте новую базу данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение существующих свойств таблицы.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание связей таблиц.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение параметров безопасности.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Поддержка атрибута сжатия для данных столбцов.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение сохраненных, базовых SQL запросов или представлений.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создавать постоянные запросы, доступные только через код.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Создавайте запросы, доступные через контейнер базы данных, пользовательский интерфейс и код.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Компактная или кодированная база данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Кэш обновления.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>Сделайте базу данных реплицируемым.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Сделайте реплики базы данных.</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Синхронизировать реплики.</p></td>
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
<td><p>Создание настраиваемой базы данных.</p></td>
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


\* Доступно только при работе с базами данных Microsoft Access. Будущие версии поставщика SQL могут предоставлять эту функциональность в проектах Microsoft Access (ADP).

\*\* Доступно только при работе с проектами Access.

\*\*\* Хотя механизм баз данных Access поддерживает некоторые SQL ANSI 92, он еще не полностью совместим с ANSI92.

1 Использует **объект Connection** для ссылки на базу данных.

2 Использует объект **Catalog** для ссылки на базу данных.

3 Использует **объект Replica** для ссылки на базу данных.

4 Использует объект **JetEngine** для ссылки на базу данных.


> [!NOTE]
> В отличие от DAO, объекты ADO и ADOX могут выполнять помеченные действия в базах данных, кроме Jet, если поставщик этих баз данных поддерживает это действие.


