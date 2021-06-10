---
title: Макрокоманда OpenTable
TOCTitle: OpenTable macro action
ms:assetid: 4220ad3a-d064-0034-2806-ec1a447cebac
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192909(v=office.15)
ms:contentKeyID: 48544469
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm149011
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 48a3797c2008f261eda8acc3391b39561fec05f3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288296"
---
# <a name="opentable-macro-action"></a>Макрокоманда OpenTable

**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие OpenTable** для открытия таблицы в представлении таблицы Datasheet, представлении "Дизайн" или "Предварительный просмотр печати". Вы также можете выбрать режим ввода данных для таблицы.

## <a name="setting"></a>Параметр

Действие **OpenTable** имеет следующие аргументы.

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
<td><p><strong>Имя таблицы</strong></p></td>
<td><p>Имя открытой таблицы. Поле <strong>Имя таблицы</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder отображает все таблицы в текущей базе данных. Это обязательный аргумент. Если вы запустите макрос, содержащий действие <strong>OpenTable</strong> в базе данных библиотеки, Microsoft Microsoft Access сначала ищет таблицу с этим именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Представление, в котором откроется таблица. Щелкните <strong>таблицу</strong>данных, <strong>дизайн,</strong> <strong>предварительный</strong>просмотр печати, <strong>pivotTable</strong>или сводная диаграмма в <strong>поле Просмотр.</strong> <strong></strong> По умолчанию — <strong>таблица данных.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Режим данных</strong></p></td>
<td><p>Режим ввода данных для таблицы. Это касается только таблиц, открытых в представлении Datasheet. Щелкните <strong>Добавить</strong> (пользователь может добавлять новые записи, но не может изменять существующие записи), <strong></strong> изменить (пользователь может изменять существующие записи и добавлять новые записи) или <strong>Только</strong> для чтения (пользователь может просматривать только записи). По умолчанию <strong>изменить</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Примечания

Это действие аналогично дважды щелкнув таблицу в области навигации или щелкнув правой кнопкой мыши таблицу в области навигации и выбрав представление.

> [!TIP]
> Таблицу можно перетаскивать из области навигации в строку действий макроса. Это автоматически создает действие **OpenTable,** которое открывает таблицу в представлении Datasheet.

Для запуска **действия OpenTable** в Visual Basic для приложений (VBA) используйте метод **OpenTable** объекта **DoCmd.**

