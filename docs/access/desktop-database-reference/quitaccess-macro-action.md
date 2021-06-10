---
title: Макрокоманда QuitAccess
TOCTitle: QuitAccess macro action
ms:assetid: af063f65-d3b1-fa9a-4bc1-04b0d21d62b9
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821759(v=office.15)
ms:contentKeyID: 48547089
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm96777
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 424b2b2cab9bc4272052a201350a0cc2ab297b8c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32302816"
---
# <a name="quitaccess-macro-action"></a>Макрокоманда QuitAccess

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **QuitAccess** для выхода из Microsoft Access. Действие **QuitAccess** также может указать один из нескольких вариантов сохранения объектов базы данных перед выходом из Access.

> [!NOTE]
> Эта макрокоманда доступна только для доверенных баз данных. 

## <a name="setting"></a>Параметр

Действие **QuitAccess имеет** следующий аргумент.

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
<td><p><strong>Options</strong></p></td>
<td><p>Указывает, что происходит с неохабными объектами при выходе из Access. Щелкните Подсказка <strong>(чтобы</strong> отобразить диалоговые окна, которые просят сохранить каждый <strong>объект),</strong> Сохранить все (сохранить все объекты без запроса диалоговых ящиков) или <strong>Exit</strong> (чтобы выйти без сохранения каких-либо объектов) в поле <strong>Параметры</strong> в разделе <strong>Аргументы</strong> действий в области Macro Builder. По умолчанию <strong>сохраняется все</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Доступ не выполнит действий, которые следуют действию **QuitAccess в** макросе.

Это действие можно использовать, чтобы выйти из Access без подсказки из диалогов с сохранением диалогов, используя настраиваемую команду меню или кнопку на форме.  Например, у вас может быть мастер-форма, используемая для отображения объектов в настраиваемом рабочем пространстве. В этой форме может быть кнопка **Quit,** на которой выполняется макрос, содержащий действие **QuitAccess** с аргументом **Options** set to **Save All**.

Это действие имеет тот же эффект, что щелкнуть вкладку **Файл** и нажать кнопку **Exit**. Если при нажатии этой команды у вас есть какие-либо неоплаченные объекты, диалоговые  окна, которые отображаются, такие же, как и те, которые отображаются при использовании аргумента **"Подсказка"** для аргумента Параметры действия **QuitAccess.**

Вы можете использовать **действие SaveObject** в макрос для сохранения указанного объекта, не выходя из Access или закрывая объект.

Чтобы выполнить **действие QuitAccess** в Visual Basic для приложений (VBA), используйте метод **Quit** объекта **DoCmd.**

