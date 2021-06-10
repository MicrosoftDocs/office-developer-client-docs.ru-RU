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

Вы можете использовать **действие SelectObject** для выбора указанного объекта базы данных.

## <a name="setting"></a>Параметр

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
<td><p>Тип объекта базы данных, который нужно выбрать. <strong>Щелкните</strong> <strong>таблицу,</strong> <strong>запрос,</strong>форма, отчет, макрос, модуль, <strong></strong> <strong></strong>страница доступа <strong></strong> к данным, представление сервера, схема, сохраненная процедура или функция в поле Тип объекта в разделе Аргументы действий области Macro Builder. <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> <strong></strong> Это обязательный аргумент.</p></td>
</tr>
<tr class="even">
<td><p><strong>Object Name</strong></p></td>
<td><p>Имя объекта, который нужно выбрать. Поле <strong>Object Name</strong> отображает все объекты базы данных, относящиеся к типу, заданному аргументом <strong>Object Type</strong>. Это необходимый аргумент, если не задать аргументу В области навигации <strong>да.</strong></p><p><strong>ПРИМЕЧАНИЕ.</strong>Имена объектов для <STRONG>объектов Server View,</STRONG> <STRONG>Diagram</STRONG>или <STRONG>Stored Procedure</STRONG> не отображаются в поле <STRONG>Имя</STRONG> объекта проекта Access (.adp).</p></td>
</tr>
<tr class="odd">
<td><p><strong>В области навигации</strong></p></td>
<td><p>Указывает, выбирает ли Microsoft Access объект в области навигации. Щелкните <strong>Да</strong> (чтобы выбрать объект в области навигации) или <strong>Нет</strong> (чтобы не выбрать объект в области навигации). По умолчанию используется значение <strong>Нет</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Действие **SelectObject** работает с любым объектом Access, который может получить фокус. Это действие дает указанному объекту фокус и показывает объект, если он скрыт. Если объект является формой, действие **SelectObject** задает  свойство Видимый  вид формы да и возвращает форму в режим, установленный свойствами формы (например, в виде модальной или всплываемой формы).

Если объект не открыт в одном из других окон Access, его можно выбрать в области навигации, установив аргумент **"Да"** в области **навигации.** Если вы установите аргумент **"Нет"** в области навигации, при попытке выбрать объект, который не открыт, появится сообщение об ошибке.

Часто это действие можно использовать для выбора объекта, на котором необходимо выполнить дополнительные действия. Например, если у вас есть access, настроенный на использование перекрывающихся окон вместо вкладки документов, может потребоваться восстановить объект, который был сведен к минимуму (с помощью действия **RestoreWindow)** или максимально увеличить окно, с которое нужно работать (с помощью действия **MaximizeWindow).**

При выборе формы можно использовать действия **GoToControl,** **GoToRecord** и **GoToPage** для перемещения в определенные области формы. Действие **GoToRecord** также работает для таблиц данных.

Для запуска **действия SelectObject** в Visual Basic для приложений (VBA) используйте метод **SelectObject** объекта **DoCmd.**

