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
# <a name="fields-collection"></a><span data-ttu-id="a8dae-102">Коллекция Fields</span><span class="sxs-lookup"><span data-stu-id="a8dae-102">Fields collection</span></span>


<span data-ttu-id="a8dae-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="a8dae-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a8dae-104">Коллекция **Fields** является одной из встроенных коллекций ADO.</span><span class="sxs-lookup"><span data-stu-id="a8dae-104">The **Fields** collection is one of ADO's intrinsic collections.</span></span> <span data-ttu-id="a8dae-105">Коллекция — это упорядоченный набор элементов, на которые можно ссылаться как на единое целое.</span><span class="sxs-lookup"><span data-stu-id="a8dae-105">A collection is an ordered set of items that can be referred to as a unit.</span></span>

<span data-ttu-id="a8dae-106">Коллекция **Fields** содержит объект **field** для каждого поля (столбца) в **наборе записей**.</span><span class="sxs-lookup"><span data-stu-id="a8dae-106">The **Fields** collection contains a **Field** object for every field (column) in the **Recordset**.</span></span> <span data-ttu-id="a8dae-107">Как и в случае со всеми коллекциями ADO, у него есть свойства **Count** и **Item** , а также методы **append** и **Refresh** .</span><span class="sxs-lookup"><span data-stu-id="a8dae-107">Like all ADO collections, it has **Count** and **Item** properties, as well as **Append** and **Refresh** methods.</span></span> <span data-ttu-id="a8dae-108">Кроме того, у него есть методы **CancelUpdate**, **Delete**, **Resync**и **Update** , недоступные другим коллекциям ADO.</span><span class="sxs-lookup"><span data-stu-id="a8dae-108">It also has **CancelUpdate**, **Delete**, **Resync**, and **Update** methods, which are not available to other ADO collections.</span></span>

## <a name="examining-the-fields-collection"></a><span data-ttu-id="a8dae-109">Анализ коллекции Fields</span><span class="sxs-lookup"><span data-stu-id="a8dae-109">Examining the Fields Collection</span></span>

<span data-ttu-id="a8dae-110">Рассмотрим коллекцию **Fields** примера **Recordset** , представленную в этой главе.</span><span class="sxs-lookup"><span data-stu-id="a8dae-110">Consider the **Fields** collection of the sample **Recordset** introduced in this chapter.</span></span> <span data-ttu-id="a8dae-111">Пример **набора записей** получен из оператора SQL</span><span class="sxs-lookup"><span data-stu-id="a8dae-111">The sample **Recordset** was derived from the SQL statement</span></span>

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

<span data-ttu-id="a8dae-112">Таким образом, коллекция **Fields** **набора записей** содержит три поля.</span><span class="sxs-lookup"><span data-stu-id="a8dae-112">Thus, you should find that the **Recordset** **Fields** collection contains three fields.</span></span>

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

<span data-ttu-id="a8dae-113">Этот код просто определяет количество объектов **field** в коллекции **Fields** с помощью свойства **Count** и выполняет циклы по коллекции, возвращая значение свойства **Name** для каждого объекта **field** .</span><span class="sxs-lookup"><span data-stu-id="a8dae-113">This code simply determines the number of **Field** objects in the **Fields** collection using the **Count** property and loops through the collection, returning the value of the **Name** property for each **Field** object.</span></span> <span data-ttu-id="a8dae-114">Вы можете использовать множество дополнительных свойств **полей** для получения сведений о поле.</span><span class="sxs-lookup"><span data-stu-id="a8dae-114">You can use many more **Field** properties to get information about a field.</span></span> <span data-ttu-id="a8dae-115">Более подробную информацию о запросе **поля**можно узнать [в объекте Field](the-field-object.md).</span><span class="sxs-lookup"><span data-stu-id="a8dae-115">For more information about querying a **Field**, see [The Field Object](the-field-object.md).</span></span>

## <a name="counting-columns"></a><span data-ttu-id="a8dae-116">Подсчет столбцов</span><span class="sxs-lookup"><span data-stu-id="a8dae-116">Counting Columns</span></span>

