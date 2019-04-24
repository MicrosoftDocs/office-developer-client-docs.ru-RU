---
title: Пример свойств EOS и LineSeparator, а затем метод SkipLine (VB)
TOCTitle: EOS and LineSeparator Properties and SkipLine method example (VB)
ms:assetid: 66508541-cc65-e16a-0f8d-2c0b20342b05
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249396(v=office.15)
ms:contentKeyID: 48545340
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2241d61f66ea8599b60bd83a044f2073664f4bbf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293534"
---
# <a name="eos-and-lineseparator-properties-and-skipline-method-example-vb"></a><span data-ttu-id="19ee9-102">Пример свойств EOS и LineSeparator, а затем метод SkipLine (VB)</span><span class="sxs-lookup"><span data-stu-id="19ee9-102">EOS and LineSeparator Properties and SkipLine method example (VB)</span></span>


<span data-ttu-id="19ee9-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="19ee9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="19ee9-104">В этом примере показано, как управлять потоками текста по одной строке за раз.</span><span class="sxs-lookup"><span data-stu-id="19ee9-104">This example demonstrates how to manipulate text streams one line at a time.</span></span> <span data-ttu-id="19ee9-105">Отображается результат изменения разделителя строк с символа возврата каретки/перевода строки (**адкрлф**) на символ перевода строки (**адлф**) или возврата каретки (**адкр**).</span><span class="sxs-lookup"><span data-stu-id="19ee9-105">The effect of changing the line separator from the default carriage return/linefeed (**adCRLF**) to simply linefeed (**adLF**) or carriage return (**adCR**) is shown.</span></span>

```vb 
 
'BeginSkipLineVB 
Private Sub cmdSkipLine_Click() 
 On Error GoTo ErrorHandler 
 
 'Declare variables 
 Dim i As Integer 
 Dim objStream As Stream 
 Dim strLine, strChar As String 
 
 'Instantiate and open stream 
 Set objStream = New Stream 
 objStream.Open 
 
 'Set line separator to line feed 
 objStream.LineSeparator = adLF 
 
 'Load text content of list box into stream 
 'One line at a time 
 For i = 0 To (List1.ListCount - 1) 
 objStream.WriteText List1.List(i), adWriteLine 
 Next 
 
 'Display the entire stream 
 Debug.Print "Whole Stream:" 
 objStream.Position = 0 
 Debug.Print objStream.ReadText 
 
 'Display the first line 
 Debug.Print "First Line:" 
 objStream.Position = 0 
 strLine = objStream.ReadText(adReadLine) 
 Debug.Print strLine 
 Debug.Print "Line length: " + Str(Len(strLine)) 
 
 'Skip a line, then display another line 
 Debug.Print "Third Line:" 
 objStream.SkipLine 
 strLine = objStream.ReadText(adReadLine) 
 Debug.Print strLine 
 Debug.Print "Line length: " + Str(Len(strLine)) 
 
 'Switch line separator to carriage return 
 'All items from list will be considered one line 
 'Assuming no CRs have been loaded into stream 
 Debug.Print "Whole Stream/First Line:" 
 objStream.Position = 0 
 objStream.LineSeparator = adCR 
 strLine = objStream.ReadText(adReadLine) 
 Debug.Print strLine 
 Debug.Print "Line length: " + Str(Len(strLine)) 
 Debug.Print "Stream size: " + Str(objStream.Size) 
 
 'Use EOS to Determine End of Stream 
 Debug.Print "Character by character:" 
 objStream.Position = 0 
 Do Until objStream.EOS 
 strChar = objStream.ReadText(1) 
 Debug.Print strChar 
 Loop 
 
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
 
Private Sub Form_Load() 
 List1.AddItem "This is the first line" 
 List1.AddItem "This is the second line" 
 List1.AddItem "This is the third line" 
End Sub 
'EndSkipLineVB 
```

