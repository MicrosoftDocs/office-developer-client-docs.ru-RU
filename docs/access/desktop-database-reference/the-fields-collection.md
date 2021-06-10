---
title: The Fields Collection
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ce08ac5952151471ce74afd9a8a49600d8e8f633
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314135"
---
# <a name="fields-collection"></a><span data-ttu-id="9489d-102">Коллекция Fields</span><span class="sxs-lookup"><span data-stu-id="9489d-102">Fields collection</span></span>


<span data-ttu-id="9489d-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="9489d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="9489d-104">Коллекция **Fields** — это одна из внутренних коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="9489d-104">The **Fields** collection is one of ADO's intrinsic collections.</span></span> <span data-ttu-id="9489d-105">Коллекция — это упорядоченный набор элементов, которые можно называть единицей.</span><span class="sxs-lookup"><span data-stu-id="9489d-105">A collection is an ordered set of items that can be referred to as a unit.</span></span>

<span data-ttu-id="9489d-106">Коллекция **Fields** содержит объект **Field** для каждого поля (столбца) в **Наборе записей.**</span><span class="sxs-lookup"><span data-stu-id="9489d-106">The **Fields** collection contains a **Field** object for every field (column) in the **Recordset**.</span></span> <span data-ttu-id="9489d-107">Как и все коллекции ADO, он имеет свойства **Count** и **Item,** а также методы **приложения** и **обновления.**</span><span class="sxs-lookup"><span data-stu-id="9489d-107">Like all ADO collections, it has **Count** and **Item** properties, as well as **Append** and **Refresh** methods.</span></span> <span data-ttu-id="9489d-108">Он также имеет **методы CancelUpdate,** **Delete,** **Resync** и **Update,** которые недоступны для других коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="9489d-108">It also has **CancelUpdate**, **Delete**, **Resync**, and **Update** methods, which are not available to other ADO collections.</span></span>

## <a name="examining-the-fields-collection"></a><span data-ttu-id="9489d-109">Изучение коллекции Полей</span><span class="sxs-lookup"><span data-stu-id="9489d-109">Examining the Fields Collection</span></span>

<span data-ttu-id="9489d-110">Рассмотрим **коллекцию Полей** примера **Recordset,** представленную в этой главе.</span><span class="sxs-lookup"><span data-stu-id="9489d-110">Consider the **Fields** collection of the sample **Recordset** introduced in this chapter.</span></span> <span data-ttu-id="9489d-111">Пример **Recordset был** получен из SQL.</span><span class="sxs-lookup"><span data-stu-id="9489d-111">The sample **Recordset** was derived from the SQL statement</span></span>

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

<span data-ttu-id="9489d-112">Таким образом, вы должны обнаружить, что коллекция **Полей Recordset** **содержит** три поля.</span><span class="sxs-lookup"><span data-stu-id="9489d-112">Thus, you should find that the **Recordset** **Fields** collection contains three fields.</span></span>

```vb 
 
'BeginWalkFields 
 Dim objFields As ADODB.Fields 
 
 objRs.Open strSQL, strConnStr, adOpenForwardOnly, adLockReadOnly, adCmdText 
 
 Set objFields = objRs.Fields 
 
 For intLoop = 0 To (objFields.Count - 1) 
 Debug.Print objFields.Item(intLoop).Name 
 Next 
'EndWalkFields 
```

<span data-ttu-id="9489d-113">Этот код просто определяет количество объектов **Field** в коллекции **Fields** с помощью свойства **Count** и циклов через коллекцию, возвращая значение свойства **Name** для каждого объекта **Field.**</span><span class="sxs-lookup"><span data-stu-id="9489d-113">This code simply determines the number of **Field** objects in the **Fields** collection using the **Count** property and loops through the collection, returning the value of the **Name** property for each **Field** object.</span></span> <span data-ttu-id="9489d-114">Для получения сведений **о** поле можно использовать гораздо больше свойств field.</span><span class="sxs-lookup"><span data-stu-id="9489d-114">You can use many more **Field** properties to get information about a field.</span></span> <span data-ttu-id="9489d-115">Дополнительные сведения об запросе **поля** см. в поле [Object](the-field-object.md).</span><span class="sxs-lookup"><span data-stu-id="9489d-115">For more information about querying a **Field**, see [The Field Object](the-field-object.md).</span></span>

## <a name="counting-columns"></a><span data-ttu-id="9489d-116">Подсчет столбцов</span><span class="sxs-lookup"><span data-stu-id="9489d-116">Counting Columns</span></span>

