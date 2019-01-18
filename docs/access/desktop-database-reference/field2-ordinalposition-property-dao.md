---
title: Свойство Field2.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 55d89611-ad07-990d-fc33-f81d59472430
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194179(v=office.15)
ms:contentKeyID: 48544937
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052899
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 26d37bfda90f2ab4e2627b936d3cf37b5be811d5
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/18/2019
ms.locfileid: "28726332"
---
# <a name="field2ordinalposition-property-dao"></a><span data-ttu-id="531f5-102">Свойство Field2.OrdinalPosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="531f5-102">Field2.OrdinalPosition property (DAO)</span></span>


<span data-ttu-id="531f5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="531f5-103">**Applies to**: Access 2013, Office 2013</span></span>


<span data-ttu-id="531f5-104">Задает или возвращает относительное положение объекта **поле2** в коллекции **[полей](fields-collection-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="531f5-104">Sets or returns the relative position of a **Field2** object within a **[Fields](fields-collection-dao.md)** collection.</span></span> <span data-ttu-id="531f5-105">.</span><span class="sxs-lookup"><span data-stu-id="531f5-105"></span></span>

## <a name="syntax"></a><span data-ttu-id="531f5-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="531f5-106">Syntax</span></span>

<span data-ttu-id="531f5-107">*выражение* . OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="531f5-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="531f5-108">*выражение* Переменная, которая представляет собой объект- **поле2** .</span><span class="sxs-lookup"><span data-stu-id="531f5-108">*expression* A variable that represents a **Field2** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="531f5-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="531f5-109">Remarks</span></span>

<span data-ttu-id="531f5-110">Для объекта еще не добавляется в конец коллекции **полей** это свойство соответствует чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="531f5-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="531f5-111">Значение по умолчанию равно 0.</span><span class="sxs-lookup"><span data-stu-id="531f5-111">The default is 0.</span></span>

<span data-ttu-id="531f5-112">Доступность свойство **OrdinalPosition** зависит от объекта, который содержит коллекцию **полей** , как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="531f5-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="531f5-113">Если принадлежит коллекции полей</span><span class="sxs-lookup"><span data-stu-id="531f5-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="531f5-114">Затем — OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="531f5-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="531f5-115">Объект <strong>индекса</strong></span><span class="sxs-lookup"><span data-stu-id="531f5-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="531f5-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="531f5-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="531f5-117">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="531f5-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="531f5-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="531f5-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="531f5-119">Объект <strong>набора записей</strong></span><span class="sxs-lookup"><span data-stu-id="531f5-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="531f5-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="531f5-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="531f5-121"><strong>Отношения</strong> объектов</span><span class="sxs-lookup"><span data-stu-id="531f5-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="531f5-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="531f5-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="531f5-123">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="531f5-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="531f5-124">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="531f5-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="531f5-125">Как правило порядковый номер объекта, который необходимо добавить в семейство сайтов зависит от порядка, в котором необходимо добавить объект.</span><span class="sxs-lookup"><span data-stu-id="531f5-125">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object.</span></span> <span data-ttu-id="531f5-126">Первый объект добавленный в начале (0), второй добавленный объект является второй позиции (1) и т. д.</span><span class="sxs-lookup"><span data-stu-id="531f5-126">The first appended object is in the first position (0), the second appended object is in the second position (1), and so on.</span></span> <span data-ttu-id="531f5-127">Последний добавленный объект находится в порядковый номер count – 1, где число — это число объектов в коллекции, указанный параметром свойство **[Count](containers-count-property-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="531f5-127">The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="531f5-128">Свойство **OrdinalPosition** используется для указания порядковый для новых объектов **поле2** , отличается от порядка, в котором необходимо добавить эти объекты в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="531f5-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field2** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="531f5-129">Это позволяет указать порядок полей для таблиц, запросов и наборов записей при использовании в приложении.</span><span class="sxs-lookup"><span data-stu-id="531f5-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="531f5-130">Например, заказа, возвращенные поля в ВЫБЕРИТЕ \* запроса определяется с текущими значениями свойств **OrdinalPosition** .</span><span class="sxs-lookup"><span data-stu-id="531f5-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="531f5-131">Без возможности восстановления может сбросить порядок, в котором поля возвращаются в наборах записей путем установки свойства **OrdinalPosition** до любого положительного целого числа.</span><span class="sxs-lookup"><span data-stu-id="531f5-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="531f5-132">Два или несколько объектов **поле2** в одном семействе может иметь такое же значение свойства **OrdinalPosition** , в противном случае они будут упорядочены в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="531f5-132">Two or more **Field2** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically.</span></span> <span data-ttu-id="531f5-133">Например при наличии поле с именем срок хранения в значение 4 и задать второе поле с именем вес 4, вес возвращается после срока хранения.</span><span class="sxs-lookup"><span data-stu-id="531f5-133">For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="531f5-134">Можно указать номер, который больше, чем количество полей минус 1.</span><span class="sxs-lookup"><span data-stu-id="531f5-134">You can specify a number that is greater than the number of fields minus 1.</span></span> <span data-ttu-id="531f5-135">Поля будут возвращены в порядке относительно наибольшее число.</span><span class="sxs-lookup"><span data-stu-id="531f5-135">The field will be returned in an order relative to the largest number.</span></span> <span data-ttu-id="531f5-136">Например, если значение поля **OrdinalPosition** 20 (и имеется только 5 полей) и установки свойства **OrdinalPosition** для двух других полей на 10 и 30, соответственно, возвращаются поля значение 20 между полями, равным 10 и 30.</span><span class="sxs-lookup"><span data-stu-id="531f5-136">For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>


> [!NOTE]
> <span data-ttu-id="531f5-137">Даже в том случае, если коллекции **полей** объекта **[TableDef](tabledef-object-dao.md)** не обновлялись порядок полей в **[набор записей](recordset-object-dao.md)** , открывается из **TableDef** будет отражать данные **OrdinalPosition** объекта **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="531f5-137">Even if the **Fields** collection of a **[TableDef](tabledef-object-dao.md)** object has not been refreshed, the field order in a **[Recordset](recordset-object-dao.md)** opened from the **TableDef** will reflect the **OrdinalPosition** data of the **TableDef** object.</span></span> <span data-ttu-id="531f5-138">Тип таблицы **записей** будут иметь те же данные **OrdinalPosition** , как и базовая таблица, но любой другой тип **набора записей** будут иметь новые **OrdinalPosition** данные (начиная с 0), следуйте порядке, определяется \*\* OrdinalPosition\*\* данных **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="531f5-138">A table-type **Recordset** will have the same **OrdinalPosition** data as the underlying table, but any other type of **Recordset** will have new **OrdinalPosition** data (starting with 0) that follow the order determined by the **OrdinalPosition** data of the **TableDef**.</span></span>



## <a name="example"></a><span data-ttu-id="531f5-139">Пример</span><span class="sxs-lookup"><span data-stu-id="531f5-139">Example</span></span>

<span data-ttu-id="531f5-140">В этом примере изменяется значения свойства **OrdinalPosition** в сотрудников **TableDef** для управления порядком **поле2** в результирующий **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="531f5-140">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field2** order in a resulting **Recordset**.</span></span> <span data-ttu-id="531f5-141">Задав **OrdinalPosition** всех **полей** значение 1, любой результирующий **набор записей** будет упорядочивать **полей** в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="531f5-141">By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically.</span></span> <span data-ttu-id="531f5-142">Обратите внимание на то, что не соответствуют значениям в **TableDef** **OrdinalPosition** значения в **набор записей** , но просто отражают конечный результат изменений **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="531f5-142">Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field2 
     Dim rstEmployees As Recordset 
     
     Set dbsNorthwind = OpenDatabase("Northwind.mdb") 
     Set tdfEmployees = dbsNorthwind.TableDefs("Employees") 
     
     With tdfEmployees 
     ' Display and store original OrdinalPosition data. 
     Debug.Print _ 
     "Original OrdinalPosition data in TableDef." 
     ReDim aintPosition(0 To .Fields.Count - 1) As Integer 
     ReDim astrFieldName(0 To .Fields.Count - 1) As String 
     For intTemp = 0 To .Fields.Count - 1 
     aintPosition(intTemp) = _ 
     .Fields(intTemp).OrdinalPosition 
     astrFieldName(intTemp) = .Fields(intTemp).Name 
     Debug.Print , aintPosition(intTemp), _ 
     astrFieldName(intTemp) 
     Next intTemp 
     
     ' Change OrdinalPosition data. 
     For Each fldTemp In .Fields 
     fldTemp.OrdinalPosition = 1 
     Next fldTemp 
     
     ' Open new Recordset object to show how the 
     ' OrdinalPosition data has affected the record order. 
     Debug.Print _ 
     "OrdinalPosition data from resulting Recordset." 
     Set rstEmployees = dbsNorthwind.OpenRecordset( _ 
     "SELECT * FROM Employees") 
     For Each fldTemp In rstEmployees.Fields 
     Debug.Print , fldTemp.OrdinalPosition, fldTemp.Name 
     Next fldTemp 
     rstEmployees.Close 
     
     ' Restore original OrdinalPosition data because this is 
     ' a demonstration. 
     For intTemp = 0 To .Fields.Count - 1 
     .Fields(astrFieldName(intTemp)).OrdinalPosition = _ 
     aintPosition(intTemp) 
     Next intTemp 
     
     End With 
     
     dbsNorthwind.Close 
     
    End Sub
```
