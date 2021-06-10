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

Вы можете использовать **действие OnError,** чтобы указать, что должно произойти при ошибке на макросе.

## <a name="setting"></a>Параметр

Действие **OnError приводит** следующие аргументы.

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
<td><p>Укажите общее поведение, которое должно происходить при столкновении с ошибкой. Щелкните выпадаемую стрелку и нажмите один из следующих параметров:</p>
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
<td><p>Microsoft Office Access 2007 записи сведений об ошибке в <strong>объекте MacroError,</strong> но не останавливает макрос. Макрос продолжается следующим действием.</p></td>
</tr>
<tr class="even">
<td><p><strong>Имя макроса</strong></p></td>
<td><p>Доступ останавливает текущий макрос и запускает макрос, названный в <strong>аргументе Macro Name.</strong></p></td>
</tr>
<tr class="odd">
<td><p><strong>Fail</strong></p></td>
<td><p>Доступ останавливает текущий макрос и отображает сообщение об ошибке.</p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p>Имя макроса</p></td>
<td><p>Если аргумент Go to set to Macro Name, введите имя макроса, который будет использоваться для обработки ошибок. Имя, которое вы введите, должно совпадать с именем в столбце <strong>Имя макроса</strong> текущего макроса; вы не можете ввести имя другого объекта макроса. В приведенном ниже примере макрос <strong>ErrorHandler</strong> содержится в том же объекте макроса, что и <strong>действие OnError.</strong> Этот аргумент должен быть оставлен пустым, если аргумент Go to argument настроен на <strong>Next</strong> или <strong>Fail</strong>.</p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

- Действие **OnError** обычно помещается в начале макроса, но вы также можете поместить действие позже в макрос. Правила, установленные действием, вступает в силу при запуске действия.

- Если вы задаёте аргумент Go to **Fail,** access ведет себя так же, как если бы в макросе не было действий **OnError.** То есть, если ошибка встречается, Access останавливает макрос и отображает стандартное сообщение об ошибке. Основное использование параметра **Fail** — отключить обработку ошибок, установленную ранее на макросе.

## <a name="example"></a>Пример

Следующий макрос демонстрирует использование действия **OnError.** В этом примере действие **OnError** указывает, что при ошибке Access запустится настраиваемый макрос обработки ошибок с именем ErrorHandler. При ошибке называется submacro CatchErrors. Если номер ошибки 2102, отображается определенное сообщение и выполнение макроса прекращается. В противном случае отображается сообщение с описанием ошибки и приостановка макроса, чтобы можно было выполнить дополнительные устранения неполадок. Макрос ErrorHandler отображает поле сообщений, которое ссылается на объект **MacroError** для отображения сведений об ошибке.

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
