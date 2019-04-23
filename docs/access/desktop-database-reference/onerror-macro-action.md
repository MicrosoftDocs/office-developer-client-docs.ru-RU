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
localization_priority: Normal
ms.openlocfilehash: a2288d64241f3289505a8b0fafb98062830b0e97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288457"
---
# <a name="onerror-macro-action"></a>Макрокоманда OnError

**Область применения**: Access 2013, Office 2013

Вы можете использовать действие **OnError** , чтобы указать, что должно происходить при возникновении ошибки в макросе.

## <a name="setting"></a>Параметр

Действие **OnError** имеет следующие аргументы.

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
<td><p>Укажите общее поведение, которое должно происходить при обнаружении ошибки. Щелкните стрелку раскрывающегося списка и выберите один из следующих параметров:</p>
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
<td><p><strong>Next</strong></p></td>
<td><p>Microsoft Office Access 2007 записывает сведения об ошибке в объекте <strong>MacroError</strong> , но не останавливает макрос. Макрос переходит к следующему действию.</p></td>
</tr>
<tr class="even">
<td><p><strong>Имя макроса</strong></p></td>
<td><p>Access применяет текущий макрос и запускает макрос с именем в аргументе <strong>имя макроса</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>Ошибк</strong></p></td>
<td><p>Access приостановил текущий макрос и выводит сообщение об ошибке.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>Имя макроса</p></td>
<td><p>Если аргументу Go присвоено значение имя макроса, введите имя макроса, который будет использоваться для обработки ошибок. Введенное имя должно соискать имя в столбце " <strong>имя макроса</strong> " текущего макроса; невозможно ввести имя другого объекта макроса. В приведенном ниже примере макрос <strong>ErrorHandler</strong> находится в том же объекте макроса, что и <strong></strong> действие OnError. Этот аргумент должен оставаться пустым, если аргументу Go присвоено значение <strong>Next</strong> или <strong>Fail</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Замечания

- Действие **OnError** обычно размещается в начале макроса, но вы также можете поместить это действие позже в макрос. Правила, установленные с помощью этого действия, вступят в силу при каждом запуске действия.

- Если присвоить аргументу Go значение **Failed**, то приложение Access работает так же, как при отсутствии действия OnError в макросе. **** То есть при возникновении ошибки Access отключает макрос и отображает стандартное сообщение об ошибке. Основной способ использования параметра **Fail** — отключить обработку ошибок, установленную ранее в макросе.

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
