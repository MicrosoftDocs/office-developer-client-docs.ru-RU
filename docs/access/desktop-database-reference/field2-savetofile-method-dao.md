---
title: Метод Field2.SaveToFile (DAO)
TOCTitle: SaveToFile Method
ms:assetid: 250f9596-1a03-471d-96f9-718cd57dc94f
ms:mtpsurl: https://msdn.microsoft.com/library/Ff191852(v=office.15)
ms:contentKeyID: 48543776
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1101191
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 78b08575b1fde304dc47b8219c1143cda265baf8
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28706984"
---
# <a name="field2savetofile-method-dao"></a><span data-ttu-id="312a2-102">Метод Field2.SaveToFile (DAO)</span><span class="sxs-lookup"><span data-stu-id="312a2-102">Field2.SaveToFile Method (DAO)</span></span>

<span data-ttu-id="312a2-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="312a2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="312a2-104">Сохраняет вложение на диске.</span><span class="sxs-lookup"><span data-stu-id="312a2-104">Saves an attachment to disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="312a2-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="312a2-105">Version information</span></span>

<span data-ttu-id="312a2-106">Добавлен в версии: Access 2007</span><span class="sxs-lookup"><span data-stu-id="312a2-106">Version Added: Access 2007
</span></span>

## <a name="syntax"></a><span data-ttu-id="312a2-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="312a2-107">Syntax</span></span>

<span data-ttu-id="312a2-108">*expression* .SaveToFile(***FileName***)</span><span class="sxs-lookup"><span data-stu-id="312a2-108">*expression* .SaveToFile(***FileName***)</span></span>

<span data-ttu-id="312a2-109">*expression* — переменная, представляющая объект **Field2**.</span><span class="sxs-lookup"><span data-stu-id="312a2-109">*expression* A variable that represents a **Sheets** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="312a2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="312a2-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="312a2-111">Имя</span><span class="sxs-lookup"><span data-stu-id="312a2-111">Name</span></span></p></th>
<th><p><span data-ttu-id="312a2-112">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="312a2-112">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="312a2-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="312a2-113">Data type</span></span></p></th>
<th><p><span data-ttu-id="312a2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="312a2-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="312a2-115"><em>FileName</em></span><span class="sxs-lookup"><span data-stu-id="312a2-115"><em>FileName</em></span></span></p></td>
<td><p><span data-ttu-id="312a2-116">Обязательный</span><span class="sxs-lookup"><span data-stu-id="312a2-116">Required</span></span></p></td>
<td><p><span data-ttu-id="312a2-117"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="312a2-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="312a2-118">Полный путь к файлу, в котором требуется сохранить вложение.</span><span class="sxs-lookup"><span data-stu-id="312a2-118">The fully qualified path of the file to which you want to save the attachment.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="312a2-119">Пример</span><span class="sxs-lookup"><span data-stu-id="312a2-119">Example</span></span>

<span data-ttu-id="312a2-120">В представленном ниже фрагменте кода показано, как использовать метод **SaveToFile**, чтобы сохранить все вложения для определенного сотрудника на диск.</span><span class="sxs-lookup"><span data-stu-id="312a2-120">The following code snippet illustrates how to use the **SaveToFile** method to save all of the attachments for a specific employee to disk.</span></span>

```vb
    '  Instantiate the parent recordset.  
       Set rsEmployees = db.OpenRecordset("Employees") 
      
       … Code to move to desired employee 
      
       ' Instantiate the child recordset. 
       Set rsPictures = rsEmployees.Fields("Pictures").Value  
     
       '  Loop through the attachments. 
       While Not rsPictures.EOF 
      
          '  Save current attachment to disk in the "My Documents" folder. 
          rsPictures.Fields("FileData").SaveToFile _ 
                      "C:\Documents and Settings\Username\My Documents" 
          rsPictures.MoveNext 
       Wend 
```

<br/>

<span data-ttu-id="312a2-121">В приведенном ниже примере показано, как сохранить файлы, хранящиеся в поле вложения, в папку с указанным путем.</span><span class="sxs-lookup"><span data-stu-id="312a2-121">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

<span data-ttu-id="312a2-122">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="312a2-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
