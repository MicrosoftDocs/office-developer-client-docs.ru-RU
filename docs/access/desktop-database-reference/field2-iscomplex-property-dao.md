---
title: Field2.IsComplex Property (DAO)
TOCTitle: IsComplex Property
ms:assetid: ffc90e6e-e3ee-4f9b-ca6b-615199300d45
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837318(v=office.15)
ms:contentKeyID: 48548970
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1b7e5634256a3f0acf7dc058f36c5a7d9d0581b0
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482461"
---
# <a name="field2iscomplex-property-dao"></a><span data-ttu-id="6e702-102">Field2.IsComplex Property (DAO)</span><span class="sxs-lookup"><span data-stu-id="6e702-102">Field2.IsComplex Property (DAO)</span></span>

<span data-ttu-id="6e702-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6e702-103">**Applies to**: Access 2013 | Office 2013</span></span> 

<span data-ttu-id="6e702-104">Возвращает значение **типа Boolean** , указывающее, является ли указанное поле Тип данных, поддерживающий несколько значений.</span><span class="sxs-lookup"><span data-stu-id="6e702-104">Returns **Boolean** that indicates whether the specified field is a multi-valued data type.</span></span> <span data-ttu-id="6e702-105">Только для чтения.</span><span class="sxs-lookup"><span data-stu-id="6e702-105">Read-only.</span></span>

## <a name="version-information"></a><span data-ttu-id="6e702-106">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="6e702-106">Version information</span></span>

<span data-ttu-id="6e702-107">Добавлена версия: Access 2007
</span><span class="sxs-lookup"><span data-stu-id="6e702-107">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="6e702-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6e702-108">Syntax</span></span>

<span data-ttu-id="6e702-109">*выражение* . IsComplex</span><span class="sxs-lookup"><span data-stu-id="6e702-109">*expression* .IsComplex</span></span>

<span data-ttu-id="6e702-110">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="6e702-110">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="example"></a><span data-ttu-id="6e702-111">Пример</span><span class="sxs-lookup"><span data-stu-id="6e702-111">Example</span></span>

<span data-ttu-id="6e702-112">Следующем примере показано, как переходить набор записей с несколькими значениями полей.</span><span class="sxs-lookup"><span data-stu-id="6e702-112">The following example shows how to navigate a Recordset that contains a multi-value field.</span></span>

<span data-ttu-id="6e702-113">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="6e702-113">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
