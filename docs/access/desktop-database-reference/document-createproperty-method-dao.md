---
title: Метод Document.CreateProperty (DAO)
TOCTitle: CreateProperty Method
ms:assetid: 834fda60-1edf-38df-a9a5-d9d15e55e425
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196739(v=office.15)
ms:contentKeyID: 48546003
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052967
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: d1e2e2200953580406dded7d5c014b533129b133
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32293821"
---
# <a name="documentcreateproperty-method-dao"></a><span data-ttu-id="05d3f-102">Метод Document.CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="05d3f-102">Document.CreateProperty method (DAO)</span></span>

<span data-ttu-id="05d3f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="05d3f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="05d3f-104">Создает новый объект Свойства, определенный **[пользователем](property-object-dao.md)** (только рабочие пространства Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="05d3f-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="05d3f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="05d3f-105">Syntax</span></span>

<span data-ttu-id="05d3f-106">*выражения* . CreateProperty(Имя , ***Тип***, ***Значение***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="05d3f-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="05d3f-107">*выражение* Переменная, представляюная объект **Document.**</span><span class="sxs-lookup"><span data-stu-id="05d3f-107">*expression* A variable that represents a **Document** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="05d3f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="05d3f-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="05d3f-109">Имя</span><span class="sxs-lookup"><span data-stu-id="05d3f-109">Name</span></span></p></th>
<th><p><span data-ttu-id="05d3f-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="05d3f-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="05d3f-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="05d3f-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="05d3f-112">Описание</span><span class="sxs-lookup"><span data-stu-id="05d3f-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="05d3f-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="05d3f-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="05d3f-114">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="05d3f-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="05d3f-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="05d3f-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="05d3f-116"><strong>Строка,</strong> уникально именуемая новым <strong>объектом Свойства.</strong></span><span class="sxs-lookup"><span data-stu-id="05d3f-116">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="05d3f-117">Сведения о <strong>допустимом</strong> имени свойства см. в свойстве <strong>Name.</strong></span><span class="sxs-lookup"><span data-stu-id="05d3f-117">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05d3f-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="05d3f-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="05d3f-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="05d3f-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="05d3f-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="05d3f-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="05d3f-121">Константа, определяемая типом данных нового объекта <strong>Property.</strong></span><span class="sxs-lookup"><span data-stu-id="05d3f-121">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="05d3f-122">Допустимые типы данных см. в свойстве <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="05d3f-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="05d3f-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="05d3f-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="05d3f-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="05d3f-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="05d3f-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="05d3f-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="05d3f-126"><strong>Вариант,</strong> содержащий начальное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="05d3f-126">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="05d3f-127">Сведения <strong><a href="field-value-property-dao.md">см.</a></strong> в свойстве Value.</span><span class="sxs-lookup"><span data-stu-id="05d3f-127">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="05d3f-128"><em>DDL</em></span><span class="sxs-lookup"><span data-stu-id="05d3f-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="05d3f-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="05d3f-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="05d3f-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="05d3f-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="05d3f-131"><strong>Подтип</strong> <strong>Variant (Boolean),</strong> который указывает, является ли <strong>свойство</strong> объектом DDL.</span><span class="sxs-lookup"><span data-stu-id="05d3f-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="05d3f-132">Значение по умолчанию - <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="05d3f-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="05d3f-133">Если DDL является <strong>true,</strong>пользователи не могут изменить или удалить этот объект <strong>Property,</strong> если у них нет <strong>разрешения dbSecWriteDef.</strong></span><span class="sxs-lookup"><span data-stu-id="05d3f-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="05d3f-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="05d3f-134">Return value</span></span>

<span data-ttu-id="05d3f-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="05d3f-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="05d3f-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="05d3f-136">Remarks</span></span>

<span data-ttu-id="05d3f-137">Вы можете создать объект **Свойства,** определенный пользователем, только в коллекции **[Свойств](properties-collection-dao.md)** сохраняемого объекта.</span><span class="sxs-lookup"><span data-stu-id="05d3f-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="05d3f-138">Если при использовании **CreateProperty** вы опустить одну или несколько необязательных частей, можно использовать соответствующее заявление о назначении, чтобы задать или сбросить соответствующее свойство, прежде чем примкнуть новый объект к коллекции.</span><span class="sxs-lookup"><span data-stu-id="05d3f-138">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="05d3f-139">После приложения объекта можно изменить некоторые параметры свойств, но не все.</span><span class="sxs-lookup"><span data-stu-id="05d3f-139">After you append the object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="05d3f-140">Дополнительные сведения см. в разделы **Имя,** **Тип** и **Значение** свойств.</span><span class="sxs-lookup"><span data-stu-id="05d3f-140">See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="05d3f-141">Если имя относится к объекту, который уже входит в коллекцию, при использовании метода **[Append](fields-append-method-dao.md)** возникает ошибка времени запуска.</span><span class="sxs-lookup"><span data-stu-id="05d3f-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="05d3f-142">Чтобы удалить определенный пользователем **объект Property** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции **Свойств.**</span><span class="sxs-lookup"><span data-stu-id="05d3f-142">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="05d3f-143">Вы не можете удалить встроенные свойства.</span><span class="sxs-lookup"><span data-stu-id="05d3f-143">You can't delete built-in properties.</span></span>


> [!NOTE]
> <span data-ttu-id="05d3f-144">Если упустить аргумент DDL, он по умолчанию будет ложным (не-DDL).</span><span class="sxs-lookup"><span data-stu-id="05d3f-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="05d3f-145">Поскольку соответствующее свойство DDL не подвергается воздействию, необходимо удалить и повторно создать объект **Property,** который необходимо изменить с DDL на non-DDL.</span><span class="sxs-lookup"><span data-stu-id="05d3f-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


