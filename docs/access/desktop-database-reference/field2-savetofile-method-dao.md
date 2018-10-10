---
title: Field2.SaveToFile Method (DAO)
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
ms.openlocfilehash: 3b9da4d42b1b2cece2c829988d3d8906b9f1383b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480996"
---
# <a name="field2savetofile-method-dao"></a><span data-ttu-id="92228-102">Field2.SaveToFile Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="92228-102">Field2.SaveToFile Method (DAO)</span></span>

<span data-ttu-id="92228-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="92228-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="92228-104">Сохранение вложений на диске.</span><span class="sxs-lookup"><span data-stu-id="92228-104">Saves an attachment to disk.</span></span>

## <a name="version-information"></a><span data-ttu-id="92228-105">Сведения о версии</span><span class="sxs-lookup"><span data-stu-id="92228-105">Version Information</span></span>

<span data-ttu-id="92228-106">Добавлена версия: Access 2007
</span><span class="sxs-lookup"><span data-stu-id="92228-106">Version Added: Access 2007</span></span>

## <a name="syntax"></a><span data-ttu-id="92228-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92228-107">Syntax</span></span>

<span data-ttu-id="92228-108">*выражение* . SaveToFile (***имя файла***)</span><span class="sxs-lookup"><span data-stu-id="92228-108">*expression* .SaveToFile(***FileName***)</span></span>

<span data-ttu-id="92228-109">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="92228-109">*expression* A variable that represents a **Field2** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="92228-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="92228-110">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="92228-111">Имя</span><span class="sxs-lookup"><span data-stu-id="92228-111">Name</span></span></p></th>
<th><p><span data-ttu-id="92228-112">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="92228-112">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="92228-113">Тип данных</span><span class="sxs-lookup"><span data-stu-id="92228-113">Data Type</span></span></p></th>
<th><p><span data-ttu-id="92228-114">Описание</span><span class="sxs-lookup"><span data-stu-id="92228-114">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="92228-115">FileName</span><span class="sxs-lookup"><span data-stu-id="92228-115">FileName</span></span></p></td>
<td><p><span data-ttu-id="92228-116">Обязательный</span><span class="sxs-lookup"><span data-stu-id="92228-116">Required</span></span></p></td>
<td><p><span data-ttu-id="92228-117"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="92228-117"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="92228-118">Полный путь к файлу, к которому вы хотите сохранить вложение.</span><span class="sxs-lookup"><span data-stu-id="92228-118">The fully qualified path of the file to which you want to save the attachment.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="92228-119">Пример</span><span class="sxs-lookup"><span data-stu-id="92228-119">Example</span></span>

<span data-ttu-id="92228-120">В следующем фрагменте кода показано, как использовать метод **SaveToFile** для сохранения всех вложений для конкретного сотрудника на диске.</span><span class="sxs-lookup"><span data-stu-id="92228-120">The following code snippet illustrates how to use the **SaveToFile** method to save all of the attachments for a specific employee to disk.</span></span>

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

<span data-ttu-id="92228-121">Следующем примере показано, как для сохранения файлов, сохраненных в поля вложения для указанной папки.</span><span class="sxs-lookup"><span data-stu-id="92228-121">The following example shows how to save the files stored in an attachment field to the specified folder path.</span></span>

<span data-ttu-id="92228-122">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="92228-122">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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
