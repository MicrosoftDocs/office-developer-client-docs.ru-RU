---
title: Макрокоманда RunMenuCommand
TOCTitle: RunMenuCommand macro action
ms:assetid: cc4a4f72-0c73-91b7-8cec-6cbcda7e5b1c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff834420(v=office.15)
ms:contentKeyID: 48547735
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm6446
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c2b5a19b7a92fb68dfb774afeec5cd6ba456f38d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306505"
---
# <a name="runmenucommand-macro-action"></a>Макрокоманда RunMenuCommand

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **Макрокоманда runmenucommand** для выполнения встроенной команды Microsoft Access.

## <a name="setting"></a>Параметр

Действие **Макрокоманда runmenucommand** имеет следующий аргумент action (действие).

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
<td><p><strong>Command</strong></p></td>
<td><p>Имя команды, которую необходимо выполнить. В поле <strong>команд</strong> отображаются доступные встроенные команды Access в алфавитном порядке. Обязательный аргумент.</p></td>
</tr>
</tbody>
</table>

## <a name="remarks"></a>Замечания

Действие **Макрокоманда runmenucommand** можно использовать для запуска команды доступа из настраиваемой строки меню, глобальной строки меню, настраиваемого контекстного меню или глобального контекстного меню.

Макрокоманду **Макрокоманда runmenucommand** можно использовать в макросе с условными выражениями для выполнения команды в зависимости от определенных условий.

> [!NOTE]
> Перейдите на вкладку **файл** , а затем в меню **последние** отображаются последние использованные базы данных. Вместо нажатия кнопки **Открыть**можно щелкнуть одну из этих баз данных. Эти элементы базы данных не отображаются в раскрывающемся списке для аргумента **команды** и недоступны с помощью действия **Макрокоманда runmenucommand** в макросе.

При преобразовании базы данных Access из предыдущей версии Access некоторые команды могут стать недоступными. Возможно, команда была переименована, перемещена в другое меню или больше недоступна в Access. Действия **доменуитем** для таких команд не могут быть преобразованы в действия **Макрокоманда runmenucommand** . Когда вы откроете макрос, Access отобразит действие **Макрокоманда runmenucommand** с пустым аргументом **Command** для таких команд. Необходимо изменить макрос и ввести допустимый аргумент команды или удалить действие **Макрокоманда runmenucommand** .

Чтобы запустить действие **Макрокоманда runmenucommand** в модуле Visual Basic для приложений (VBA), используйте метод **RunCommand** объекта **Application** . (Это эквивалентно методу **RunCommand** объекта DoCmd **** .)

