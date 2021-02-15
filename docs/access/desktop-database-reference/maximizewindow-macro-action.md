---
title: Макрокоманда MaximizeWindow
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289751"
---
# <a name="maximizewindow-macro-action"></a>Макрокоманда MaximizeWindow

**Область применения**: Access 2013, Office 2013

Если Access настроен на использование перекрывающихся окон вместо документов с вкладками, можно использовать действие **MaximizeWindow** для увеличения активного окна, чтобы оно заполняло окно Access. Это действие позволит увидеть как можно больше объектов в активном окне.

> [!NOTE]
> Это действие нельзя применить к окнам кода в редакторе Visual Basic. Сведения о том, как повлиять на окна кода, см. в разделе о **свойстве WindowState.**

## <a name="setting"></a>Setting

Действие **MaximizeWindow** не имеет аргументов.

## <a name="remarks"></a>Заметки

Это действие имеет тот же  эффект, что и нажатие кнопки "Развернуть" в правом верхнем углу окна или нажатие кнопки **"Развернуть"** в меню "Управление" **окна.**

С помощью действия **RestoreWindow** можно восстановить максимальное окно предыдущего размера.

> [!TIP]
> - Вам может потребоваться использовать **действие SelectObject,** если окно, для достижения максимального увеличения, не является активным окном.
> - При максимальном наличии окна в Access все остальные окна также будут максимально раскрыт при их отключении или переключении на них. Однако всплывающие формы не являются максимальные. Если вы хотите, чтобы форма сохраняла свой размер при максимальном масштабе других окон, установите для ее свойства **PopUp** свойство **Yes.**

Для запуска действия **MaximizeWindow** в Visual Basic для приложений используйте метод **Maximize** объекта **DoCmd.**

