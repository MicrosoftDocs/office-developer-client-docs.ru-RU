---
title: Recordset2 Object (DAO)
TOCTitle: Recordset2 Object
ms:assetid: 964f9961-807c-e4f3-5919-74e25f6e9069
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197737(v=office.15)
ms:contentKeyID: 48546446
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 39b7df1856588875f88735ec01f05cf0e1a4a1d9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25885271"
---
# <a name="recordset2-object-dao"></a><span data-ttu-id="9291e-102">Recordset2 Object (DAO)</span><span class="sxs-lookup"><span data-stu-id="9291e-102">Recordset2 Object (DAO)</span></span>

<span data-ttu-id="9291e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9291e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9291e-104">Объект **Recordset2** представляет записей в базовой таблице или записи, в результате выполнения запроса.</span><span class="sxs-lookup"><span data-stu-id="9291e-104">A **Recordset2** object represents the records in a base table or the records that result from running a query.</span></span>

## <a name="remarks"></a><span data-ttu-id="9291e-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="9291e-105">Remarks</span></span>

<span data-ttu-id="9291e-106">Объект **Recordset2** — содержит все же свойства и методы объекта **[набора записей](recordset-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="9291e-106">A **Recordset2** object is contains all of the same properties and methods as the **[Recordset](recordset-object-dao.md)** object.</span></span> <span data-ttu-id="9291e-107">Объект **Recordset2** содержит новое свойство **[ParentRecordset](recordset2-parentrecordset-property-dao.md)**, поддерживающие типы полей, поддерживающий несколько значений.</span><span class="sxs-lookup"><span data-stu-id="9291e-107">The **Recordset2** object contains a new property, **[ParentRecordset](recordset2-parentrecordset-property-dao.md)**, that support multi-valued field types.</span></span>

## <a name="example"></a><span data-ttu-id="9291e-108">Пример</span><span class="sxs-lookup"><span data-stu-id="9291e-108">Example</span></span>

<span data-ttu-id="9291e-109">Следующем примере показано, как переходить набор записей с несколькими значениями полей.</span><span class="sxs-lookup"><span data-stu-id="9291e-109">The following example shows how to navigate a Recordset that contains a multi-value field.</span></span>

<span data-ttu-id="9291e-110">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="9291e-110">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub PrintStudentsAndClasses()
        Dim dbs As DAO.Database
        Dim rsStudents As DAO.Recordset2  'Recordset for students
        Dim rsClasses As DAO.Recordset2  'Recordset for classes
        Dim fld As DAO.Field2
    
        'open the database
        Set dbs = CurrentDb()
    
        'get the table of students
        Set rsStudents = dbs.OpenRecordset("tblStudents")
    
        'loop through the students
        Do While Not rsStudents.EOF
            
            'get the classes field
            Set fld = rsStudents("Classes")
    
            'get the classes Recordset
            'make sure the field is a multi-valued field before
            'getting a Recordset object
            If fld.IsComplex Then
                Set rsClasses = fld.Value
            End If
    
            'access all records in the Recordset
            If Not (rsClasses.BOF And rsClasses.EOF) Then
                rsClasses.MoveLast
                rsClasses.MoveFirst
            End If
    
            'print the student and number of classes
            Debug.Print rsStudents("FirstName") & " " & rsStudents("LastName"), _
                "Number of classes: " & rsClasses.RecordCount
    
            'print the classes for this student
            Do While Not rsClasses.EOF
                Debug.Print , rsClasses("Value")
                rsClasses.MoveNext
            Loop
    
            'close the Classes Recordset
            rsClasses.Close
    
            'get the next student
            rsStudents.MoveNext
    
        Loop
        
        'cleanup
        rsStudents.Close
    
        Set fld = Nothing
        Set rsStudents = Nothing
        Set dbs = Nothing
    
    End Sub
```

<br/>

<span data-ttu-id="9291e-111">Следующем примере показано, как для перемещения файлов в поле вложения.</span><span class="sxs-lookup"><span data-stu-id="9291e-111">The following example shows how to navigate the files in an attachment field.</span></span> <span data-ttu-id="9291e-112">Тип файла и имя файла для каждого вложения печать в окне Интерпретация.</span><span class="sxs-lookup"><span data-stu-id="9291e-112">The file type and filename of each attachment is printed in the Immediate window.</span></span>

```vb
    Sub ListAttachments()
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Print the first and last name
            Debug.Print rst("FirstName") & " " & rst("LastName")
            
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Print all attachments in the field
            Do While Not rsA.EOF
                Debug.Print , rsA("FileType"), rsA("FileName")
                
                'Next attachment
                rsA.MoveNext
            Loop
            
            rsA.Close
            
            'Next record
            rst.MoveNext
        Loop
        
            
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Sub
```

<br/>

<span data-ttu-id="9291e-113">Следующем примере показано, как добавить файлы из указанной папки путь полем вложения.</span><span class="sxs-lookup"><span data-stu-id="9291e-113">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

```vb
    Public Function LoadAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld  As DAO.Field2
        Dim strFile As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Load all attachments in the specified directory
            strFile = Dir(strPath & "\*.*")
            
            rst.Edit
            Do While Len(strFile) > 0
                'Add a new attachment that matches the pattern.
                'Pass "" to match all files.
                If strFile Like strPattern Then
                    rsA.AddNew
                    rsA("FileData").LoadFromFile strPath & "\" & strFile
                    rsA.Update
                    
                    'Increment the number of files added
                    LoadAttachments = LoadAttachments + 1
                End If
                strFile = Dir
            Loop
            rsA.Close
            
            rst.Update
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```

<br/>

<span data-ttu-id="9291e-114">Следующем примере показано, как для сохранения файлов, сохраненных в поля вложения для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="9291e-114">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

```vb
    Public Function SaveAttachments(strPath As String, Optional strPattern As String = "*.*") As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        Dim strFullPath As String
        
        'Get the database, recordset, and attachment field
        Set dbs = CurrentDb
        Set rst = dbs.OpenRecordset("tblAttachments")
        Set fld = rst("Attachments")
        
        'Navigate through the table
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Save all attachments in the field
            Do While Not rsA.EOF
                If rsA("FileName") Like strPattern Then
                    strFullPath = strPath & "\" & rsA("FileName")
                    
                    'Make sure the file does not exist and save
                    If Dir(strFullPath) = "" Then
                        rsA("FileData").SaveToFile strFullPath
                    End If
                    
                    'Increment the number of files saved
                    SaveAttachments = SaveAttachments + 1
                End If
                
                'Next attachment
                rsA.MoveNext
            Loop
            rsA.Close
            
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        
        Set fld = Nothing
        Set rsA = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```

<br/>

<span data-ttu-id="9291e-115">Следующем примере показано, как для удаления файлов, хранящихся в поле вложения.</span><span class="sxs-lookup"><span data-stu-id="9291e-115">The following example shows how to delete a file stored in an attachment field.</span></span>

```vb
    Function RemoveAttachment(strRemoveFile As String, Optional strFilter As String) As Long
        Dim dbs As DAO.Database
        Dim rst As DAO.Recordset2
        Dim rsA As DAO.Recordset2
        Dim fld As DAO.Field2
        
        'Get the database
        Set dbs = CurrentDb
        
        'Open the recordset. If the strFilter is supplied, add it to the WHERE
        'clause for the recordset. Otherwise, any files matching strFileName
        'will be deleted
        If Len(strFilter) > 0 Then
            Set rst = dbs.OpenRecordset("SELECT * FROM tblAttachments WHERE " & strFilter)
        Else
            Set rst = dbs.OpenRecordset("tblAttachments")
        End If
        
        'Get the Attachment field
        Set fld = rst("Attachments")
        
        'Navigate through the recordset
        Do While Not rst.EOF
        
            'Get the recordset for the Attachments field
            Set rsA = fld.Value
            
            'Walk the attachments and look for the file name to remove
            Do While Not rsA.EOF
                If rsA("FileName") Like strRemoveFile Then
                    rsA.Delete
                    
                    'Increment the number of files removed
                    RemoveAttachment = RemoveAttachment + 1
                End If
                rsA.MoveNext
            Loop
                    
            'Cleanup the Attachments recordset
            rsA.Close
            Set rsA = Nothing
            
            'Next record
            rst.MoveNext
        Loop
        
        rst.Close
        dbs.Close
        Set fld = Nothing
        Set rst = Nothing
        Set dbs = Nothing
    End Function
```

