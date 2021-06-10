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

Вы можете использовать **действие DisplayHourglassPointer,** чтобы изменить указатель мыши на изображение песочных часов (или другой выбранный значок) во время работы макроса. Это действие может дать наглядное представление о том, что макрос запущен. Это особенно полезно, когда макрос или сам макрос занимает много времени для запуска.

## <a name="setting"></a>Параметр

Действие **DisplayHourglassPointer имеет** следующий аргумент.

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
<td><p>Щелкните <strong>Да</strong> (отобразить значок) или <strong>Нет</strong> <strong></strong> (отобразить <strong></strong> обычную указатель мыши) в поле Песочные часы в разделе Аргументы действий области Macro Builder. По умолчанию — <strong>Да.</strong></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Вы часто используете это действие, если вы отключили эхо с помощью **действия Echo.** Когда эхо отключено, Access приостанавливать обновления экрана до завершения макроса.

При запуске макроса доступ автоматически сбрасывает песочные часы **На** **аргументе Нет.**

> [!NOTE]
> - В microsoft Windows это значок, заданной для занят в диалоговом окне **Свойства** мыши Windows панели управления.  По умолчанию для всех Windows операционных систем является анимированный значок песочных часов.
> - Вы можете выбрать другой значок, если хотите.

Чтобы выполнить **действие DisplayHourglassPointer** в модуле Visual Basic для приложений (VBA), используйте метод **Песочные** часы объекта **DoCmd.**

