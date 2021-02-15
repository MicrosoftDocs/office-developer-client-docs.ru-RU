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

С помощью действия **CloseWindow** можно закрыть указанную вкладку документа Access или активную вкладку документа, если она не указана.

## <a name="setting"></a>Setting

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
<td><p>Тип объекта, вкладку документа которого нужно закрыть. Щелкните <strong>"Таблица",</strong>"Запрос", "Форма", "Отчет", "Макрос", <strong></strong> "Модуль", <strong></strong> "Страница доступа к данным", "Представление сервера", "Схема", "Хранимая процедура" или "Функция" в поле "Тип объекта" в разделе "Аргументы действий" области построитель макроса. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> Чтобы выбрать активную вкладку документа, оставьте этот аргумент пустым.</p>

> [!NOTE]
> При закрытии модуля в редакторе Visual Basic необходимо использовать **модуль** в аргументе **"Тип объекта".**


<p></p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя объекта, который необходимо закрыть. Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>. Щелкните объект, чтобы закрыть его. Если оставить аргумент <strong>Object Type</strong> пустым, также оставьте этот аргумент пустым.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Save</strong></p></td>
<td><p>Следует ли сохранять изменения в объекте при его закрытии. Нажмите <strong>кнопку "Да"</strong> (сохранить объект), <strong>"Нет"</strong> (закроем объект без сохранения) или <strong>"Запрос"</strong> (запросите у пользователя, нужно ли сохранять объект). Значение по умолчанию — <strong>Prompt</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Действие **CloseWindow** работает на всех объектах базы данных, которые пользователь может явным образом открыть или закрыть. Это действие действует так же, как при выборе объекта и его закрытии, щелкнув правой кнопкой мыши вкладку  документа объекта, а затем нажав кнопку "Закрыть" в меню "Закрыть" или нажав кнопку "Закрыть" для объекта. 

Если для аргумента **Save** установлено имя **Prompt,** а объект еще не был сохранен до того, как будет выполнено действие **CloseWindow,** пользователю будет предложено сохранить объект, прежде чем макрос закроет его. Если для аргумента **Warnings On** действия **SetWarnings** установлено **"Нет",** диалоговое окно не отображается, и объект автоматически сохраняются.

Чтобы запустить действие **CloseWindow** в модуле Visual Basic для приложений (VBA), используйте метод **CloseWindow** объекта **DoCmd.**

