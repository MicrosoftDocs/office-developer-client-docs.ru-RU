---
title: Служба курсоров (Майкрософт) для OLE DB (компонент службы ADO)
TOCTitle: Microsoft Cursor Service for OLE DB (ADO Service Component)
ms:assetid: 6818fc05-9c9f-9b67-07d2-e622c93133c2
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249405(v=office.15)
ms:contentKeyID: 48545376
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 1f164e2671fb27a8e8a8721010bdad518f2d199e
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25879052"
---
# <a name="microsoft-cursor-service-for-ole-db-ado-service-component"></a><span data-ttu-id="8d141-102">Служба курсоров (Майкрософт) для OLE DB (компонент службы ADO)</span><span class="sxs-lookup"><span data-stu-id="8d141-102">Microsoft Cursor Service for OLE DB (ADO Service Component)</span></span>


<span data-ttu-id="8d141-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8d141-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8d141-104">Служба курсора для OLE DB дополняет функции поддержки курсора поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="8d141-104">The Microsoft Cursor Service for OLE DB supplements the cursor support functions of data providers.</span></span> <span data-ttu-id="8d141-105">В результате пользователь понимает относительно универсальный код функции из всех поставщиков данных.</span><span class="sxs-lookup"><span data-stu-id="8d141-105">As a result, the user perceives relatively uniform functionality from all data providers.</span></span>

