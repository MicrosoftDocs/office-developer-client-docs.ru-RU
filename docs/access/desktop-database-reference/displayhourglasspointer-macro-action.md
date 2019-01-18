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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715132"
---
# <a name="displayhourglasspointer-macro-action"></a>Макрокоманда DisplayHourglassPointer


**Применимо к**: Access 2013, Office 2013

Чтобы изменить указатель мыши на изображение песочными можно использовать действие **DisplayHourglassPointer** (или другой значок выбора) во время выполнения макроса. Это действие может предоставить визуальный индикатор, на котором выполняется макрос. Эта функция особенно полезна, когда действия макроса или самого макроса занимает много времени для запуска.

## <a name="setting"></a>Setting

Действие **DisplayHourglassPointer** использует следующий аргумент.

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
<td><p><strong>Включить</strong></p></td>
<td><p>Нажмите кнопку <strong>Да</strong> (отображение значка) или <strong>Нет</strong> (Отображение обычной указателем мыши) в поле <strong>Включить</strong> в разделе <strong>Действие аргументы</strong> в области построения макросов. По умолчанию используется значение <strong>Да</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

Это действие часто используется, если вы отключили эхо с помощью действия **эхо** . При отключенном эхо приостанавливается обновления экрана до завершения макроса.

Access автоматически устанавливает **Песочные часы для** аргумента **не** после завершения выполнения макроса.

> [!NOTE]
> - В Microsoft Windows это значок, заданные для **«занят»** в диалоговом окне **Свойства: мышь** панели управления Windows. Значение по умолчанию для всех операционных систем Windows — значок анимационной песочными часами.
> - Если вы хотите, чтобы можно выбрать другой значок.

Чтобы выполнить действие **DisplayHourglassPointer** в Visual Basic для приложений (VBA) модуль, используйте метод **песочные часы** **объекта** .

