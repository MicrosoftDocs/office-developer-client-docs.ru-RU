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

При работе с **наборОм записей** в режиме интерпретации возникает вероятность возникновения проблем с параллелизмом. С другой стороны, если ваше приложение использует обновление в пакетном режиме, может возникнуть подозрение, что один пользователь изменит запись, прежде чем изменения, внесенные другим пользователем при редактировании той же записи, будут сохранены. В этом случае вам потребуется, чтобы ваше приложение корректно обрабатывал конфликт. Возможно, вы хотите, чтобы последний пользователь отправлял обновление на сервер "WINS". Или вы можете предоставить самому последнему пользователю выбрать, какое обновление будет иметь приоритет, предоставив ему выбор между двумя конфликтующими значениями.

Как и в случае, ADO предоставляет свойства **UnderlyingValue** и **originalValue** объекта **field** для обработки этих типов конфликтов. Используйте эти свойства в сочетании с методом **Resync** и свойством **Filter** объекта **Recordset**.

## <a name="detecting-errors"></a>Detecting Errors

Если при пакетном обновлении ADO обнаруживает конфликт, в коллекцию **Errors** будет включено предупреждение. Таким образом, следует всегда проверять наличие ошибок сразу же после вызова **батчупдате**, и если вы их обнаружите, начните проверку предположения, что вы столкнулись с конфликтом. Первый шаг — установка свойства **Filter** в **наборе записей** , равного **адфилтерконфликтингрекордс** (свойство **Filter** рассматривается в предыдущей главе). Это ограничит представление объекта **Recordset** только теми записями, в которых возник конфликт. Если после этого шага свойство **RecordCount** равно нулю, вы знаете, что ошибка вызвана не с помощью конфликта.

При вызове **батчупдате**ADO и поставщик создают инструкции SQL для выполнения обновлений источника данных. Помните, что определенные источники данных имеют ограничения на типы столбцов, которые можно использовать в предложении WHERE.

Затем вызовите метод **Resync** для объекта **Recordset** с набором аргументов *аффектрекордс* , равным **адаффектграуп** , а аргумент *ресинквалуес* , равным **адресинкундерлингвалуес**. Метод **Resync** обновляет данные в текущем объекте **Recordset** из базовой базы данных. С помощью **адаффектграуп**вы гарантируете, что только записи, отображаемые с текущим параметром фильтра, то есть только конфликтующие записи, повторно синхронизируются с базой данных. Это может значительно увеличить производительность, если вы работаете с большим **наборОм записей**. Если присвоить аргументу *ресинквалуес* значение **адресинкундерлингвалуес** при вызове Resync, убедитесь, что в свойстве **UnderlyingValue** будет содержаться значение (конфликтующее) из базы данных, то есть **значение** **** Свойство сохранит значение, введенное пользователем, и что свойство **originalValue** будет содержать исходное значение поля (значение, которое оно имело до последнего успешного вызова **UpdateBatch** ). Затем эти значения можно использовать для программного разрешения конфликта или для того, чтобы пользователь мог выбрать значение, которое будет использоваться.

Этот метод показан в приведенном ниже примере кода. В этом примере искусственно создается конфликт с помощью отдельного **набора записей** для изменения значения в базовой таблице перед вызовом **UpdateBatch** .

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

Можно использовать свойство **Status** текущей **записи** или определенного **поля** , чтобы определить, какой тип конфликта был вызван.

Более подробную информацию об обработке ошибок можно найти в [главе 6: обработка ошибок](chapter-6-error-handling.md).