<span data-ttu-id="a8dae-117">Как можно ожидать, свойство **Count** возвращает фактическое число объектов **field** в коллекции **Fields** .</span><span class="sxs-lookup"><span data-stu-id="a8dae-117">As you might expect, the **Count** property returns the actual number of **Field** objects in the **Fields** collection.</span></span> <span data-ttu-id="a8dae-118">Так как нумерация элементов коллекции начинается с нуля, всегда следует всегда кодировать циклы, начиная с нулевого элемента и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="a8dae-118">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="a8dae-119">Если вы используете Microsoft Visual Basic и хотите перебрать элементы коллекции, не проверяя свойство **Count** , используйте оператор **for** **Each... Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="a8dae-119">If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="a8dae-120">Если свойство **Count** равно нулю, в коллекции отсутствуют объекты.</span><span class="sxs-lookup"><span data-stu-id="a8dae-120">If the **Count** property is zero, there are no objects in the collection.</span></span>

## <a name="getting-to-the-field"></a><span data-ttu-id="a8dae-121">Обращение к полю</span><span class="sxs-lookup"><span data-stu-id="a8dae-121">Getting to the Field</span></span>

<span data-ttu-id="a8dae-122">Как и в случае с любой коллекцией ADO, свойство **Item** является свойством по умолчанию для коллекции.</span><span class="sxs-lookup"><span data-stu-id="a8dae-122">As with any ADO collection, the **Item** property is the default property of the collection.</span></span> <span data-ttu-id="a8dae-123">Он возвращает отдельный объект **field** , заданный именем или индексом, переданным ему.</span><span class="sxs-lookup"><span data-stu-id="a8dae-123">It returns the individual **Field** object specified by the name or index passed to it.</span></span> <span data-ttu-id="a8dae-124">Таким образом, следующие операторы эквивалентны для примера **Recordset**:</span><span class="sxs-lookup"><span data-stu-id="a8dae-124">Therefore, the following statements are equivalent for the sample **Recordset**:</span></span>

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

<span data-ttu-id="a8dae-125">Если эти методы являются эквивалентными, что лучше?</span><span class="sxs-lookup"><span data-stu-id="a8dae-125">If these methods are equivalent, which is best?</span></span> <span data-ttu-id="a8dae-126">У всех по-разному.</span><span class="sxs-lookup"><span data-stu-id="a8dae-126">It depends.</span></span> <span data-ttu-id="a8dae-127">Использование индекса для извлечения **поля** из коллекции выполняется быстрее, так как он получает доступ к **полю** напрямую без необходимости выполнять поиск строки.</span><span class="sxs-lookup"><span data-stu-id="a8dae-127">Using an index to retrieve a **Field** from the collection is faster because it accesses the **Field** directly without having to perform a string lookup.</span></span> <span data-ttu-id="a8dae-128">С другой стороны, порядок **полей** в коллекции должен быть известен, и если порядок изменяется, то ссылка на индекс **поля** будет изменяться везде, где это происходит.</span><span class="sxs-lookup"><span data-stu-id="a8dae-128">On the other hand, the order of **Fields** within the collection must be known, and if the order changes, the reference to the **Field's** index will have to be changed wherever it occurs.</span></span> <span data-ttu-id="a8dae-129">Хотя несколько медленнее, использование имени **поля** является более гибким, так как оно не зависит от порядка **полей** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="a8dae-129">Although slightly slower, using the name of the **Field** is more flexible because it doesn't depend on the order of the **Fields** in the collection.</span></span>

## <a name="using-the-refresh-method"></a><span data-ttu-id="a8dae-130">Использование метода Refresh</span><span class="sxs-lookup"><span data-stu-id="a8dae-130">Using the Refresh Method</span></span>

