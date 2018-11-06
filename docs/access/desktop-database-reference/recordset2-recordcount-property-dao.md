---
title: Свойство Recordset2.RecordCount (DAO)
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
ms.openlocfilehash: a7dd162b9bc95e601cb5e2a8a41c81705764372c
ms.sourcegitcommit: 1dd744993ecb4bed241ace874ad26edaef1778b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/06/2018
ms.locfileid: "25997786"
---
# <a name="recordset2recordcount-property-dao"></a><span data-ttu-id="96669-102">Свойство Recordset2.RecordCount (DAO)</span><span class="sxs-lookup"><span data-stu-id="96669-102">Recordset2.RecordCount property (DAO)</span></span>

<span data-ttu-id="96669-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96669-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96669-104">Возвращает число записей в объект **[набора записей](recordset-object-dao.md)** или общее число записей в таблице тип объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="96669-104">Returns the number of records accessed in a **[Recordset](recordset-object-dao.md)** object, or the total number of records in a table-type **Recordset** object.</span></span> <span data-ttu-id="96669-105">или **[TableDef](tabledef-object-dao.md)** объект.</span><span class="sxs-lookup"><span data-stu-id="96669-105">or **[TableDef](tabledef-object-dao.md)** object.</span></span> <span data-ttu-id="96669-106">Только для чтения **времени**.</span><span class="sxs-lookup"><span data-stu-id="96669-106">Read-only **Long**.</span></span>

## <a name="syntax"></a><span data-ttu-id="96669-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="96669-107">Syntax</span></span>

<span data-ttu-id="96669-108">*выражение* . RecordCount</span><span class="sxs-lookup"><span data-stu-id="96669-108">*expression* .RecordCount</span></span>

<span data-ttu-id="96669-109">*выражение* Переменная, которая представляет собой объект- **Recordset2** .</span><span class="sxs-lookup"><span data-stu-id="96669-109">*expression* A variable that represents a **Recordset2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="96669-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="96669-110">Remarks</span></span>

<span data-ttu-id="96669-111">Используйте свойство **RecordCount** найдете количество записей в **записей** или объект **TableDef** осуществлялся.</span><span class="sxs-lookup"><span data-stu-id="96669-111">Use the **RecordCount** property to find out how many records in a **Recordset** or **TableDef** object have been accessed.</span></span> <span data-ttu-id="96669-112">Свойство **RecordCount** не указывает количество записей содержащихся в динамический набор –, моментальный снимок – или объекта **набора записей** прямого — только — тип до получения доступа к все записи.</span><span class="sxs-lookup"><span data-stu-id="96669-112">The **RecordCount** property doesn't indicate how many records are contained in a dynaset–, snapshot–, or forward–only–type **Recordset** object until all records have been accessed.</span></span> <span data-ttu-id="96669-113">После обращения последней записи свойство **RecordCount** показывает общее количество неудаленные записей в объекте **TableDef** или **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="96669-113">Once the last record has been accessed, the **RecordCount** property indicates the total number of undeleted records in the **Recordset** or **TableDef** object.</span></span> <span data-ttu-id="96669-114">Чтобы принудительно последней записи для доступа, используйте метод **[MoveLast](recordset2-movelast-method-dao.md)** на объекте **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="96669-114">To force the last record to be accessed, use the **[MoveLast](recordset2-movelast-method-dao.md)** method on the **Recordset** object.</span></span> <span data-ttu-id="96669-115">Также можно использовать функцию SQL **Count** для определения приблизительное число записей, которые возвращает запрос.</span><span class="sxs-lookup"><span data-stu-id="96669-115">You can also use an SQL **Count** function to determine the approximate number of records your query will return.</span></span>

> [!NOTE]
> <span data-ttu-id="96669-116">С помощью метода **MoveLast** для заполнения открываемые **записей** негативно влияет на производительность.</span><span class="sxs-lookup"><span data-stu-id="96669-116">Using the **MoveLast** method to populate a newly opened **Recordset** negatively impacts performance.</span></span> <span data-ttu-id="96669-117">Если нет необходимости иметь точных **RecordCount** сразу же после открытия набора **записей**, лучше Подождите, пока заполнения **записей** с другими частями кода перед проверкой свойство **RecordCount** .</span><span class="sxs-lookup"><span data-stu-id="96669-117">Unless it is necessary to have an accurate **RecordCount** as soon as you open a **Recordset**, it's better to wait until you populate the **Recordset** with other portions of code before checking the **RecordCount** property.</span></span>

<span data-ttu-id="96669-118">Как приложение удаляет записи в объекте **набора записей** добавляющий, значение свойства **RecordCount** снижается.</span><span class="sxs-lookup"><span data-stu-id="96669-118">As your application deletes records in a dynaset-type **Recordset** object, the value of the **RecordCount** property decreases.</span></span> <span data-ttu-id="96669-119">Тем не менее удаленные другими пользователями записи не вступят в силу в свойстве **RecordCount** до текущей записи находится в удаленных запись.</span><span class="sxs-lookup"><span data-stu-id="96669-119">However, records deleted by other users aren't reflected by the **RecordCount** property until the current record is positioned to a deleted record.</span></span> <span data-ttu-id="96669-120">При выполнении транзакции, влияющей на значение свойства **RecordCount** и и впоследствии ее откат, свойство **RecordCount** могут не отражать фактическое число оставшихся записей.</span><span class="sxs-lookup"><span data-stu-id="96669-120">If you execute a transaction that affects the **RecordCount** property setting and you subsequently roll back the transaction, the **RecordCount** property won't reflect the actual number of remaining records.</span></span>

<span data-ttu-id="96669-121">Свойство **RecordCount** объекта **набора записей** моментальный снимок – прямого — только — тип или не влияет на изменения в таблицах.</span><span class="sxs-lookup"><span data-stu-id="96669-121">The **RecordCount** property of a snapshot– or forward–only–type **Recordset** object isn't affected by changes in the underlying tables.</span></span>

<span data-ttu-id="96669-122">Объект **TableDef** или **набора записей** с записи не имеет значение свойства **RecordCount** 0.</span><span class="sxs-lookup"><span data-stu-id="96669-122">A **Recordset** or **TableDef** object with no records has a **RecordCount** property setting of 0.</span></span>

<span data-ttu-id="96669-123">С помощью метода **[повторный запрос](recordset2-requery-method-dao.md)** на объект **набора записей** сбрасывает свойство **RecordCount** , как если бы были повторно выполнить запрос.</span><span class="sxs-lookup"><span data-stu-id="96669-123">Using the **[Requery](recordset2-requery-method-dao.md)** method on a **Recordset** object resets the **RecordCount** property just as if the query were re-executed.</span></span>

## <a name="example"></a><span data-ttu-id="96669-124">Пример</span><span class="sxs-lookup"><span data-stu-id="96669-124">Example</span></span>

<span data-ttu-id="96669-125">В этом примере демонстрируется свойство **RecordCount** с использованием разных типов наборов **записей** перед и после их в случае заполнения.</span><span class="sxs-lookup"><span data-stu-id="96669-125">This example demonstrates the **RecordCount** property with different types of **Recordsets** before and after they're populated.</span></span>

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
