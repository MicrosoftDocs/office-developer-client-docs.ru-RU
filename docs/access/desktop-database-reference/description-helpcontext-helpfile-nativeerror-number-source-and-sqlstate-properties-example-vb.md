---
title: Пример свойств Description, HelpContext и HelpFile (VB)
TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VB)
ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15)
ms:contentKeyID: 48544304
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 526a393cba640f55e0cab5424752c047c7286a2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294003"
---
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a><span data-ttu-id="3c7b6-102">Пример использования свойств Description, HelpContext, HelpFile, NativeError, Number, Source и SQLState (VB)</span><span class="sxs-lookup"><span data-stu-id="3c7b6-102">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VB)</span></span>


<span data-ttu-id="3c7b6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3c7b6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3c7b6-104">В этом примере вызывается ошибка, она ловка и [](error-object-ado.md) отображаются свойства [Description,](description-property-ado.md) [HelpContext,](helpcontext-helpfile-properties-ado.md) [HelpFile,](helpcontext-helpfile-properties-ado.md) [NativeError,](nativeerror-property-ado.md) [Number,](number-property-ado.md) [Source](source-property-ado-error.md)и [SQLState](sqlstate-property-ado.md) итоговой ошибки.</span><span class="sxs-lookup"><span data-stu-id="3c7b6-104">This example triggers an error, traps it, and displays the [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md), and [SQLState](sqlstate-property-ado.md) properties of the resulting [Error](error-object-ado.md) object.</span></span>

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
