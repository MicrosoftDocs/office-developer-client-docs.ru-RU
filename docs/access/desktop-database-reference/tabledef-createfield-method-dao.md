---
title: TableDef.CreateField Method (DAO)
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
ms.openlocfilehash: 89b42c1afe60add3b1eab33c13dd215b572e3ef5
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25483226"
---
# <a name="tabledefcreatefield-method-dao"></a><span data-ttu-id="f4e3e-102">TableDef.CreateField Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="f4e3e-102">TableDef.CreateField Method (DAO)</span></span>

<span data-ttu-id="f4e3e-103">**Применимо к:** Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="f4e3e-103">**Applies to:** Access 2013 | Office 2013</span></span>

<span data-ttu-id="f4e3e-104">Создает новый объект **[поля](field-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="f4e3e-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e3e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f4e3e-105">Syntax</span></span>

<span data-ttu-id="f4e3e-106">*выражение* . CreateField (_**имя**_, _**Тип**_, _**размер**_)</span><span class="sxs-lookup"><span data-stu-id="f4e3e-106">*expression* .CreateField(_**Name**_, _**Type**_, _**Size**_)</span></span>

<span data-ttu-id="f4e3e-107">*выражение* Переменная, которая представляет собой объект- **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="f4e3e-107">*expression* A variable that represents a **TableDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="f4e3e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="f4e3e-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4e3e-109">Имя</span><span class="sxs-lookup"><span data-stu-id="f4e3e-109">Name</span></span></p></th>
<th><p><span data-ttu-id="f4e3e-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="f4e3e-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="f4e3e-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f4e3e-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="f4e3e-112">Описание</span><span class="sxs-lookup"><span data-stu-id="f4e3e-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4e3e-113">Имя</span><span class="sxs-lookup"><span data-stu-id="f4e3e-113">Name</span></span></p></td>
<td><p><span data-ttu-id="f4e3e-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="f4e3e-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="f4e3e-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f4e3e-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f4e3e-116">Строка, уникальным образом новый объект <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="f4e3e-116">A String that uniquely names the new <strong>Field</strong> object.</span></span> <span data-ttu-id="f4e3e-117">Свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см на допустимый имена <strong>полей</strong> .</span><span class="sxs-lookup"><span data-stu-id="f4e3e-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4e3e-118">Тип</span><span class="sxs-lookup"><span data-stu-id="f4e3e-118">Type</span></span></p></td>
<td><p><span data-ttu-id="f4e3e-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="f4e3e-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="f4e3e-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f4e3e-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f4e3e-121">Константа, которая определяет тип данных на новый объект <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="f4e3e-121">A constant that determines the data type of the new <strong>Field</strong> object.</span></span> <span data-ttu-id="f4e3e-122">В разделе свойства <strong><a href="field-type-property-dao.md">Type</a></strong> для типов данных.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4e3e-123">Size</span><span class="sxs-lookup"><span data-stu-id="f4e3e-123">Size</span></span></p></td>
<td><p><span data-ttu-id="f4e3e-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="f4e3e-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="f4e3e-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="f4e3e-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="f4e3e-126">Целое число, которое указывает максимальный размер в байтах, объект <strong>поля</strong> , который содержит текст.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-126">An Integer that indicates the maximum size, in bytes, of a <strong>Field</strong> object that contains text.</span></span> <span data-ttu-id="f4e3e-127">В разделе <strong><a href="field-size-property-dao.md">свойства Size для значений допустимый размер</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="f4e3e-127">See the <strong><a href="field-size-property-dao.md">Size</a></strong> property for valid size values.</span></span> <span data-ttu-id="f4e3e-128">Этот аргумент игнорируется для полей числовые и половинной ширины.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-128">This argument is ignored for numeric and fixed-width fields.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="f4e3e-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f4e3e-129">Return Value</span></span>

<span data-ttu-id="f4e3e-130">Поле</span><span class="sxs-lookup"><span data-stu-id="f4e3e-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e3e-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="f4e3e-131">Remarks</span></span>

<span data-ttu-id="f4e3e-132">Чтобы создать новое поле, а также указать имя, тип данных и размер поля можно использовать метод **CreateField** .</span><span class="sxs-lookup"><span data-stu-id="f4e3e-132">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field.</span></span> <span data-ttu-id="f4e3e-133">Если опустить одно или несколько частей необязательно при использовании **CreateField**, можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-133">If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="f4e3e-134">После добавления нового объекта, можно изменить некоторые, но не для всех параметров его свойств.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-134">After you append the new object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="f4e3e-135">Обратитесь к соответствующим разделам отдельных свойств для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-135">See the individual property topics for more details.</span></span>

<span data-ttu-id="f4e3e-136">Тип и размер аргументов применяются только к объектам **поля** в объекте **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="f4e3e-136">The type and Size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="f4e3e-137">Пропускать следующие аргументы объекта **поля** связан с объектом **индекса** или **связи** .</span><span class="sxs-lookup"><span data-stu-id="f4e3e-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="f4e3e-138">Если имя ссылается на объект, который уже входит в коллекции, то во время выполнения возникает ошибка при использовании метода **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="f4e3e-138">If Name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="f4e3e-139">Чтобы удалить объект **поля** из коллекции **полей** , используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-139">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span> <span data-ttu-id="f4e3e-140">Невозможно удалить объект **поля** из коллекции **полей** объектов **TableDef** после создания индекса, которая ссылается на поле.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-140">You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

<span data-ttu-id="f4e3e-141">**Автор ссылку** [UtterAccess](https://www.utteraccess.com) сообщества.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-141">**Link provided by** the [UtterAccess](https://www.utteraccess.com) community.</span></span> <span data-ttu-id="f4e3e-142">UtterAccess — это премьер форум вики-сайт и Справка по Microsoft Access.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-142">UtterAccess is the premier Microsoft Access wiki and help forum.</span></span>

- [<span data-ttu-id="f4e3e-143">Добавление поля гиперссылки в существующую таблицу с DAO</span><span class="sxs-lookup"><span data-stu-id="f4e3e-143">Adding a hyperlink field to an existing table with DAO</span></span>](https://www.utteraccess.com/wiki/index.php/adding_a_hyperlink_field_to_an_existing_table_with_dao)

## <a name="example"></a><span data-ttu-id="f4e3e-144">Пример</span><span class="sxs-lookup"><span data-stu-id="f4e3e-144">Example</span></span>

<span data-ttu-id="f4e3e-145">Следующий пример демонстрирует создание вычисляемого поля.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-145">The following example shows how to create a calculated field.</span></span> <span data-ttu-id="f4e3e-146">Метод CreateField создает поле с именем **полное имя**.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-146">The CreateField method creates a field named **FullName**.</span></span> <span data-ttu-id="f4e3e-147">Выражение затем задано значение выражения, вычисляющий значение поля.</span><span class="sxs-lookup"><span data-stu-id="f4e3e-147">The Expression property is then set to the expression that calculates the value of the field.</span></span>

<span data-ttu-id="f4e3e-148">**Пример кода предоставлен** [Справочник программиста Microsoft Access 2010](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span><span class="sxs-lookup"><span data-stu-id="f4e3e-148">**Sample code provided by** the [Microsoft Access 2010 Programmer’s Reference](https://www.amazon.com/Microsoft-Access-2010-Programmers-Reference/dp/8126528125).</span></span>

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

