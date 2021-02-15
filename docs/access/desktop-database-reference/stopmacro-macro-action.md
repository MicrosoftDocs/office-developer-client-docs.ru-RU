---
title: Макрокоманда StopMacro
TOCTitle: StopMacro macro action
ms:assetid: 6bbf9026-4536-43f2-aa43-3f2ecea01005
ms:mtpsurl: https://msdn.microsoft.com/library/Ff195473(v=office.15)
ms:contentKeyID: 48545455
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe319e0f7a811d3bcd3b2fc18c4a3d951187fbe8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308500"
---
# <a name="stopmacro-macro-action"></a>Макрокоманда StopMacro

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **StopMacro,** чтобы остановить текущий запущенный макрос.

## <a name="setting"></a>Setting

У **действия StopMacro** нет аргументов.

## <a name="remarks"></a>Заметки

Обычно это действие используется, когда условие делает необходимым остановить макрос. В строке действий макроса можно использовать условное выражение, которое содержит это действие. Если выражение имеет  true (–1), Microsoft Access останавливает макрос.

Например, можно создать макрос, который открывает форму, в которой отображаются ежедневные итоговые числа заказов для даты, введенной в настраиваемом диалоговом окне. Можно использовать условное выражение, чтобы  убедиться, что в поле "Дата заказа" содержится допустимая дата. Если это не так, действие **MessageBox** может отображать сообщение об ошибке, а действие **StopMacro** может остановить макрос.

Если макрос использовал действия **Echo** или **SetWarnings** для отключения эха или отображения системных сообщений, действие **StopMacro** автоматически включает их.

Это действие не доступно в модуле Visual Basic для приложений (VBA).

## <a name="example"></a>Пример

Следующий макрос демонстрирует использование действия **OnError.** В этом примере действие **OnError** указывает, что Access при ошибке запустит пользовательский макрос обработки ошибок с именем ErrorHandler. При ошибке будет вызван подмакро CatchErrors. Если номер ошибки 2102, отображается определенное сообщение и выполнение макроса остановлено. В противном случае отображается сообщение с описанием ошибки и макрос приостанавлется, чтобы можно было выполнить дополнительные устранение неполадок. Макрос ErrorHandler отображает окно сообщения, которое ссылается на объект **MacroError** для отображения сведений об ошибке.

**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).

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
