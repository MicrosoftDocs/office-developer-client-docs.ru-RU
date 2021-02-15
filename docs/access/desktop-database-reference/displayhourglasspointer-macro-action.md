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

С помощью действия **DisplayHourglassPointer** можно изменить указатель мыши на изображение песочных часов (или другого выбранного значка) во время работы макроса. Это действие может предоставить визуальное указание на то, что макрос запущен. Это особенно полезно, если макрос или сам макрос занимает много времени.

## <a name="setting"></a>Setting

Действие **DisplayHourglassPointer** имеет следующий аргумент.

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
<td><p><strong>Hourglass On</strong></p></td>
<td><p>Нажмите <strong>кнопку "Да"</strong> (отобразить значок) или "Нет" <strong></strong> <strong>(отображается</strong> обычный указатель мыши) в поле "Песочные часы <strong>на",</strong> в разделе "Аргументы действий" области построитель макроса. Значение по умолчанию <strong>— Да.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Заметки

Это действие часто используется, если вы отключили эхо с помощью действия **Echo.** Когда эхо выключено, Access приостанавливать обновления экрана, пока макрос не будет завершен.

Access автоматически сбрасывает аргумент **Hourglass On** на **"Нет",** когда макрос завершает работу.

> [!NOTE]
> - В Microsoft Windows это значок,  который вы настроите для "Занят" в диалоговом **окне** "Свойства мыши" панели управления Windows. По умолчанию для всех операционных систем Windows имеется анимированный значок песочных часов.
> - При этом можно выбрать другой значок.

Чтобы запустить действие **DisplayHourglassPointer** в модуле Visual Basic для приложений (VBA), используйте метод **Hourglass** объекта **DoCmd.**