<span data-ttu-id="9489d-117">Как и ожидается, свойство **Count** возвращает фактическое количество объектов **Field** в коллекции **Fields.**</span><span class="sxs-lookup"><span data-stu-id="9489d-117">As you might expect, the **Count** property returns the actual number of **Field** objects in the **Fields** collection.</span></span> <span data-ttu-id="9489d-118">Так как нуминг для членов коллекции начинается с нуля, всегда следует использовать циклы кода, начиная с нулевого члена и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="9489d-118">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="9489d-119">Если вы используете microsoft Visual Basic и хотите проциклить членов коллекции без проверки свойства **Count,** используйте **для каждого...** **Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="9489d-119">If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="9489d-120">Если свойство **Count** нулевое, в коллекции нет объектов.</span><span class="sxs-lookup"><span data-stu-id="9489d-120">If the **Count** property is zero, there are no objects in the collection.</span></span>

## <a name="getting-to-the-field"></a><span data-ttu-id="9489d-121">Как добраться до поля</span><span class="sxs-lookup"><span data-stu-id="9489d-121">Getting to the Field</span></span>

<span data-ttu-id="9489d-122">Как и в любой коллекции ADO, **свойство Item** является свойством коллекции по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9489d-122">As with any ADO collection, the **Item** property is the default property of the collection.</span></span> <span data-ttu-id="9489d-123">Он возвращает отдельный **объект Field,** указанный именем или индексом, переданным ему.</span><span class="sxs-lookup"><span data-stu-id="9489d-123">It returns the individual **Field** object specified by the name or index passed to it.</span></span> <span data-ttu-id="9489d-124">Таким образом, для примера Recordset эквивалентны следующие **утверждения:**</span><span class="sxs-lookup"><span data-stu-id="9489d-124">Therefore, the following statements are equivalent for the sample **Recordset**:</span></span>

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

<span data-ttu-id="9489d-125">Если эти методы эквивалентны, что лучше всего?</span><span class="sxs-lookup"><span data-stu-id="9489d-125">If these methods are equivalent, which is best?</span></span> <span data-ttu-id="9489d-126">У всех по-разному.</span><span class="sxs-lookup"><span data-stu-id="9489d-126">It depends.</span></span> <span data-ttu-id="9489d-127">Использование индекса для получения **поля** из коллекции выполняется  быстрее, так как оно напрямую выполняет просмотр поля без выполнения строки.</span><span class="sxs-lookup"><span data-stu-id="9489d-127">Using an index to retrieve a **Field** from the collection is faster because it accesses the **Field** directly without having to perform a string lookup.</span></span> <span data-ttu-id="9489d-128">С другой стороны, необходимо  знать порядок полей в коллекции, и если  порядок изменяется, ссылку на индекс Поля необходимо изменить везде, где это происходит.</span><span class="sxs-lookup"><span data-stu-id="9489d-128">On the other hand, the order of **Fields** within the collection must be known, and if the order changes, the reference to the **Field's** index will have to be changed wherever it occurs.</span></span> <span data-ttu-id="9489d-129">Хотя немного медленнее, использование имени **Поля** является более гибким, так как оно не зависит от порядка **полей** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="9489d-129">Although slightly slower, using the name of the **Field** is more flexible because it doesn't depend on the order of the **Fields** in the collection.</span></span>

## <a name="using-the-refresh-method"></a><span data-ttu-id="9489d-130">Использование метода обновления</span><span class="sxs-lookup"><span data-stu-id="9489d-130">Using the Refresh Method</span></span>

<span data-ttu-id="9489d-131">В отличие от некоторых других коллекций ADO, использование метода **Обновления** в коллекции **Fields** не оказывает видимого эффекта.</span><span class="sxs-lookup"><span data-stu-id="9489d-131">Unlike some other ADO collections, using the **Refresh** method on the **Fields** collection has no visible effect.</span></span> <span data-ttu-id="9489d-132">Чтобы получить изменения из основной структуры базы данных, необходимо использовать метод **Requery** или если объект **Recordset** не поддерживает закладки, метод **MoveFirst,** который приведет к повторному выполнению команды в отношении поставщика.</span><span class="sxs-lookup"><span data-stu-id="9489d-132">To retrieve changes from the underlying database structure, you must use either the **Requery** method, or if the **Recordset** object does not support bookmarks, the **MoveFirst** method, which will cause the command to be executed against the provider again.</span></span>

## <a name="adding-fields-to-a-recordset"></a><span data-ttu-id="9489d-133">Добавление полей в набор recordset</span><span class="sxs-lookup"><span data-stu-id="9489d-133">Adding Fields to a Recordset</span></span>

