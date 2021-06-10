---
title: Макрокоманда ShowToolbar
TOCTitle: ShowToolbar macro action
ms:assetid: 9e53009b-1e5e-1bee-3bcc-f82dc1b0dc48
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198288(v=office.15)
ms:contentKeyID: 48546649
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm27417
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 01ba59ce0898068788adb9269b3203794d1f31d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306477"
---
# <a name="showtoolbar-macro-action"></a>Макрокоманда ShowToolbar

**Область применения**: Access 2013, Office 2013

Вы можете использовать **действие ShowToolbar** для отображения или сокрытия группы команд на вкладке **Надстройки.**

> [!NOTE]
> - Действие **ShowToolbar** не влияет на меню ярлыков.
> - Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **ShowToolbar** имеет следующие аргументы.

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
<td><p><strong>Имя панели инструментов</strong></p></td>
<td><p>Имя группы команд на <strong></strong> вкладке Надстройки, отобразить или скрыть. Поле <strong>Имя панели инструментов</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder показывает все доступные группы, на которые может повлиять это действие. Это обязательный аргумент. При запуске макроса, содержащего действие <strong>ShowToolbar</strong> в базе данных библиотеки, Access сначала ищет группу с этим именем в базе данных библиотеки, а затем в текущей базе данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Show</strong></p></td>
<td><p>Указывает, следует ли отображать или скрывать группу и в каких представлениях ее отображать или скрывать. По умолчанию — <strong>да</strong> (покажите группу всегда). Вы можете выбрать <strong>Да</strong> для отображения группы в любой <strong>момент,</strong> если необходимо отображать группу <strong></strong> только при активной форме или отчете, или Нет, чтобы скрыть группу во все времена.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Это действие можно использовать в макросе с условными выражениями для отображения или сокрытия группы в зависимости от определенных условий.

Если вы хотите показать определенную группу только в одной форме или отчете, можно задать свойство **OnActivate** формы или отчет имени макроса, который содержит действие **ShowToolbar,** чтобы показать группу. Затем установите **свойство OnDeactivate** формы или отчета на имя макроса, который содержит действие **ShowToolbar,** чтобы скрыть группу.

Встроенные панели инструментов недоступны для отображения или сокрытия с помощью этого действия, если вы установите свойство **AllowBuiltInToolbars** false (0) в модуле Visual Basic для приложений (VBA) или если вы установите параметр **Allow Built-in Toolbars** false в VBA с помощью **метода SetOption.**  

Чтобы выполнить **действие ShowToolbar** в модуле VBA, используйте **метод ShowToolbar** объекта **DoCmd.**

