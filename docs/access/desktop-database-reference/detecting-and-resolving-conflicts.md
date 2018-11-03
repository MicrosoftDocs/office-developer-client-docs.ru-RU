---
title: Обнаружение и устранение конфликтов
TOCTitle: Detecting and resolving conflicts
ms:assetid: 8299745b-e595-21d5-26c1-a078d00a1c0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249566(v=office.15)
ms:contentKeyID: 48545983
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: c267f33577f3fb2a8d586d33949325517bcc16ba
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944419"
---
# <a name="detecting-and-resolving-conflicts"></a>Обнаружение и устранение конфликтов

**Применимо к**: Access 2013, Office 2013

## <a name="detecting-and-resolving-conflicts"></a>Обнаружение и разрешение конфликтов

Если вы имеете дело с вашего **набора записей** в режиме интерпретации, существует значительно снижают вероятность возникновения проблем параллелизма в случае. С другой стороны, если приложение использует режим обновление пакета, может существовать хорошо вероятность того, что один пользователь будет изменение записи перед сохранением изменений, внесенных другим пользователем, редактирования и той же записи. В этом случае требуется приложение дело конфликта. Может быть нежелательным, последний участник отправить обновление на сервере «wins.» Или может понадобиться разрешить самыми последними пользователю решить, какие обновления должны имеют приоритет, предоставляя ему возможность выбора из двух конфликтующие значения.

В любом случае ADO предоставляет свойства **UnderlyingValue** и **OriginalValue** объекта **поля** для обработки подобных конфликтов. Используйте эти свойства в сочетании с **выполнить повторную синхронизацию** методов и свойств **фильтра** набора **записей**.

## <a name="detecting-errors"></a>Обнаружение ошибок

Когда ADO обнаруживает конфликт во время пакетного обновления, предупреждение переводятся в семейство **Errors** . Таким образом следует всегда проверять наличие ошибок сразу же после вызова **BatchUpdate**и если, найти начать тестирование предполагается, что вы столкнулись конфликта. Первым шагом является установка свойств **фильтра** для **набора записей** равно **adFilterConflictingRecords** (свойство **фильтра** , описывается в предыдущей главе). Этот параметр ограничивает представления на набора **записей** только те записи, которые находятся в конфликта. Если свойство **RecordCount** равна нулю после выполнения этого шага, известно, что не конфликта возникшей ошибке.

При вызове **BatchUpdate**, ADO и поставщика Создание инструкций SQL для выполнения операций обновления в источнике данных. Помните, что некоторые источники данных ограничения, на которых можно использовать типы столбцов в предложении WHERE.

Затем вызовите метод **выполнить повторную синхронизацию** для **набора записей** с аргументом *AffectRecords* , равным **adAffectGroup** и *ResyncValues* аргумент, равным **adResyncUnderlyingValues**. Метод **выполнить повторную синхронизацию** обновляет данные в текущий объект **набора записей** из базы данных. С помощью **adAffectGroup**, проверка того, что только записи, видны с текущий фильтр, параметр, то есть только конфликтующие записи заново синхронизируются с базой данных. Это может сделать значительную разницу в производительности при работе с большого **набора записей**. Путем установки для параметра аргумент *ResyncValues* **adResyncUnderlyingValues** при вызове **выполнить повторную синхронизацию**, убедитесь, что свойство **UnderlyingValue** будет содержать значение (конфликтующие) из базы данных, **значение** свойство будет обрабатывать значения, введенные пользователем, и, что свойство **OriginalValue** будет использоваться для хранения исходное значение для поля (значение, что и до последнего успешного вызова **UpdateBatch** ). Затем можно использовать эти значения программным путем разрешения конфликта или требуют, чтобы выбрать значение, которое будет использоваться пользователь.

В следующем примере кода показан этот метод. Конфликт искусственно создается с помощью отдельных **записей** для изменения значения в таблице до вызова **UpdateBatch** .

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

Чтобы определить, какой тип конфликта произошла можно использовать свойство **состояние** текущей **записи** или **поля** .

Более подробные сведения об ошибках, см [Глава 6: обработки ошибок](chapter-6-error-handling.md).

