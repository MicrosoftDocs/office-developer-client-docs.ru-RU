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
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a><span data-ttu-id="1e829-102">Служба курсора (Майкрософт) для OLE DB (компонент службы ADO)</span><span class="sxs-lookup"><span data-stu-id="1e829-102">Microsoft Cursor Service for OLE DB (ADO Service Component)</span></span>


<span data-ttu-id="1e829-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="1e829-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1e829-104">Служба Microsoft Cursor для OLE DB дополняет функции поддержки курсоров поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="1e829-104">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers.</span></span> <span data-ttu-id="1e829-105">В результате пользователь воспринимает относительно однородные функции всех поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="1e829-105">As a result, the user perceives relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="1e829-106">Служба Cursor делает динамические свойства доступными и улучшает поведение определенных методов.</span><span class="sxs-lookup"><span data-stu-id="1e829-106">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods.</span></span> <span data-ttu-id="1e829-107">Например, [динамическое](optimize-property-dynamic-ado.md) свойство Оптимизируйте позволяет создавать временные индексы для облегчения определенных операций, например метода [Find.](find-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1e829-107">For example, the [Optimize](optimize-property-dynamic-ado.md) dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the [Find](find-method-ado.md) method.</span></span>

<span data-ttu-id="1e829-108">Служба Cursor во всех случаях поддерживает пакетное обновление.</span><span class="sxs-lookup"><span data-stu-id="1e829-108">The Cursor Service enables support for batch updating in all cases.</span></span> <span data-ttu-id="1e829-109">Он также имитирует более способные типы курсоров, например динамические курсоры, когда поставщик данных может поставлять только менее способные курсоры, например статические курсоры.</span><span class="sxs-lookup"><span data-stu-id="1e829-109">It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

## <a name="keyword"></a><span data-ttu-id="1e829-110">Ключевое слово</span><span class="sxs-lookup"><span data-stu-id="1e829-110">Keyword</span></span>

<span data-ttu-id="1e829-111">Чтобы вызвать этот компонент службы, [](connection-object-ado.md) установите свойство [CursorLocation](cursorlocation-property-ado.md) объекта [Recordset](recordset-object-ado.md) или Connection **в adUseClient.**</span><span class="sxs-lookup"><span data-stu-id="1e829-111">To invoke this service component, set the [Recordset](recordset-object-ado.md) or [Connection](connection-object-ado.md) object's [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a><span data-ttu-id="1e829-112">Dynamic Properties</span><span class="sxs-lookup"><span data-stu-id="1e829-112">Dynamic Properties</span></span>

<span data-ttu-id="1e829-113">При вызове службы cursor для OLE DB в коллекцию Свойств объекта **Recordset** добавляются следующие [динамические](properties-collection-ado.md) свойства.</span><span class="sxs-lookup"><span data-stu-id="1e829-113">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the **Recordset** object's [Properties](properties-collection-ado.md) collection.</span></span> <span data-ttu-id="1e829-114">Полный список динамических свойств **объектов Подключения** и **Recordset** указан в [индексе динамического свойства ADO.](ado-dynamic-property-index.md)</span><span class="sxs-lookup"><span data-stu-id="1e829-114">The full list of **Connection** and **Recordset** object dynamic properties is listed in the [ADO Dynamic Property Index](ado-dynamic-property-index.md).</span></span> <span data-ttu-id="1e829-115">Соответствующие имена свойств OLE DB, если это необходимо, включаются в скобки после имени свойства ADO.</span><span class="sxs-lookup"><span data-stu-id="1e829-115">The associated OLE DB property names, where appropriate, are included in parenthesis after the ADO property name.</span></span>

<span data-ttu-id="1e829-116">Изменения некоторых динамических свойств не видны основному источнику данных после вызова службы Cursor.</span><span class="sxs-lookup"><span data-stu-id="1e829-116">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked.</span></span> <span data-ttu-id="1e829-117">Например, установка свойства *Командное время в* **наборе записей** не будет видна основному поставщику данных.</span><span class="sxs-lookup"><span data-stu-id="1e829-117">For example, setting the *Command Time out* property on a **Recordset** will not be visible to the underlying data provider.</span></span>

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

