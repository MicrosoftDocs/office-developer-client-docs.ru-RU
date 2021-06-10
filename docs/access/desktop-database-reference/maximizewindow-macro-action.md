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

Если Access настроен на использование перекрывающихся окон вместо вкладки документов, можно использовать действие **MaximizeWindow** для расширения активного окна, чтобы оно заполняло окно Access. Это действие позволит увидеть как можно больше объекта в активном окне.

> [!NOTE]
> Это действие нельзя применить к окнам кода в редакторе Visual Basic. Сведения о том, как повлиять на окна кода, см. в разделе **Свойство WindowState.**

## <a name="setting"></a>Параметр

Действие **MaximizeWindow** не имеет аргументов.

## <a name="remarks"></a>Примечания

Это действие имеет такой же  эффект, как нажатие кнопки "Максимизируем" в верхнем правом углу окна или кнопка **"Максимизируем"** в меню **Управления окном.**

Вы можете использовать действие **RestoreWindow** для восстановления максимального окна до предыдущего размера.

> [!TIP]
> - Возможно, вам потребуется использовать **действие SelectObject,** если окно, в который требуется максимальное время, не является активным окном.
> - При максимальном окне Access все остальные окна также максимально открываются или переключаются на них. Однако всплывающие формы не являются максимальной. Если требуется, чтобы форма сохраняла свой размер при максимальном максимальном наборе других окон, задай свойство **PopUp** **да.**

Чтобы выполнить **действие MaximizeWindow** в Visual Basic для приложений, используйте метод **Maximize** объекта **DoCmd.**

