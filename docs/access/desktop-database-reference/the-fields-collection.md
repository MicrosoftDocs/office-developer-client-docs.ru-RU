---
title: The Fields Collection
TOCTitle: The Fields Collection
ms:assetid: 3bda8e5d-eceb-9605-c4d7-c1f4cc00ce6b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249154(v=office.15)
ms:contentKeyID: 48544297
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 67f16c9c4dd27fdbd57a2c082580ead0606298e9
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25874876"
---
# <a name="the-fields-collection"></a><span data-ttu-id="6a26b-102">The Fields Collection</span><span class="sxs-lookup"><span data-stu-id="6a26b-102">The Fields Collection</span></span>


<span data-ttu-id="6a26b-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="6a26b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6a26b-104">Коллекции **полей** — это один из встроенных ADO семейств сайтов.</span><span class="sxs-lookup"><span data-stu-id="6a26b-104">The **Fields** collection is one of ADO's intrinsic collections.</span></span> <span data-ttu-id="6a26b-105">Коллекция — это упорядоченный набор элементов, которые может называться блоком.</span><span class="sxs-lookup"><span data-stu-id="6a26b-105">A collection is an ordered set of items that can be referred to as a unit.</span></span>

<span data-ttu-id="6a26b-106">Коллекция **полей** содержит объект **поля** для каждого поля (столбца) в **набор записей**.</span><span class="sxs-lookup"><span data-stu-id="6a26b-106">The **Fields** collection contains a **Field** object for every field (column) in the **Recordset**.</span></span> <span data-ttu-id="6a26b-107">Как все коллекции ADO имеет свойства **Count** и **элементов** , а также методы **добавления** и **обновления** .</span><span class="sxs-lookup"><span data-stu-id="6a26b-107">Like all ADO collections, it has **Count** and **Item** properties, as well as **Append** and **Refresh** methods.</span></span> <span data-ttu-id="6a26b-108">Он также имеет **CancelUpdate**, **удаления**, **выполнить повторную синхронизацию**и методов **обновления** , не являющихся другим семействам ADO.</span><span class="sxs-lookup"><span data-stu-id="6a26b-108">It also has **CancelUpdate**, **Delete**, **Resync**, and **Update** methods, which are not available to other ADO collections.</span></span>

## <a name="examining-the-fields-collection"></a><span data-ttu-id="6a26b-109">Проверка коллекции полей</span><span class="sxs-lookup"><span data-stu-id="6a26b-109">Examining the Fields Collection</span></span>

<span data-ttu-id="6a26b-110">Рассмотрите возможность коллекции **полей** , **записей** , представленные в этой главе примера.</span><span class="sxs-lookup"><span data-stu-id="6a26b-110">Consider the **Fields** collection of the sample **Recordset** introduced in this chapter.</span></span> <span data-ttu-id="6a26b-111">Пример **набора записей** является производным от инструкции SQL</span><span class="sxs-lookup"><span data-stu-id="6a26b-111">The sample **Recordset** was derived from the SQL statement</span></span>

```sql 
 
SELECT ProductID, ProductName, UnitPrice FROM Products WHERE CategoryID = 7 
```

<span data-ttu-id="6a26b-112">Таким образом можно найти, что семейство **набора записей** **поля** содержит три поля.</span><span class="sxs-lookup"><span data-stu-id="6a26b-112">Thus, you should find that the **Recordset** **Fields** collection contains three fields.</span></span>

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

<span data-ttu-id="6a26b-113">Этот код определяет число объектов **поля** в коллекцию **полей** , с помощью свойства **Count** и выполняется цикл по коллекции, возврат значения свойства **Name** для каждого объекта **поля** .</span><span class="sxs-lookup"><span data-stu-id="6a26b-113">This code simply determines the number of **Field** objects in the **Fields** collection using the **Count** property and loops through the collection, returning the value of the **Name** property for each **Field** object.</span></span> <span data-ttu-id="6a26b-114">Многие другие свойства **поля** можно использовать для получения сведений о поле.</span><span class="sxs-lookup"><span data-stu-id="6a26b-114">You can use many more **Field** properties to get information about a field.</span></span> <span data-ttu-id="6a26b-115">Дополнительные сведения о запросе на **поле** [Объекта поля](the-field-object.md)см.</span><span class="sxs-lookup"><span data-stu-id="6a26b-115">For more information about querying a **Field**, see [The Field Object](the-field-object.md).</span></span>