<span data-ttu-id="1e829-118">Если вашему приложению требуется служба Cursor, но вам необходимо установить динамические свойства на основном поставщике, установите свойства перед обращением к службе Cursor.</span><span class="sxs-lookup"><span data-stu-id="1e829-118">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service.</span></span> <span data-ttu-id="1e829-119">Параметры свойства объектов команд всегда передаются основному поставщику данных независимо от расположения курсора.</span><span class="sxs-lookup"><span data-stu-id="1e829-119">Command object property settings are always passed to the underlying data provider regardless of cursor location.</span></span> <span data-ttu-id="1e829-120">Таким образом, вы также можете использовать объект команды для набора свойств в любое время.</span><span class="sxs-lookup"><span data-stu-id="1e829-120">Therefore, you can also use a command object to set the properties at any time.</span></span>

> [!NOTE]
> <span data-ttu-id="1e829-121">Динамическое свойство DBPROP_SERVERDATAONINSERT не поддерживается службой курсоров, даже если она поддерживается поставщиком данных.</span><span class="sxs-lookup"><span data-stu-id="1e829-121">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e829-122">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="1e829-122">Property Name</span></span></p></th>
<th><p><span data-ttu-id="1e829-123">Description</span><span class="sxs-lookup"><span data-stu-id="1e829-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e829-124">Автоматический пересчет</span><span class="sxs-lookup"><span data-stu-id="1e829-124">Auto Recalc</span></span><br />
<span data-ttu-id="1e829-125">(DBPROP_ADC_AUTORECALC)</span><span class="sxs-lookup"><span data-stu-id="1e829-125">(DBPROP_ADC_AUTORECALC)</span></span></p></td>
<td><p><span data-ttu-id="1e829-126">Для записей, созданных с помощью службы формирования данных, это значение указывает, как часто вычисляются и вычисляются совокупные столбцы.</span><span class="sxs-lookup"><span data-stu-id="1e829-126">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated.</span></span> <span data-ttu-id="1e829-127">По умолчанию (значение=1) необходимо пересчитать каждый раз, когда служба формирования данных определяет, что значения изменились.</span><span class="sxs-lookup"><span data-stu-id="1e829-127">The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed.</span></span> <span data-ttu-id="1e829-128">Если значение 0, вычисляются или совокупные столбцы вычисляются только при первоначальном построении иерархии.</span><span class="sxs-lookup"><span data-stu-id="1e829-128">If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-129">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="1e829-129">Batch Size</span></span><br />
<span data-ttu-id="1e829-130">(DBPROP_ADC_BATCHSIZE)</span><span class="sxs-lookup"><span data-stu-id="1e829-130">(DBPROP_ADC_BATCHSIZE)</span></span></p></td>
<td><p><span data-ttu-id="1e829-131">Указывает количество заявлений об обновлении, которые можно пакетно отправить перед отправлением в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="1e829-131">Indicates the number of update statements that can be batched before being sent to the data store.</span></span> <span data-ttu-id="1e829-132">Чем больше заявлений в пакете, тем меньше поездок в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="1e829-132">The more statements in a batch, the fewer round trips to the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-133">Детские строки кэша</span><span class="sxs-lookup"><span data-stu-id="1e829-133">Cache Child Rows</span></span><br />
<span data-ttu-id="1e829-134">(DBPROP_ADC_CACHECHILDROWS)</span><span class="sxs-lookup"><span data-stu-id="1e829-134">(DBPROP_ADC_CACHECHILDROWS)</span></span></p></td>
<td><p><span data-ttu-id="1e829-135">Для наборов записей, созданных службой формирования данных, это значение указывает, хранятся ли детские записи в кэше для более позднего использования.</span><span class="sxs-lookup"><span data-stu-id="1e829-135">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-136">Версия двигателя cursor</span><span class="sxs-lookup"><span data-stu-id="1e829-136">Cursor Engine Version</span></span><br />
<span data-ttu-id="1e829-137">(DBPROP_ADC_CEVER)</span><span class="sxs-lookup"><span data-stu-id="1e829-137">(DBPROP_ADC_CEVER)</span></span></p></td>
<td><p><span data-ttu-id="1e829-138">Указывает версию используемой службы Cursor.</span><span class="sxs-lookup"><span data-stu-id="1e829-138">Indicates the version of the Cursor Service being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-139">Сохранение состояния изменений</span><span class="sxs-lookup"><span data-stu-id="1e829-139">Maintain Change Status</span></span><br />
<span data-ttu-id="1e829-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span><span class="sxs-lookup"><span data-stu-id="1e829-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span></span></p></td>
<td><p><span data-ttu-id="1e829-141">Указывает текст команды, используемой для повторной синхронизации одной или нескольких строк в нескольких таблицах.</span><span class="sxs-lookup"><span data-stu-id="1e829-141">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-142"><a href="optimize-property-dynamic-ado.md">Оптимизация</a></span><span class="sxs-lookup"><span data-stu-id="1e829-142"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="1e829-143">Указывает, следует ли создавать индекс.</span><span class="sxs-lookup"><span data-stu-id="1e829-143">Indicates whether an index should be created.</span></span> <span data-ttu-id="1e829-144">При наборе <strong>True</strong>разрешает временное создание индексов для улучшения выполнения определенных операций.</span><span class="sxs-lookup"><span data-stu-id="1e829-144">When set to <strong>True</strong>, authorizes the temporary creation of indexes to improve the execution of certain operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-145"><a href="reshape-name-property-dynamic-ado.md">Переописываю имя</a></span><span class="sxs-lookup"><span data-stu-id="1e829-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="1e829-146">Указывает имя <strong>recordset</strong>.</span><span class="sxs-lookup"><span data-stu-id="1e829-146">Indicates the name of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="1e829-147">Можно ссылаться в текущих или последующих командах формирования данных.</span><span class="sxs-lookup"><span data-stu-id="1e829-147">May be referenced within the current, or subsequent, data shaping commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-148"><a href="resync-command-property-dynamic-ado.md">Команда Resync</a></span><span class="sxs-lookup"><span data-stu-id="1e829-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="1e829-149">Указывает настраиваемую строку команд, которая используется методом <a href="resync-method-ado.md">Resync,</a> когда свойство <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> действует.</span><span class="sxs-lookup"><span data-stu-id="1e829-149">Indicates a custom command string that is used by the <a href="resync-method-ado.md">Resync</a> method when the <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> property is in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальный каталог</a></span><span class="sxs-lookup"><span data-stu-id="1e829-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="1e829-151">Указывает имя базы данных, содержащей таблицу, указанную в <strong>свойстве Unique Table.</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-151">Indicates the name of the database containing the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная схема</a></span><span class="sxs-lookup"><span data-stu-id="1e829-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span></span></p></td>
<td><p><span data-ttu-id="1e829-153">Указывает имя владельца таблицы, ссылаясь на свойство <strong>Unique Table.</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-153">Indicates the name of the owner of the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная таблица</a></span><span class="sxs-lookup"><span data-stu-id="1e829-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span></span></p></td>
<td><p><span data-ttu-id="1e829-155">Указывает имя одной таблицы в наборе <strong>записей,</strong> созданных из нескольких таблиц, которые могут изменяться вставки, обновления или удаления.</span><span class="sxs-lookup"><span data-stu-id="1e829-155">Indicates the name of the one table in a <strong>Recordset</strong> created from multiple tables that may be modified by insertions, updates, or deletions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-156">Критерии обновления</span><span class="sxs-lookup"><span data-stu-id="1e829-156">Update Criteria</span></span><br />
<span data-ttu-id="1e829-157">(DBPROP_ADC_UPDATECRITERIA)</span><span class="sxs-lookup"><span data-stu-id="1e829-157">(DBPROP_ADC_UPDATECRITERIA)</span></span></p></td>
<td><p><span data-ttu-id="1e829-158">Указывает, какие поля в пункте <strong>WHERE</strong> используются для обработки столкновений, происходящих во время обновления.</span><span class="sxs-lookup"><span data-stu-id="1e829-158">Indicates which fields in the <strong>WHERE</strong> clause are used to handle collisions occurring during an update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-159"><a href="update-resync-property-dynamic-ado.md">Обновление Resync</a>(DBPROP_ADC_UPDATERESYNC)</span><span class="sxs-lookup"><span data-stu-id="1e829-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span></span></p></td>
<td><p><span data-ttu-id="1e829-160">Указывает, вызывается ли метод <strong>Resync</strong> неявно после метода <a href="updatebatch-method-ado.md">UpdateBatch</a> (и его поведения), когда свойство <strong>Unique Table</strong> действует.</span><span class="sxs-lookup"><span data-stu-id="1e829-160">Indicates whether the <strong>Resync</strong> method is implicitly invoked after the <a href="updatebatch-method-ado.md">UpdateBatch</a> method (and its behavior), when the <strong>Unique Table</strong> property is in effect.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1e829-161">Вы также можете задать или получить динамическое свойство, указав его имя в качестве индекса для коллекции **Свойств.**</span><span class="sxs-lookup"><span data-stu-id="1e829-161">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** collection.</span></span> <span data-ttu-id="1e829-162">Например, получите и распечатайте текущее значение динамического свойства Оптимизируйте, а затем установите новое значение, например: [](optimize-property-dynamic-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1e829-162">For example, get and print the current value of the [Optimize](optimize-property-dynamic-ado.md) dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a><span data-ttu-id="1e829-163">Встроенное поведение свойств</span><span class="sxs-lookup"><span data-stu-id="1e829-163">Built-in Property Behavior</span></span>

