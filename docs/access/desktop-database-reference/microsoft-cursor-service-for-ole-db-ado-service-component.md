---
title: Служба курсора (Майкрософт) для OLE DB (компонент службы ADO)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d79d060922c6e7f28209242ebe82821c2ba97bfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32288990"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a><span data-ttu-id="2dcaa-102">Служба курсора (Майкрософт) для OLE DB (компонент службы ADO)</span><span class="sxs-lookup"><span data-stu-id="2dcaa-102">Microsoft Cursor Service for OLE DB (ADO Service Component)</span></span>


<span data-ttu-id="2dcaa-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2dcaa-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2dcaa-104">Служба курсора Майкрософт для OLE DB дополняет функциональные возможности поставщиков данных поддержкой курсоров.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-104">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers.</span></span> <span data-ttu-id="2dcaa-105">В результате пользователь воспринимает сравнительно единообразные функциональные возможности у всех поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-105">As a result, the user perceives relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="2dcaa-106">Служба курсора делает динамические свойства доступными и улучшает поведение определенных методов.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-106">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods.</span></span> <span data-ttu-id="2dcaa-107">Например, динамическое свойство [optimize](optimize-property-dynamic-ado.md) позволяет создавать временные индексы для упрощения определенных операций, например метода [Find](find-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2dcaa-107">For example, the [Optimize](optimize-property-dynamic-ado.md) dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the [Find](find-method-ado.md) method.</span></span>

<span data-ttu-id="2dcaa-108">Служба курсоров обеспечивает поддержку пакетного обновления во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-108">The Cursor Service enables support for batch updating in all cases.</span></span> <span data-ttu-id="2dcaa-109">Он также имитирует дополнительные типы курсоров, например динамические курсоры, когда поставщик данных может предоставлять только менее доступные курсоры, например статические курсоры.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-109">It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

## <a name="keyword"></a><span data-ttu-id="2dcaa-110">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="2dcaa-110">Keyword</span></span>

<span data-ttu-id="2dcaa-111">Чтобы вызвать этот компонент службы, присвойте свойству [CursorLocation](cursorlocation-property-ado.md) объекта [Recordset](recordset-object-ado.md) или объекта [подключения](connection-object-ado.md) значение **адусеклиент**.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-111">To invoke this service component, set the [Recordset](recordset-object-ado.md) or [Connection](connection-object-ado.md) object's [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a><span data-ttu-id="2dcaa-112">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="2dcaa-112">Dynamic Properties</span></span>

<span data-ttu-id="2dcaa-113">При вызове службы курсора для OLE DB следующие динамические свойства добавляются в коллекцию [свойств](properties-collection-ado.md) объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2dcaa-113">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the **Recordset** object's [Properties](properties-collection-ado.md) collection.</span></span> <span data-ttu-id="2dcaa-114">Полный список динамических свойств **подключения** и объекта **Recordset** указан в динамическом индексе [свойства ADO](ado-dynamic-property-index.md).</span><span class="sxs-lookup"><span data-stu-id="2dcaa-114">The full list of **Connection** and **Recordset** object dynamic properties is listed in the [ADO Dynamic Property Index](ado-dynamic-property-index.md).</span></span> <span data-ttu-id="2dcaa-115">Соответствующие имена свойств OLE DB, где это уместно, включаются в скобки после имени свойства ADO.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-115">The associated OLE DB property names, where appropriate, are included in parenthesis after the ADO property name.</span></span>

<span data-ttu-id="2dcaa-116">Изменения, внесенные в некоторые динамические свойства, не отображаются в базовом источнике данных после вызова службы курсора.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-116">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked.</span></span> <span data-ttu-id="2dcaa-117">Например, установка свойства *времени ожидания для команды* для объекта **Recordset** не будет отображаться для базового поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-117">For example, setting the *Command Time out* property on a **Recordset** will not be visible to the underlying data provider.</span></span>

