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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708860"
---
# <a name="indexignorenulls-property-dao"></a><span data-ttu-id="e8887-102">Свойство Index.IgnoreNulls (DAO)</span><span class="sxs-lookup"><span data-stu-id="e8887-102">Index.IgnoreNulls property (DAO)</span></span>


<span data-ttu-id="e8887-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8887-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e8887-104">Задает или возвращает значение, указывающее, имеют ли записи, для которых значения Null в полях индекса записи индекса (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e8887-104">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8887-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e8887-105">Syntax</span></span>

<span data-ttu-id="e8887-106">*выражение* . IgnoreNulls</span><span class="sxs-lookup"><span data-stu-id="e8887-106">*expression* .IgnoreNulls</span></span>

<span data-ttu-id="e8887-107">*выражение* Переменная, которая представляет объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="e8887-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8887-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="e8887-108">Remarks</span></span>

<span data-ttu-id="e8887-109">Это свойство является чтение и запись для нового объекта **[индекс](index-object-dao.md)** еще не добавлены в семейство сайтов и только для чтения для существующего объекта **индексу** в коллекции **[индексов](indexes-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="e8887-109">This property is read/write for a new **[Index](index-object-dao.md)** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection.</span></span>

<span data-ttu-id="e8887-110">Чтобы ускорить процесс поиска записей, можно определить индекс для поля.</span><span class="sxs-lookup"><span data-stu-id="e8887-110">To speed up the process of searching for records, you can define an index for a field.</span></span> <span data-ttu-id="e8887-111">Если разрешить **значение null,** записей в индексированных полей и рассчитывают многие из записей должен иметь **значение null**, можно задать свойству **IgnoreNulls** **индекс** объекта значение **True** для сокращения объема дискового пространства, который использует индекс.</span><span class="sxs-lookup"><span data-stu-id="e8887-111">If you allow **null** entries in an indexed field and expect many of the entries to be **null**, you can set the **IgnoreNulls** property for the **Index** object to **True** to reduce the amount of storage space that the index uses.</span></span>

<span data-ttu-id="e8887-112">Настройка свойства **IgnoreNulls** и настройки свойства **[необходимые](field-required-property-dao.md)** вместе определить, имеет ли запись с **нулевое** значение индекса элемента.</span><span class="sxs-lookup"><span data-stu-id="e8887-112">The **IgnoreNulls** property setting and the **[Required](field-required-property-dao.md)** property setting together determine whether a record with a **null** index value has an index entry.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e8887-113">Если IgnoreNulls</span><span class="sxs-lookup"><span data-stu-id="e8887-113">If IgnoreNulls is</span></span></p></th>
<th><p><span data-ttu-id="e8887-114">Который требуется</span><span class="sxs-lookup"><span data-stu-id="e8887-114">And Required is</span></span></p></th>
<th><p><span data-ttu-id="e8887-115">То</span><span class="sxs-lookup"><span data-stu-id="e8887-115">Then</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8887-116">Истина</span><span class="sxs-lookup"><span data-stu-id="e8887-116">True</span></span></p></td>
<td><p><span data-ttu-id="e8887-117">Ложь</span><span class="sxs-lookup"><span data-stu-id="e8887-117">False</span></span></p></td>
<td><p><span data-ttu-id="e8887-118">Значение null разрешено в поле индекса; не добавлена запись индекса.</span><span class="sxs-lookup"><span data-stu-id="e8887-118">A null value is allowed in the index field; no index entry added.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8887-119">Ложь</span><span class="sxs-lookup"><span data-stu-id="e8887-119">False</span></span></p></td>
<td><p><span data-ttu-id="e8887-120">Ложь</span><span class="sxs-lookup"><span data-stu-id="e8887-120">False</span></span></p></td>
<td><p><span data-ttu-id="e8887-121">Значение null разрешено в поле индекса; добавлена запись индекса.</span><span class="sxs-lookup"><span data-stu-id="e8887-121">A null value is allowed in the index field; index entry added.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8887-122">True (Истина) или False (Ложь)</span><span class="sxs-lookup"><span data-stu-id="e8887-122">True or False</span></span></p></td>
<td><p><span data-ttu-id="e8887-123">True</span><span class="sxs-lookup"><span data-stu-id="e8887-123">True</span></span></p></td>
<td><p><span data-ttu-id="e8887-124">Нулевое значение не является допустимым в поле индекса; не добавлена запись индекса.</span><span class="sxs-lookup"><span data-stu-id="e8887-124">A null value isn't allowed in the index field; no index entry added.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="e8887-125">Пример</span><span class="sxs-lookup"><span data-stu-id="e8887-125">Example</span></span>

<span data-ttu-id="e8887-126">В этом примере присваивает свойству **IgnoreNulls** нового **индекса** значение **True** или **False** на основе ввода пользователя, а затем влияние на **набора записей** с записью, чьи ключевое поле содержит значение **Null** .</span><span class="sxs-lookup"><span data-stu-id="e8887-126">This example sets the **IgnoreNulls** property of a new **Index** to **True** or **False** based on user input, and then demonstrates the effect on a **Recordset** with a record whose key field contains a **Null** value.</span></span>

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