<span data-ttu-id="1e829-164">Служба cursor для OLE DB также влияет на поведение определенных встроенных свойств.</span><span class="sxs-lookup"><span data-stu-id="1e829-164">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1e829-165">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="1e829-165">Property Name</span></span></p></th>
<th><p><span data-ttu-id="1e829-166">Description</span><span class="sxs-lookup"><span data-stu-id="1e829-166">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e829-167"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="1e829-167"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="1e829-168">Дополняет типы курсоров, доступные для <strong>Recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-168">Supplements the types of cursors that are available for a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e829-169"><a href="locktype-property-ado.md">LockType</a></span><span class="sxs-lookup"><span data-stu-id="1e829-169"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="1e829-170">Дополняет типы замков, доступных для <strong>recordset.</strong></span><span class="sxs-lookup"><span data-stu-id="1e829-170">Supplements the types of locks available for a <strong>Recordset</strong>.</span></span> <span data-ttu-id="1e829-171">Включает пакетные обновления.</span><span class="sxs-lookup"><span data-stu-id="1e829-171">Enables batch updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e829-172"><a href="sort-property-ado.md">Sort</a></span><span class="sxs-lookup"><span data-stu-id="1e829-172"><a href="sort-property-ado.md">Sort</a></span></span></p></td>
<td><p><span data-ttu-id="1e829-173">Указывает одно или несколько имен полей, в которых сортируется <strong>Набор</strong> записей, и отсортирует ли каждое поле в порядке по возрастанию или убыванию.</span><span class="sxs-lookup"><span data-stu-id="1e829-173">Specifies one or more field names that the <strong>Recordset</strong> is sorted on, and whether each field is sorted in ascending or descending order.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a><span data-ttu-id="1e829-174">Поведение метода</span><span class="sxs-lookup"><span data-stu-id="1e829-174">Method Behavior</span></span>

<span data-ttu-id="1e829-175">Служба cursor для OLE DB включает или [](field-object-ado.md) влияет на поведение метода приложения объекта [Field;](append-method-ado.md) и методы **Open,** [](open-method-ado-recordset.md) [Resync,](resync-method-ado.md)UpdateBatch и Save объекта [Recordset.](updatebatch-method-ado.md) [](save-method-ado.md)</span><span class="sxs-lookup"><span data-stu-id="1e829-175">The Cursor Service for OLE DB enables or affects the behavior of the [Field](field-object-ado.md) object's [Append](append-method-ado.md) method; and the **Recordset** object's [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [Save](save-method-ado.md) methods.</span></span>

