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

Чтобы остановить выполняемый в данный момент макрос, можно использовать действие **Макрокоманда StopMacro** .

## <a name="setting"></a>Параметр

Макрокоманда **Макрокоманда StopMacro** не содержит аргументов.

## <a name="remarks"></a>Примечания

Обычно это действие используется при условии, что необходимо остановить макрос. В строке действий макроса, содержащей это действие, можно использовать условное выражение. Если выражение имеет **значение true** (– 1), макрос будет остановлен.

Например, вы можете создать макрос, который открывает форму, в которой показаны ежедневные итоговые значения для даты, введенной в настраиваемом диалоговом окне. Можно использовать условное выражение, чтобы убедиться, что элемент управления " **Дата заказа** " в диалоговом окне содержит допустимую дату. В противном случае действие **MessageBox** может отобразить сообщение об ошибке, а действие **Макрокоманда StopMacro** может остановить макрос.

Если в макросе используются действия **echo** или **сетварнингс** , чтобы включить эхо или отображение системных сообщений, действие **Макрокоманда StopMacro** автоматически включает их снова.

Это действие недоступно в модуле Visual Basic для приложений (VBA).

## <a name="example"></a>Пример

В следующем макросе показано использование действия **OnError** . В этом примере действие **OnError** указывает, что Access выполняет макрос обработки настраиваемых ошибок с именем ErrorHandler при возникновении ошибки. При возникновении ошибки вызывается вложенный макрос Катчеррорс. Если номер ошибки 2102, отображается конкретное сообщение, а выполнение макроса приостанавливается. В противном случае отображается сообщение об ошибке, и макрос приостанавливается, чтобы можно было выполнить дополнительные действия по устранению неполадок. В макросе ErrorHandler отображается окно сообщения, которое ссылается на объект **MacroError** , чтобы отобразить сведения об ошибке.

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
