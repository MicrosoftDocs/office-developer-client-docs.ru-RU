---
title: Метод TableDef.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: a83d797f-ea42-4a07-dd9e-b254755f0891
ms:mtpsurl: https://msdn.microsoft.com/library/Ff821396(v=office.15)
ms:contentKeyID: 48546897
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052971
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: 713f2530369a824a6d7204655ded4333f7fe2765
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308444"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="d83c7-102">Метод TableDef.CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="d83c7-102">TableDef.CreateField Method (DAO)</span></span>

<span data-ttu-id="d83c7-103">**Область применения**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="d83c7-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="d83c7-104">Создает новый объект **[Field](field-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="d83c7-104">Creates a new **[TableDef](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="d83c7-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d83c7-105">Syntax</span></span>

<span data-ttu-id="d83c7-106">*выражение* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span><span class="sxs-lookup"><span data-stu-id="d83c7-106">*expression* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span></span>

<span data-ttu-id="d83c7-107">*выражение*: переменная, представляющая объект **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="d83c7-107">*expression* A variable that represents a **TableDef** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="d83c7-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="d83c7-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d83c7-109">Имя</span><span class="sxs-lookup"><span data-stu-id="d83c7-109">Name</span></span></p></th>
<th><p><span data-ttu-id="d83c7-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="d83c7-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="d83c7-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d83c7-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="d83c7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="d83c7-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d83c7-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="d83c7-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="d83c7-114">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="d83c7-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="d83c7-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d83c7-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d83c7-116">Строка, присваивающая уникальное имя новому объекту <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="d83c7-116">A String that uniquely names the new <strong>Field</strong> object.</span></span> <span data-ttu-id="d83c7-117">См. свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения более подробных сведений о допустимых именах <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="d83c7-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>TableDef</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d83c7-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="d83c7-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="d83c7-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="d83c7-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="d83c7-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d83c7-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d83c7-121">Константа, определяющая тип данных нового объекта <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="d83c7-121">A constant that determines the data type of the new <strong>Field</strong> object.</span></span> <span data-ttu-id="d83c7-122">Допустимые типы данных см. в свойстве <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="d83c7-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d83c7-123"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="d83c7-123"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="d83c7-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="d83c7-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="d83c7-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="d83c7-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="d83c7-126">Целое число, указывающее максимальный размер в байтах объекта <strong>Field</strong>, содержащего текст.</span><span class="sxs-lookup"><span data-stu-id="d83c7-126">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text.</span></span> <span data-ttu-id="d83c7-127">Допустимые значения размеров см. в свойстве <strong><a href="field-size-property-dao.md">Size</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="d83c7-127">See the <strong><a href="field-size-property-dao.md">Size</a></strong> property for valid size values.</span></span> <span data-ttu-id="d83c7-128">Этот аргумент игнорируется для числовых полей и полей фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="d83c7-128">This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="d83c7-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d83c7-129">Return value</span></span>

<span data-ttu-id="d83c7-130">Поле</span><span class="sxs-lookup"><span data-stu-id="d83c7-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="d83c7-131">Примечания</span><span class="sxs-lookup"><span data-stu-id="d83c7-131">Remarks</span></span>

<span data-ttu-id="d83c7-132">Можно использовать метод **CreateField**, чтобы создать новое поле, а также указать имя, тип данных и размер поля.</span><span class="sxs-lookup"><span data-stu-id="d83c7-132">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field.</span></span> <span data-ttu-id="d83c7-133">Если опустить одну или несколько необязательных частей при использовании метода **CreateField**, вы можете воспользоваться соответствующим оператором присваивания, чтобы задать или сбросить соответствующее свойство перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="d83c7-133">If you omit one or more of the optional parts when you use the **CreateTableDef** method, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="d83c7-134">После добавления нового объекта вы можете изменять некоторые, но не все параметры его свойств.</span><span class="sxs-lookup"><span data-stu-id="d83c7-134">After you append the object, you can alter some but not all of its properties.</span></span> <span data-ttu-id="d83c7-135">См. разделы для отдельных свойств для получения дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="d83c7-135">See the individual property topics for more details.</span></span>

<span data-ttu-id="d83c7-136">Аргументы Type и Size применяются только для объектов **Field** в объекте **TableDef**.</span><span class="sxs-lookup"><span data-stu-id="d83c7-136">The type and Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="d83c7-137">Эти аргументы игнорируются, если объект **Field** связан с объектом **Index** или **Relation**.</span><span class="sxs-lookup"><span data-stu-id="d83c7-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="d83c7-138">Если аргумент Name ссылается на объект, который уже являются элементом коллекции, возникает ошибка выполнения при использовании метода **[Append](fields-append-method-dao.md)**.</span><span class="sxs-lookup"><span data-stu-id="d83c7-138">If name refers to an object that is already a member of the collection, or you specify an invalid property in the TableDef or Field object you're appending, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="d83c7-139">Чтобы удалить объект **Field** из коллекции **Fields**, используйте метод **[Delete](fields-delete-method-dao.md)** для коллекции.</span><span class="sxs-lookup"><span data-stu-id="d83c7-139">To remove a TableDef object from the  TableDefs  collection, use the  Delete  method on the collection.</span></span> <span data-ttu-id="d83c7-140">Вы не можете удалить объект **Field** из коллекции **Fields** объекта **TableDef** после создания индекса, ссылающегося на поле.</span><span class="sxs-lookup"><span data-stu-id="d83c7-140">You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="d83c7-141">**Ссылка, предоставляемая** сообществом [UtterAccess](https://www.utteraccess.com).</span><span class="sxs-lookup"><span data-stu-id="d83c7-141">**Link provided byCommunity Member Icon** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="d83c7-142">UtterAccess — это премиальный вики-портал и форум, посвященный Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="d83c7-142">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="d83c7-143">Добавление поля гиперссылки в существующую таблицу с помощью DAO</span><span class="sxs-lookup"><span data-stu-id="d83c7-143">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="d83c7-144">Пример</span><span class="sxs-lookup"><span data-stu-id="d83c7-144">Example</span></span>

<span data-ttu-id="d83c7-145">В приведенном ниже примере показано, как создать вычисляемое поле.</span><span class="sxs-lookup"><span data-stu-id="d83c7-145">The following example shows how to create a calculated field.</span></span> <span data-ttu-id="d83c7-146">Метод CreateField создает поле с именем **FullName**.</span><span class="sxs-lookup"><span data-stu-id="d83c7-146">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="d83c7-147">Затем для свойства Expression устанавливается выражение, вычисляющее значение поля.</span><span class="sxs-lookup"><span data-stu-id="d83c7-147">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="d83c7-148">**Пример кода из** [справочника программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="d83c7-148">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

```vb
    Sub CreateCalculatedField()
        Dim dbs As DAO.Database
        Dim tdf As DAO.TableDef
        Dim fld As DAO.Field2
        
        ' get the database
        Set dbs = CurrentDb()
        
        ' create the table
        Set tdf = dbs.CreateTableDef("tblContactsCalcField")
        
        ' create the fields: first name, last name
        tdf.Fields.Append tdf.CreateField("FirstName", dbText, 20)
        tdf.Fields.Append tdf.CreateField("LastName", dbText, 20)
        
        ' create the calculated field: full name
        Set fld = tdf.CreateField("FullName", dbText, 50)
        fld.Expression = "[FirstName] & "" "" & [LastName]"
        tdf.Fields.Append fld
        
        ' append the table and cleanup
        dbs.TableDefs.Append tdf
        
    Cleanup:
        Set fld = Nothing
        Set tdf = Nothing
        Set dbs = Nothing
    End Sub
```

