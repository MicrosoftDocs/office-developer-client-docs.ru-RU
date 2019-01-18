---
title: Пример использования методов Read, ReadText, Write и WriteText (VB)
TOCTitle: Read, ReadText, Write, and WriteText methods example (VB)
ms:assetid: 13e0bb73-0077-2a15-9ea3-4fd7b3b34787
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248911(v=office.15)
ms:contentKeyID: 48543377
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 44e961d7b3f4b12d8801429ecb78a1a186f5547a
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28714460"
---
# <a name="read-readtext-write-and-writetext-methods-example-vb"></a>Пример использования методов Read, ReadText, Write и WriteText (VB)


**Применимо к**: Access 2013, Office 2013

В этом примере показано, как чтение текстового поля в текст [потока](stream-object-ado.md) и двоичного **потока**. Других свойств и методов, отображаемых включают [позицию](position-property-ado.md), [размер](size-property-ado.md), [набор символов](charset-property-ado.md)и [SetEOS](seteos-method-ado.md).

```vb 
 
'BeginReadVB 
Private Sub cmdRead_Click() 
 On Error GoTo ErrorHandler 
 
 'Declare variables 
 Dim objStream As Stream 
 Dim varA As Variant 
 Dim bytA() As Byte 
 Dim i As Integer 
 Dim strBytes As String 
 
 'Instantiate and Open Stream 
 Set objStream = New Stream 
 objStream.Open 
 
 'Write the text content of a textbox to the stream 
 If Text1.Text = "" Then 
 Err.Raise 1, , "The text field is blank." 
 End If 
 objStream.WriteText Text1.Text 
 
 'Display the text contents and size of the stream 
 objStream.Position = 0 
 Debug.Print "Default text:" 
 Debug.Print objStream.ReadText 
 Debug.Print objStream.Size 
 
 'Switch character set and display 
 objStream.Position = 0 
 objStream.Charset = "Windows-1252" 
 Debug.Print "New Charset text:" 
 Debug.Print objStream.ReadText 
 Debug.Print objStream.Size 
 
 'Switch to a binary stream and display 
 objStream.Position = 0 
 objStream.Type = adTypeBinary 
 Debug.Print "Binary:" 
 Debug.Print objStream.Read 
 Debug.Print objStream.Size 
 
 'Load an array of bytes with the text box text 
 ReDim bytA(Len(Text1.Text)) 
 For i = 1 To Len(Text1.Text) 
 bytA(i - 1) = CByte(Asc(Mid(Text1.Text, i, 1))) 
 Next 
 
 'Write the buffer to the binary stream and display 
 objStream.Position = 0 
 objStream.Write bytA() 
 objStream.SetEOS 
 objStream.Position = 0 
 Debug.Print "Binary after Write:" 
 Debug.Print objStream.Read 
 Debug.Print objStream.Size 
 
 'Switch back to a text stream and display 
 Debug.Print "Translated back:" 
 objStream.Position = 0 
 objStream.Type = adTypeText 
 Debug.Print objStream.ReadText 
 Debug.Print objStream.Size 
 
 ' clean up 
 objStream.Close 
 Set objStream = Nothing 
 Exit Sub 
 
ErrorHandler: 
 ' clean up 
 If Not objStream Is Nothing Then 
 If objStream.State = adStateOpen Then objStream.Close 
 End If 
 Set objStream = Nothing 
 
 If Err <> 0 Then 
 MsgBox Err.Source & "-->" & Err.Description, , "Error" 
 End If 
End Sub 
'EndReadVB 
```

