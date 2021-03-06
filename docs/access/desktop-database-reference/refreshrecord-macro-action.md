---
title: Макрокоманда RefreshRecord
TOCTitle: RefreshRecord macro action
ms:assetid: 68c90d7d-f59c-9e83-bc30-8f37cf5a3696
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195261(v=office.15)
ms:contentKeyID: 48545396
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62122
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d8682c19686650ab193536658c6b56961f289174
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307086"
---
# <a name="refreshrecord-macro-action"></a>Макрокоманда RefreshRecord


**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие RefreshRecord** для обновления источника записей для активной формы или таблицы данных для отражения изменений, внесенных в записи текущего набора.

## <a name="remarks"></a>Примечания

в **действии RefreshRecord** показаны только изменения, внесенные в записи текущего набора. Так как действие **RefreshRecord** фактически не переописывало базу данных, текущий набор не будет включать записи, которые были добавлены или исключены записи, которые были удалены с момента последней повторной записи базы данных; Кроме того, не будут исключены записи, которые больше не соответствуют критериям запроса или фильтра. Чтобы повторно запросить базу данных, используйте метод **[Requery](requery-macro-action.md)**. При повторном запросе источника записей текущий набор записей будет точно отражать все данные в источнике записей.

Поведение этого макроса зависит от того, вызываете ли вы его в клиентской базе данных или в веб-базе данных.

## <a name="client-database"></a>Клиентская база данных

В клиентской базе данных можно использовать действие **RefreshRecord** для обновления источника записи для активной формы или таблицы данных, чтобы отразить изменения, внесенные в данные текущего набора. Изменения включают изменения, внесенные текущим пользователем или другими пользователями в многоуровневой среде. Это эквивалентно методу **[Обновления.](https://docs.microsoft.com/office/vba/api/Access.Form.Refresh)**

**Макро-действие RefreshRecord** содержит следующие действия в клиентской базе данных:

1.  Обновляет источник записей для активной формы или таблицы данных, чтобы отразить изменения, внесенные в строки в текущем наборе. Для связанных таблиц ODBC извлекает изменения в записи текущего набора из источника данных.

2.  Обновляет текущий набор, чтобы отразить изменения. Если строка в источнике записи удалена, она меняется, чтобы показать \# Удаленный.

3.  Обновляет активную или таблицу данных для отображения всех измененных записей и удаленных записей \# в текущем наборе.

4.  Requeries any subforms and subreports on the active form or datasheet.

## <a name="web-database"></a>Веб-база данных

В веб-базе данных можно использовать действие **RefreshRecord** для обновления источника записей для активной формы или таблицы данных для отражения изменений, внесенных в записи текущего набора. Изменения включают изменения, внесенные текущим пользователем или другими пользователями.

**Макро-действие RefreshRecord** содержит следующие действия в веб-базе данных:

1.  Извлекает изменения с сервера для любых базовых таблиц в текущем наборе. Для связанных таблиц ODBC извлекает изменения в записи текущего набора из источника данных.

2.  Обновляет текущий набор, чтобы отразить изменения. Если строка в текущем наборе удалена, она меняется, чтобы показать \# Удаленный.

3.  Обновляет активную форму или таблицу данных для отображения всех измененных записей и удаленных записей \# в текущем наборе.

4.  Requeries any subforms and subreports on the active form or datasheet.

