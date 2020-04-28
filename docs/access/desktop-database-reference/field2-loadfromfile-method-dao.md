---
title: Метод field2. LoadFromFile (DAO)
TOCTitle: LoadFromFile Method
ms:assetid: 8ffe4636-d4da-0579-f4b5-14f423647562
ms:mtpsurl: https://msdn.microsoft.com/library/Ff197396(v=office.15)
ms:contentKeyID: 48546314
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101190
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: bdb1ba92c4a0f4fbee7204b2f4fee8a96c87cc1b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292792"
---
# <a name="field2loadfromfile-method-dao"></a><span data-ttu-id="30ca6-102">Метод field2. LoadFromFile (DAO)</span><span class="sxs-lookup"><span data-stu-id="30ca6-102">Field2.LoadFromFile method (DAO)</span></span>

<span data-ttu-id="30ca6-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="30ca6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="30ca6-104">Загружает указанный файл с диска.</span><span class="sxs-lookup"><span data-stu-id="30ca6-104">Loads the specified file from disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="30ca6-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="30ca6-105">Version information</span></span>

<span data-ttu-id="30ca6-106">Добавлен в версии: Access 2007</span><span class="sxs-lookup"><span data-stu-id="30ca6-106">Version added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="30ca6-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="30ca6-107">Syntax</span></span>

<span data-ttu-id="30ca6-108">*Expression* . LoadFromFile (***filename***)</span><span class="sxs-lookup"><span data-stu-id="30ca6-108">*expression* .LoadFromFile(***FileName***)</span></span>

<span data-ttu-id="30ca6-109">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="30ca6-109">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="30ca6-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="30ca6-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="30ca6-111">Имя</span><span class="sxs-lookup"><span data-stu-id="30ca6-111">Name</span></span></p></th>
<th><p><span data-ttu-id="30ca6-112">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="30ca6-112">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="30ca6-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="30ca6-113">Data type</span></span></p></th>
<th><p><span data-ttu-id="30ca6-114">Описание</span><span class="sxs-lookup"><span data-stu-id="30ca6-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30ca6-115"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="30ca6-115"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="30ca6-116">Обязательный</span><span class="sxs-lookup"><span data-stu-id="30ca6-116">Required</span></span></p></td>
<td><p><span data-ttu-id="30ca6-117"><strong>String</strong></span><span class="sxs-lookup"><span data-stu-id="30ca6-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="30ca6-118">Полный путь к файлу, который необходимо загрузить.</span><span class="sxs-lookup"><span data-stu-id="30ca6-118">The fully qualified path of the file to that you want to load.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="30ca6-119">Пример</span><span class="sxs-lookup"><span data-stu-id="30ca6-119">Example</span></span>

<span data-ttu-id="30ca6-120">В следующем фрагменте кода используется метод **LoadFromFile** для загрузки изображения сотрудника с диска.</span><span class="sxs-lookup"><span data-stu-id="30ca6-120">The following code snippet uses the **LoadFromFile** method to load an employee's picture from disk.</span></span>

```vb 
   '  Instantiate the parent recordset.  
   Set rsEmployees = db.OpenRecordset("Employees") 
  
   … Code to move to desired employee 
  
   ' Activate edit mode. 
   rsEmployees.Edit 
  
   ' Instantiate the child recordset. 
   Set rsPictures = rsEmployees.Fields("Pictures").Value  
  
   ' Add a new attachment. 
   rsPictures.AddNew 
   rsPictures.Fields("FileData").LoadFromFile "EmpPhoto39392.jpg" 
   rsPictures.Update 
  
   ' Update the parent record 
   rsEmployees.Update 
```

<br/>

<span data-ttu-id="30ca6-121">В примере ниже показано, как добавить файлы из папки с указанным путем в поле вложений.</span><span class="sxs-lookup"><span data-stu-id="30ca6-121">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

<span data-ttu-id="30ca6-122">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="30ca6-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
