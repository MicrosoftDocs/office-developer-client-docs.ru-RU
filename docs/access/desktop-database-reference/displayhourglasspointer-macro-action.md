---
title: Макрокоманда DisplayHourglassPointer
TOCTitle: DisplayHourglassPointer macro action
ms:assetid: 2c93039a-f75c-abeb-1dfa-e632a5bdf6f2
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192103(v=office.15)
ms:contentKeyID: 48543957
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm117200
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: a5635b2b97066394b8596dbcdb50c84abf429719
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293835"
---
# <a name="displayhourglasspointer-macro-action"></a>Макрокоманда DisplayHourglassPointer


**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **дисплайхаургласспоинтер** , чтобы изменить указатель мыши на изображение песочных часов (или другой значок, который вы выбрали) во время выполнения макроса. Это действие может предоставить визуальную индикацию выполнения макроса. Это особенно полезно, если для запуска макрокоманды или самого макроса требуется много времени.

## <a name="setting"></a>Параметр

Действие **дисплайхаургласспоинтер** имеет следующий аргумент.

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
<td><p><strong>Песочные часы</strong></p></td>
<td><p>Нажмите кнопку <strong>Да</strong> (отображать значок) или <strong>нет</strong> (отображать обычный указатель мыши) в поле <strong>Песочные часы</strong> в разделе <strong>аргументы макрокоманды</strong> в области построителя макросов. Значение по умолчанию — <strong>Yes</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Это действие часто используется, если вы отключили эхо с помощью макрокоманды **echo** . Когда ECHO отключено, Access приостанавливает обновление экрана до завершения макроса.

Access автоматически сбрасывает значение параметра " **песочНые часы** " в значение " **нет** " при завершении выполнения макроса.

> [!NOTE]
> - В Microsoft Windows это значок, заданный для свойства " **занято** " в диалоговом окне " **Свойства мыши** " на панели управления Windows. По умолчанию для всех операционных систем Windows используется анимированный значок песочных часов.
> - При необходимости можно выбрать другой значок.

Чтобы запустить действие **дисплайхаургласспоинтер** в модуле Visual Basic для приложений (VBA), используйте метод песочных **часов** объекта DoCmd **** .

