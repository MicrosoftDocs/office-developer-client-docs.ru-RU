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

Вы можете использовать **действие SetProperty** для набора свойства для управления в форме или отчете.

## <a name="setting"></a>Параметр

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
<td><p>Введите имя поля или управления, для которого необходимо установить значение свойства. Используйте только имя управления, а не полный синтаксис. Оставьте этот аргумент пустым, чтобы завести свойство для текущей формы или отчета.</p></td>
</tr>
<tr class="even">
<td><p>Свойство</p></td>
<td><p>Выберите свойство, которое необходимо установить. Список <strong></strong> свойств, которые можно установить с помощью этого действия, см. в разделе Замечания в этой статье.</p></td>
</tr>
<tr class="odd">
<td><p>Значение</p></td>
<td><p>Введите значение, за которое должно быть установлено свойство. Для свойств, значения которых либо да, либо нет, используйте <strong>-1</strong> для да и <strong>0</strong> для No.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

- Вы можете использовать **действие SetProperty** для набора следующих свойств управления: **Включено,** Видимо, Заблокировано **,** Слева **,** **Верхняя**, Ширина **,** Высота **,** **Fore Color**, Back **Color**, или **подпись**.

- Если для аргумента ***Value*** введите недействительное значение, ошибка не возникает, но Access может изменить свойство на другое, в зависимости от того, как он интерпретирует аргумент.

- Действие **SetProperty** можно использовать в отдельном макросе только в том случае, если оно предшествует действию, которое выбирает форму или отчет, содержащий управление, для которого задается свойство. Если форма или отчет не открыты, для ее открытия и выбора можно использовать действие **OpenForm** или **OpenReport.** Если форма или отчет уже открыты, для ее выбора можно использовать **действие SelectObject.** Затем можно использовать **действие SetProperty** для набора свойства. Выбор объекта не требуется, если вы используете действие **SetProperty** в макросе, встроенном в элемент управления в той же форме или отчете, что и элемент управления, для которого устанавливается свойство.

- Чтобы выполнить **действие SetProperty** в модуле VBA, используйте метод **SetProperty** объекта **DoCmd.**

## <a name="example"></a>Пример

В следующем примере показано, как использовать действие SetProperty для перенастройки видимости текстового окна **MyTextBox.**

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    Submacro: TestVisible
        SetProperty
            Control Name Text40
            Property Visible
            Value =Not[Text40].[Visible]
    End Submacro
```
