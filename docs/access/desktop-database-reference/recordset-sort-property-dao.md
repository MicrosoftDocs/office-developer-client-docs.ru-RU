---
title: Свойство Recordset.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 9be9bf62-f713-537e-4df0-3a54d485a523
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198077(v=office.15)
ms:contentKeyID: 48546582
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1053063
f1_categories:
- Office.Version=v15
ms.openlocfilehash: b8dc3c551c9aa75da205717fef682f0abed7a54b
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25998730"
---
# <a name="recordsetsort-property-dao"></a><span data-ttu-id="4b5ec-102">Свойство Recordset.Sort (DAO)</span><span class="sxs-lookup"><span data-stu-id="4b5ec-102">Recordset.Sort property (DAO)</span></span>

<span data-ttu-id="4b5ec-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4b5ec-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4b5ec-104">Задает или возвращает порядок сортировки для записей в объекте **[набора записей](recordset-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4b5ec-104">Sets or returns the sort order for records in a **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4b5ec-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4b5ec-105">Syntax</span></span>

<span data-ttu-id="4b5ec-106">*выражение* . Сортировка</span><span class="sxs-lookup"><span data-stu-id="4b5ec-106">*expression* .Sort</span></span>

<span data-ttu-id="4b5ec-107">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="4b5ec-107">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4b5ec-108">Примечания</span><span class="sxs-lookup"><span data-stu-id="4b5ec-108">Remarks</span></span>

<span data-ttu-id="4b5ec-109">Можно использовать свойство **сортировки** с динамический набор – и моментальный снимок — тип объектов **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="4b5ec-109">You can use the **Sort** property with dynaset– and snapshot–type **Recordset** objects.</span></span>

<span data-ttu-id="4b5ec-110">Если значение этого свойства для объекта, сортировка происходит при последующих объекта **набора записей** из этого объекта.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-110">When you set this property for an object, sorting occurs when a subsequent **Recordset** object is created from that object.</span></span> <span data-ttu-id="4b5ec-111">Свойство **сортировки** переопределяет любой порядок сортировки, указанный для объекта **[QueryDef](querydef-object-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="4b5ec-111">The **Sort** property setting overrides any sort order specified for a **[QueryDef](querydef-object-dao.md)** object.</span></span>

<span data-ttu-id="4b5ec-112">Порядок сортировки по возрастанию (A-Z или 0 до 100).</span><span class="sxs-lookup"><span data-stu-id="4b5ec-112">The default sort order is ascending (A to Z or 0 to 100).</span></span>

<span data-ttu-id="4b5ec-113">Свойство **сортировки** не применяется к таблице – прямого – только для – тип или объектов **наборов записей** .</span><span class="sxs-lookup"><span data-stu-id="4b5ec-113">The **Sort** property doesn't apply to table– or forward–only–type **Recordset** objects.</span></span> <span data-ttu-id="4b5ec-114">Чтобы отсортировать объекта **набора записей** в таблице — тип, используйте свойство **[индекса](recordset-index-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="4b5ec-114">To sort a table–type **Recordset** object, use the **[Index](recordset-index-property-dao.md)** property.</span></span>

> [!NOTE]
> <span data-ttu-id="4b5ec-115">Во многих случаях это быстрее, чтобы открыть новый объект **набора записей** с помощью инструкции SQL, которая включает в себя критерия сортировки.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes the sorting criteria.</span></span>

## <a name="example"></a><span data-ttu-id="4b5ec-116">Пример</span><span class="sxs-lookup"><span data-stu-id="4b5ec-116">Example</span></span>

<span data-ttu-id="4b5ec-117">В этом примере демонстрируется свойство **сортировки** , изменив его значение и создание нового **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-117">This example demonstrates the **Sort** property by changing its value and creating a new **Recordset**.</span></span> <span data-ttu-id="4b5ec-118">Функция SortOutput является обязательным для выполнения этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-118">The SortOutput function is required for this procedure to run.</span></span>

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     Dim rstSortEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     
     With rstEmployees 
     SortOutput "Original Recordset:", rstEmployees 
     .Sort = "LastName, FirstName" 
     ' Print report showing Sort property and record order. 
     SortOutput _ 
     "Recordset after changing Sort property:", _ 
     rstEmployees 
     ' Open new Recordset from current one. 
     Set rstSortEmployees = .OpenRecordset 
     ' Print report showing Sort property and record order. 
     SortOutput "New Recordset:", rstSortEmployees 
     rstSortEmployees.Close 
     .Close 
     End With 
     
     dbsNorthwind.Close 
     
    End Sub 
     
    Function SortOutput(strTemp As String, _ 
     rstTemp As Recordset) 
     
     With rstTemp 
     Debug.Print strTemp 
     Debug.Print " Sort = " & _ 
     IIf(.Sort <> "", .Sort, "[Empty]") 
     .MoveFirst 
     
     ' Enumerate Recordset. 
     Do While Not .EOF 
     Debug.Print " " & !LastName & _ 
     ", " & !FirstName 
     .MoveNext 
     Loop 
     
     End With 
     
    End Function 
```

<br/>

<span data-ttu-id="4b5ec-119">Если вы знаете данных, которые нужно выбрать, обычно более эффективно создание **набора записей** с помощью инструкции SQL.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-119">When you know the data you want to select, it's usually more efficient to create a **Recordset** with an SQL statement.</span></span> <span data-ttu-id="4b5ec-120">В этом примере показано, как можно создать только один **набор записей** и получить те же результаты, как показано в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="4b5ec-120">This example shows how you can create just one **Recordset** and obtain the same results as in the preceding example.</span></span>

```vb
    Sub SortX2() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     ' Open a Recordset from an SQL statement that specifies a 
     ' sort order. 
     Set rstEmployees = _ 
     dbsNorthwind.OpenRecordset("SELECT * " & _ 
     "FROM Employees ORDER BY LastName, FirstName", _ 
     dbOpenDynaset) 
     
     dbsNorthwind.Close 
     
    End Sub
```
