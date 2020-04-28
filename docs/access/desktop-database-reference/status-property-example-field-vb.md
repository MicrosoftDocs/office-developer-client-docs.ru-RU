---
title: Пример использования свойства Status (Field) (VB)
TOCTitle: Status property example (Field) (VB)
ms:assetid: 1dc2807f-f469-de97-1280-4b1984b271b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248969(v=office.15)
ms:contentKeyID: 48543601
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 68583b1ee211802a3cade63e85f0f62bbf3cb686
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308507"
---
# <a name="status-property-example-field-vb"></a><span data-ttu-id="70610-102">Пример использования свойства Status (Field) (VB)</span><span class="sxs-lookup"><span data-stu-id="70610-102">Status property example (Field) (VB)</span></span>


<span data-ttu-id="70610-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="70610-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="70610-104">Следующий пример открывает документ из папки для чтения и записи с помощью [поставщика публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="70610-104">The following example opens a document from a read/write folder using the [Internet Publishing Provider](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="70610-105">Сначала свойству [Status](status-property-ado-field.md) объекта [field](field-object-ado.md) [записи](record-object-ado.md) будет присвоено значение **адфиелдпендингинсерт**, а затем оно будет обновлено до **адфиелдок**.</span><span class="sxs-lookup"><span data-stu-id="70610-105">The [Status](status-property-ado-field.md) property of a [Field](field-object-ado.md) object of the [Record](record-object-ado.md) will first be set to **adFieldPendingInsert**, then be updated to **adFieldOk**.</span></span>

```vb
    'BeginStatusFieldVB
        
     ' to integrate this code replace the values in the source string
    
    Sub Main()
        
       Dim File As ADODB.Record
       Dim strFile As String
       Dim Cnxn As ADODB.Connection
       Dim strCnxn As String
       
       Set Cnxn = New ADODB.Connection
       strCnxn = "url=https://MyServer/"
       Cnxn.Open strCnxn
       
       Set File = New ADODB.Record
       strFile = "Folder/FileName"
       ' Open a read/write document
       File.Source = strFile
       File.ActiveConnection = Cnxn
       File.Mode = adModeReadWrite
       File.Open
    
       Debug.Print "Append a couple of fields"
       
       File.Fields.Append "chektest:fld1", adWChar, 42, adFldUpdatable, "fld1"
       File.Fields.Append "chektest:fld2", adWChar, 42, adFldUpdatable, "fld2"
       
       Debug.Print "status for the fields"
       Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert
       Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert
       
        'turn off error-handling to verify field status
       On Error Resume Next
       
       File.Fields.Update
       
       Debug.Print "Update succeeds"
       Debug.Print File.Fields("chektest:fld1").Status 'adfldpendinginsert + adFieldUnavailable
       Debug.Print File.Fields("chektest:fld2").Status 'adfldpendinginsert + adFieldUnavailable
        
        ' resume default error-handling
       On Error GoTo 0
         
         ' clean up
        File.Close
        Cnxn.Close
        Set File = Nothing
        Set Cnxn = Nothing
          
    End Sub
    'EndStatusFieldVB
```

<br/>

<span data-ttu-id="70610-106">В следующем примере показано, как удалить известное **поле** из **записи** , открытой из документа.</span><span class="sxs-lookup"><span data-stu-id="70610-106">The following example deletes a known **Field** from a **Record** opened from a document.</span></span> <span data-ttu-id="70610-107">Для свойства **Status** сначала будет задано значение **адфиелдок**, а затем **адфиелдпендингункновн**.</span><span class="sxs-lookup"><span data-stu-id="70610-107">The **Status** property will first be set to **adFieldOK**, then **adFieldPendingUnknown**.</span></span>

```vb
    'BeginStatusField2VB
    
    ' to integrate this code replace the values in the source string
    
    Sub Main()
    
       Dim File As ADODB.Record
       Dim fld As ADODB.Field
       Dim strFile As String
       
       Dim Cnxn As ADODB.Connection
       Dim strCnxn As String
       
        ' create connection as a URL
       Set Cnxn = New ADODB.Connection
       strCnxn = "url=https://MyServer/"
       Cnxn.Open strCnxn
       Set File = New ADODB.Record
       strFile = "Folder/FileName"
       ' Open a read/write document
       File.Open strFile, Cnxn, adModeReadWrite
       Debug.Print File.Fields("chektest:fld1").Status ' should be adFldOK
       
       ' Delete a field which already exists in the collection
       File.Fields.Delete "chektest:fld1"
       Set fld = File.Fields("chektest:fld1")
       Debug.Print File.Fields("chektest:fld1").Status   ' Pending delete
       
        'turn off error-handling to verify field status
       On Error Resume Next
       
       File.Fields.Update
       
       Debug.Print "Deleted"
       Debug.Print fld.Status   ' Pending unknown
    
        ' resume default error-handling
       On Error GoTo 0
         
         ' clean up
        File.Close
        Cnxn.Close
        Set File = Nothing
        Set Cnxn = Nothing
    
    End Sub
    'EndStatusField2VB
```

<br/>

<span data-ttu-id="70610-108">Следующий код удаляет **поле** из **записи** , открытой в документе, доступном только для чтения.</span><span class="sxs-lookup"><span data-stu-id="70610-108">The following code deletes a **Field** from a **Record** opened on a read-only document.</span></span> <span data-ttu-id="70610-109">В качестве **состояния** будет задано значение **адфиелдпендингделете**.</span><span class="sxs-lookup"><span data-stu-id="70610-109">**Status** will be set to **adFieldPendingDelete**.</span></span> <span data-ttu-id="70610-110">При [обновлении обновление](update-method-ado.md)будет завершено с ошибками, а **состояние** будет **адфиелдпендингделете** плюс **адфиелдпермиссиондениед**.</span><span class="sxs-lookup"><span data-stu-id="70610-110">At [Update](update-method-ado.md), the delete will fail and **Status** will be **adFieldPendingDelete** plus **adFieldPermissionDenied**.</span></span> <span data-ttu-id="70610-111">[CancelUpdate](cancelupdate-method-ado.md) очищает параметр **состояния** Pending.</span><span class="sxs-lookup"><span data-stu-id="70610-111">[CancelUpdate](cancelupdate-method-ado.md) clears the pending **Status** setting.</span></span>

```vb
    Sub Main()
       Dim File As ADODB.Record
       Dim fld As ADODB.Field
       Dim Cnxn As ADODB.Connection
       Dim strCnxn As String
       Dim strFile As String
       
        ' create connection as a URL
       Set Cnxn = New ADODB.Connection
       strCnxn = "url=https://MyServer/"
       Cnxn.Open strCnxn
    
       ' Open a read/write document
       Set File = New ADODB.Record
       strFile = "Folder/FileName"
       File.Open strFile, Cnxn, adModeReadWrite, adCreateCollection Or adOpenIfExists
    
       Debug.Print "Try to delete something without permission"
       File.Fields.Delete ("RESOURCE_PARSENAME")
       Set fld = File.Fields("RESOURCE_PARSENAME")
       
       Debug.Print "Pending delete"
       Debug.Print fld.Status   ' Pending delete
       Debug.Print "Delete should fail on Update"
       
        'turn off error-handling to verify field status
       On Error Resume Next
       
       File.Fields.Update   ' Should fail
       
       Debug.Print fld.Status   ' Pending delete plus error
       File.Fields.CancelUpdate
       Debug.Print fld.Status   ' Okay
        
        ' resume default error-handling
       On Error GoTo 0
            
         ' clean up
        File.Close
        Cnxn.Close
        Set File = Nothing
        Set Cnxn = Nothing
       
    End Sub
    'EndStatusField3VB
```
