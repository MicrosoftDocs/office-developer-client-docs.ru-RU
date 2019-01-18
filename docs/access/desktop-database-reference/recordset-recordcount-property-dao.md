---
title: Свойство Recordset.RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: aa1fed4f-ca51-918f-0a46-2b755b5f861a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821452(v=office.15)
ms:contentKeyID: 48546941
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Priority
ms.openlocfilehash: b9bdc243aae48bd928468362cb86ca077f4abe52
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707614"
---
# <a name="recordsetrecordcount-property-dao"></a><span data-ttu-id="59384-102">Свойство Recordset.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="59384-102">Recordset.RecordCount property (DAO)</span></span>

<span data-ttu-id="59384-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="59384-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="59384-104">Возвращает число записей в объект **[набора записей](recordset-object-dao.md)** или общее число записей в таблице тип объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="59384-104">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object.</span></span> <span data-ttu-id="59384-105">или **[TableDef](tabledef-object-dao.md)** объект.</span><span class="sxs-lookup"><span data-stu-id="59384-105">or **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="59384-106">Только для чтения **времени**.</span><span class="sxs-lookup"><span data-stu-id="59384-106">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="59384-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="59384-107">Syntax</span></span>

<span data-ttu-id="59384-108">*выражение* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="59384-108">*expression* .RecordCount</span></span>

<span data-ttu-id="59384-109">*выражение* Переменная, которая представляет собой объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="59384-109">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="59384-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="59384-110">Remarks</span></span>

<span data-ttu-id="59384-111">Используйте свойство **RecordCount** найдете количество записей в **записей** или объект **TableDef** осуществлялся.</span><span class="sxs-lookup"><span data-stu-id="59384-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="59384-112">Свойство **RecordCount** не указывает количество записей содержащихся в динамический набор –, моментальный снимок – или объекта **набора записей** прямого — только — тип до получения доступа к все записи.</span><span class="sxs-lookup"><span data-stu-id="59384-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="59384-113">После обращения последней записи свойство **RecordCount** показывает общее количество неудаленные записей в объекте **TableDef** или **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="59384-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="59384-114">Чтобы принудительно последней записи для доступа, используйте метод **[MoveLast](recordset-movelast-method-dao.md)** на объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="59384-114">To force the last record to be accessed, use the **[MoveLast](recordset-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="59384-115">Также можно использовать функцию SQL **Count** для определения приблизительное число записей, которые возвращает запрос.</span><span class="sxs-lookup"><span data-stu-id="59384-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="59384-116">С помощью метода **MoveLast** для заполнения открываемые **записей** негативно влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="59384-116">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance.</span></span> <span data-ttu-id="59384-117">Если нет необходимости иметь точных **RecordCount** сразу же после открытия набора **записей**, лучше Подождите, пока заполнения **записей** с другими частями кода перед проверкой свойство **RecordCount** .</span><span class="sxs-lookup"><span data-stu-id="59384-117">Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="59384-118">Как приложение удаляет записи в объекте **набора записей** добавляющий, значение свойства **RecordCount** снижается.</span><span class="sxs-lookup"><span data-stu-id="59384-118">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases.</span></span> <span data-ttu-id="59384-119">Тем не менее удаленные другими пользователями записи не вступят в силу в свойстве **RecordCount** до текущей записи находится в удаленных запись.</span><span class="sxs-lookup"><span data-stu-id="59384-119">However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record.</span></span> <span data-ttu-id="59384-120">При выполнении транзакции, влияющей на значение свойства **RecordCount** и и впоследствии ее откат, свойство **RecordCount** могут не отражать фактическое число оставшихся записей.</span><span class="sxs-lookup"><span data-stu-id="59384-120">If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="59384-121">Свойство **RecordCount** объекта **набора записей** моментальный снимок – прямого — только — тип или не влияет на изменения в таблицах.</span><span class="sxs-lookup"><span data-stu-id="59384-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="59384-122">Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.</span><span class="sxs-lookup"><span data-stu-id="59384-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="59384-123">С помощью метода **[повторный запрос](recordset-requery-method-dao.md)** на объект **набора записей** сбрасывает свойство **RecordCount** , как если бы были повторно выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="59384-123">Using the **[Requery](recordset-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="59384-124">Пример</span><span class="sxs-lookup"><span data-stu-id="59384-124">Example</span></span>

<span data-ttu-id="59384-125">В этом примере демонстрируется свойство **RecordCount** с использованием разных типов наборов **записей** перед и после их в случае заполнения.</span><span class="sxs-lookup"><span data-stu-id="59384-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     
     With dbsNorthwind 
     ' Open table-type Recordset and show RecordCount 
     ' property. 
     Set rstEmployees = .OpenRecordset("Employees") 
     Debug.Print _ 
     "Table-type recordset from Employees table" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open dynaset-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenDynaset) 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Dynaset-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open snapshot-type Recordset and show RecordCount 
     ' property before populating the Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenSnapshot) 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after populating the 
     ' Recordset. 
     rstEmployees.MoveLast 
     Debug.Print "Snapshot-type recordset " & _ 
     "from Employees table after MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     ' Open forward-only-type Recordset and show 
     ' RecordCount property before populating the 
     ' Recordset. 
     Set rstEmployees = .OpenRecordset("Employees", _ 
     dbOpenForwardOnly) 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table before MoveLast" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     
     ' Show the RecordCount property after calling the 
     ' MoveNext method. 
     rstEmployees.MoveNext 
     Debug.Print "Forward-only-type recordset " & _ 
     "from Employees table after MoveNext" 
     Debug.Print " RecordCount = " & _ 
     rstEmployees.RecordCount 
     rstEmployees.Close 
     
     .Close 
     End With 
     
    End Sub
```
