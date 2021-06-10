---
title: Свойство Recordset2.Sort (DAO)
TOCTitle: Sort Property
ms:assetid: 523a8c29-46e2-564f-205d-03c214f277fe
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193917(v=office.15)
ms:contentKeyID: 48544842
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a5784054ce195a1a2ea516d4f6a3417c5a8db71c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309271"
---
# <a name="recordset2sort-property-dao"></a><span data-ttu-id="c03e1-102">Свойство Recordset2.Sort (DAO)</span><span class="sxs-lookup"><span data-stu-id="c03e1-102">Recordset2.Sort property (DAO)</span></span>

<span data-ttu-id="c03e1-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="c03e1-103">**Applies to**: Access 2013, Office 2013</span></span> 

<span data-ttu-id="c03e1-104">Задает или возвращает порядок сортировки для записей в объекте **[Recordset](recordset-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="c03e1-104">Sets or returns the sort order for records in a **[Recordset](recordset-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="c03e1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c03e1-105">Syntax</span></span>

<span data-ttu-id="c03e1-106">*expression* .Sort</span><span class="sxs-lookup"><span data-stu-id="c03e1-106">*expression* .Sort</span></span>

<span data-ttu-id="c03e1-107">*выражение* Переменная, представляюная объект **Recordset2.**</span><span class="sxs-lookup"><span data-stu-id="c03e1-107">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="c03e1-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c03e1-108">Remarks</span></span>

<span data-ttu-id="c03e1-109">Вы можете использовать свойство **Sort** с объектами **Recordset** типа dynaset и моментальный снимок.</span><span class="sxs-lookup"><span data-stu-id="c03e1-109">You can use the **Sort** property with dynaset– and snapshot–type **Recordset** objects.</span></span>

<span data-ttu-id="c03e1-110">Если вы задаете это свойство для объекта, сортировка будет выполнена при создании последующего объекта **Recordset** из данного объекта.</span><span class="sxs-lookup"><span data-stu-id="c03e1-110">When you set this property for an object, sorting occurs when a subsequent **Recordset** object is created from that object.</span></span> <span data-ttu-id="c03e1-111">Настройка свойства **Sort** будет переопределять любой порядок сортировки, указанный для объекта **[QueryDef](querydef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c03e1-111">The **Sort** property setting overrides any sort order specified for a **[QueryDef](querydef-object-dao.md)** object.</span></span>

<span data-ttu-id="c03e1-112">Стандартный порядок сортировки по возрастанию (от А до Я или от 0 до 100).</span><span class="sxs-lookup"><span data-stu-id="c03e1-112">The default sort order is ascending (A to Z or 0 to 100).</span></span>

<span data-ttu-id="c03e1-113">Свойство **Sort** не оказывает влияние на объекты **Recordset** табличного или однонаправленного типа.</span><span class="sxs-lookup"><span data-stu-id="c03e1-113">The **Sort** property doesn't apply to table– or forward–only–type **Recordset** objects.</span></span> <span data-ttu-id="c03e1-114">Чтобы отсортировать табличный тип объекта **Recordset** используйте свойство **[Index](recordset2-index-property-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="c03e1-114">To sort a table–type **Recordset** object, use the **[Index](recordset2-index-property-dao.md)** property.</span></span>

> [!NOTE]
> <span data-ttu-id="c03e1-115">Во многих случаях быстрее будет открыть новый объект **Recordset** с помощью оператора SQL, который включает условия сортировки.</span><span class="sxs-lookup"><span data-stu-id="c03e1-115">In many cases, it's faster to open a new **Recordset** object by using an SQL statement that includes the sorting criteria.</span></span>

## <a name="example"></a><span data-ttu-id="c03e1-116">Пример</span><span class="sxs-lookup"><span data-stu-id="c03e1-116">Example</span></span>

<span data-ttu-id="c03e1-117">В этом примере показано свойство **Sort**, изменение его значения, а также создание нового объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="c03e1-117">This example demonstrates the **Sort** property by changing its value and creating a new **Recordset**.</span></span> <span data-ttu-id="c03e1-118">Функция SortOutput обязательна для запуска этой процедуры.</span><span class="sxs-lookup"><span data-stu-id="c03e1-118">The SortOutput function is required for this procedure to run.</span></span>

```vb
    Sub SortX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     Dim rstSortEmployees As Recordset2 
     
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

<span data-ttu-id="c03e1-119">Если вы знаете данные, которые вы хотите выбрать, как правило, более рационально будет создать **Recordset** с оператором SQL.</span><span class="sxs-lookup"><span data-stu-id="c03e1-119">When you know the data you want to select, it's usually more efficient to create a **Recordset** with an SQL statement.</span></span> <span data-ttu-id="c03e1-120">В этом примере показано, как можно создать только один объект **Recordset** и получить те же результаты, что и в предыдущем примере.</span><span class="sxs-lookup"><span data-stu-id="c03e1-120">This example shows how you can create just one **Recordset** and obtain the same results as in the preceding example.</span></span>

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
