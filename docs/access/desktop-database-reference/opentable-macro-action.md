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

Действие **OpenTable** можно использовать для открытия таблицы в представлении таблицы, представлении конструктора или предварительном просмотре печати. Можно также выбрать режим ввода данных для таблицы.

## <a name="setting"></a>Setting

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
<td><p>Имя открытой таблицы. В <strong>поле "Имя таблицы"</strong> в разделе <strong>"Аргументы</strong> действий" области построитель макроса показаны все таблицы в текущей базе данных. Это обязательный аргумент. При запуске макроса, содержащего действие <strong>OpenTable</strong> в базе данных библиотеки, Microsoft Access сначала ищет таблицу с этим именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong></p></td>
<td><p>Представление, в котором откроется таблица. Щелкните <strong></strong> <strong>"Таблица</strong> <strong>данных", "Конструктор",</strong>"Предварительный <strong>просмотр",</strong> <strong>"Сводная диаграмма</strong> в поле <strong>"Вид".</strong> Значение по умолчанию <strong>— Таблица.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Режим данных</strong></p></td>
<td><p>Режим ввода данных для таблицы. Это относится только к таблицам, открытым в представлении таблиц. Нажмите <strong></strong> кнопку "Добавить" (пользователь может добавлять новые записи, но не может редактировать существующие <strong>записи),</strong> изменить (пользователь может редактировать существующие записи и добавлять новые) или "Только чтение" <strong>(пользователь</strong> может просматривать только записи). Значение по умолчанию — <strong>Edit</strong>.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Заметки

Это действие аналогично двойному щелчку таблицы в области навигации или щелчку правой кнопкой мыши таблицы в области навигации и выбору представления.

> [!TIP]
> Можно перетащить таблицу из области навигации в строку макроса. При этом автоматически создается действие **OpenTable,** которое открывает таблицу в представлении таблицы.

Чтобы запустить действие **OpenTable** в модуле Visual Basic для приложений (VBA), используйте метод **OpenTable** объекта **DoCmd.**

