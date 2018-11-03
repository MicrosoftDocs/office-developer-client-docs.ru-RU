---
title: Метод Fields.Delete (DAO)
TOCTitle: Delete Method
ms:assetid: a8e249e7-7526-3eff-a5cf-70cab2081970
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821417(v=office.15)
ms:contentKeyID: 48546913
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052868
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 4faa23fa2b7bdedc85bba5151c04a804a560155e
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923674"
---
# <a name="fieldsdelete-method-dao"></a><span data-ttu-id="185ed-102">Метод Fields.Delete (DAO)</span><span class="sxs-lookup"><span data-stu-id="185ed-102">Fields.Delete method (DAO)</span></span>


<span data-ttu-id="185ed-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="185ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="185ed-104">Удаление **[поля](field-object-dao.md)** из коллекции **[полей](fields-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="185ed-104">Deletes a **[Field](field-object-dao.md)** from the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="185ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="185ed-105">Syntax</span></span>

<span data-ttu-id="185ed-106">*выражение* . Удаление (***имя***)</span><span class="sxs-lookup"><span data-stu-id="185ed-106">*expression* .Delete(***Name***)</span></span>

<span data-ttu-id="185ed-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="185ed-107">*expression* A variable that represents a **Fields** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="185ed-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="185ed-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="185ed-109">Имя</span><span class="sxs-lookup"><span data-stu-id="185ed-109">Name</span></span></p></th>
<th><p><span data-ttu-id="185ed-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="185ed-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="185ed-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="185ed-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="185ed-112">Описание</span><span class="sxs-lookup"><span data-stu-id="185ed-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="185ed-113">Имя</span><span class="sxs-lookup"><span data-stu-id="185ed-113">Name</span></span></p></td>
<td><p><span data-ttu-id="185ed-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="185ed-114">Required</span></span></p></td>
<td><p><span data-ttu-id="185ed-115"><strong>Строка</strong></span><span class="sxs-lookup"><span data-stu-id="185ed-115"><strong>String</strong></span></span></p></td>
<td><p><span data-ttu-id="185ed-116">Чтобы удалить поле.</span><span class="sxs-lookup"><span data-stu-id="185ed-116">The field to delete.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="185ed-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="185ed-117">Remarks</span></span>

<span data-ttu-id="185ed-118">Удаление сохраненных объекта выполняется немедленно, но следует использовать метод **Refresh** в семействах сайтов, которые может затронуть изменения структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="185ed-118">The deletion of a stored object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

## <a name="example"></a><span data-ttu-id="185ed-119">Пример</span><span class="sxs-lookup"><span data-stu-id="185ed-119">Example</span></span>

<span data-ttu-id="185ed-120">В этом примере используется метод **Append** или метода **Delete** для изменения коллекции **полей** **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="185ed-120">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**.</span></span> <span data-ttu-id="185ed-121">Процедура AppendDeleteField является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="185ed-121">The AppendDeleteField procedure is required for this procedure to run.</span></span>

```vb
    Sub AppendX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim fldLoop As Field 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs!Employees 
     
     ' Add three new fields. 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "E-mail", dbText, 50 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Http", dbText, 80 
     AppendDeleteField tdfEmployees, "APPEND", _ 
     "Quota", dbInteger, 5 
     
     Debug.Print "Fields after Append" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show the new fields. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     ' Delete the newly added fields. 
     AppendDeleteField tdfEmployees, "DELETE", "E-mail" 
     AppendDeleteField tdfEmployees, "DELETE", "Http" 
     AppendDeleteField tdfEmployees, "DELETE", "Quota" 
     
     Debug.Print "Fields after Delete" 
     Debug.Print , "Type", "Size", "Name" 
     
     ' Enumerate the Fields collection to show that the new 
     ' fields have been deleted. 
     For Each fldLoop In tdfEmployees.Fields 
     Debug.Print , fldLoop.Type, fldLoop.Size, fldLoop.Name 
     Next fldLoop 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Sub AppendDeleteField(tdfTemp As TableDef, _ 
     strCommand As String, strName As String, _ 
     Optional varType, Optional varSize) 
     
     With tdfTemp 
     
     ' Check first to see if the TableDef object is 
     ' updatable. If it isn't, control is passed back to 
     ' the calling procedure. 
     If .Updatable = False Then 
     MsgBox "TableDef not Updatable! " & _ 
     "Unable to complete task." 
     Exit Sub 
     End If 
     
     ' Depending on the passed data, append or delete a 
     ' field to the Fields collection of the specified 
     ' TableDef object. 
     If strCommand = "APPEND" Then 
     .Fields.Append .CreateField(strName, _ 
     varType, varSize) 
     Else 
     If strCommand = "DELETE" Then .Fields.Delete _ 
     strName 
     End If 
     
     End With 
     
    End Sub
```
