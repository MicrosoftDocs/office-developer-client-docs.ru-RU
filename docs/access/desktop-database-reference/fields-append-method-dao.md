---
title: Fields.Append Method (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0bfd430231517f3c4f3a4d5f9c14109dc3381363
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25482102"
---
# <a name="fieldsappend-method-dao"></a><span data-ttu-id="a578d-102">Fields.Append Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="a578d-102">Fields.Append Method (DAO)</span></span>


<span data-ttu-id="a578d-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="a578d-103">**Applies to**: Access 2013 | Office 2013</span></span>


<span data-ttu-id="a578d-104">Добавляет новое **[поле](field-object-dao.md)** в коллекцию **[полей](fields-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="a578d-104">Adds a new **[Field](field-object-dao.md)** to the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="a578d-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a578d-105">Syntax</span></span>

<span data-ttu-id="a578d-106">*выражение* . Добавление (***объект***)</span><span class="sxs-lookup"><span data-stu-id="a578d-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="a578d-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="a578d-107">*expression* A variable that represents a **Fields** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="a578d-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="a578d-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a578d-109">Имя</span><span class="sxs-lookup"><span data-stu-id="a578d-109">Name</span></span></p></th>
<th><p><span data-ttu-id="a578d-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="a578d-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="a578d-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a578d-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="a578d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a578d-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a578d-113">Объект</span><span class="sxs-lookup"><span data-stu-id="a578d-113">Object</span></span></p></td>
<td><p><span data-ttu-id="a578d-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="a578d-114">Required</span></span></p></td>
<td><p><span data-ttu-id="a578d-115"><strong>Объект</strong></span><span class="sxs-lookup"><span data-stu-id="a578d-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="a578d-116">Объектная переменная, представляющий поле, добавленный в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="a578d-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="a578d-117">Замечания</span><span class="sxs-lookup"><span data-stu-id="a578d-117">Remarks</span></span>

<span data-ttu-id="a578d-118">Метод **Append** используется для добавления новой таблицы в базе данных, Добавление поля в таблицу и добавить поле индекса.</span><span class="sxs-lookup"><span data-stu-id="a578d-118">You can use the **Append** method to add a new table to a database, add a field to a table, and add a field to an index.</span></span>

<span data-ttu-id="a578d-119">Добавленный объект становится сохраняемого объекта, хранящиеся на диске, пока не будет удалена с помощью метода **Delete** .</span><span class="sxs-lookup"><span data-stu-id="a578d-119">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="a578d-120">Добавление нового объекта выполняется немедленно, но следует использовать метод **Refresh** в семействах сайтов, которые может затронуть изменения структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="a578d-120">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="a578d-121">Если объект, в которую добавляются не завершена (например, при любые объекты **поля** еще не добавлены в коллекцию **полей** **индекс** объекта до добавляется к коллекции **индексов** ) или задать свойства в одном или нескольких неправильные подчиненных объектов, с помощью метода **Append** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="a578d-121">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="a578d-122">Например если вы еще не указан тип поля и попытайтесь добавьте объект **поля** в коллекцию **полей** в объекте **TableDef** , с помощью метода **Append** запускает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="a578d-122">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="a578d-123">Пример</span><span class="sxs-lookup"><span data-stu-id="a578d-123">Example</span></span>

<span data-ttu-id="a578d-124">В этом примере используется метод **Append** или метода **Delete** для изменения коллекции **полей** **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="a578d-124">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**.</span></span> <span data-ttu-id="a578d-125">Процедура AppendDeleteField является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="a578d-125">The AppendDeleteField procedure is required for this procedure to run.</span></span>

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