```vb 
... 
Recordset1.CursorLocation = adUseClient 'invokes cursor service 
Recordset1.Open "authors", _ 
 "Provider=SQLOLEDB;Data Source=DBServer;User Id=usr;" & _ 
 "Password=pwd;Initial Catalog=pubs;",,adCmdTable 
Recordset1.Properties.Item("Command Time out") = 50 
' 'Command Time out' property on DBServer is still default (30). 
... 

```

<span data-ttu-id="2dcaa-118">Если для приложения требуется служба курсора, но вам нужно задать динамические свойства для базового поставщика, задайте свойства перед вызовом службы курсора.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-118">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service.</span></span> <span data-ttu-id="2dcaa-119">Параметры свойства объекта Command всегда передаются базовому поставщику данных независимо от положения курсора.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-119">Command object property settings are always passed to the underlying data provider regardless of cursor location.</span></span> <span data-ttu-id="2dcaa-120">Таким образом, вы также можете использовать объект Command для задания свойств в любое время.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-120">Therefore, you can also use a command object to set the properties at any time.</span></span>

> [!NOTE]
> <span data-ttu-id="2dcaa-121">Служба курсора ДБПРОП_СЕРВЕРДАТАОНИНСЕРТ не поддерживает динамическое свойство, даже если оно поддерживается базовым поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-121">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dcaa-122">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="2dcaa-122">Property Name</span></span></p></th>
<th><p><span data-ttu-id="2dcaa-123">Описание</span><span class="sxs-lookup"><span data-stu-id="2dcaa-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dcaa-124">Автоматическое перерасчет</span><span class="sxs-lookup"><span data-stu-id="2dcaa-124">Auto Recalc</span></span><br />
<span data-ttu-id="2dcaa-125">(ДБПРОП_АДК_АУТОРЕКАЛК)</span><span class="sxs-lookup"><span data-stu-id="2dcaa-125">(DBPROP_ADC_AUTORECALC)</span></span></p></td>
<td><p><span data-ttu-id="2dcaa-126">Для наборов записей, созданных с помощью службы формирования данных, это значение указывает, как часто рассчитываются вычисляемые и статистические вычисляемые столбцы.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-126">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated.</span></span> <span data-ttu-id="2dcaa-127">Значение по умолчанию (Value = 1) используется для пересчета, когда служба формирования данных определит, что значения изменились.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-127">The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed.</span></span> <span data-ttu-id="2dcaa-128">Если значение равно 0, вычисляемые или статистические столбцы рассчитываются только при первоначальном построении иерархии.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-128">If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcaa-129">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="2dcaa-129">Batch Size</span></span><br />
<span data-ttu-id="2dcaa-130">(ДБПРОП_АДК_БАТЧСИЗЕ)</span><span class="sxs-lookup"><span data-stu-id="2dcaa-130">(DBPROP_ADC_BATCHSIZE)</span></span></p></td>
<td><p><span data-ttu-id="2dcaa-131">Указывает количество инструкций UPDATE, которые можно пакетировать перед отправкой в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-131">Indicates the number of update statements that can be batched before being sent to the data store.</span></span> <span data-ttu-id="2dcaa-132">Чем больше инструкций в пакете, тем меньше обращений к хранилищу данных.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-132">The more statements in a batch, the fewer round trips to the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcaa-133">ДоЧерние строки кэша</span><span class="sxs-lookup"><span data-stu-id="2dcaa-133">Cache Child Rows</span></span><br />
<span data-ttu-id="2dcaa-134">(ДБПРОП_АДК_КАЧЕЧИЛДРОВС)</span><span class="sxs-lookup"><span data-stu-id="2dcaa-134">(DBPROP_ADC_CACHECHILDROWS)</span></span></p></td>
<td><p><span data-ttu-id="2dcaa-135">Для наборов записей, созданных с помощью службы формирования данных, это значение указывает, хранятся ли в кэше дочерние наборы записей для последующего использования.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-135">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcaa-136">Версия обработчика курсора</span><span class="sxs-lookup"><span data-stu-id="2dcaa-136">Cursor Engine Version</span></span><br />
<span data-ttu-id="2dcaa-137">(ДБПРОП_АДК_ЦЕВЕР)</span><span class="sxs-lookup"><span data-stu-id="2dcaa-137">(DBPROP_ADC_CEVER)</span></span></p></td>
<td><p><span data-ttu-id="2dcaa-138">Указывает версию используемой службы курсоров.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-138">Indicates the version of the Cursor Service being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcaa-139">Ведение состояния изменения</span><span class="sxs-lookup"><span data-stu-id="2dcaa-139">Maintain Change Status</span></span><br />
<span data-ttu-id="2dcaa-140">(ДБПРОП_АДК_МАИНТАИНЧАНЖЕСТАТУС)</span><span class="sxs-lookup"><span data-stu-id="2dcaa-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span></span></p></td>
<td><p><span data-ttu-id="2dcaa-141">Указывает текст команды, используемой для повторной синхронизации одной или нескольких строк в соединении с несколькими таблицами.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-141">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcaa-142"><a href="optimize-property-dynamic-ado.md">Оптимизация</a></span><span class="sxs-lookup"><span data-stu-id="2dcaa-142"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="2dcaa-143">Указывает, следует ли создать индекс.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-143">Indicates whether an index should be created.</span></span> <span data-ttu-id="2dcaa-144">Если задано <strong>значение true, выполняется</strong>авторизация временного создания индексов для оптимизации выполнения определенных операций.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-144">When set to <strong>True</strong>, authorizes the temporary creation of indexes to improve the execution of certain operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcaa-145"><a href="reshape-name-property-dynamic-ado.md">Изменение имени фигуры</a></span><span class="sxs-lookup"><span data-stu-id="2dcaa-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="2dcaa-146">Указывает имя объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-146">Indicates the name of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="2dcaa-147">Могут быть указаны в текущих или последующих командах формирования данных.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-147">May be referenced within the current, or subsequent, data shaping commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcaa-148"><a href="resync-command-property-dynamic-ado.md">Команда Resync</a></span><span class="sxs-lookup"><span data-stu-id="2dcaa-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="2dcaa-149">Указывает пользовательскую строку команды, используемую методом <a href="resync-method-ado.md">Resync</a> , когда действует свойство <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">UNIQUE Table</a> .</span><span class="sxs-lookup"><span data-stu-id="2dcaa-149">Indicates a custom command string that is used by the <a href="resync-method-ado.md">Resync</a> method when the <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> property is in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcaa-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальный каталог</a></span><span class="sxs-lookup"><span data-stu-id="2dcaa-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="2dcaa-151">Указывает имя базы данных, содержащей таблицу, на которую ссылается свойство <strong>UNIQUE Table</strong> .</span><span class="sxs-lookup"><span data-stu-id="2dcaa-151">Indicates the name of the database containing the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcaa-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная схема</a></span><span class="sxs-lookup"><span data-stu-id="2dcaa-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span></span></p></td>
<td><p><span data-ttu-id="2dcaa-153">Указывает имя владельца таблицы, указанной в свойстве <strong>UNIQUE Table</strong> .</span><span class="sxs-lookup"><span data-stu-id="2dcaa-153">Indicates the name of the owner of the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcaa-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная таблица</a></span><span class="sxs-lookup"><span data-stu-id="2dcaa-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span></span></p></td>
<td><p><span data-ttu-id="2dcaa-155">Указывает имя одной таблицы в <strong>наборе записей</strong> , созданной на основе нескольких таблиц, которые могут быть изменены при вставке, обновлении или удалении.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-155">Indicates the name of the one table in a <strong>Recordset</strong> created from multiple tables that may be modified by insertions, updates, or deletions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcaa-156">Условия обновления</span><span class="sxs-lookup"><span data-stu-id="2dcaa-156">Update Criteria</span></span><br />
<span data-ttu-id="2dcaa-157">(ДБПРОП_АДК_УПДАТЕКРИТЕРИА)</span><span class="sxs-lookup"><span data-stu-id="2dcaa-157">(DBPROP_ADC_UPDATECRITERIA)</span></span></p></td>
<td><p><span data-ttu-id="2dcaa-158">Указывает, какие поля в предложении <strong>WHERE</strong> используются для обработки конфликтов, происходящих во время обновления.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-158">Indicates which fields in the <strong>WHERE</strong> clause are used to handle collisions occurring during an update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcaa-159"><a href="update-resync-property-dynamic-ado.md">Повторная синхронизация обновлений</a> (ДБПРОП_АДК_УПДАТЕРЕСИНК)</span><span class="sxs-lookup"><span data-stu-id="2dcaa-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span></span></p></td>
<td><p><span data-ttu-id="2dcaa-160">Указывает, является <strong></strong> ли метод Resync неявно вызванным после метода <a href="updatebatch-method-ado.md">UpdateBatch</a> (и его поведения), когда действует свойство <strong>UNIQUE Table</strong> .</span><span class="sxs-lookup"><span data-stu-id="2dcaa-160">Indicates whether the <strong>Resync</strong> method is implicitly invoked after the <a href="updatebatch-method-ado.md">UpdateBatch</a> method (and its behavior), when the <strong>Unique Table</strong> property is in effect.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2dcaa-161">Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса для коллекции **свойств** .</span><span class="sxs-lookup"><span data-stu-id="2dcaa-161">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** collection.</span></span> <span data-ttu-id="2dcaa-162">Например, получите и распечатайте текущее значение динамического свойства [Оптимизация](optimize-property-dynamic-ado.md) , а затем задайте новое значение, как показано ниже:</span><span class="sxs-lookup"><span data-stu-id="2dcaa-162">For example, get and print the current value of the [Optimize](optimize-property-dynamic-ado.md) dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a><span data-ttu-id="2dcaa-163">Поведение встроенного свойства</span><span class="sxs-lookup"><span data-stu-id="2dcaa-163">Built-in Property Behavior</span></span>

