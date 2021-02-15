---
title: Макрокоманда SelectObject
TOCTitle: SelectObject macro action
ms:assetid: a90539a0-c5a0-e997-9c25-e0972d28f2a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821420(v=office.15)
ms:contentKeyID: 48546914
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm41840
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6287bc8a66858d51d65c37477eed7a86cd7839af
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308731"
---
# <a name="selectobject-macro-action"></a>Макрокоманда SelectObject

**Область применения**: Access 2013, Office 2013

С помощью действия **SelectObject можно** выбрать указанный объект базы данных.

## <a name="setting"></a>Setting

Действие **SelectObject** имеет следующие аргументы.

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
<td><p>Тип объекта базы данных, который необходимо выбрать. Щелкните <strong>"Таблица",</strong>"Запрос", "Форма", "Отчет", "Макрос", <strong></strong> "Модуль", <strong></strong> "Страница доступа к данным", "Представление сервера", "Схема", "Хранимая процедура" или "Функция" в поле "Тип объекта" в разделе "Аргументы действий" области построитель макроса. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> Это обязательный аргумент.</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя выбираемого объекта. Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>. Это необходимый аргумент, если только для аргумента "В области навигации" не установлено <strong>"Да".</strong></p><p><strong>ПРИМЕЧАНИЕ.</strong>Имена объектов <STRONG>представления</STRONG> <STRONG>сервера,</STRONG>схемы или хранимых <STRONG></STRONG> процедур не отображаются в поле "Имя объекта" проекта Access (ADP). <STRONG></STRONG></p></td>
</tr>
<tr class="odd">
<td><p><strong>В области навигации</strong></p></td>
<td><p>Указывает, выбирает ли Microsoft Access объект в области навигации. Нажмите <strong>кнопку</strong> "Да" (чтобы выбрать объект в области навигации) или <strong>"Нет"</strong> (чтобы не выбирать объект в области навигации). По умолчанию используется значение <strong>Нет</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Действие **SelectObject** работает с любым объектом Access, который может получить фокус. Это действие предоставляет указанному объекту фокус и показывает объект, если он скрыт. Если объект является формой, действие **SelectObject** задает для свойства **Visible** формы свойство **Yes** и возвращает форму в режим, замеенный свойствами формы (например, в виде модальной или всплывающее формы).

Если объект не открыт в одном из других окон Access, его можно выбрать  в области навигации, установив для аргумента в области навигации **"Да".** Если для  аргумента в области навигации установлено **"Нет",** при попытке выбрать объект, который не открыт, появляется сообщение об ошибке.

Часто это действие можно использовать для выбора объекта, для которого необходимо выполнить дополнительные действия. Например, если в Access настроено использование перекрывающихся окон вместо документов с вкладками, может потребоваться восстановить свернутый объект (с помощью действия **RestoreWindow)** или развернуть окно с объектом, с помощью действия **MaximizeWindow.**

При выборе формы можно использовать действия **GoToControl,** **GoToRecord** и **GoToPage** для перемещения в определенные области формы. Действие **GoToRecord** также работает для таблиц.

Чтобы запустить **действие SelectObject** в модуле Visual Basic для приложений (VBA), используйте метод **SelectObject** объекта **DoCmd.**

