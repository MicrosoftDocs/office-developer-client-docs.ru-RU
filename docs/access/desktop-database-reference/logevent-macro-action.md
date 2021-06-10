---
title: Макрокоманда LogEvent
TOCTitle: LogEvent macro action
ms:assetid: 3578c725-64b9-385e-ef73-a15cdf751c33
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192460(v=office.15)
ms:contentKeyID: 48544148
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 4106e66074975f08a5058aafbfc0c6deac156277
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289838"
---
# <a name="logevent-macro-action"></a>Макрокоманда LogEvent

**Область применения**: Access 2013, Office 2013

Действие **LogEvent** записывает сведения в таблицу **системы USysApplicationLog.**

> [!NOTE]
> Действие **LogEvent** доступно только в макросах данных.

## <a name="setting"></a>Параметр

Действие **LogEvent** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Описание</strong></p></td>
<td><p>Нет</p></td>
<td><p>Строка, описываемая условием, которое необходимо входить в журнал. Описание не может превышать 255 символов.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Примечания

Действие **LogEvent** можно использовать для записи сведений о состоянии в таблицу **системы USysApplicationLog,** которая не заслуживает использования действия **[RaiseError](raiseerror-macro-action.md)** для метания ошибки. Например, можно внести изменения в определенное поле или использовать элементы, написанные в **USysApplicationLog,** чтобы помочь вам отладить макрос.

При использовании **действия LogEvent** для записи в таблицу **USysApplicationLog** столбец **Category** автоматически задается **пользователю.**

Чтобы увидеть **таблицу USysApplicationLog,** используйте следующие действия:

1.  Щелкните **меню File** и нажмите кнопку **Параметры**.

2.  В **диалоговом окне Параметры** доступа щелкните вкладку **Current Database.**

3.  В разделе **Навигация** нажмите **кнопку Параметры навигации**.

4.  В **диалоговом окне Параметры** навигации щелкните **Показать объекты системы** и нажмите **кнопку ОК**.

5.  Нажмите **кнопку ОК,** чтобы **отклонять диалоговое** окно Access Options.

