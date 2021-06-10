---
title: Обнаружение и разрешение конфликтов
TOCTitle: Detecting and resolving conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ddd7566be2581fe449872eb576bf7f11e5a806fb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293926"
---
# <a name="detecting-and-resolving-conflicts"></a>Обнаружение и разрешение конфликтов

**Область применения**: Access 2013, Office 2013

## <a name="detecting-and-resolving-conflicts"></a>Detecting and Resolving Conflicts

Если вы имеете дело с **набором записей** в непосредственном режиме, вероятность возникновения проблем с валютой значительно меньше. С другой стороны, если в приложении используется пакетное обновление режима, существует вероятность того, что один пользователь изменит запись перед тем, как будут сохранены изменения, внесенные другим пользователем, редактирует ту же запись. В этом случае необходимо, чтобы ваше приложение изящно справив конфликт. Это может быть ваше желание, чтобы последний человек, чтобы отправить обновление на сервер "выигрывает". Или вы можете позволить последнему пользователю решить, какое обновление должно иметь приоритет, предоставив ему выбор между двумя противоречивыми значениями.

В любом случае ADO предоставляет свойства **UnderlyingValue** и **OriginalValue** объекта **Field** для обработки конфликтов такого типа. Используйте эти свойства в сочетании с методом **Resync** и **свойством Filter** в **Recordset.**

## <a name="detecting-errors"></a>Detecting Errors

Когда ADO сталкивается с конфликтом во время пакетного обновления, предупреждение будет помещено в коллекцию **Ошибок.** Поэтому всегда следует проверять ошибки сразу после вызова **BatchUpdate,** и если вы их найдете, начните проверку предположения о том, что вы столкнулись с конфликтом. Первый шаг — установить свойство **Filter** в **наборе Recordset,** равное **adFilterConflictingRecords** (свойство **Filter** обсуждается в предыдущей главе). Это ограничивает представление в наборе **записей** только теми записями, которые находятся в конфликте. Если после этого шага свойство **RecordCount** равно нулю, вы знаете, что ошибка была поднята чем-то другим, кроме конфликта.

При **вызове BatchUpdate** ADO и поставщик генерируют SQL для выполнения обновлений в источнике данных. Помните, что у определенных источников данных есть ограничения, какие типы столбцов можно использовать в пункте WHERE.

Далее позвоните **методу Resync** в **Recordset** с аргументом *AffectRecords,* равным **adAffectGroup** и *аргументу ResyncValues,* равному **adResyncUnderlyingValues**. Метод **Resync** обновляет данные текущего объекта **Recordset** из баз данных. Используя **adAffectGroup,** вы обеспечиваете, чтобы только записи, видимые с текущим параметром фильтра, то есть только конфликтующие записи, ресинхронизировались с базой данных. Это может существенно изменить производительность, если вы имеете дело с большим **набором записей.** Задав аргумент  *ResyncValues* **adResyncUnderlyingValues** при вызове **Resync,** вы убедитесь, что свойство **UnderlyingValue** будет содержать (конфликтующие) значения из базы данных, что свойство Value будет поддерживать значение, введенное пользователем, и что свойство **OriginalValue** будет содержать исходное значение для поля (значение, которое было до последнего успешного вызова **UpdateBatch).** Затем эти значения можно использовать для решения конфликта программным образом или потребовать от пользователя выбора используемой величины.

Этот метод показан в приведенной ниже примере кода. В примере искусственно создается конфликт,  используя отдельный набор записей, чтобы изменить значение в таблице перед тем, как **будет вызвана UpdateBatch.**

```vb 
 
'BeginConflicts 
    On Error GoTo ErrHandler: 
     
    Dim objRs1 As New ADODB.Recordset 
    Dim objRs2 As New ADODB.Recordset 
    Dim strSQL As String 
    Dim strMsg As String 
     
    strSQL = "SELECT * FROM Shippers WHERE ShipperID = 2" 
                  
    'Open Rs and change a value 
    objRs1.CursorLocation = adUseClient 
    objRs1.Open strSQL, strConn, adOpenStatic, adLockBatchOptimistic, adCmdText 
    objRs1("Phone") = "(111) 555-1111" 
     
    'Introduce a conflict at the db... 
    objRs2.Open strSQL, strConn, adOpenKeyset, adLockOptimistic, adCmdText 
    objRs2("Phone") = "(999) 555-9999" 
    objRs2.Update 
    objRs2.Close 
    Set objRs2 = Nothing 
     
    On Error Resume Next 
    objRs1.UpdateBatch 
     
    If objRs1.ActiveConnection.Errors.Count <> 0 Then 
        Dim intConflicts As Integer 
         
        intConflicts = 0 
         
        objRs1.Filter = adFilterConflictingRecords 
         
        intConflicts = objRs1.RecordCount 
         
        'Resync so we can see the UnderlyingValue and offer user a choice. 
        'This sample only displays all three values and resets to original. 
        objRs1.Resync adAffectGroup, adResyncUnderlyingValues 
         
        If intConflicts > 0 Then 
            strMsg = "A conflict occurred with updates for " & intConflicts & _ 
                     " record(s)." & vbCrLf & "The values will be restored" & _ 
                     " to their original values." & vbCrLf & vbCrLf 
                      
            objRs1.MoveFirst 
            While Not objRs1.EOF 
                strMsg = strMsg & "SHIPPER = " & objRs1("CompanyName") & vbCrLf 
                strMsg = strMsg & "Value = " & objRs1("Phone").Value & vbCrLf 
                strMsg = strMsg & "UnderlyingValue = " & _ 
                                   objRs1("Phone").UnderlyingValue & vbCrLf 
                strMsg = strMsg & "OriginalValue = " & _ 
                                   objRs1("Phone").OriginalValue & vbCrLf 
                strMsg = strMsg & vbCrLf & "Original value has been restored." 
                   
                MsgBox strMsg, vbOKOnly, _ 
                      "Conflict " & objRs1.AbsolutePosition & _ 
                      " of " & intConflicts 
                   
                objRs1("Phone").Value = objRs1("Phone").OriginalValue 
                objRs1.MoveNext 
            Wend 
             
            objRs1.UpdateBatch adAffectGroup 
        Else 
            'Other error occurred. Minimal handling in this example. 
             strMsg = "Errors occurred during the update. " & _ 
                        objRs1.ActiveConnection.Errors(0).Number & " " & _ 
                        objRs1.ActiveConnection.Errors(0).Description 
        End If 
         
        On Error GoTo 0 
    End If 
     
    objRs1.MoveFirst 
     
    'Clean up 
    objRs1.Close 
    Set objRs1 = Nothing 
    Exit Sub 
     
ErrHandler: 
    
    If Not objRs1 Is Nothing Then 
        If objRs1.State = adStateOpen Then objRs1.Close 
        Set objRs1 = Nothing 
    End If 
     
    If Not objRs2 Is Nothing Then 
        If objRs2.State = adStateOpen Then objRs2.Close 
        Set objRs2 = Nothing 
    End If 
     
    If Err <> 0 Then 
        MsgBox Err.Source & "-->" & Err.Description, , "Error" 
    End If 
     
'EndConflicts 
```

Для определения того, какой  конфликт произошел,  можно использовать свойство Status текущей записи или определенное поле. 

Дополнительные сведения об обработке ошибок см. в [главе 6. Обработка ошибок.](chapter-6-error-handling.md)

