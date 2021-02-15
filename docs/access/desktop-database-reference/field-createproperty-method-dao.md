---
title: Метод Field.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: b3c1d303-7cab-89c3-8e90-f18a0445d304
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822050(v=office.15)
ms:contentKeyID: 48547202
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: b9a88dce09798fa05aa602799f18a22e28d39c53
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293142"
---
# <a name="fieldcreateproperty-method-dao"></a><span data-ttu-id="e51dc-102">Метод Field.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="e51dc-102">Field.CreateProperty method (DAO)</span></span>


<span data-ttu-id="e51dc-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="e51dc-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="e51dc-104">Создает объект свойства, определяемого **[пользователем](property-object-dao.md)** (только для рабочих пространств Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="e51dc-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="e51dc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e51dc-105">Syntax</span></span>

<span data-ttu-id="e51dc-106">*выражение .* CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="e51dc-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="e51dc-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="e51dc-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="e51dc-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="e51dc-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="e51dc-109">Имя</span><span class="sxs-lookup"><span data-stu-id="e51dc-109">Name</span></span></p></th>
<th><p><span data-ttu-id="e51dc-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="e51dc-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="e51dc-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="e51dc-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="e51dc-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e51dc-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e51dc-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="e51dc-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="e51dc-114">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="e51dc-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="e51dc-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e51dc-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e51dc-116"><strong>Строка,</strong> однозначно именовав новый <strong>объект Property.</strong></span><span class="sxs-lookup"><span data-stu-id="e51dc-116">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="e51dc-117">Сведения о <strong>допустимом</strong> имени свойства см. в свойстве <strong>Name.</strong></span><span class="sxs-lookup"><span data-stu-id="e51dc-117">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e51dc-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="e51dc-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="e51dc-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="e51dc-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="e51dc-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e51dc-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e51dc-121">Константа, которая определяет тип данных нового объекта <strong>Property.</strong></span><span class="sxs-lookup"><span data-stu-id="e51dc-121">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="e51dc-122">Допустимые типы данных см. в свойстве <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="e51dc-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e51dc-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="e51dc-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="e51dc-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="e51dc-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="e51dc-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e51dc-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e51dc-126"><strong>Вариант,</strong> содержащий начальное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="e51dc-126">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="e51dc-127">Подробные <strong><a href="field-value-property-dao.md">сведения см.</a></strong> в свойстве Value.</span><span class="sxs-lookup"><span data-stu-id="e51dc-127">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e51dc-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="e51dc-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="e51dc-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="e51dc-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="e51dc-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="e51dc-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="e51dc-131">Variant <strong></strong> (<strong>Boolean</strong> subtype), который указывает, является ли <strong>свойство</strong> объектом DDL.</span><span class="sxs-lookup"><span data-stu-id="e51dc-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="e51dc-132">Значение по умолчанию - <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="e51dc-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="e51dc-133">Если DDL <strong>имеет</strong>true, пользователи не могут изменить или удалить этот объект <strong>Property,</strong> если у них нет разрешения <strong>dbSecWriteDef.</strong></span><span class="sxs-lookup"><span data-stu-id="e51dc-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="e51dc-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e51dc-134">Return value</span></span>

<span data-ttu-id="e51dc-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="e51dc-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="e51dc-136">Заметки</span><span class="sxs-lookup"><span data-stu-id="e51dc-136">Remarks</span></span>

<span data-ttu-id="e51dc-137">Пользовательский объект **Property** можно создать только в коллекции **[свойств](properties-collection-dao.md)** сохраняемого объекта.</span><span class="sxs-lookup"><span data-stu-id="e51dc-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="e51dc-138">Если при использовании **CreateProperty** опустить одну или несколько необязательных частей, можно использовать соответствующий отчет о назначении, чтобы установить или сбросить соответствующее свойство перед тем, как приместь новый объект в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="e51dc-138">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="e51dc-139">После того как вы примесь к объекту, вы можете изменить некоторые, но не все параметры его свойств.</span><span class="sxs-lookup"><span data-stu-id="e51dc-139">After you append the object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="e51dc-140">Дополнительные сведения **см.** в под темах свойств **Name,** Type и **Value.**</span><span class="sxs-lookup"><span data-stu-id="e51dc-140">See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="e51dc-141">Если имя ссылается на объект, который уже является членом коллекции, при использовании метода **[Append](fields-append-method-dao.md)** возникает ошибка во время работы.</span><span class="sxs-lookup"><span data-stu-id="e51dc-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="e51dc-142">Чтобы удалить пользовательский объект **Property** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в **коллекции Properties.**</span><span class="sxs-lookup"><span data-stu-id="e51dc-142">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="e51dc-143">Встроенные свойства удалить нельзя.</span><span class="sxs-lookup"><span data-stu-id="e51dc-143">You can't delete built-in properties.</span></span>


> [!NOTE]
> <span data-ttu-id="e51dc-144">Если опустить аргумент DDL, он по умолчанию будет задаваем значение False (не DDL).</span><span class="sxs-lookup"><span data-stu-id="e51dc-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="e51dc-145">Так как соответствующее свойство DDL не выявилось, необходимо удалить и повторно создать объект **Property,** который нужно изменить с DDL на non-DDL.</span><span class="sxs-lookup"><span data-stu-id="e51dc-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


