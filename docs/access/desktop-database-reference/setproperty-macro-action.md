---
title: Макрокоманда SetProperty
TOCTitle: SetProperty macro action
ms:assetid: 58d2eac3-35b2-e9f8-47e0-62c9b52f2c24
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194340(v=office.15)
ms:contentKeyID: 48545004
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm139044
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c5972ad630efe3afe27565924c7c6a8a2230a9f2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314576"
---
# <a name="setproperty-macro-action"></a>Макрокоманда SetProperty

**Область применения**: Access 2013, Office 2013

С помощью действия **SetProperty можно** установить свойство для управления в форме или отчете.

## <a name="setting"></a>Setting

Действие **SetProperty** имеет следующие аргументы.

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
<td><p>Контрольное имя</p></td>
<td><p>Введите имя поля или управления, для которого необходимо установить значение свойства. Используйте только имя, а не полный синтаксис. Оставьте этот аргумент пустым, чтобы установить свойство для текущей формы или отчета.</p></td>
</tr>
<tr class="even">
<td><p>Свойство</p></td>
<td><p>Выберите свойство, которое нужно установить. Список <strong>свойств,</strong> которые можно настроить с помощью этого действия, см. в разделе "Примечаний" этой статьи.</p></td>
</tr>
<tr class="odd">
<td><p>Значение</p></td>
<td><p>Введите значение, которое должно быть установлено для свойства. Для свойств со значениями "Да" или "Нет" используйте <strong>-1</strong> для "Да" и <strong>0</strong> для "Нет".</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

- С помощью действия **SetProperty** можно настроить следующие свойства управления: **Enabled,** **Visible,** **Locked,** **Left,** **Top,** **Width,** **Height,** **Fore Color,** **Back Color** или **Caption**.

- Если ввести недопустимое значение для аргумента ***Value,*** ошибка не возникает, но Access может изменить свойство на другое значение в зависимости от того, как он интерпретирует аргумент.

- Действие **SetProperty** в отдельном макросе можно использовать только в том случае, если перед ним установлено действие, которое выбирает форму или отчет, содержащий объект управления, для которого задается свойство. Если форма или отчет не открыты, вы можете открыть и выбрать действие **OpenForm** или **OpenReport.** Если форма или отчет уже открыты, вы можете выбрать ее с помощью действия **SelectObject.** Затем можно использовать действие **SetProperty,** чтобы установить свойство. Выбор объекта не требуется, если вы используете действие **SetProperty** в макросе, внедренном в элемент управления в той же форме или отчете, что и элемент управления, для которого вы устанавливаете свойство.

- Чтобы запустить действие **SetProperty** в модуле VBA, используйте метод **SetProperty** объекта **DoCmd.**

## <a name="example"></a>Пример

В следующем примере показано, как использовать действие SetProperty для перестройки видимости текстового окна **MyTextBox.**

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
