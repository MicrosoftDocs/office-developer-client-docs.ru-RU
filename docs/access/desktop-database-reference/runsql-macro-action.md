---
title: Макрокоманда RunSQL
TOCTitle: RunSQL macro action
ms:assetid: 3692142d-f8a8-e194-0b38-051167f46319
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192476(v=office.15)
ms:contentKeyID: 48544174
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm12983
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: f3ef598ad50747d99ca884043e03ebfabfef8f63
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308997"
---
# <a name="runsql-macro-action"></a>Макрокоманда RunSQL

**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие RunSQL** для выполнения запроса действий Access с помощью соответствующего SQL. Можно также выполнить запрос определения данных.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **RunSQL имеет** следующие аргументы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>SQL Заявление</strong></p></td>
<td><p>Необходимо SQL для запроса действий или запроса определения данных. Максимальная длина этого утверждения — 255 символов. Это обязательный аргумент.</p></td>
</tr>
<tr class="even">
<td><p><strong>Использование транзакции</strong></p></td>
<td><p>Выберите <strong>Да,</strong> чтобы включить этот запрос в транзакцию. Выберите <strong>Нет,</strong> если вы не хотите использовать транзакцию. По умолчанию — <strong>Да.</strong> Если для этого <strong>аргумента выбрано</strong> "Нет", запрос может работать быстрее.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Запросы действий можно использовать для приложения, удаления и обновления записей, а также для сохранения результата запроса, заданного в качестве новой таблицы. Запросы определения данных можно использовать для создания, изменения и удаления таблиц, а также для создания и удаления индексов. Вы можете использовать **действие RunSQL** для выполнения этих операций непосредственно с макроса без использования сохраненных запросов.

Если требуется ввести SQL более 255 символов, используйте метод **RunSQL** объекта **DoCmd** в модуле Visual Basic для приложений (VBA). Вы можете ввести SQL в VBA с 32 768 символами.

Запросы доступа — это SQL, созданные при разработке запроса с помощью сетки разработки в окне Запрос. В следующей таблице показаны запросы действий Access и запросы определения данных и их соответствующие SQL отчеты.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Тип запроса</p></th>
<th><p>SQL</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Действие</strong></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Приложение</p></td>
<td><p>INSERT INTO</p></td>
</tr>
<tr class="odd">
<td><p>Удалить</p></td>
<td><p>DELETE</p></td>
</tr>
<tr class="even">
<td><p>Make-table</p></td>
<td><p>ВЫБЕРИТЕ... INTO</p></td>
</tr>
<tr class="odd">
<td><p>Update</p></td>
<td><p>UPDATE</p></td>
</tr>
<tr class="even">
<td><p><strong>Определение данных (SQL определенное)</strong></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создание таблицы</p></td>
<td><p>СОЗДАНИЕ ТАБЛИЦЫ</p></td>
</tr>
<tr class="even">
<td><p>Изменение таблицы</p></td>
<td><p>ALTER TABLE</p></td>
</tr>
<tr class="odd">
<td><p>Удаление таблицы</p></td>
<td><p>ТАБЛИЦА DROP</p></td>
</tr>
<tr class="even">
<td><p>Создание индекса</p></td>
<td><p>СОЗДАНИЕ ИНДЕКСА</p></td>
</tr>
<tr class="odd">
<td><p>Удаление индекса</p></td>
<td><p>DROP INDEX</p></td>
</tr>
</tbody>
</table>

Вы также можете использовать пункт IN с этими утверждениями для изменения данных в другой базе данных.

> [!NOTE]
> Чтобы выполнить выбранный запрос или перекрестный запрос с макроса, используйте аргумент View действия **OpenQuery** для открытия существующего запроса выбора или перекрестного запроса в представлении Datasheet. Вы также можете запускать существующие запросы действий и SQL определенным запросам таким же образом.
