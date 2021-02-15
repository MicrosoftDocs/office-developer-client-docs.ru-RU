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

Если вы имеете дело с набором **записей** в немедленном режиме, вероятность возникновения проблем с совме характера значительно ниже. С другой стороны, если приложение использует пакетное обновление, существует вероятность того, что один пользователь изменит запись, прежде чем изменения, внесенные другим пользователем, редактирует эту же запись, будут сохранены. В таком случае необходимо, чтобы приложение корректно обрабатывал конфликт. Возможно, вы хотите, чтобы последнее лицо отправило обновление на сервер "wins". Или вы можете позволить последнему пользователю решить, какое обновление должно иметь приоритет, предоставив ему возможность выбора между двумя конфликтующие значениями.

В любом случае ADO предоставляет свойства **UnderlyingValue** и **OriginalValue** объекта **Field** для обработки таких типов конфликтов. Используйте эти свойства в сочетании с методом **Resync** и **свойством Filter** объекта **Recordset.**

## <a name="detecting-errors"></a>Detecting Errors

Когда ADO сталкивается с конфликтом во время пакетного обновления, в коллекцию **ошибок** помещается предупреждение. Поэтому всегда следует проверять ошибки сразу после вызова **BatchUpdate,** и если они находятся, начните проверку предположения о том, что возник конфликт. Первый шаг — установить для свойства **Filter** в наборе **записей** свойство **adFilterConflictingRecords** (свойство **Filter** обсуждается в предыдущей главе). Это ограничивает представление в наборе **recordset** только теми записями, которые находятся в конфликте. Если после этого шага свойство **RecordCount** равно нулю, вы знаете, что ошибка была иной, чем конфликт.

При **вызове BatchUpdate** ADO и поставщик SQL для выполнения обновлений в источнике данных. Помните, что определенные источники данных имеют ограничения на типы столбцов, которые можно использовать в предложении WHERE.

Затем вызовите метод **Resync** в **наборе recordset** с аргументом *AffectRecords,* равным **adAffectGroup,** а аргумент *ResyncValues* равен **adResyncUnderlyingValues.** Метод **Resync** обновляет данные в текущем объекте **Recordset** из баз данных. Используя **adAffectGroup,** вы обеспечиваете синхронизацию с базой данных только записей, видимых с помощью текущего параметра фильтра, то есть только конфликтующих записей. Это может существенно изменить производительность при работе с большим набором **записей.** Задав для аргумента *ResyncValues* значение **adResyncUnderlyingValues** при вызове **Resync,** вы гарантируете, что свойство **UnderlyingValue** будет содержать (конфликтующие) значения из базы данных, что свойство **Value** будет поддерживать введенное пользователем значение, а свойство **OriginalValue** будет содержать исходное значение поля (значение, которое оно было до последнего успешного вызова **UpdateBatch).** Затем вы можете использовать эти значения для разрешения конфликта программным путем или потребовать от пользователя выбрать значение, которое будет использоваться.

Этот метод показан в примере кода ниже. В этом примере искусственно создается  конфликт с помощью отдельного наборов записей для изменения значения в таблице перед тем, как будет вызван **UpdateBatch.**

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

Можно использовать свойство **Status** текущей  записи или  определенного поля, чтобы определить, какой тип конфликта произошел.

Дополнительные сведения об обработке ошибок см. в главе [6 "Обработка ошибок".](chapter-6-error-handling.md)

