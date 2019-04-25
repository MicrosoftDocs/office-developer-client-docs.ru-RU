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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307639"
---
# <a name="recordsetrecordcount-property-dao"></a><span data-ttu-id="20422-102">Свойство Recordset.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="20422-102">Recordset.RecordCount Property (DAO)</span></span>

<span data-ttu-id="20422-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="20422-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="20422-104">Возвращает число записей, доступных в объекте **[Recordset](recordset-object-dao.md)**, или общее количество записей в **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="20422-104">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object.</span></span> <span data-ttu-id="20422-105">или объекте **[TableDef](tabledef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="20422-105">or **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="20422-106">Только для чтения, **Long**.</span><span class="sxs-lookup"><span data-stu-id="20422-106">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="20422-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="20422-107">Syntax</span></span>

<span data-ttu-id="20422-108">*выражение* .RecordCount</span><span class="sxs-lookup"><span data-stu-id="20422-108">*expression* .RecordCount</span></span>

<span data-ttu-id="20422-109">*выражение*: переменная, представляющая объект **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="20422-109">*expression* A variable that represents a **Recordset** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="20422-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="20422-110">Remarks</span></span>

<span data-ttu-id="20422-111">Используйте свойство **RecordCount**, чтобы узнать, ко скольким записям в объекте **Recordset** или **TableDef** получен доступ.</span><span class="sxs-lookup"><span data-stu-id="20422-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="20422-112">Свойство **RecordCount** не указывает, сколько записей содержится в объекте **Recordset** типа "Динамический набор", "Статический набор" или однонаправленного типа, пока не будет получен доступ ко всем записям.</span><span class="sxs-lookup"><span data-stu-id="20422-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="20422-113">После получения доступа к последней записи свойство **RecordCount** указывает общее число неудаленных записей в объекте **Recordset** или **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="20422-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="20422-114">Чтобы принудительно получить доступ к последней записи, используйте метод **[MoveLast](recordset-movelast-method-dao.md)** объекта **Recordset**.</span><span class="sxs-lookup"><span data-stu-id="20422-114">To force the last record to be accessed, use the **[MoveLast](recordset-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="20422-115">Вы также можете использовать функцию SQL **Count**, чтобы определить приблизительное число записей, возвращаемых запросом.</span><span class="sxs-lookup"><span data-stu-id="20422-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="20422-116">Использование метода **MoveLast** для заполнения только что открытого объекта **Recordset** негативно влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="20422-116">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance.</span></span> <span data-ttu-id="20422-117">Если не нужно получать точное значение **RecordCount** сразу при открытии объекта **Recordset**, лучше подождать заполнения объекта **Recordset** другими фрагментами кода, прежде чем проверять свойство **RecordCount**.</span><span class="sxs-lookup"><span data-stu-id="20422-117">Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="20422-118">Когда приложение удаляет записи в объекте **Recordset** типа "Статический набор", значение свойства **RecordCount** уменьшается.</span><span class="sxs-lookup"><span data-stu-id="20422-118">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases.</span></span> <span data-ttu-id="20422-119">Однако записи, удаленные другими пользователями, не отображаются в свойстве **RecordCount**, пока текущая запись расположена в удаленной записи.</span><span class="sxs-lookup"><span data-stu-id="20422-119">However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record.</span></span> <span data-ttu-id="20422-120">Если выполняется транзакция, влияющая на значение свойства **RecordCount**, с последующей отменой транзакции, свойство **RecordCount** не будет отражать фактическое количество оставшихся записей.</span><span class="sxs-lookup"><span data-stu-id="20422-120">If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="20422-121">Свойство **RecordCount** объекта **Recordset** типа "Динамический набор" или "Статический набор" не затрагивается изменениями в базовых таблицах.</span><span class="sxs-lookup"><span data-stu-id="20422-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="20422-122">У объекта **Recordset** или **TableDef** без записей свойству **RecordCount** соответствует значение 0.</span><span class="sxs-lookup"><span data-stu-id="20422-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="20422-123">Использование метода **[Requery](recordset-requery-method-dao.md)** для объекта **Recordset** сбрасывает свойство **RecordCount**, как при повторном выполнении запроса.</span><span class="sxs-lookup"><span data-stu-id="20422-123">Using the **[Requery](recordset-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="20422-124">Пример</span><span class="sxs-lookup"><span data-stu-id="20422-124">Example</span></span>

<span data-ttu-id="20422-125">В этом примере показано свойство **RecordCount** с разными типами объектов **Recordset** до и после их заполнения.</span><span class="sxs-lookup"><span data-stu-id="20422-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

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
