---
title: Submacro Macro Statement
TOCTitle: Submacro Macro Statement
ms:assetid: fb580c19-52cd-c0bd-9117-4fa721eead6b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837173(v=office.15)
ms:contentKeyID: 48548867
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 822875db1cab865ce508b75673539b6c4a426917
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480988"
---
# <a name="submacro-macro-statement"></a>Submacro Macro Statement

**Применимо к**: Access 2013 | Office 2013

Оператор **Вложенный макрос** определяет отдельные макроса в окне конструктор макросов.

## <a name="setting"></a>Параметр

Действие **Вложенный макрос** состоит из следующих аргументов.

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Argument</p></th>
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