<span data-ttu-id="8d141-106">Служба курсора доступны динамические свойства и расширяет поведение некоторых методов.</span><span class="sxs-lookup"><span data-stu-id="8d141-106">The Cursor Service makes dynamic properties available and enhances the behavior of certain methods.</span></span> <span data-ttu-id="8d141-107">К примеру динамическое свойство [оптимизировать](optimize-property-dynamic-ado.md) позволяет создавать временных индексов для облегчения определенные операции, такие как метод [поиска](find-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="8d141-107">For example, the [Optimize](optimize-property-dynamic-ado.md) dynamic property enables the creation of temporary indexes to facilitate certain operations, such as the [Find](find-method-ado.md) method.</span></span>

<span data-ttu-id="8d141-108">Служба курсора обеспечивает поддержку для пакетного обновления во всех случаях.</span><span class="sxs-lookup"><span data-stu-id="8d141-108">The Cursor Service enables support for batch updating in all cases.</span></span> <span data-ttu-id="8d141-109">Также более производительные курсора типов, таких как динамические курсоры моделирует, когда поставщик данных может поддерживать только менее производительные курсоры, такие как статические курсоры.</span><span class="sxs-lookup"><span data-stu-id="8d141-109">It also simulates more capable cursor types, such as dynamic cursors, when a data provider can only supply less capable cursors, such as static cursors.</span></span>

## <a name="keyword"></a><span data-ttu-id="8d141-110">Keyword</span><span class="sxs-lookup"><span data-stu-id="8d141-110">Keyword</span></span>

<span data-ttu-id="8d141-111">Чтобы вызвать этот компонент службы, свойства объекта [записей](recordset-object-ado.md) или [подключения к](connection-object-ado.md) [CursorLocation](cursorlocation-property-ado.md) значение **adUseClient**.</span><span class="sxs-lookup"><span data-stu-id="8d141-111">To invoke this service component, set the [Recordset](recordset-object-ado.md) or [Connection](connection-object-ado.md) object's [CursorLocation](cursorlocation-property-ado.md) property to **adUseClient**.</span></span>

`connection.CursorLocation=adUseClientrecordset.CursorLocation=adUseClient`

## <a name="dynamic-properties"></a><span data-ttu-id="8d141-112">Динамические свойства</span><span class="sxs-lookup"><span data-stu-id="8d141-112">Dynamic Properties</span></span>

<span data-ttu-id="8d141-113">При вызове служба курсора для OLE DB следующие динамические свойства добавляются в коллекцию [свойств](properties-collection-ado.md) объекта **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8d141-113">When the Cursor Service for OLE DB is invoked, the following dynamic properties are added to the **Recordset** object's [Properties](properties-collection-ado.md) collection.</span></span> <span data-ttu-id="8d141-114">Полный список динамических свойств объекта **подключения** и **записей** отображается в [ADO динамических свойство индекса](ado-dynamic-property-index.md).</span><span class="sxs-lookup"><span data-stu-id="8d141-114">The full list of **Connection** and **Recordset** object dynamic properties is listed in the [ADO Dynamic Property Index](ado-dynamic-property-index.md).</span></span> <span data-ttu-id="8d141-115">Связанные имена свойств OLE DB, при необходимости включаются в скобках после имени свойства ADO.</span><span class="sxs-lookup"><span data-stu-id="8d141-115">The associated OLE DB property names, where appropriate, are included in parenthesis after the ADO property name.</span></span>

<span data-ttu-id="8d141-116">Изменения в некоторые динамические свойства не видны в источнике данных после выполнялся вызов службы курсора.</span><span class="sxs-lookup"><span data-stu-id="8d141-116">Changes to some dynamic properties are not visible to the underlying data source after the Cursor Service has been invoked.</span></span> <span data-ttu-id="8d141-117">Например задание свойства *Команда времени ожидания* для **набора записей** будет недоступен для базового поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="8d141-117">For example, setting the *Command Time out* property on a **Recordset** will not be visible to the underlying data provider.</span></span>

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

<span data-ttu-id="8d141-118">Если приложения требуются службы курсора, но необходимо задать динамические свойства в базовом поставщика, задайте свойства до вызова службы курсора.</span><span class="sxs-lookup"><span data-stu-id="8d141-118">If your application requires the Cursor Service, but you need to set dynamic properties on the underlying provider, set the properties before invoking the Cursor Service.</span></span> <span data-ttu-id="8d141-119">Параметры свойства объекта команды, всегда передаются базового поставщика данных, независимо от расположения курсора.</span><span class="sxs-lookup"><span data-stu-id="8d141-119">Command object property settings are always passed to the underlying data provider regardless of cursor location.</span></span> <span data-ttu-id="8d141-120">Таким образом можно также использовать объект команды для установки свойств в любое время.</span><span class="sxs-lookup"><span data-stu-id="8d141-120">Therefore, you can also use a command object to set the properties at any time.</span></span>

> [!NOTE]
> <span data-ttu-id="8d141-121">Свойство DBPROP_SERVERDATAONINSERT не поддерживается службой курсора, даже в том случае, если он поддерживается базового поставщика данных.</span><span class="sxs-lookup"><span data-stu-id="8d141-121">The dynamic property DBPROP_SERVERDATAONINSERT is not supported by the cursor service, even if it is supported by the underlying data provider.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d141-122">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="8d141-122">Property Name</span></span></p></th>
<th><p><span data-ttu-id="8d141-123">Описание</span><span class="sxs-lookup"><span data-stu-id="8d141-123">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d141-124">Автоматическое обновление ссылок</span><span class="sxs-lookup"><span data-stu-id="8d141-124">Auto Recalc</span></span><br />
<span data-ttu-id="8d141-125">(DBPROP_ADC_AUTORECALC)</span><span class="sxs-lookup"><span data-stu-id="8d141-125">(DBPROP_ADC_AUTORECALC)</span></span></p></td>
<td><p><span data-ttu-id="8d141-126">Для наборов записей, созданных с помощью служба формирования данных, это значение указывает, как часто рассчитываются столбцы вычисляемые и статистической обработки.</span><span class="sxs-lookup"><span data-stu-id="8d141-126">For recordsets created with the Data Shaping Service, this value indicates how often calculated and aggregate columns are calculated.</span></span> <span data-ttu-id="8d141-127">Значение по умолчанию (значение = 1) — для пересчета каждый раз, когда служба формирования данных определяет, что значения были изменены.</span><span class="sxs-lookup"><span data-stu-id="8d141-127">The default (value=1) is to recalculate whenever the Data Shaping Service determines that the values have changed.</span></span> <span data-ttu-id="8d141-128">Если значение равно 0, вычисляемых или статистической обработки столбцов рассчитываются только при построенных иерархии.</span><span class="sxs-lookup"><span data-stu-id="8d141-128">If the value is 0, the calculated or aggregate columns are only calculated when the hierarchy is initially built.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d141-129">Размер пакета</span><span class="sxs-lookup"><span data-stu-id="8d141-129">Batch Size</span></span><br />
<span data-ttu-id="8d141-130">(DBPROP_ADC_BATCHSIZE)</span><span class="sxs-lookup"><span data-stu-id="8d141-130">(DBPROP_ADC_BATCHSIZE)</span></span></p></td>
<td><p><span data-ttu-id="8d141-131">Показывает, сколько инструкций update, которые могут быть помещены в пакет перед отправкой в хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="8d141-131">Indicates the number of update statements that can be batched before being sent to the data store.</span></span> <span data-ttu-id="8d141-132">Дополнительные инструкции в пакете, хранить меньшее количество обращений к данным.</span><span class="sxs-lookup"><span data-stu-id="8d141-132">The more statements in a batch, the fewer round trips to the data store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d141-133">Кэш дочерних строк</span><span class="sxs-lookup"><span data-stu-id="8d141-133">Cache Child Rows</span></span><br />
<span data-ttu-id="8d141-134">(DBPROP_ADC_CACHECHILDROWS)</span><span class="sxs-lookup"><span data-stu-id="8d141-134">(DBPROP_ADC_CACHECHILDROWS)</span></span></p></td>
<td><p><span data-ttu-id="8d141-135">Для наборов записей, созданных с помощью службы формирования данных это значение указывает ли наборы дочерних записей хранятся в кэше для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="8d141-135">For recordsets created with the Data Shaping Service, this value indicates whether child recordsets are stored in a cache for later use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d141-136">Версия модуля текущей позиции</span><span class="sxs-lookup"><span data-stu-id="8d141-136">Cursor Engine Version</span></span><br />
<span data-ttu-id="8d141-137">(DBPROP_ADC_CEVER)</span><span class="sxs-lookup"><span data-stu-id="8d141-137">(DBPROP_ADC_CEVER)</span></span></p></td>
<td><p><span data-ttu-id="8d141-138">Указывает версию используемой службой курсора.</span><span class="sxs-lookup"><span data-stu-id="8d141-138">Indicates the version of the Cursor Service being used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d141-139">Обслуживание изменений состояния</span><span class="sxs-lookup"><span data-stu-id="8d141-139">Maintain Change Status</span></span><br />
<span data-ttu-id="8d141-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span><span class="sxs-lookup"><span data-stu-id="8d141-140">(DBPROP_ADC_MAINTAINCHANGESTATUS)</span></span></p></td>
<td><p><span data-ttu-id="8d141-141">Указывает текст команды, используемой для повторной синхронизации одна или несколько строк в нескольких присоединиться к таблице.</span><span class="sxs-lookup"><span data-stu-id="8d141-141">Indicates the text of the command used for resynchronizing a one or more rows in a multiple table join.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d141-142"><a href="optimize-property-dynamic-ado.md">Оптимизация</a></span><span class="sxs-lookup"><span data-stu-id="8d141-142"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="8d141-143">Указывает, должен быть создан индекс.</span><span class="sxs-lookup"><span data-stu-id="8d141-143">Indicates whether an index should be created.</span></span> <span data-ttu-id="8d141-144">Если параметр имеет значение <strong>True</strong>, авторизует временные создание индексов для улучшения выполнение определенных операций.</span><span class="sxs-lookup"><span data-stu-id="8d141-144">When set to <strong>True</strong>, authorizes the temporary creation of indexes to improve the execution of certain operations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d141-145"><a href="reshape-name-property-dynamic-ado.md">Изменить форму имя</a></span><span class="sxs-lookup"><span data-stu-id="8d141-145"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="8d141-146">Указывает имя <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="8d141-146">Indicates the name of the <strong>Recordset</strong>.</span></span> <span data-ttu-id="8d141-147">Возможно, на который указывает ссылка в текущем или последующих, формирования команд данных.</span><span class="sxs-lookup"><span data-stu-id="8d141-147">May be referenced within the current, or subsequent, data shaping commands.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d141-148"><a href="resync-command-property-dynamic-ado.md">Команда синхронизации</a></span><span class="sxs-lookup"><span data-stu-id="8d141-148"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="8d141-149">Указывает строку пользовательской команды, используемый с помощью метода <a href="resync-method-ado.md">выполнить повторную синхронизацию</a> , если свойство <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальной таблицы</a> .</span><span class="sxs-lookup"><span data-stu-id="8d141-149">Indicates a custom command string that is used by the <a href="resync-method-ado.md">Resync</a> method when the <a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a> property is in effect.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d141-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальный каталога</a></span><span class="sxs-lookup"><span data-stu-id="8d141-150"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="8d141-151">Указывает имя базы данных, содержащий таблицу, указанный в свойстве <strong>Уникальной таблицы</strong> .</span><span class="sxs-lookup"><span data-stu-id="8d141-151">Indicates the name of the database containing the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d141-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальный схемы</a></span><span class="sxs-lookup"><span data-stu-id="8d141-152"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Schema</a></span></span></p></td>
<td><p><span data-ttu-id="8d141-153">Указывает имя владельца таблицы, указанный в свойстве <strong>Уникальной таблицы</strong> .</span><span class="sxs-lookup"><span data-stu-id="8d141-153">Indicates the name of the owner of the table referenced in the <strong>Unique Table</strong> property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d141-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Уникальная таблица</a></span><span class="sxs-lookup"><span data-stu-id="8d141-154"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table</a></span></span></p></td>
<td><p><span data-ttu-id="8d141-155">Указывает, что имя одной таблицы в <strong>набор записей</strong> , созданного из нескольких таблиц, которые можно изменить путем вставки, обновления или удаления.</span><span class="sxs-lookup"><span data-stu-id="8d141-155">Indicates the name of the one table in a <strong>Recordset</strong> created from multiple tables that may be modified by insertions, updates, or deletions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d141-156">Обновление критериев</span><span class="sxs-lookup"><span data-stu-id="8d141-156">Update Criteria</span></span><br />
<span data-ttu-id="8d141-157">(DBPROP_ADC_UPDATECRITERIA)</span><span class="sxs-lookup"><span data-stu-id="8d141-157">(DBPROP_ADC_UPDATECRITERIA)</span></span></p></td>
<td><p><span data-ttu-id="8d141-158">Указывает, какие поля в предложения <strong>WHERE</strong> используются для обработки конфликтов, которые возникают в процессе обновления.</span><span class="sxs-lookup"><span data-stu-id="8d141-158">Indicates which fields in the <strong>WHERE</strong> clause are used to handle collisions occurring during an update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d141-159"><a href="update-resync-property-dynamic-ado.md">Выполнить повторную синхронизацию обновления</a> (DBPROP_ADC_UPDATERESYNC)</span><span class="sxs-lookup"><span data-stu-id="8d141-159"><a href="update-resync-property-dynamic-ado.md">Update Resync</a>(DBPROP_ADC_UPDATERESYNC)</span></span></p></td>
<td><p><span data-ttu-id="8d141-160">Указывает ли метод <strong>выполнить повторную синхронизацию</strong> неявно вызывается метод <a href="updatebatch-method-ado.md">UpdateBatch</a> (и его поведение), если свойство <strong>Уникальной таблицы</strong> фактически имеет.</span><span class="sxs-lookup"><span data-stu-id="8d141-160">Indicates whether the <strong>Resync</strong> method is implicitly invoked after the <a href="updatebatch-method-ado.md">UpdateBatch</a> method (and its behavior), when the <strong>Unique Table</strong> property is in effect.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d141-161">Можно также задать или получить динамического свойства, указав его имя в качестве индекса в коллекции **свойств** .</span><span class="sxs-lookup"><span data-stu-id="8d141-161">You may also set or retrieve a dynamic property by specifying its name as the index to the **Properties** collection.</span></span> <span data-ttu-id="8d141-162">К примеру получить и печать текущее значение свойства динамической [оптимизировать](optimize-property-dynamic-ado.md) , а затем задать новое значение, следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8d141-162">For example, get and print the current value of the [Optimize](optimize-property-dynamic-ado.md) dynamic property, then set a new value, like this:</span></span>

```vb 
 
Debug.Print rs.Properties("Optimize") 
rs.Properties("Optimize") = True 
```

## <a name="built-in-property-behavior"></a><span data-ttu-id="8d141-163">Поведение встроенных свойств</span><span class="sxs-lookup"><span data-stu-id="8d141-163">Built-in Property Behavior</span></span>

<span data-ttu-id="8d141-164">Служба курсора для OLE DB также влияет на поведение некоторых встроенных свойств.</span><span class="sxs-lookup"><span data-stu-id="8d141-164">The Cursor Service for OLE DB also affects the behavior of certain built-in properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8d141-165">Имя свойства</span><span class="sxs-lookup"><span data-stu-id="8d141-165">Property Name</span></span></p></th>
<th><p><span data-ttu-id="8d141-166">Описание</span><span class="sxs-lookup"><span data-stu-id="8d141-166">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d141-167"><a href="cursortype-property-ado.md">CursorType</a></span><span class="sxs-lookup"><span data-stu-id="8d141-167"><a href="cursortype-property-ado.md">CursorType</a></span></span></p></td>
<td><p><span data-ttu-id="8d141-168">Дополнения типов курсоров, доступных для <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="8d141-168">Supplements the types of cursors that are available for a <strong>Recordset</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d141-169"><a href="locktype-property-ado.md">LockType для</a></span><span class="sxs-lookup"><span data-stu-id="8d141-169"><a href="locktype-property-ado.md">LockType</a></span></span></p></td>
<td><p><span data-ttu-id="8d141-170">Текстовое дополнение типах блокировок, доступные для <strong>набора записей</strong>.</span><span class="sxs-lookup"><span data-stu-id="8d141-170">Supplements the types of locks available for a <strong>Recordset</strong>.</span></span> <span data-ttu-id="8d141-171">Позволяет производить пакетную обновлений.</span><span class="sxs-lookup"><span data-stu-id="8d141-171">Enables batch updates.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d141-172"><a href="sort-property-ado.md">Sort</a></span><span class="sxs-lookup"><span data-stu-id="8d141-172"><a href="sort-property-ado.md">Sort</a></span></span></p></td>
<td><p><span data-ttu-id="8d141-173">Указывает одно или несколько имен полей сортировки <strong>набора записей</strong> , которые ли сортироваться в каждом поле в возрастающем или убывающем порядке.</span><span class="sxs-lookup"><span data-stu-id="8d141-173">Specifies one or more field names that the <strong>Recordset</strong> is sorted on, and whether each field is sorted in ascending or descending order.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="method-behavior"></a><span data-ttu-id="8d141-174">Метод поведение</span><span class="sxs-lookup"><span data-stu-id="8d141-174">Method Behavior</span></span>

<span data-ttu-id="8d141-175">Служба курсора для OLE DB позволяет включать и влияет на поведение метод [Append](append-method-ado.md) объекта [поля](field-object-ado.md) ; и методов [Open](open-method-ado-recordset.md), [выполнить повторную синхронизацию](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md)и [Сохраните](save-method-ado.md) объект **набора записей** .</span><span class="sxs-lookup"><span data-stu-id="8d141-175">The Cursor Service for OLE DB enables or affects the behavior of the [Field](field-object-ado.md) object's [Append](append-method-ado.md) method; and the **Recordset** object's [Open](open-method-ado-recordset.md), [Resync](resync-method-ado.md), [UpdateBatch](updatebatch-method-ado.md), and [Save](save-method-ado.md) methods.</span></span>