<span data-ttu-id="9489d-134">Метод **Append** используется для добавления полей в **Набор записей.**</span><span class="sxs-lookup"><span data-stu-id="9489d-134">The **Append** method is used to add fields to a **Recordset**.</span></span>

<span data-ttu-id="9489d-135">Метод **Append** можно использовать для того, чтобы программным образом издать **набор записей,** не открывая подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="9489d-135">You can use the **Append** method to fabricate a **Recordset** programmatically without opening a connection to a data source.</span></span> <span data-ttu-id="9489d-136">Ошибка при запуске произойдет, если метод **Append** вызван в  коллекцию **Полей** открытого набора записей или в наборе записей, где задано свойство  **ActiveConnection.**</span><span class="sxs-lookup"><span data-stu-id="9489d-136">A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset** or on a **Recordset** where the **ActiveConnection** property has been set.</span></span> <span data-ttu-id="9489d-137">Поля можно примедить только к **набору записей,** который еще не открыт и еще не подключен к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="9489d-137">You can append fields only to a **Recordset** that is not open and has not yet been connected to a data source.</span></span> <span data-ttu-id="9489d-138">Однако, чтобы указать значения для недавно добавленных полей, сначала необходимо открыть **Набор** записей.</span><span class="sxs-lookup"><span data-stu-id="9489d-138">However, to specify values for the newly appended **Fields**, the **Recordset** must first be opened.</span></span>

<span data-ttu-id="9489d-139">Разработчикам часто требуется место для временного хранения некоторых данных или требуется, чтобы некоторые данные действовали так, как будто они поступили с сервера, чтобы они могли участвовать в привязке данных в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="9489d-139">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface.</span></span> <span data-ttu-id="9489d-140">ADO (совместно с службой [Microsoft Cursor для OLE DB)](microsoft-cursor-service-for-ole-db-ado-service-component.md)позволяет разработчику создать пустой объект **Recordset,** указав сведения о столбцах и позвонив **в Open.**</span><span class="sxs-lookup"><span data-stu-id="9489d-140">ADO (in conjunction with the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) enables the developer to build an empty **Recordset** object by specifying column information and calling **Open**.</span></span> <span data-ttu-id="9489d-141">В следующем примере к новому объекту **Recordset** примыкают три новых поля.</span><span class="sxs-lookup"><span data-stu-id="9489d-141">In the following example, three new fields are appended to a new **Recordset** object.</span></span> <span data-ttu-id="9489d-142">Затем **открывается Набор** записей, добавляются две новые записи, и **запись** сохраняется в файле.</span><span class="sxs-lookup"><span data-stu-id="9489d-142">Then the **Recordset** is opened, two new records are added, and the **Recordset** is persisted to a file.</span></span> <span data-ttu-id="9489d-143">(Дополнительные сведения о **сохраняемости Recordset** см. в главе [5: Обновление и сохранение данных.)](chapter-5-updating-and-persisting-data.md)</span><span class="sxs-lookup"><span data-stu-id="9489d-143">(For more information about **Recordset** persistence, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).)</span></span>

```vb 
 
 'BeginFabricate 
 Dim objRs As New ADODB.Recordset 
 
 With objRs.Fields 
 .Append "StudentID", adChar, 11, adFldUpdatable 
 .Append "FullName", adVarChar, 50, adFldUpdatable 
 .Append "PhoneNmbr", adVarChar, 20, adFldUpdatable 
 End With 
 
 With objRs 
 .Open 
 
 .AddNew 
 .Fields(0) = "123-45-6789" 
 .Fields(1) = "John Doe" 
 .Fields(2) = "(425) 555-5555" 
 .Update 
 
 .AddNew 
 .Fields(0) = "123-45-6780" 
 .Fields(1) = "Jane Doe" 
 .Fields(2) = "(615) 555-1212" 
 .Update 
 End With 
 
 objRs.Save App.Path & "\FabriTest.adtg", adPersistADTG 
 
 objRs.Close 
 'EndFabricate 
```

<span data-ttu-id="9489d-144">Использование метода **приложения Fields** **отличается** между объектом **Recordset** и **объектом Record.**</span><span class="sxs-lookup"><span data-stu-id="9489d-144">The usage of the **Fields** **Append** method differs between the **Recordset** object and the **Record** object.</span></span> <span data-ttu-id="9489d-145">Дополнительные сведения об объекте **Запись** см. [в главе 10: Записи и Потоки.](chapter-10-records-and-streams.md)</span><span class="sxs-lookup"><span data-stu-id="9489d-145">For more information about the **Record** object, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

