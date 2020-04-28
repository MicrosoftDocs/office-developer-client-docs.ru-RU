---
title: Оператор макроса Submacro
TOCTitle: Submacro macro statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: caabfb0f4e90134c10d5ab728f19e1fd2a4437dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308472"
---
# <a name="submacro-macro-statement"></a>Оператор макроса Submacro

**Область применения**: Access 2013, Office 2013

Оператор **подмакроса** определяет отдельный макрос в окне конструктора макросов.

## <a name="setting"></a>Параметр

Действие вложенного **макроса** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент</p></th>
<th><p>Обязательный</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Имя</p></td>
<td><p>Да</p></td>
<td><p>Строка, которая отображается как имя макроса.</p></td>
</tr>
</tbody>
</table>


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
