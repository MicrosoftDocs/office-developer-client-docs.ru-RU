---
title: Свойство Index.IgnoreNulls (DAO)
TOCTitle: IgnoreNulls Property
ms:assetid: f49f17b8-d7c1-18ab-07a8-e1be61488519
ms:mtpsurl: https://msdn.microsoft.com/library/Ff836698(v=office.15)
ms:contentKeyID: 48548694
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052931
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 6c306f76e34e24abb5065c627d9325b48c3acead
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291805"
---
# <a name="indexignorenulls-property-dao"></a><span data-ttu-id="5d4e4-102">Свойство Index.IgnoreNulls (DAO)</span><span class="sxs-lookup"><span data-stu-id="5d4e4-102">Index.IgnoreNulls property (DAO)</span></span>


<span data-ttu-id="5d4e4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="5d4e4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5d4e4-104">Задает или возвращает значение, которое указывает, имеют ли записи с значениями Null в своих полях индексов записи индексов (только в рабочей области Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="5d4e4-104">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d4e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5d4e4-105">Syntax</span></span>

<span data-ttu-id="5d4e4-106">*выражения* . IgnoreNulls</span><span class="sxs-lookup"><span data-stu-id="5d4e4-106">*expression* .IgnoreNulls</span></span>

<span data-ttu-id="5d4e4-107">*выражение* Переменная, представляюная объект **Index.**</span><span class="sxs-lookup"><span data-stu-id="5d4e4-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d4e4-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="5d4e4-108">Remarks</span></span>