## <a name="counting-columns"></a><span data-ttu-id="6a26b-116">Подсчет столбцов</span><span class="sxs-lookup"><span data-stu-id="6a26b-116">Counting Columns</span></span>

<span data-ttu-id="6a26b-117">Как можно было бы ожидать, свойство **Count** возвращает число объектов **поля** в коллекции **полей** .</span><span class="sxs-lookup"><span data-stu-id="6a26b-117">As you might expect, the **Count** property returns the actual number of **Field** objects in the **Fields** collection.</span></span> <span data-ttu-id="6a26b-118">Поскольку нумерация для элементов коллекции начинается с нуля, всегда должны кода циклов, начиная с нуля элемента и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="6a26b-118">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="6a26b-119">Если используется Microsoft Visual Basic и хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , используйте **для** **каждого... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="6a26b-119">If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="6a26b-120">Если свойство **Count** равно нулю, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="6a26b-120">If the **Count** property is zero, there are no objects in the collection.</span></span>

## <a name="getting-to-the-field"></a><span data-ttu-id="6a26b-121">Приступая к полю</span><span class="sxs-lookup"><span data-stu-id="6a26b-121">Getting to the Field</span></span>

<span data-ttu-id="6a26b-122">Как с любой коллекции ADO свойство **Item** является свойством по умолчанию коллекции.</span><span class="sxs-lookup"><span data-stu-id="6a26b-122">As with any ADO collection, the **Item** property is the default property of the collection.</span></span> <span data-ttu-id="6a26b-123">Возвращает отдельный объект **поля** , указанного по имени или индекса, переданным в него.</span><span class="sxs-lookup"><span data-stu-id="6a26b-123">It returns the individual **Field** object specified by the name or index passed to it.</span></span> <span data-ttu-id="6a26b-124">Таким образом следующие инструкции для образца **набора записей**эквивалентны:</span><span class="sxs-lookup"><span data-stu-id="6a26b-124">Therefore, the following statements are equivalent for the sample **Recordset**:</span></span>

```vb 
 
objField = objRecordset.Fields.Item("ProductID") 
objField = objRecordset.Fields("ProductID") 
objField = objRecordset.Fields.Item(0) 
objField = objRecordset.Fields(0) 
```

<span data-ttu-id="6a26b-125">Если эти методы эквивалентны, который лучше всего подходит?</span><span class="sxs-lookup"><span data-stu-id="6a26b-125">If these methods are equivalent, which is best?</span></span> <span data-ttu-id="6a26b-126">Смотря как.</span><span class="sxs-lookup"><span data-stu-id="6a26b-126">It depends.</span></span> <span data-ttu-id="6a26b-127">Использования индекса, чтобы извлечь **поля** из коллекции, работает быстрее, так как он получает доступ к **поля** напрямую, без необходимости выполнять поиск строки.</span><span class="sxs-lookup"><span data-stu-id="6a26b-127">Using an index to retrieve a **Field** from the collection is faster because it accesses the **Field** directly without having to perform a string lookup.</span></span> <span data-ttu-id="6a26b-128">С другой стороны порядок **полей** в коллекции должно быть известно, и при изменении порядка ссылку на индекс **поля** придется изменить везде, где оно становится.</span><span class="sxs-lookup"><span data-stu-id="6a26b-128">On the other hand, the order of **Fields** within the collection must be known, and if the order changes, the reference to the **Field's** index will have to be changed wherever it occurs.</span></span> <span data-ttu-id="6a26b-129">Хотя несколько медленнее, более гибкий с помощью имени **поля** , так как он не зависит от порядка **полей** в коллекции.</span><span class="sxs-lookup"><span data-stu-id="6a26b-129">Although slightly slower, using the name of the **Field** is more flexible because it doesn't depend on the order of the **Fields** in the collection.</span></span>

## <a name="using-the-refresh-method"></a><span data-ttu-id="6a26b-130">С помощью метода обновления</span><span class="sxs-lookup"><span data-stu-id="6a26b-130">Using the Refresh Method</span></span>

<span data-ttu-id="6a26b-131">В отличие от некоторые другие коллекции ADO с помощью метода **обновления** на коллекции **полей** не действует видимым.</span><span class="sxs-lookup"><span data-stu-id="6a26b-131">Unlike some other ADO collections, using the **Refresh** method on the **Fields** collection has no visible effect.</span></span> <span data-ttu-id="6a26b-132">Чтобы извлечь изменения из базовой структуры базы данных, необходимо использовать либо метод **повторный запрос** , или если объект **набора записей** не поддерживает закладки, метод **MoveFirst** , который будет отображено команду для выполнения Поставщик еще раз.</span><span class="sxs-lookup"><span data-stu-id="6a26b-132">To retrieve changes from the underlying database structure, you must use either the **Requery** method, or if the **Recordset** object does not support bookmarks, the **MoveFirst** method, which will cause the command to be executed against the provider again.</span></span>

