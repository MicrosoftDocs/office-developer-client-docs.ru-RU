---
title: Макрокоманда AddMenu
TOCTitle: AddMenu macro action
ms:assetid: 4eb2afa0-ed1f-41b1-d27f-b3ce7a73d2bb
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193760(v=office.15)
ms:contentKeyID: 48544762
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm37891
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 119e824cae71d54bb398aa68f476a667f14a6888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280275"
---
# <a name="addmenu-macro-action"></a>Макрокоманда AddMenu


**Область применения**: Access 2013, Office 2013

В этой статье описывается базовая операция **макроса AddMenu.**

Действие **AddMenu** можно использовать для создания:

- Настраиваемые меню на **вкладке "Надстройки"** для определенной формы или отчета.

- Настраиваемое меню ярлыка для формы, отчета или управления. Настраиваемые ярлыки заменяют встроенное меню для формы, отчета или управления.

- Глобальное меню ярлыка. Глобальное меню заменяет встроенное ярлыкное меню для полей в таблицах и таблицах данных запросов, формах и отчетах, за исключением случаев, когда добавлено настраиваемое меню для формы, отчета или управления.

## <a name="setting"></a>Setting

Действие **AddMenu** имеет следующие аргументы.

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
<td><p><strong>Имя меню</strong></p></td>
<td><p>Имя меню, например "Команды &quot; отчета" &quot; или &quot; "Инструменты". &quot; Чтобы создать клавишу доступа для выбора меню с помощью клавиатуры, введите амперанд () перед буквой, которая должна быть <strong>&amp;</strong> клавишей доступа. Эта буква будет подчеркивается в имени меню на вкладке <strong>"Надстройки".</strong></p></td>
</tr>
<tr class="even">
<td><p><strong>Имя макроса меню</strong></p></td>
<td><p>Имя группы макроса, которая содержит макрос для команд меню. Это обязательный аргумент.</p>
<p><strong>ПРИМЕЧАНИЕ.</strong>При запуске макроса, содержащего действие <strong>AddMenu</strong> в базе данных библиотеки, Microsoft Office Access 2007 ищет группу макроса с этим именем только в текущей базе данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Текст в панели состояния</strong></p></td>
<td><p>Текст, который будет отображаться в панели состояния при выборе меню. Этот аргумент игнорируется для ярлыков меню.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Чтобы запустить **действие AddMenu** в модуле Visual Basic для приложений (VBA), используйте метод **AddMenu** объекта **DoCmd.** Вы также можете настроить свойство **MenuBar** или **ShortcutMenuBar** в VBA, чтобы создать настраиваемые меню на вкладке "Надстройки" или прикрепить настраиваемые ярлыки к форме, отчету или управления.  Вы можете настроить свойство **ShortcutMenuBar** объекта **Application,** чтобы создать глобальное меню.

