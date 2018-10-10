---
title: MaximizeWindow Macro Action
TOCTitle: MaximizeWindow Macro Action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b612d050d6c523ae836b21aa27826ff180e8f977
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481249"
---
# <a name="maximizewindow-macro-action"></a>MaximizeWindow Macro Action


**Применимо к**: Access 2013 | Office 2013

Если доступа настроены на использование перекрывающиеся windows вместо вкладками, можно использовать действие **MaximizeWindow** увеличить размер активного окна, чтобы он заполняет окна клиента. Это действие позволит увидеть столько объекта в активном окне ответов.


> [!NOTE]
> <P>Это действие не может применяться к windows кода в редакторе Visual Basic. Для получения сведений о действиях с кодом windows приведены в разделе свойство <STRONG>WindowState</STRONG> .</P>



## <a name="setting"></a>Параметр

Действие **MaximizeWindow** не требует аргументов.

## <a name="remarks"></a>Замечания

Это действие имеет тот же эффект, нажав кнопку **Развернуть** в правом верхнем углу окна или нажав кнопку **Развернуть** в **элемент управления** меню.

Действие **RestoreWindow** можно использовать для восстановления предыдущих размеров развернутого окна.

**Советы **

  - Может потребоваться **Макрокоманда Если окно, которое требуется развернуть, не является активным** .

  - При развертывании окна в Access все остальные окна также будут развернуты при открытии или переключении на них. Тем не менее не развертываются всплывающих форм. Форма для сохранения его размер при развертывании других окон, установите его свойство **всплывающее окно** значение **Да**.

Чтобы выполнить действие **MaximizeWindow** в Visual Basic для приложений модуль, используйте метод **Развернуть** **объекта** .

