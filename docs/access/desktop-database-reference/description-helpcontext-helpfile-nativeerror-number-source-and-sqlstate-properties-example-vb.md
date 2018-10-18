---
<span data-ttu-id="bed38-101"><<<<<<< Название HEAD: описание HelpContext, пример свойства HelpFile (VB) TOCTitle: описание, HelpContext, файл справки, NativeError, номер, исходный и пример свойства SQLState (VB) === название: описание, HelpContext, пример свойств HelpFile (VB) TOCTitle: описание, HelpContext, файл справки, NativeError, номер, исходный и SQLState пример свойств (VB)</span><span class="sxs-lookup"><span data-stu-id="bed38-101"><<<<<<< HEAD title: Description, HelpContext, HelpFile Properties Example (VB) TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VB) ======= title: Description, HelpContext, HelpFile properties example (VB) TOCTitle: Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="bed38-102">главные ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15) ms:contentKeyID: 48544304 ms.date: 09/18/2015 mtps_version: v=office.15</span><span class="sxs-lookup"><span data-stu-id="bed38-102">master ms:assetid: 3c129aec-cd69-5822-4dad-ebef226538e1 ms:mtpsurl: https://msdn.microsoft.com/library/JJ249156(v=office.15) ms:contentKeyID: 48544304 ms.date: 09/18/2015 mtps_version: v=office.15</span></span>
---

<span data-ttu-id="bed38-103"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="bed38-103"><<<<<<< HEAD</span></span>
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a><span data-ttu-id="bed38-104">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VB)</span><span class="sxs-lookup"><span data-stu-id="bed38-104">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState Properties Example (VB)</span></span>
=======
# <a name="description-helpcontext-helpfile-nativeerror-number-source-and-sqlstate-properties-example-vb"></a><span data-ttu-id="bed38-105">Пример свойства Description, HelpContext, файл справки, NativeError, номер, исходный и SQLState (VB)</span><span class="sxs-lookup"><span data-stu-id="bed38-105">Description, HelpContext, HelpFile, NativeError, Number, Source, and SQLState properties example (VB)</span></span>
>>>>>>> <span data-ttu-id="bed38-106">master</span><span class="sxs-lookup"><span data-stu-id="bed38-106">master</span></span>


<span data-ttu-id="bed38-107">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="bed38-107">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="bed38-108">В этом примере вызывает ошибку, его перехватывает и отображает [Описание](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [файл справки](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [номер](number-property-ado.md), [источника](source-property-ado-error.md)и свойства [SQLState](sqlstate-property-ado.md) итоговый [Ошибка](error-object-ado.md) объект.</span><span class="sxs-lookup"><span data-stu-id="bed38-108">This example triggers an error, traps it, and displays the [Description](description-property-ado.md), [HelpContext](helpcontext-helpfile-properties-ado.md), [HelpFile](helpcontext-helpfile-properties-ado.md), [NativeError](nativeerror-property-ado.md), [Number](number-property-ado.md), [Source](source-property-ado-error.md), and [SQLState](sqlstate-property-ado.md) properties of the resulting [Error](error-object-ado.md) object.</span></span>

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
