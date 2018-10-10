---
title: Status Property Example (Field) (VB)
TOCTitle: Status Property Example (Field) (VB)
ms:assetid: 1dc2807f-f469-de97-1280-4b1984b271b4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248969(v=office.15)
ms:contentKeyID: 48543601
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ed9f0c90e994b221762588ab941174dbb9c4c764
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483203"
---
# <a name="status-property-example-field-vb"></a><span data-ttu-id="b4799-102">Status Property Example (Field) (VB)</span><span class="sxs-lookup"><span data-stu-id="b4799-102">Status Property Example (Field) (VB)</span></span>


<span data-ttu-id="b4799-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b4799-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b4799-104">В следующем примере открывается документ из папки чтения и записи, с использованием [Поставщика средств публикации в Интернете](microsoft-ole-db-provider-for-internet-publishing.md).</span><span class="sxs-lookup"><span data-stu-id="b4799-104">The following example opens a document from a read/write folder using the [Internet Publishing Provider](microsoft-ole-db-provider-for-internet-publishing.md).</span></span> <span data-ttu-id="b4799-105">Свойство [Status](status-property-ado-field.md) объекта [поля](field-object-ado.md) [записей](record-object-ado.md) сначала иметь значение **adFieldPendingInsert**, а затем следует обновить до **adFieldOk**.</span><span class="sxs-lookup"><span data-stu-id="b4799-105">The [Status](status-property-ado-field.md) property of a [Field](field-object-ado.md) object of the [Record](record-object-ado.md) will first be set to **adFieldPendingInsert**, then be updated to **adFieldOk**.</span></span>

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

<span data-ttu-id="b4799-106">В следующем примере удаляется **поле** из **записи** из документа.</span><span class="sxs-lookup"><span data-stu-id="b4799-106">The following example deletes a known **Field** from a **Record** opened from a document.</span></span> <span data-ttu-id="b4799-107">Свойство **Status** будет сначала задать значение **adFieldOK**, а затем **adFieldPendingUnknown**.</span><span class="sxs-lookup"><span data-stu-id="b4799-107">The **Status** property will first be set to **adFieldOK**, then **adFieldPendingUnknown**.</span></span>

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

<span data-ttu-id="b4799-108">Следующий код удаляет **поля** из **записи** , открывается документ только для чтения.</span><span class="sxs-lookup"><span data-stu-id="b4799-108">The following code deletes a **Field** from a **Record** opened on a read-only document.</span></span> <span data-ttu-id="b4799-109">**Состояние** будет иметь значение **adFieldPendingDelete**.</span><span class="sxs-lookup"><span data-stu-id="b4799-109">**Status** will be set to **adFieldPendingDelete**.</span></span> <span data-ttu-id="b4799-110">В [обновления](update-method-ado.md)удаления завершится с ошибкой и **состояние** будет **adFieldPendingDelete** , а также **adFieldPermissionDenied**.</span><span class="sxs-lookup"><span data-stu-id="b4799-110">At [Update](update-method-ado.md), the delete will fail and **Status** will be **adFieldPendingDelete** plus **adFieldPermissionDenied**.</span></span> <span data-ttu-id="b4799-111">[CancelUpdate](cancelupdate-method-ado.md) очищает отложенные параметр **состояния** .</span><span class="sxs-lookup"><span data-stu-id="b4799-111">[CancelUpdate](cancelupdate-method-ado.md) clears the pending **Status** setting.</span></span>

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
