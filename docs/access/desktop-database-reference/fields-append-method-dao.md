---
title: Метод Fields.Append (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 70fa0aba5385157453a1e9b009a167f036dc874b
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929120"
---
# <a name="fieldsappend-method-dao"></a><span data-ttu-id="095f9-102">Метод Fields.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="095f9-102">Fields.Append method (DAO)</span></span>


<span data-ttu-id="095f9-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="095f9-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="095f9-104">Добавляет новое **[поле](field-object-dao.md)** в коллекцию **[полей](fields-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="095f9-104">Adds a new **[Field](field-object-dao.md)** to the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="095f9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="095f9-105">Syntax</span></span>

<span data-ttu-id="095f9-106">*выражение* . Добавление (***объект***)</span><span class="sxs-lookup"><span data-stu-id="095f9-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="095f9-107">*выражение* Переменная, которая представляет собой объект- **поля** .</span><span class="sxs-lookup"><span data-stu-id="095f9-107">*expression* A variable that represents a **Fields** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="095f9-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="095f9-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="095f9-109">Имя</span><span class="sxs-lookup"><span data-stu-id="095f9-109">Name</span></span></p></th>
<th><p><span data-ttu-id="095f9-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="095f9-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="095f9-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="095f9-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="095f9-112">Описание</span><span class="sxs-lookup"><span data-stu-id="095f9-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="095f9-113">Объект</span><span class="sxs-lookup"><span data-stu-id="095f9-113">Object</span></span></p></td>
<td><p><span data-ttu-id="095f9-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="095f9-114">Required</span></span></p></td>
<td><p><span data-ttu-id="095f9-115"><strong>Объект</strong></span><span class="sxs-lookup"><span data-stu-id="095f9-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="095f9-116">Объектная переменная, представляющий поле, добавленный в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="095f9-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="095f9-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="095f9-117">Remarks</span></span>

<span data-ttu-id="095f9-118">Метод **Append** используется для добавления новой таблицы в базе данных, Добавление поля в таблицу и добавить поле индекса.</span><span class="sxs-lookup"><span data-stu-id="095f9-118">You can use the **Append** method to add a new table to a database, add a field to a table, and add a field to an index.</span></span>

<span data-ttu-id="095f9-119">Добавленный объект становится сохраняемого объекта, хранящиеся на диске, пока не будет удалена с помощью метода **Delete** .</span><span class="sxs-lookup"><span data-stu-id="095f9-119">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="095f9-120">Добавление нового объекта выполняется немедленно, но следует использовать метод **Refresh** в семействах сайтов, которые может затронуть изменения структуры базы данных.</span><span class="sxs-lookup"><span data-stu-id="095f9-120">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="095f9-121">Если объект, в которую добавляются не завершена (например, при любые объекты **поля** еще не добавлены в коллекцию **полей** **индекс** объекта до добавляется к коллекции **индексов** ) или задать свойства в одном или нескольких неправильные подчиненных объектов, с помощью метода **Append** приводит к ошибке.</span><span class="sxs-lookup"><span data-stu-id="095f9-121">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="095f9-122">Например если вы еще не указан тип поля и попытайтесь добавьте объект **поля** в коллекцию **полей** в объекте **TableDef** , с помощью метода **Append** запускает ошибку времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="095f9-122">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="095f9-123">Пример</span><span class="sxs-lookup"><span data-stu-id="095f9-123">Example</span></span>

<span data-ttu-id="095f9-124">В этом примере используется метод **Append** или метода **Delete** для изменения коллекции **полей** **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="095f9-124">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**.</span></span> <span data-ttu-id="095f9-125">Процедура AppendDeleteField является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="095f9-125">The AppendDeleteField procedure is required for this procedure to run.</span></span>

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
