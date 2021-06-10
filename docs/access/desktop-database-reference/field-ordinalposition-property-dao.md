---
title: Свойство Field.OrdinalPosition (DAO)
TOCTitle: OrdinalPosition Property
ms:assetid: 07f2344e-2a72-33d8-be47-b37d76ecca47
ms:mtpsurl: https://msdn.microsoft.com/library/Ff845002(v=office.15)
ms:contentKeyID: 48543088
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d45f0362831d91b83b3a2449affbbfb5ac2b4e51
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293037"
---
# <a name="fieldordinalposition-property-dao"></a><span data-ttu-id="86d0e-102">Свойство Field.OrdinalPosition (DAO)</span><span class="sxs-lookup"><span data-stu-id="86d0e-102">Field.OrdinalPosition property (DAO)</span></span>


<span data-ttu-id="86d0e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="86d0e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="86d0e-104">Задает или возвращает относительное положение объекта **[Field](field-object-dao.md)** в коллекции **[Fields.](fields-collection-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="86d0e-104">Sets or returns the relative position of a **[Field](field-object-dao.md)** object within a **[Fields](fields-collection-dao.md)** collection.</span></span> <span data-ttu-id="86d0e-105">.</span><span class="sxs-lookup"><span data-stu-id="86d0e-105">.</span></span>

## <a name="syntax"></a><span data-ttu-id="86d0e-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="86d0e-106">Syntax</span></span>

<span data-ttu-id="86d0e-107">*выражения* . OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="86d0e-107">*expression* .OrdinalPosition</span></span>

<span data-ttu-id="86d0e-108">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="86d0e-108">*expression* A variable that represents a **Field** object.</span></span>

## <a name="remarks"></a><span data-ttu-id="86d0e-109">Примечания</span><span class="sxs-lookup"><span data-stu-id="86d0e-109">Remarks</span></span>

<span data-ttu-id="86d0e-110">Для объекта, еще не примыкаемого к коллекции **Fields,** это свойство является чтением и написанием.</span><span class="sxs-lookup"><span data-stu-id="86d0e-110">For an object not yet appended to the **Fields** collection, this property is read/write.</span></span>

<span data-ttu-id="86d0e-111">По умолчанию используется значение 0.</span><span class="sxs-lookup"><span data-stu-id="86d0e-111">The default is 0.</span></span>

<span data-ttu-id="86d0e-112">Доступность свойства **OrdinalPosition** зависит от объекта, который содержит коллекцию **Полей,** как показано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="86d0e-112">The availability of the **OrdinalPosition** property depends on the object that contains the **Fields** collection, as shown in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="86d0e-113">Если коллекция Fields принадлежит</span><span class="sxs-lookup"><span data-stu-id="86d0e-113">If the Fields collection belongs to a</span></span></p></th>
<th><p><span data-ttu-id="86d0e-114">Затем OrdinalPosition</span><span class="sxs-lookup"><span data-stu-id="86d0e-114">Then OrdinalPosition is</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="86d0e-115">Объект <strong>Index</strong></span><span class="sxs-lookup"><span data-stu-id="86d0e-115"><strong>Index</strong> object</span></span></p></td>
<td><p><span data-ttu-id="86d0e-116">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="86d0e-116">Not supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86d0e-117">Объект <strong>QueryDef</strong></span><span class="sxs-lookup"><span data-stu-id="86d0e-117"><strong>QueryDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="86d0e-118">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="86d0e-118">Read-only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86d0e-119">Объект <strong>Recordset</strong></span><span class="sxs-lookup"><span data-stu-id="86d0e-119"><strong>Recordset</strong> object</span></span></p></td>
<td><p><span data-ttu-id="86d0e-120">Только для чтения</span><span class="sxs-lookup"><span data-stu-id="86d0e-120">Read-only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="86d0e-121">Объект <strong>Relation</strong></span><span class="sxs-lookup"><span data-stu-id="86d0e-121"><strong>Relation</strong> object</span></span></p></td>
<td><p><span data-ttu-id="86d0e-122">Не поддерживается</span><span class="sxs-lookup"><span data-stu-id="86d0e-122">Not supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="86d0e-123">Объект <strong>TableDef</strong></span><span class="sxs-lookup"><span data-stu-id="86d0e-123"><strong>TableDef</strong> object</span></span></p></td>
<td><p><span data-ttu-id="86d0e-124">Чтение и запись</span><span class="sxs-lookup"><span data-stu-id="86d0e-124">Read/write</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="86d0e-125">Как правило, расположение объекта, который вы примыкаете к коллекции, зависит от порядка, в котором вы привносим объект.</span><span class="sxs-lookup"><span data-stu-id="86d0e-125">Generally, the ordinal position of an object that you append to a collection depends on the order in which you append the object.</span></span> <span data-ttu-id="86d0e-126">Первый примыкает к объекту в первой позиции (0), второй — во второй позиции (1) и так далее.</span><span class="sxs-lookup"><span data-stu-id="86d0e-126">The first appended object is in the first position (0), the second appended object is in the second position (1), and so on.</span></span> <span data-ttu-id="86d0e-127">Последний примыкает к объекту в порядковом расположении — 1, где количество объектов в коллекции определяется параметром **[свойства Count.](containers-count-property-dao.md)**</span><span class="sxs-lookup"><span data-stu-id="86d0e-127">The last appended object is in ordinal position count – 1, where count is the number of objects in the collection as specified by the **[Count](containers-count-property-dao.md)** property setting.</span></span>

<span data-ttu-id="86d0e-128">Свойство **OrdinalPosition** можно использовать для указания расположения для новых объектов **Field,** которое отличается от порядка, в котором вы привносимы эти объекты в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="86d0e-128">You can use the **OrdinalPosition** property to specify an ordinal position for new **Field** objects that differs from the order in which you append those objects to a collection.</span></span> <span data-ttu-id="86d0e-129">Это позволяет указать порядок поля для таблиц, запросов и записей при их использовании в приложении.</span><span class="sxs-lookup"><span data-stu-id="86d0e-129">This enables you to specify a field order for your tables, queries, and recordsets when you use them in an application.</span></span> <span data-ttu-id="86d0e-130">Например, порядок возврата полей в запросе SELECT определяется текущими значениями \* свойств **OrdinalPosition.**</span><span class="sxs-lookup"><span data-stu-id="86d0e-130">For example, the order in which fields are returned in a SELECT \* query is determined by the current **OrdinalPosition** property values.</span></span>

<span data-ttu-id="86d0e-131">Вы можете окончательно сбросить порядок, в котором поля возвращаются в записях, установив свойство **OrdinalPosition** для любого положительного integer.</span><span class="sxs-lookup"><span data-stu-id="86d0e-131">You can permanently reset the order in which fields are returned in recordsets by setting the **OrdinalPosition** property to any positive integer.</span></span>

<span data-ttu-id="86d0e-132">Два или несколько **объектов Field** в одной коллекции могут иметь одно и то же значение **свойства OrdinalPosition,** в этом случае они будут упорядочены в алфавитном порядке.</span><span class="sxs-lookup"><span data-stu-id="86d0e-132">Two or more **Field** objects in the same collection can have the same **OrdinalPosition** property value, in which case they will be ordered alphabetically.</span></span> <span data-ttu-id="86d0e-133">Например, если у вас есть поле с именем Age set to 4, а второе поле с именем Weight — 4, вес возвращается после Age.</span><span class="sxs-lookup"><span data-stu-id="86d0e-133">For example, if you have a field named Age set to 4 and you set a second field named Weight to 4, Weight is returned after Age.</span></span>

<span data-ttu-id="86d0e-134">Можно указать номер, который превышает число полей минус 1.</span><span class="sxs-lookup"><span data-stu-id="86d0e-134">You can specify a number that is greater than the number of fields minus 1.</span></span> <span data-ttu-id="86d0e-135">Поле будет возвращено в порядке относительно наибольшего числа.</span><span class="sxs-lookup"><span data-stu-id="86d0e-135">The field will be returned in an order relative to the largest number.</span></span> <span data-ttu-id="86d0e-136">Например, если вы установите свойство **OrdinalPosition** поля до 20 (а есть только 5 полей) и задали свойство **OrdinalPosition** для двух других полей соответственно 10 и 30, поле, замещеное до 20, возвращается между полями, за набором 10 и 30.</span><span class="sxs-lookup"><span data-stu-id="86d0e-136">For example, if you set a field's **OrdinalPosition** property to 20 (and there are only 5 fields) and you've set the **OrdinalPosition** property for two other fields to 10 and 30, respectively, the field set to 20 is returned between the fields set to 10 and 30.</span></span>

> [!NOTE]
> <span data-ttu-id="86d0e-137">Даже если коллекция **Fields** [tableDef](tabledef-object-dao.md) не была обновлена, порядок поля в наборе записей, открываемом в **TableDef,** будет отражать данные **OrdinalPosition** объекта **TableDef.** [](recordset-object-dao.md)</span><span class="sxs-lookup"><span data-stu-id="86d0e-137">Even if the **Fields** collection of a [TableDef](tabledef-object-dao.md) has not been refreshed, the field order in a [Recordset](recordset-object-dao.md) opened from the **TableDef** will reflect the **OrdinalPosition** data of the **TableDef** object.</span></span> <span data-ttu-id="86d0e-138">Набор записей  типа таблицы будет иметь те же данные **OrdinalPosition,** что и в исходной таблице, но любой другой тип **Recordset** будет иметь новые данные **OrdinalPosition** (начиная с 0), которые следуют порядку, определенному **данными OrdinalPosition** **tableDef**.</span><span class="sxs-lookup"><span data-stu-id="86d0e-138">A table-type **Recordset** will have the same **OrdinalPosition** data as the underlying table, but any other type of **Recordset** will have new **OrdinalPosition** data (starting with 0) that follow the order determined by the **OrdinalPosition** data of the **TableDef**.</span></span>

## <a name="example"></a><span data-ttu-id="86d0e-139">Пример</span><span class="sxs-lookup"><span data-stu-id="86d0e-139">Example</span></span>

<span data-ttu-id="86d0e-140">В этом примере изменяется значение свойств **OrdinalPosition** в **TableDef** employees, чтобы контролировать порядок поля в итоговом **наборе записей.** </span><span class="sxs-lookup"><span data-stu-id="86d0e-140">This example changes the **OrdinalPosition** property values in the Employees **TableDef** in order to control the **Field** order in a resulting **Recordset**.</span></span> <span data-ttu-id="86d0e-141">Установив **OrdinalPosition** всех полей до 1, любой результат **recordset** будет заказать **Поля в** алфавитном порядке. </span><span class="sxs-lookup"><span data-stu-id="86d0e-141">By setting the **OrdinalPosition** of all the **Fields** to 1, any resulting **Recordset** will order the **Fields** alphabetically.</span></span> <span data-ttu-id="86d0e-142">Обратите внимание, что значения **OrdinalPosition** в **Наборе** записей не соответствуют значениям **в TableDef,** а просто отражают конечный результат изменений **TableDef.**</span><span class="sxs-lookup"><span data-stu-id="86d0e-142">Note that the **OrdinalPosition** values in the **Recordset** don't match the values in the **TableDef**, but simply reflect the end result of the **TableDef** changes.</span></span>

```vb
    Sub OrdinalPositionX() 
     
     Dim dbsNorthwind As Database 
     Dim tdfEmployees As TableDef 
     Dim aintPosition() As Integer 
     Dim astrFieldName() As String 
     Dim intTemp As Integer 
     Dim fldTemp As Field 
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
