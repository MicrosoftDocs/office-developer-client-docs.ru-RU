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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28700362"
---
# <a name="opentable-macro-action"></a>Макрокоманда OpenTable

**Применимо к**: Access 2013, Office 2013

Чтобы открыть таблицу в режиме таблицы, конструктора или просмотра можно использовать **ОткрытьТаблицу** . Также можно выбрать режим ввода данных для таблицы.

## <a name="setting"></a>Setting

**ОткрытьТаблицу** имеет следующие аргументы.

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
<td><p>Имя таблицы. В поле <strong>Имя таблицы</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов содержит все таблицы в текущей базе данных. Обязательный аргумент. Если макрос, содержащий <strong>ОткрытьТаблицу в базе данных библиотеки</strong> , Microsoft Microsoft Access выполняет поиск таблицы с указанным именем сначала в библиотеке базы данных, а затем в текущей базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Представление, в котором будут открываться в таблице. Выберите <strong>таблицы</strong>, <strong>разработки</strong>, <strong>Режим предварительного просмотра</strong>, <strong>сводной таблицы</strong>или <strong>сводной диаграммы</strong> в поле <strong>View</strong> . Значение по умолчанию — <strong>таблицы данных</strong>.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Режим данных</strong></p></td>
<td><p>Режим ввода данных для таблицы. Это относится только к таблиц, открытых в режиме таблицы. Нажмите кнопку <strong>Add</strong> (пользователь может добавлять новые записи, но не могут изменять существующие записи), <strong>Изменение</strong> (пользователь может изменять существующие записи и добавление новых записей), или <strong>Только для чтения</strong> (пользователь может только просматривать записи). Значение по умолчанию — <strong>Изменить</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Замечания

Это действие аналогична таблице на левой панели навигации, дважды щелкнув или щелкнув правой кнопкой мыши таблицу в области навигации и выбрав представления.

> [!TIP]
> Таблица можно перетаскивать из области переходов в строку действие в макросе. Это автоматически создает **ОткрытьТаблицу** действие, которое открывается таблицы в представлении таблицы данных.

Чтобы запустить **ОткрытьТаблицу** в Visual Basic для приложений (VBA) модуль, используйте метод **ОткрытьТаблицу** **объекта** .

