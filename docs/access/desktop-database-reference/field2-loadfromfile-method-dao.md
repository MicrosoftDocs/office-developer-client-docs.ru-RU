---
title: Field2.LoadFromFile Method (DAO)
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
ms.openlocfilehash: 620d692693696c4a76a31d51fdda5ebb85acd5b0
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25873315"
---
# <a name="field2loadfromfile-method-dao"></a><span data-ttu-id="f3aee-102">Field2.LoadFromFile Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="f3aee-102">Field2.LoadFromFile Method (DAO)</span></span>

<span data-ttu-id="f3aee-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f3aee-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f3aee-104">Загружает указанный файл с диска.</span><span class="sxs-lookup"><span data-stu-id="f3aee-104">Loads the specified file from disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="f3aee-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="f3aee-105">Version Information</span></span>

<span data-ttu-id="f3aee-106">Добавлена версия: Access 2007
</span><span class="sxs-lookup"><span data-stu-id="f3aee-106">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="f3aee-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f3aee-107">Syntax</span></span>

<span data-ttu-id="f3aee-108">*выражение* . LoadFromFile (***имя файла***)</span><span class="sxs-lookup"><span data-stu-id="f3aee-108">*expression* .LoadFromFile(***FileName***)</span></span>

<span data-ttu-id="f3aee-109">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="f3aee-109">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="f3aee-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="f3aee-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f3aee-111">Имя</span><span class="sxs-lookup"><span data-stu-id="f3aee-111">Name</span></span></p></th>
<th><p><span data-ttu-id="f3aee-112">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="f3aee-112">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f3aee-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f3aee-113">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f3aee-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f3aee-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f3aee-115">FileName</span><span class="sxs-lookup"><span data-stu-id="f3aee-115">FileName</span></span></p></td>
<td><p><span data-ttu-id="f3aee-116">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f3aee-116">Required</span></span></p></td>
<td><p><span data-ttu-id="f3aee-117"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="f3aee-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="f3aee-118">Полный путь к файлу, который требуется загрузить.</span><span class="sxs-lookup"><span data-stu-id="f3aee-118">The fully qualified path of the file to that you want to load.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="f3aee-119">Пример</span><span class="sxs-lookup"><span data-stu-id="f3aee-119">Example</span></span>

<span data-ttu-id="f3aee-120">В следующем фрагменте кода используется метод **LoadFromFile** загрузить изображение сотрудника с диска.</span><span class="sxs-lookup"><span data-stu-id="f3aee-120">The following code snippet uses the **LoadFromFile** method to load an employee's picture from disk.</span></span>

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

<span data-ttu-id="f3aee-121">Следующем примере показано, как добавить файлы из указанной папки путь полем вложения.</span><span class="sxs-lookup"><span data-stu-id="f3aee-121">The following example shows how to add files from a specified folder path to an attachment field.</span></span>

<span data-ttu-id="f3aee-122">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="f3aee-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