## <a name="adding-fields-to-a-recordset"></a><span data-ttu-id="6a26b-133">Добавление полей в наборе записей</span><span class="sxs-lookup"><span data-stu-id="6a26b-133">Adding Fields to a Recordset</span></span>

<span data-ttu-id="6a26b-134">Метод **Append** используется для добавления поля **набора записей**.</span><span class="sxs-lookup"><span data-stu-id="6a26b-134">The **Append** method is used to add fields to a **Recordset**.</span></span>

<span data-ttu-id="6a26b-135">Метод **Append** используется для программного создания **записей** без открытия подключения к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="6a26b-135">You can use the **Append** method to fabricate a **Recordset** programmatically without opening a connection to a data source.</span></span> <span data-ttu-id="6a26b-136">При вызове метода **Append** на коллекцию **полей** open **записей** или **набора записей** , где было установлено свойство **ActiveConnection** произойдет ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="6a26b-136">A run-time error will occur if the **Append** method is called on the **Fields** collection of an open **Recordset** or on a **Recordset** where the **ActiveConnection** property has been set.</span></span> <span data-ttu-id="6a26b-137">После добавления поля только для **записей** , не открыт и еще не был подключен к источнику данных.</span><span class="sxs-lookup"><span data-stu-id="6a26b-137">You can append fields only to a **Recordset** that is not open and has not yet been connected to a data source.</span></span> <span data-ttu-id="6a26b-138">Тем не менее чтобы указать значения для добавленного **полей**, **записей** необходимо открыть.</span><span class="sxs-lookup"><span data-stu-id="6a26b-138">However, to specify values for the newly appended **Fields**, the **Recordset** must first be opened.</span></span>

<span data-ttu-id="6a26b-139">Разработчики часто требуется место для временного хранения некоторые данные или некоторые данные действовать как если бы он поступил от сервера, он может принимать участие в привязке данных в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="6a26b-139">Developers often need a place to temporarily store some data, or want some data to act as if it came from a server so it can participate in data binding in a user interface.</span></span> <span data-ttu-id="6a26b-140">ADO (в сочетании с помощью [Службы Microsoft курсора для OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) позволяет разработчикам создавать **пустой Recordset** , указав сведения о столбце и вызова метода **Open**.</span><span class="sxs-lookup"><span data-stu-id="6a26b-140">ADO (in conjunction with the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md)) enables the developer to build an empty **Recordset** object by specifying column information and calling **Open**.</span></span> <span data-ttu-id="6a26b-141">В следующем примере трех новых полей присоединяются к новый объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="6a26b-141">In the following example, three new fields are appended to a new **Recordset** object.</span></span> <span data-ttu-id="6a26b-142">Затем открывается **набор записей** , добавлены два новых записей и **записей** сохраняется в файл.</span><span class="sxs-lookup"><span data-stu-id="6a26b-142">Then the **Recordset** is opened, two new records are added, and the **Recordset** is persisted to a file.</span></span> <span data-ttu-id="6a26b-143">(Дополнительные сведения о сохранения **записей** можно [Глава 5: обновления и сохранение данных](chapter-5-updating-and-persisting-data.md).)</span><span class="sxs-lookup"><span data-stu-id="6a26b-143">(For more information about **Recordset** persistence, see [Chapter 5: Updating and Persisting Data](chapter-5-updating-and-persisting-data.md).)</span></span>

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

<span data-ttu-id="6a26b-144">Использование метода **Append** **поля** отличается от объекта **набора записей** и объект **записи** .</span><span class="sxs-lookup"><span data-stu-id="6a26b-144">The usage of the **Fields** **Append** method differs between the **Recordset** object and the **Record** object.</span></span> <span data-ttu-id="6a26b-145">Дополнительные сведения об объекте **записи** можно [Глава 10: записей и потоков](chapter-10-records-and-streams.md).</span><span class="sxs-lookup"><span data-stu-id="6a26b-145">For more information about the **Record** object, see [Chapter 10: Records and Streams](chapter-10-records-and-streams.md).</span></span>

