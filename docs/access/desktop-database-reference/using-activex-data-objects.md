---
title: Using ActiveX Data Objects
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480896"
---
# <a name="using-activex-data-objects"></a>Using ActiveX Data Objects


**Применимо к**: Access 2013 | Office 2013

Microsoft Access предоставляет три объектных моделей для использования в создании, поддержке и управлению баз данных Access и их данных, связанных с ними с помощью Visual Basic.

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data Objects (ADO)

ADO содержит объекты, необходимые для создания, обслуживания и удаления записей в заданном источнике данных.

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Внешний Microsoft ADO для DDL и безопасности (ADOX)

ADOX предоставляет Language(DDL) определения данных объекты, необходимые для создания новой базы данных и ее вложенные объекты, помимо объекты, необходимые для управления безопасностью.

**Библиотека объектов 2.5 репликации (JRO) и Microsoft Jet**

Поскольку объекты ADO были предназначена для работы с использованием многих баз данных, кроме баз данных Microsoft Jet, функциональные возможности, относящиеся к Jet был разбиваются на библиотеку JRO.

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
(Только 's MDB)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Создание наборов записей</p></td>
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение параметров запуска</p></td>
<td><p>X </p></td>
<td><p>X **</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Поддержка ANSI92 SQL ***</p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Создание таблиц</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание новой базы данных</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение свойств существующей таблицы</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание связи между таблицами</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение параметров безопасности</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Поддержка сжатия для столбцы данных.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение сохраненных, основных SQL-запросов или представлений</p></td>
<td><p>X </p></td>
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
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Сжать/кодирование базы данных</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>Обновление кэша</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
</tr>
<tr class="odd">
<td><p>Сделать реплицированной базы данных</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Сделать репликами баз данных</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>Синхронизации реплик</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>Изменение свойств базы данных</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание настраиваемой базы данных свойств</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Изменение свойств столбца в таблице</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\*Доступно только при работе с базами данных Microsoft Access. В будущих версиях поставщика SQL можно указать эту функцию в проектах Microsoft Access (файлы с расширением ADP).

\*\*Доступно только при работе с проектами Access.

\*\*\*Хотя ядро СУБД Access поддерживают некоторые ANSI SQL-92 его еще не является полностью ANSI92 спецификации.

Объект 1 использует **подключения** для обращения к базе данных

2 использует **каталога** объектов для базы данных ссылок

3 объект использует **реплики** для базы данных ссылок

4 объекта использует **JetEngine** для базы данных ссылок


> [!NOTE]
> <P>В отличие от DAO ADO и ADOX объекты можно выполнить помеченные действия в базах данных других затем Jet до тех пор, пока поставщик для этих баз данных поддерживает это действие.</P>


