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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28715951"
---
# <a name="maximizewindow-macro-action"></a>Макрокоманда MaximizeWindow

**Применимо к**: Access 2013, Office 2013

Если доступа настроены на использование перекрывающиеся windows вместо вкладками, можно использовать действие **MaximizeWindow** увеличить размер активного окна, чтобы он заполняет окна клиента. Это действие позволит увидеть столько объекта в активном окне ответов.

> [!NOTE]
> Это действие не может применяться к windows кода в редакторе Visual Basic. Для получения сведений о действиях с кодом windows приведены в разделе свойство **WindowState** .

## <a name="setting"></a>Setting

Действие **MaximizeWindow** не требует аргументов.

## <a name="remarks"></a>Замечания

Это действие имеет тот же эффект, нажав кнопку **Развернуть** в правом верхнем углу окна или нажав кнопку **Развернуть** в **элемент управления** меню.

Действие **RestoreWindow** можно использовать для восстановления предыдущих размеров развернутого окна.

> [!TIP]
> - Может потребоваться **Макрокоманда Если окно, которое требуется развернуть, не является активным** .
> - При развертывании окна в Access все остальные окна также будут развернуты при открытии или переключении на них. Тем не менее не развертываются всплывающих форм. Форма для сохранения его размер при развертывании других окон, установите его свойство **всплывающее окно** значение **Да**.

Чтобы выполнить действие **MaximizeWindow** в Visual Basic для приложений модуль, используйте метод **Развернуть** **объекта** .

