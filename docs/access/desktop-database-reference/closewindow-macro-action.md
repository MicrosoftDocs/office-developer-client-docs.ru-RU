---
title: Макрокоманда CloseWindow
TOCTitle: CloseWindow macro action
ms:assetid: ba96bc26-7f3f-fd3d-8d3a-e18bfe90cdf0
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822510(v=office.15)
ms:contentKeyID: 48547377
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm64319
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 4397846abdc0d10b6bfa0e6a1eb5c0c435fc862a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296292"
---
# <a name="closewindow-macro-action"></a>Макрокоманда CloseWindow


**Область применения**: Access 2013, Office 2013

Действие **CloseWindow** можно использовать для закрытия указанной вкладки документа Access или активной вкладки документа, если ее нет.

## <a name="setting"></a>Параметр

Действие **CloseWindow** имеет следующие аргументы.

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
<td><p><strong>Object Type</strong></p></td>
<td><p>Тип объекта, на вкладке документа которого необходимо закрыть. <strong>Щелкните</strong> <strong>таблицу,</strong> <strong>запрос,</strong>форма, отчет, макрос, модуль, <strong></strong> <strong></strong>страница доступа <strong></strong> к данным, представление сервера, схема, сохраненная процедура или функция в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> Чтобы выбрать активную вкладку документа, оставьте этот аргумент пустым.</p>

> [!NOTE]
> Если вы закрываете модуль в редакторе Visual Basic, необходимо использовать **модуль** в **аргументе Object Type.**


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя объекта, который будет закрыт. Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>. Щелкните объект, чтобы закрыть. Если оставить аргумент <strong>Object Type</strong> пустым, оставьте этот аргумент пустым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Save</strong></p></td>
<td><p>Следует ли сохранять изменения в объекте при его закрытии. Нажмите <strong>кнопку Да</strong> (сохраните объект), <strong>Нет</strong> (закрой объект, не сэкономив его) или Запрос <strong>(подскажут</strong> пользователю, следует ли сохранять объект). По умолчанию — <strong>запрос</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Действие **CloseWindow работает** на всех объектах базы данных, которые пользователь может открыто открыть или закрыть. Это действие имеет тот же эффект, что и выбор объекта, а затем его закрытие, щелкнув правой кнопкой мыши  вкладку документа объекта, а затем щелкнув кнопку **Закрыть** в меню ярлык, или нажав кнопку Закрыть для объекта.

Если для аргумента **Сохранить** установлено имя **"Запрос",** а объект еще не был сохранен до того, как будет выполнено действие **CloseWindow,** диалоговое окно подсказает пользователю сохранить объект до закрытия макроса. Если для аргумента действия **SetWarnings** заочно установлено предупреждение, диалоговое окно не отображается, и объект автоматически сберегается. 

Чтобы выполнить действие **CloseWindow** в Visual Basic для приложений (VBA), используйте метод **CloseWindow** объекта **DoCmd.**

