---
title: Свойство Recordset2. RecordCount (DAO)
TOCTitle: RecordCount Property
ms:assetid: 77852966-11e9-1773-6e58-53927b84c03b
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196071(v=office.15)
ms:contentKeyID: 48545728
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052890
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: c23de433f26b5a54b3fee5cc69f67a07b53f8a3b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309158"
---
# <a name="recordset2recordcount-property-dao"></a><span data-ttu-id="4d0a4-102">Свойство Recordset2. RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="4d0a4-102">Recordset2.RecordCount property (DAO)</span></span>

<span data-ttu-id="4d0a4-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4d0a4-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d0a4-104">Возвращает число записей, доступных в объекте **[Recordset](recordset-object-dao.md)**, или общее количество записей в **Recordset** табличного типа.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-104">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object.</span></span> <span data-ttu-id="4d0a4-105">или объекте **[TableDef](tabledef-object-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-105">or **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="4d0a4-106">Только для чтения, **Long**.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-106">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4d0a4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4d0a4-107">Syntax</span></span>

<span data-ttu-id="4d0a4-108">*Expression* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="4d0a4-108">*expression* .RecordCount</span></span>

<span data-ttu-id="4d0a4-109">*Expression (выражение* ) Переменная, представляющая объект **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="4d0a4-109">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d0a4-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="4d0a4-110">Remarks</span></span>

<span data-ttu-id="4d0a4-111">Используйте свойство **RecordCount** , чтобы узнать, сколько записей в объекте **Recordset** или объекте **tabledef** было получено.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="4d0a4-112">Свойство **RecordCount** не указывает количество записей, содержащихся в объекте **Recordset** динамического подмножества, снимка или перенаправлении, пока не будут доступны все записи.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="4d0a4-113">После получения доступа к последней записи свойство **RecordCount** указывает общее число неудаленных записей в объекте **Recordset** или **tabledef** .</span><span class="sxs-lookup"><span data-stu-id="4d0a4-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="4d0a4-114">Чтобы принудительно получить доступ к последней записи, используйте метод **[MoveLast](recordset2-movelast-method-dao.md)** объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="4d0a4-114">To force the last record to be accessed, use the **[MoveLast](recordset2-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="4d0a4-115">Вы также можете использовать функцию **счетчика** SQL, чтобы определить примерное количество записей, возвращаемых запросом.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="4d0a4-116">Использование метода **MoveLast** для заполнения недавно открытого **набора записей** отрицательно влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-116">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance.</span></span> <span data-ttu-id="4d0a4-117">Если вам не требуется точный **RecordCount** , как только вы откроете объект **Recordset**, лучше дождаться заполнения объекта **Recordset** другими частями кода, прежде чем проверять свойство **RecordCount** .</span><span class="sxs-lookup"><span data-stu-id="4d0a4-117">Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="4d0a4-118">Когда ваше приложение удаляет записи в объекте **Recordset** типа динамического подмножества, значение свойства **RecordCount** уменьшается.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-118">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases.</span></span> <span data-ttu-id="4d0a4-119">Однако записи, удаленные другими пользователями, не отражаются в свойстве **RecordCount** до тех пор, пока текущая запись не будет размещена в удаленной записи.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-119">However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record.</span></span> <span data-ttu-id="4d0a4-120">Если выполнить транзакцию, влияющую на настройку свойства **RecordCount** , и затем выполнить откат транзакции, свойство **RecordCount** не будет отражать фактическое количество оставшихся записей.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-120">If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="4d0a4-121">Изменения в базовых таблицах для свойства **RecordCount** объекта **Recordset** с типом "снимок" или "вперед" не затрагиваются.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="4d0a4-122">Для объекта **Recordset** или объекта **tabledef** без записей задано свойство **RecordCount** , равное 0.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="4d0a4-123">При использовании **[](recordset2-requery-method-dao.md)** метода Requery объекта **Recordset** сбрасывается значение свойства **RecordCount** так же, как если бы запрос выполнялся повторно.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-123">Using the **[Requery](recordset2-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="4d0a4-124">Пример</span><span class="sxs-lookup"><span data-stu-id="4d0a4-124">Example</span></span>

<span data-ttu-id="4d0a4-125">В этом примере показано свойство **RecordCount** с различными типами **наборов записей** до и после заполнения.</span><span class="sxs-lookup"><span data-stu-id="4d0a4-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

```vb
    Sub RecordCountX() 
     
     Dim dbsNorthwind As Database 
     Dim rstEmployees As Recordset2 
     
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
