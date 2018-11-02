---
title: Макрокоманда OnError
TOCTitle: OnError macro action
ms:assetid: 5c6073c4-2c0f-0ed2-83b0-477636e2d81c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194562(v=office.15)
ms:contentKeyID: 48545088
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm62274
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 38dc9491a03d2bfa043bddec84efd7fc12c5d08a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25919124"
---
# <a name="onerror-macro-action"></a>Макрокоманда OnError

**Применимо к**: Access 2013, Office 2013

Чтобы указать, что должно происходить при возникновении ошибки в макросе, можно использовать **ПриОшибке** .

## <a name="setting"></a>Параметр

**ПриОшибке** имеет следующие аргументы.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Аргумент макрокоманды</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Перейти к разделу</p></td>
<td><p>Укажите общее поведение, которое должно происходить при возникновении ошибки. Щелкните стрелку раскрывающегося списка и выберите один из следующих параметров:</p>
<div class="tableSection">
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Параметр</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Далее</strong></p></td>
<td><p>Microsoft Office Access 2007 записывает сведения об ошибке в объекте <strong>MacroError</strong> , но не останавливается макрос. Макрос по-прежнему производится с помощью следующего действия.</p></td>
</tr>
<tr class="even">
<td><p><strong>Имя макроса</strong></p></td>
<td><p>Access останавливает текущего макроса и запускает макрос, который называется в качестве аргумента <strong>Имя макроса</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>Ошибка</strong></p></td>
<td><p>Access останавливает текущего макроса и отображает сообщение об ошибке.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>Имя макроса</p></td>
<td><p>Если имя макроса перейти к аргумент, введите имя макроса, которое будет использоваться для обработки ошибок. Имя, введенное должно соответствовать имени в столбце <strong>Имя макроса</strong> текущего макроса; не удается введите имя объекта другого макроса. В приведенном ниже примере макрос <strong>ErrorHandler</strong> содержится в один и тот же объект макрос как <strong>ПриОшибке</strong> . Этот аргумент должно остаться пустым, если значение перейти к аргумент <strong>следующий</strong> или <strong>с ошибкой</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

- **ПриОшибке** обычно размещается в начале макросов, но также можно помещать действие далее в макрос. Правила, созданные действие вступят в силу при запуске действия.

- Если аргумент к **сбою**значение находится вне офиса, Access ведет себя так же, как при не выполнялись никаких действий **OnError** в макрос. То есть если обнаружена ошибка, Access останавливает макрос и отображает сообщение об ошибке стандартный. Параметр **с ошибкой** в главном используется для отключения обработки ошибок, установленная ранее в макрос.

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
