---
title: Макрокоманда RestoreWindow
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 35637781035b7a449ba574cf5f6c84f2cb5223db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32306589"
---
# <a name="restorewindow-macro-action"></a>Макрокоманда RestoreWindow

**Область применения**: Access 2013, Office 2013

С помощью действия **RestoreWindow** можно восстановить максимальное или свернутое окно до предыдущего размера.

> [!NOTE]
> Это действие нельзя применить к окнам кода в редакторе Visual Basic. Сведения о том, как повлиять на окна кода, см. в разделе о **свойстве WindowState.**

## <a name="setting"></a>Setting

Действие **RestoreWindow** не имеет аргументов.

## <a name="remarks"></a>Заметки

Это действие работает с выбранным объектом. Если объект свернут, вы можете сначала выбрать его с помощью действия **SelectObject,** а затем восстановить его предыдущий размер с помощью действия **RestoreWindow.**

Действие **MoveAndSizeWindow** можно использовать для перемещения или размера восстановленного окна.

Действие **RestoreWindow** имеет тот же эффект, что и нажатие кнопки "Восстановить" в правом верхнем углу окна или нажатие команды "Восстановить" в меню "Управление" **окна.**  

Чтобы запустить действие **RestoreWindow** в модуле Visual Basic для приложений (VBA), используйте метод **Restore** объекта **DoCmd.**