<span data-ttu-id="a8dae-131">В отличие от других коллекций ADO, использование метода **Refresh** в коллекции **Fields** не оказывает никакого действия.</span><span class="sxs-lookup"><span data-stu-id="a8dae-131">Unlike some other ADO collections, using the **Refresh** method on the **Fields** collection has no visible effect.</span></span> <span data-ttu-id="a8dae-132">Чтобы получить изменения из базовой структуры базы данных, необходимо использовать метод **Requery** или, если объект **Recordset** не поддерживает закладки, метод **MoveFirst** , который будет приводить к повторному выполнению команды для поставщика.</span><span class="sxs-lookup"><span data-stu-id="a8dae-132">To retrieve changes from the underlying database structure, you must use either the **Requery** method, or if the **Recordset** object does not support bookmarks, the **MoveFirst** method, which will cause the command to be executed against the provider again.</span></span>

## <a name="adding-fields-to-a-recordset"></a><span data-ttu-id="a8dae-133">Добавление полей в набор записей</span><span class="sxs-lookup"><span data-stu-id="a8dae-133">Adding Fields to a Recordset</span></span>

<span data-ttu-id="a8dae-134">Метод **append** используется для добавления полей в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="a8dae-134">The **Append** method is used to add fields to a **Recordset**.</span></span>

<span data-ttu-id="a8dae-135">Метод **append** можно использовать для программного собственного **набора записей** без открытия подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="a8dae-135">You can use the **Append** method to fabricate a **Recordset** programmatically without opening a connection to a data source.</span></span> <span data-ttu-id="a8dae-136">При вызове метода **append** для коллекции **Fields** открытого **набора записей** или для объекта **Recordset** , где было задано свойство **ActiveConnection** , возникает ошибка времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="a8dae-136">A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset** or on a **Recordset** where the **ActiveConnection** property has been set.</span></span> <span data-ttu-id="a8dae-137">Вы можете добавлять поля только к **набору записей** , который не открыт и еще не подключен к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="a8dae-137">You can append fields only to a **Recordset** that is not open and has not yet been connected to a data source.</span></span> <span data-ttu-id="a8dae-138">Тем не менее, чтобы указать значения для вновь добавленных **полей**, сначала необходимо открыть **набор записей** .</span><span class="sxs-lookup"><span data-stu-id="a8dae-138">However, to specify values for the newly appended **Fields**, the **Recordset** must first be opened.</span></span>

<span data-ttu-id="a8dae-139">Разработчикам часто требуется место для временного хранения некоторых данных или необходимо, чтобы некоторые данные действовали так, как если бы они поступили с сервера, чтобы он мог участвовать в привязке данных в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="a8dae-139">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface.</span></span> <span data-ttu-id="a8dae-140">ADO (в сочетании со [службой Microsoft Cursor Cursor for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) позволяет разработчику создать пустой объект **Recordset** , указав сведения о столбцах и вызове **Open**.</span><span class="sxs-lookup"><span data-stu-id="a8dae-140">ADO (in conjunction with the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) enables the developer to build an empty **Recordset** object by specifying column information and calling **Open**.</span></span> <span data-ttu-id="a8dae-141">В следующем примере три новых поля добавляются к новому объекту **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="a8dae-141">In the following example, three new fields are appended to a new **Recordset** object.</span></span> <span data-ttu-id="a8dae-142">Затем открывается **набор записей** , добавляются две новые записи, а **набор записей** сохраняется в файл.</span><span class="sxs-lookup"><span data-stu-id="a8dae-142">Then the **Recordset** is opened, two new records are added, and the **Recordset** is persisted to a file.</span></span> <span data-ttu-id="a8dae-143">(Дополнительные сведения о сохранении **наборов записей** содержатся в [главе 5: обновление и сохранение данных](chapter-5-updating-and-persisting-data.md).)</span><span class="sxs-lookup"><span data-stu-id="a8dae-143">(For more information about **Recordset** persistence, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).)</span></span>

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

<span data-ttu-id="a8dae-144">Использование метода **append** в **полях** зависит от объекта **Recordset** и объекта **Record** .</span><span class="sxs-lookup"><span data-stu-id="a8dae-144">The usage of the **Fields** **Append** method differs between the **Recordset** object and the **Record** object.</span></span> <span data-ttu-id="a8dae-145">Дополнительные сведения об объекте **Record** содержатся в [главе 10: записи и потоки](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="a8dae-145">For more information about the **Record** object, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

