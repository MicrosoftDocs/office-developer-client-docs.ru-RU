---
title: Действия ОстановитьМакрос макроса
TOCTitle: StopMacro Macro Action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3880b57e235520e3351ef16282fb8883d93b11e3
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873714"
---
# <a name="stopmacro-macro-action"></a>Действия ОстановитьМакрос макроса

**Применимо к**: Access 2013, Office 2013

Можно использовать действие **ОстановитьМакрос** Остановка текущего выполняемого макроса.

## <a name="setting"></a>Параметр

Действие **ОстановитьМакрос** не требует аргументов.

## <a name="remarks"></a>Замечания

Это действие обычно используется для остановки макроса при выполнении определенного условия. В строке действие макрос, содержащий это действие можно использовать условного выражения. Когда вычисление выражения дает значение **True** (– 1), Microsoft Access останавливает макрос.

Например можно создать макрос, который открывает формы с ежедневного итоговых значений для даты, введенные в настраиваемого диалогового окна. Чтобы убедиться, что к элементу управления **Дата заказа** на диалоговое окно содержит допустимая дата можно использовать условного выражения. В противном случае действие **MessageBox** может отображаться сообщение об ошибке и завершить действие **ОстановитьМакрос** макрос.

Если макрос действия **эхо** или **УстановитьСообщения** эхо или вывод системных сообщений, действие **ОстановитьМакрос** автоматически включает их обратно.

Это действие недоступно в Visual Basic для приложений (VBA) модуля.

## <a name="example"></a>Пример

Следующий макрос демонстрируется использование **ПриОшибке** . В этом примере **ПриОшибке** выполнение доступа обработка макрос с именем ErrorHandler при возникновении ошибки настраиваемых ошибок. При возникновении ошибки называется вложенный макрос CatchErrors. Если номер ошибки 2102, отображается определенное сообщение и выполнение макроса прекращается. В противном случае отображается сообщение об ошибке и макрос приостановлен, поэтому можно выполнить дополнительные настройки. Макрос ErrorHandler отображается окно сообщения, на который ссылается на объект **MacroError** для отображения сведений об ошибке.

**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

```vb
    /* MACRO: mcrThrowErrors                                  */
    /* PURPOSE: Error handling using macros in Access 2010    */
    
    OnError
        Go to Macro Name
        Macro Name CatchErrors
    
    OpenForm 
        Form Name frmSamples
        View Form
        Filter Name
        Where Condition
        Data Mode
        Window Mode Normal
    
    MessageBox 
        Message This message appears after the OpenForm action
        Beep Yes
        Type None
        Title
    
    
    /* SUBMACRO: CatchErrors                                   */
    
    SubMacro: CatchErrors
        If [MacroError].[Number]=2101 Then
            MessageBox
                Message Cannot find the specified form!
                Beep Yes
                Type Critical
                Title
            StopMacro
    
        Else
            MessageBox
                Message =[MacroErro].[Description]
                Beep Yes
                Type None
                Title Unhandled Error
    
            SingleStep
        End If
    
    End SubMacro
```