<span data-ttu-id="5d4e4-109">Это свойство читается или записи для нового объекта **[Index,](index-object-dao.md)** который еще не был придан коллекции и только для чтения для существующего объекта **Index** в коллекции **[Indexes.](indexes-collection-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="5d4e4-109">This property is read/write for a new **[Index](index-object-dao.md)** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection.</span></span>

<span data-ttu-id="5d4e4-110">Чтобы ускорить процесс поиска записей, можно определить индекс поля.</span><span class="sxs-lookup"><span data-stu-id="5d4e4-110">To speed up the process of searching for records, you can define an index for a field.</span></span> <span data-ttu-id="5d4e4-111">Если вы  разрешаете недействительными записи в индексном поле и ожидаете, что многие записи будут  **null,** вы можете установить свойство **IgnoreNulls** для объекта **Index** true, чтобы уменьшить объем пространства хранения, который использует индекс.</span><span class="sxs-lookup"><span data-stu-id="5d4e4-111">If you allow **null** entries in an indexed field and expect many of the entries to be **null**, you can set the **IgnoreNulls** property for the **Index** object to **True** to reduce the amount of storage space that the index uses.</span></span>

<span data-ttu-id="5d4e4-112">Параметр **свойства IgnoreNulls** и параметр **[Обязательное](field-required-property-dao.md)** свойство вместе определяют, имеет ли запись с значением **null** index запись индекса.</span><span class="sxs-lookup"><span data-stu-id="5d4e4-112">The **IgnoreNulls** property setting and the **[Required](field-required-property-dao.md)** property setting together determine whether a record with a **null** index value has an index entry.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5d4e4-113">Если IgnoreNulls</span><span class="sxs-lookup"><span data-stu-id="5d4e4-113">If IgnoreNulls is</span></span></p></th>
<th><p><span data-ttu-id="5d4e4-114">И обязательно</span><span class="sxs-lookup"><span data-stu-id="5d4e4-114">And Required is</span></span></p></th>
<th><p><span data-ttu-id="5d4e4-115">Then</span><span class="sxs-lookup"><span data-stu-id="5d4e4-115">Then</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d4e4-116">True (Истина)</span><span class="sxs-lookup"><span data-stu-id="5d4e4-116">True</span></span></p></td>
<td><p><span data-ttu-id="5d4e4-117">False (Ложь)</span><span class="sxs-lookup"><span data-stu-id="5d4e4-117">False</span></span></p></td>
<td><p><span data-ttu-id="5d4e4-118">Значение null разрешено в поле индекса; нет добавленной записи индекса.</span><span class="sxs-lookup"><span data-stu-id="5d4e4-118">A null value is allowed in the index field; no index entry added.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d4e4-119">False (Ложь)</span><span class="sxs-lookup"><span data-stu-id="5d4e4-119">False</span></span></p></td>
<td><p><span data-ttu-id="5d4e4-120">False (Ложь)</span><span class="sxs-lookup"><span data-stu-id="5d4e4-120">False</span></span></p></td>
<td><p><span data-ttu-id="5d4e4-121">Значение null разрешено в поле индекса; Добавлена запись индекса.</span><span class="sxs-lookup"><span data-stu-id="5d4e4-121">A null value is allowed in the index field; index entry added.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d4e4-122">True или False</span><span class="sxs-lookup"><span data-stu-id="5d4e4-122">True or False</span></span></p></td>
<td><p><span data-ttu-id="5d4e4-123">True (Истина)</span><span class="sxs-lookup"><span data-stu-id="5d4e4-123">True</span></span></p></td>
<td><p><span data-ttu-id="5d4e4-124">Значение null не допускается в поле индекса; нет добавленной записи индекса.</span><span class="sxs-lookup"><span data-stu-id="5d4e4-124">A null value isn't allowed in the index field; no index entry added.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="5d4e4-125">Пример</span><span class="sxs-lookup"><span data-stu-id="5d4e4-125">Example</span></span>

<span data-ttu-id="5d4e4-126">В этом примере свойство **IgnoreNulls** нового index **to** **True** или **False** определяется на  основе ввода пользователя, а затем демонстрирует влияние на набор записей с записью, ключевое поле которой содержит значение **Null.**</span><span class="sxs-lookup"><span data-stu-id="5d4e4-126">This example sets the **IgnoreNulls** property of a new **Index** to **True** or **False** based on user input, and then demonstrates the effect on a **Recordset** with a record whose key field contains a **Null** value.</span></span>

```vb
    Sub IgnoreNullsX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim idxNew As Index 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind!Employees 
     
     With tdfEmployees 
     ' Create a new Index object. 
     Set idxNew = .CreateIndex("NewIndex") 
     idxNew.Fields.Append idxNew.CreateField("Country") 
     
     ' Set the IgnoreNulls property of the new Index object 
     ' based on the user's input. 
     Select Case MsgBox("Set IgnoreNulls to True?", _ 
     vbYesNoCancel) 
     Case vbYes 
     idxNew.IgnoreNulls = True 
     Case vbNo 
     idxNew.IgnoreNulls = False 
     Case Else 
     dbsNorthwind.Close 
     End 
     End Select 
     
     ' Append the new Index object to the Indexes 
     ' collection of the Employees table. 
     .Indexes.Append idxNew 
     .Indexes.Refresh 
     End With 
     
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees") 
     
     With rstEmployees 
     ' Add a new record to the Employees table. 
     .AddNew 
     !FirstName = "Gary" 
     !LastName = "Haarsager" 
     .Update 
     
     ' Use the new index to set the order of the records. 
     .Index = idxNew.Name 
     .MoveFirst 
     
     Debug.Print "Index = " & .Index & _ 
     ", IgnoreNulls = " & idxNew.IgnoreNulls 
     Debug.Print " Country - Name" 
     
     ' Enumerate the Recordset. The value of the 
     ' IgnoreNulls property will determine if the newly 
     ' added record appears in the output. 
     Do While Not .EOF 
     Debug.Print " " & _ 
     IIf(IsNull(!Country), "[Null]", !Country) & _ 
     " - " & !FirstName & " " & !LastName 
     .MoveNext 
     Loop 
     
     ' Delete new record because this is a demonstration. 
     .Index = "" 
     .Bookmark = .LastModified 
     .Delete 
     .Close 
     End With 
     
     ' Delete new Index because this is a demonstration. 
     tdfEmployees.Indexes.Delete idxNew.Name 
     dbsNorthwind.Close 
     
    End Sub
```
