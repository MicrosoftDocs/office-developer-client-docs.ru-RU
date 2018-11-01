---
title: 'Пример: свойства Description, HelpContext, HelpFile (VB)'
TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VB)
ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15)
ms:contentKeyID: 48544304
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1e1aeb7166a52e46951025adbbb2532e0dfa5a9b
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882366"
---
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a>Пример использования свойств Description, HelpContext, HelpFile, NativeError, Number, Source и SQLState (VB)


**Применимо к**: Access 2013, Office 2013

В этом примере вызывает ошибку, его перехватывает и отображает [Описание](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [файл справки](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [номер](number-property-ado.md), [источника](source-property-ado-error.md)и свойства [SQLState](sqlstate-property-ado.md) итоговый [Ошибка](error-object-ado.md) объект.

```vb
    'BeginDescriptionVB
    Public Sub Main()
    
        Dim Cnxn As ADODB.Connection
        Dim Err As ADODB.Error
        Dim strError As String
        
        On Error GoTo ErrorHandler
        
        ' Intentionally trigger an error
        Set Cnxn = New ADODB.Connection
        Cnxn.Open "nothing"
        
        Set Cnxn = Nothing
        Exit Sub
    
    ErrorHandler:
    
        ' Enumerate Errors collection and display
        ' properties of each Error object
        For Each Err In Cnxn.Errors
            strError = "Error #" & Err.Number & vbCr & _
                "   " & Err.Description & vbCr & _
                "   (Source: " & Err.Source & ")" & vbCr & _
                "   (SQL State: " & Err.SQLState & ")" & vbCr & _
                "   (NativeError: " & Err.NativeError & ")" & vbCr
            If Err.HelpFile = "" Then
                strError = strError & "   No Help file available"
            Else
                strError = strError & _
                   "   (HelpFile: " & Err.HelpFile & ")" & vbCr & _
                   "   (HelpContext: " & Err.HelpContext & ")" & _
                   vbCr & vbCr
            End If
             
            Debug.Print strError
        Next
    
        Resume Next
    End Sub
    'EndDescriptionVB
```
