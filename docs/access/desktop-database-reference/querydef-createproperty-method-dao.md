---
title: QueryDef.CreateProperty Method (DAO)
TOCTitle: CreateProperty Method
ms:assetid: e107b7d0-5556-7b87-f131-95f518893e4c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835663(v=office.15)
ms:contentKeyID: 48548250
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3fbe6e9749d8b51fba9af0a43844782aa3f06d12
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25606773"
---
# <a name="querydefcreateproperty-method-dao"></a><span data-ttu-id="73cc1-102">QueryDef.CreateProperty Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="73cc1-102">QueryDef.CreateProperty Method (DAO)</span></span>


<span data-ttu-id="73cc1-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="73cc1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="73cc1-104">Создание пользовательских **[свойств](property-object-dao.md)** объекта (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="73cc1-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="73cc1-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="73cc1-105">Syntax</span></span>

<span data-ttu-id="73cc1-106">*выражение* . CreateProperty (***имя***, ***Тип***, ***значение***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="73cc1-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="73cc1-107">*выражение* Переменная, которая представляет собой объект- **QueryDef** .</span><span class="sxs-lookup"><span data-stu-id="73cc1-107">*expression* A variable that represents a **QueryDef** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="73cc1-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="73cc1-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="73cc1-109">Имя</span><span class="sxs-lookup"><span data-stu-id="73cc1-109">Name</span></span></p></th>
<th><p><span data-ttu-id="73cc1-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="73cc1-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="73cc1-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="73cc1-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="73cc1-112">Описание</span><span class="sxs-lookup"><span data-stu-id="73cc1-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73cc1-113">Имя</span><span class="sxs-lookup"><span data-stu-id="73cc1-113">Name</span></span></p></td>
<td><p><span data-ttu-id="73cc1-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="73cc1-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="73cc1-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="73cc1-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="73cc1-116"><strong>Строка</strong> , уникальным образом новый объект <strong>свойство</strong> .</span><span class="sxs-lookup"><span data-stu-id="73cc1-116">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="73cc1-117">Свойство <strong>Name</strong> для получения дополнительных сведений см на допустимый имена <strong>свойств</strong> .</span><span class="sxs-lookup"><span data-stu-id="73cc1-117">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73cc1-118">Тип</span><span class="sxs-lookup"><span data-stu-id="73cc1-118">Type</span></span></p></td>
<td><p><span data-ttu-id="73cc1-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="73cc1-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="73cc1-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="73cc1-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="73cc1-121">Константа, которая определяет тип данных нового <strong>Свойства</strong> объекта.</span><span class="sxs-lookup"><span data-stu-id="73cc1-121">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="73cc1-122">В разделе свойства <strong><a href="field-type-property-dao.md">Type</a></strong> для типов данных.</span><span class="sxs-lookup"><span data-stu-id="73cc1-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73cc1-123">Значение</span><span class="sxs-lookup"><span data-stu-id="73cc1-123">Value</span></span></p></td>
<td><p><span data-ttu-id="73cc1-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="73cc1-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="73cc1-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="73cc1-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="73cc1-126"><strong>Variant</strong> содержащий исходное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="73cc1-126">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="73cc1-127">Свойство <strong><a href="field-value-property-dao.md">Value</a></strong> для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="73cc1-127">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73cc1-128">DDL</span><span class="sxs-lookup"><span data-stu-id="73cc1-128">DDL</span></span></p></td>
<td><p><span data-ttu-id="73cc1-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="73cc1-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="73cc1-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="73cc1-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="73cc1-131"><strong>Variant</strong> (<strong>логическое</strong> подтип), которое указывает, является ли <strong>свойство</strong> объектом DDL.</span><span class="sxs-lookup"><span data-stu-id="73cc1-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="73cc1-132">Значение по умолчанию — <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="73cc1-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="73cc1-133">Если DDL имеет <strong>значение True</strong>, пользователи не могут изменить и удалить этот объект <strong>Свойства</strong> , если у них есть разрешение <strong>dbSecWriteDef</strong> .</span><span class="sxs-lookup"><span data-stu-id="73cc1-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="73cc1-134"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="73cc1-134"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="73cc1-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73cc1-135">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="73cc1-136">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="73cc1-136">Return value</span></span>
>>>>>>> <span data-ttu-id="73cc1-137">master</span><span class="sxs-lookup"><span data-stu-id="73cc1-137">master</span></span>

<span data-ttu-id="73cc1-138">Свойство</span><span class="sxs-lookup"><span data-stu-id="73cc1-138">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="73cc1-139">Замечания</span><span class="sxs-lookup"><span data-stu-id="73cc1-139">Remarks</span></span>

<span data-ttu-id="73cc1-140">Объект пользовательских **свойств** можно создать только в коллекции **[свойств](properties-collection-dao.md)** объекта, который является постоянным.</span><span class="sxs-lookup"><span data-stu-id="73cc1-140">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="73cc1-141">Если при использовании **CreateProperty**опустить одно или несколько частей необязательно, можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="73cc1-141">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="73cc1-142">После добавления объекта, можно изменить некоторые, но не для всех параметров его свойств.</span><span class="sxs-lookup"><span data-stu-id="73cc1-142">After you append the object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="73cc1-143">Обратитесь к соответствующим разделам **имя**, **Тип**и **значение** свойства для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="73cc1-143">See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="73cc1-144">Если имя ссылается на объект, который уже входит в коллекции, то во время выполнения возникает ошибка при использовании метода **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="73cc1-144">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="73cc1-145">Чтобы удалить объект пользовательских **свойств** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** на **[Properties](properties-collection-dao.md)** collection.</span><span class="sxs-lookup"><span data-stu-id="73cc1-145">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **[Properties](properties-collection-dao.md)** collection.</span></span> <span data-ttu-id="73cc1-146">Не удается удалить встроенные свойства.</span><span class="sxs-lookup"><span data-stu-id="73cc1-146">You can't delete built-in properties.</span></span>


> [!NOTE]
> <P><span data-ttu-id="73cc1-147">Если опустить аргумент DDL по умолчанию используется значение False (не являющиеся DDL).</span><span class="sxs-lookup"><span data-stu-id="73cc1-147">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="73cc1-148">Так как не соответствующее свойство DDL предоставляется, необходимо удалить и повторно создать объект <STRONG>свойств</STRONG> , чтобы перейти с DDL не DDL.</span><span class="sxs-lookup"><span data-stu-id="73cc1-148">Because no corresponding DDL property is exposed, you must delete and re-create a <STRONG>Property</STRONG> object you want to change from DDL to non-DDL.</span></span></P>


