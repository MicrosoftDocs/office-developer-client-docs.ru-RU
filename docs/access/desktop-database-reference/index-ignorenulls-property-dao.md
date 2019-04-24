---
title: Свойство index. Игноренуллс (DAO)
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
# <a name="indexignorenulls-property-dao"></a><span data-ttu-id="63dce-102">Свойство index. Игноренуллс (DAO)</span><span class="sxs-lookup"><span data-stu-id="63dce-102">Index.IgnoreNulls property (DAO)</span></span>


<span data-ttu-id="63dce-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="63dce-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="63dce-104">Задает или возвращает значение, которое указывает, имеют ли записи индекса значения NULL в полях индекса (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="63dce-104">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="63dce-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="63dce-105">Syntax</span></span>

<span data-ttu-id="63dce-106">*Expression* . Игноренуллс</span><span class="sxs-lookup"><span data-stu-id="63dce-106">*expression* .IgnoreNulls</span></span>

<span data-ttu-id="63dce-107">*Expression (выражение* ) Переменная, представляющая объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="63dce-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="63dce-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="63dce-108">Remarks</span></span>

<span data-ttu-id="63dce-109">Это свойство доступно для чтения и записи для нового объекта **[index](index-object-dao.md)** , который еще не добавлен в коллекцию и доступен только для чтения для существующего объекта **index** в коллекции **[indexes](indexes-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="63dce-109">This property is read/write for a new **[Index](index-object-dao.md)** object not yet appended to a collection and read-only for an existing **Index** object in an **[Indexes](indexes-collection-dao.md)** collection.</span></span>

<span data-ttu-id="63dce-110">Чтобы ускорить процесс поиска записей, можно определить индекс для поля.</span><span class="sxs-lookup"><span data-stu-id="63dce-110">To speed up the process of searching for records, you can define an index for a field.</span></span> <span data-ttu-id="63dce-111">Если разрешить **пустые** записи в индексированном поле и предполагается, что многие из них будут иметь **значение NULL**, можно задать для свойства **игноренуллс** объекта **index** значение **true** , чтобы уменьшить объем места на диске, используемого индексом.</span><span class="sxs-lookup"><span data-stu-id="63dce-111">If you allow **null** entries in an indexed field and expect many of the entries to be **null**, you can set the **IgnoreNulls** property for the **Index** object to **True** to reduce the amount of storage space that the index uses.</span></span>

<span data-ttu-id="63dce-112">Вместе с параметром свойства **игноренуллс** и **[необходимым](field-required-property-dao.md)** параметром свойства определяется, содержит ли запись со значением **null** индекса запись индекса.</span><span class="sxs-lookup"><span data-stu-id="63dce-112">The **IgnoreNulls** property setting and the **[Required](field-required-property-dao.md)** property setting together determine whether a record with a **null** index value has an index entry.</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="63dce-113">Если Игноренуллс</span><span class="sxs-lookup"><span data-stu-id="63dce-113">If IgnoreNulls is</span></span></p></th>
<th><p><span data-ttu-id="63dce-114">И обязательно —</span><span class="sxs-lookup"><span data-stu-id="63dce-114">And Required is</span></span></p></th>
<th><p><span data-ttu-id="63dce-115">Then</span><span class="sxs-lookup"><span data-stu-id="63dce-115">Then</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="63dce-116">True</span><span class="sxs-lookup"><span data-stu-id="63dce-116">True</span></span></p></td>
<td><p><span data-ttu-id="63dce-117">False</span><span class="sxs-lookup"><span data-stu-id="63dce-117">False</span></span></p></td>
<td><p><span data-ttu-id="63dce-118">В поле индекса разрешено значение null; элемент индекса не добавлен.</span><span class="sxs-lookup"><span data-stu-id="63dce-118">A null value is allowed in the index field; no index entry added.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="63dce-119">False</span><span class="sxs-lookup"><span data-stu-id="63dce-119">False</span></span></p></td>
<td><p><span data-ttu-id="63dce-120">False</span><span class="sxs-lookup"><span data-stu-id="63dce-120">False</span></span></p></td>
<td><p><span data-ttu-id="63dce-121">В поле индекса разрешено значение null; добавлена запись индекса.</span><span class="sxs-lookup"><span data-stu-id="63dce-121">A null value is allowed in the index field; index entry added.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="63dce-122">True или False</span><span class="sxs-lookup"><span data-stu-id="63dce-122">True or False</span></span></p></td>
<td><p><span data-ttu-id="63dce-123">True</span><span class="sxs-lookup"><span data-stu-id="63dce-123">True</span></span></p></td>
<td><p><span data-ttu-id="63dce-124">Значение NULL не разрешено в поле index; элемент индекса не добавлен.</span><span class="sxs-lookup"><span data-stu-id="63dce-124">A null value isn't allowed in the index field; no index entry added.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="example"></a><span data-ttu-id="63dce-125">Пример</span><span class="sxs-lookup"><span data-stu-id="63dce-125">Example</span></span>

<span data-ttu-id="63dce-126">В этом примере для свойства **игноренуллс** нового **индекса** задается **значение true** или **false** на основе входных данных пользователя, а затем показано, \*\*\*\* как это сделать с записью, у которой ключевое поле содержит значение **null** .</span><span class="sxs-lookup"><span data-stu-id="63dce-126">This example sets the **IgnoreNulls** property of a new **Index** to **True** or **False** based on user input, and then demonstrates the effect on a **Recordset** with a record whose key field contains a **Null** value.</span></span>

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