<span data-ttu-id="2dcaa-164">Служба курсора для OLE DB также влияет на поведение определенных встроенных свойств.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-164">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2dcaa-165">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="2dcaa-165">Property Name</span></span></p></th>
<th><p><span data-ttu-id="2dcaa-166">Описание</span><span class="sxs-lookup"><span data-stu-id="2dcaa-166">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2dcaa-167"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="2dcaa-167"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="2dcaa-168">Дополняет типы курсоров, доступные для объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-168">Supplements the types of cursors that are available for a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2dcaa-169"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="2dcaa-169"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="2dcaa-170">Дополняет типы блокировок, доступные для объекта <strong>Recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-170">Supplements the types of locks available for a <strong>Recordset</strong>.</span></span> <span data-ttu-id="2dcaa-171">Включает пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-171">Enables batch updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2dcaa-172"><a href="sort-property-ado.md">Sort</a></span><span class="sxs-lookup"><span data-stu-id="2dcaa-172"><a href="sort-property-ado.md">Sort</a></span></span></p></td>
<td><p><span data-ttu-id="2dcaa-173">Задает одно или несколько имен полей, по которым сортируется <strong>набор записей</strong> , а также отсортировать каждое поле в возрастающем или убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="2dcaa-173">Specifies one or more field names that the <strong>Recordset</strong> is sorted on, and whether each field is sorted in ascending or descending order.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a><span data-ttu-id="2dcaa-174">Поведение метода</span><span class="sxs-lookup"><span data-stu-id="2dcaa-174">Method Behavior</span></span>

<span data-ttu-id="2dcaa-175">Служба курсора для OLE DB включает или влияет на поведение метода [append](append-method-ado.md) объекта [field](field-object-ado.md) ; и методы [Open](open-method-ado-recordset.md), Resync, [](resync-method-ado.md) [UpdateBatch](updatebatch-method-ado.md)и [Save](save-method-ado.md) объекта **Recordset** .</span><span class="sxs-lookup"><span data-stu-id="2dcaa-175">The Cursor Service for OLE DB enables or affects the behavior of the [Field](field-object-ado.md) object's [Append](append-method-ado.md) method; and the **Recordset** object's [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [Save](save-method-ado.md) methods.</span></span>

