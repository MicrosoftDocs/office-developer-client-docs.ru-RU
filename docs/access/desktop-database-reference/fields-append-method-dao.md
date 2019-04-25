---
title: Метод Fields.Append (DAO)
TOCTitle: Append Method
ms:assetid: a0e553ba-6a57-09af-3436-4f6ca3cbe561
ms:mtpsurl: https://msdn.microsoft.com/library/Ff820791(v=office.15)
ms:contentKeyID: 48546719
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: ec3cacbe1f1c7ac5d6bda16bdd47891dc58ebfe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292589"
---
# <a name="fieldsappend-method-dao"></a><span data-ttu-id="924fb-102">Метод Fields.Append (DAO)</span><span class="sxs-lookup"><span data-stu-id="924fb-102">Fields.Append Method (DAO)</span></span>

<span data-ttu-id="924fb-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="924fb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="924fb-104">Добавляет новый объект **[Field](field-object-dao.md)** в коллекцию **[Fields](fields-collection-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="924fb-104">Adds a new **[Field](field-object-dao.md)** to the **[Fields](fields-collection-dao.md)** collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="924fb-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="924fb-105">Syntax</span></span>

<span data-ttu-id="924fb-106">*выражение* .Append(***Object***)</span><span class="sxs-lookup"><span data-stu-id="924fb-106">*expression* .Append(***Object***)</span></span>

<span data-ttu-id="924fb-107">*выражение*: переменная, представляющая объект **Fields**.</span><span class="sxs-lookup"><span data-stu-id="924fb-107">*expression* A variable that represents a **Range** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="924fb-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="924fb-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="924fb-109">Имя</span><span class="sxs-lookup"><span data-stu-id="924fb-109">Name</span></span></p></th>
<th><p><span data-ttu-id="924fb-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="924fb-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="924fb-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="924fb-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="924fb-112">Описание</span><span class="sxs-lookup"><span data-stu-id="924fb-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="924fb-113"><em>Object</em></span><span class="sxs-lookup"><span data-stu-id="924fb-113"><em>Object</em></span></span></p></td>
<td><p><span data-ttu-id="924fb-114">Обязательный</span><span class="sxs-lookup"><span data-stu-id="924fb-114">Required</span></span></p></td>
<td><p><span data-ttu-id="924fb-115"><strong>Object</strong></span><span class="sxs-lookup"><span data-stu-id="924fb-115"><strong>Object</strong></span></span></p></td>
<td><p><span data-ttu-id="924fb-116">Объектная переменная, представляющая поле, которое добавляется в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="924fb-116">An object variable that represents the field being appended to the collection.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="remarks"></a><span data-ttu-id="924fb-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="924fb-117">Remarks</span></span>

<span data-ttu-id="924fb-118">Метод **Append** можно использовать для добавления новой таблицы в базу данных, добавления поля в таблицу и добавления поля в индекс.</span><span class="sxs-lookup"><span data-stu-id="924fb-118">You can use the **Append** method to add a new table to a database, add a field to a table, and add a field to an index.</span></span>

<span data-ttu-id="924fb-119">Добавляемый объект становится постоянным объектом, хранящимся на диске, пока вы не удалите его с помощью метода **Delete**.</span><span class="sxs-lookup"><span data-stu-id="924fb-119">The appended object becomes a persistent object, stored on disk, until you delete it by using the **Delete** method.</span></span>

<span data-ttu-id="924fb-120">Добавление нового объекта происходит незамедлительно, но следует применить метод **Refresh** для любых других коллекций, которые могут быть затронуты изменениями в структуре базы данных.</span><span class="sxs-lookup"><span data-stu-id="924fb-120">The addition of a new object occurs immediately, but you should use the **Refresh** method on any other collections that may be affected by changes to the database structure.</span></span>

<span data-ttu-id="924fb-121">Если добавляемый объект неполный (например, если не добавлены объекты **Field** в коллекцию **Fields** объекта **Index** перед его добавлением в коллекцию **Indexes**) или заданы неверные свойства в одном или нескольких подчиненных объектах, применение метода **Append** вызывает ошибку.</span><span class="sxs-lookup"><span data-stu-id="924fb-121">If the object you're appending isn't complete (such as when you haven't appended any **Field** objects to a **Fields** collection of an **Index** object before it's appended to an **Indexes** collection) or if the properties set in one or more subordinate objects are incorrect, using the **Append** method causes an error.</span></span> <span data-ttu-id="924fb-122">Например, если не указан тип поля и выполняется попытка добавить объект **Field** в коллекцию **Fields** объекта **TableDef**, применение метода **Append** вызывает ошибку во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="924fb-122">For example, if you haven’t specified a field type and then try to append the **Field** object to the **Fields** collection in a **TableDef** object, using the **Append** method triggers a run-time error.</span></span>

## <a name="example"></a><span data-ttu-id="924fb-123">Пример</span><span class="sxs-lookup"><span data-stu-id="924fb-123">Example</span></span>

<span data-ttu-id="924fb-124">В этом примере используется метод **Append** или метод **Delete** для изменения коллекции **Fields** объекта **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="924fb-124">This example uses either the **Append** method or the **Delete** method to modify the **Fields** collection of a **TableDef**.</span></span> <span data-ttu-id="924fb-125">Процедура AppendDeleteField является обязательной для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="924fb-125">The OpenRecordsetOutput procedure is required for this procedure to run.</span></span>

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
