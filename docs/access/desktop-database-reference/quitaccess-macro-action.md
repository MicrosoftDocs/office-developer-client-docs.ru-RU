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

Действие **QuitAccess** имеет следующий аргумент.

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
<td><p>Указывает, что происходит с несравняемой объектами при выходе из Access. Нажмите кнопку "Подсказка" <strong>(чтобы</strong> отобразить диалоговые окна с запросом на сохранение каждого <strong>объекта),</strong> "Сохранить все" (чтобы сохранить все <strong></strong> объекты без запроса по диалоговым окнам) или "Выйти" <strong>(чтобы</strong> выйти без сохранения объектов) в поле <strong>"Параметры"</strong> в разделе "Аргументы действий" области построитель макроса. Значение по умолчанию — <strong>"Сохранить все".</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Access не выполнит никаких действий, которые следуют действию **QuitAccess** в макросе.

Это действие можно использовать для выхода  из Access без подсказок из диалогов сохранения с помощью настраиваемой команды меню или кнопки на форме. Например, у вас может быть этаголовая форма, используемая для отображения объектов в настраиваемой рабочей области. Эта форма может иметь кнопку **Quit,** которая запускает макрос, содержащий действие **QuitAccess** с аргументом **Options,** установленным как **"Сохранить все"**.

Это действие имеет тот же  эффект, что и при нажатии на вкладку "Файл" и нажатии кнопки **"Выход".** Если при нажатии этой команды имеются какие-либо несжатые объекты, отображаются  те же диалоговые окна, что и при использовании запроса аргумента **Options** действия **QuitAccess.**

Вы можете использовать действие **SaveObject** в макросах, чтобы сохранить указанный объект без выхода из Access или закрытия объекта.

Чтобы запустить действие **QuitAccess** в модуле Visual Basic для приложений (VBA), используйте метод **Quit** объекта **DoCmd.**

