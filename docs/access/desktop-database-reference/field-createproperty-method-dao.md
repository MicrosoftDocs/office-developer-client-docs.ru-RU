---
title: Метод Field. CreateProperty (DAO)
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
# <a name="fieldcreateproperty-method-dao"></a><span data-ttu-id="4e318-102">Метод Field. CreateProperty (DAO)</span><span class="sxs-lookup"><span data-stu-id="4e318-102">Field.CreateProperty method (DAO)</span></span>


<span data-ttu-id="4e318-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="4e318-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4e318-104">Создает новый объект определяемого пользователем **[Свойства](property-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="4e318-104">Creates a new user-defined **[Property](property-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="4e318-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="4e318-105">Syntax</span></span>

<span data-ttu-id="4e318-106">*Expression* . CreateProperty (***имя***, ***Тип***, ***значение***, ***DDL***)</span><span class="sxs-lookup"><span data-stu-id="4e318-106">*expression* .CreateProperty(***Name***, ***Type***, ***Value***, ***DDL***)</span></span>

<span data-ttu-id="4e318-107">*выражение*: переменная, представляющая объект **Field**.</span><span class="sxs-lookup"><span data-stu-id="4e318-107">*expression* A variable that represents a **Field** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="4e318-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="4e318-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4e318-109">Имя</span><span class="sxs-lookup"><span data-stu-id="4e318-109">Name</span></span></p></th>
<th><p><span data-ttu-id="4e318-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="4e318-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="4e318-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="4e318-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="4e318-112">Описание</span><span class="sxs-lookup"><span data-stu-id="4e318-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4e318-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="4e318-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="4e318-114">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="4e318-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="4e318-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4e318-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4e318-116"><strong>Строка</strong> , которая уникально названа нового объекта <strong>Property</strong> .</span><span class="sxs-lookup"><span data-stu-id="4e318-116">A <strong>String</strong> that uniquely names the new <strong>Property</strong> object.</span></span> <span data-ttu-id="4e318-117">Сведения о допустимых именах <strong>свойств</strong> приведены в свойстве <strong>Name</strong> .</span><span class="sxs-lookup"><span data-stu-id="4e318-117">See the <strong>Name</strong> property for details on valid <strong>Property</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e318-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="4e318-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="4e318-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4e318-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="4e318-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4e318-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4e318-121">Константа, определяющая тип данных нового объекта <strong>Property</strong> .</span><span class="sxs-lookup"><span data-stu-id="4e318-121">A constant that defines the data type of the new <strong>Property</strong> object.</span></span> <span data-ttu-id="4e318-122">Допустимые типы данных см. в свойстве <strong><a href="field-type-property-dao.md">Type</a></strong>.</span><span class="sxs-lookup"><span data-stu-id="4e318-122">See the <strong><a href="field-type-property-dao.md">Type</a></strong> property for valid data types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4e318-123"><em>Value</em></span><span class="sxs-lookup"><span data-stu-id="4e318-123"><em>Value</em></span></span></p></td>
<td><p><span data-ttu-id="4e318-124">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4e318-124">Optional</span></span></p></td>
<td><p><span data-ttu-id="4e318-125"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4e318-125"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4e318-126"><strong>Переменная Variant</strong> , содержащая начальное значение свойства.</span><span class="sxs-lookup"><span data-stu-id="4e318-126">A <strong>Variant</strong> containing the initial property value.</span></span> <span data-ttu-id="4e318-127">Для получения подробных сведений просмотрите свойство <strong><a href="field-value-property-dao.md">value</a></strong> .</span><span class="sxs-lookup"><span data-stu-id="4e318-127">See the <strong><a href="field-value-property-dao.md">Value</a></strong> property for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4e318-128"><em>DLL</em></span><span class="sxs-lookup"><span data-stu-id="4e318-128"><em>DDL</em></span></span></p></td>
<td><p><span data-ttu-id="4e318-129">Необязательный</span><span class="sxs-lookup"><span data-stu-id="4e318-129">Optional</span></span></p></td>
<td><p><span data-ttu-id="4e318-130"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="4e318-130"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="4e318-131"><strong>Variant</strong> (<strong>логический</strong> подтип), указывающий, является ли <strong>свойство</strong> объектом DDL.</span><span class="sxs-lookup"><span data-stu-id="4e318-131">A <strong>Variant</strong> (<strong>Boolean</strong> subtype) that indicates whether or not the <strong>Property</strong> is a DDL object.</span></span> <span data-ttu-id="4e318-132">По умолчанию используется значение <strong>False</strong>.</span><span class="sxs-lookup"><span data-stu-id="4e318-132">The default is <strong>False</strong>.</span></span> <span data-ttu-id="4e318-133">Если DDL имеет <strong>значение true</strong>, пользователи не могут изменить или удалить этот объект <strong>Property</strong> , если у них нет разрешения <strong>дбсеквритедеф</strong> .</span><span class="sxs-lookup"><span data-stu-id="4e318-133">If DDL is <strong>True</strong>, users can't change or delete this <strong>Property</strong> object unless they have <strong>dbSecWriteDef</strong> permission.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="4e318-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4e318-134">Return value</span></span>

<span data-ttu-id="4e318-135">Свойство</span><span class="sxs-lookup"><span data-stu-id="4e318-135">Property</span></span>

## <a name="remarks"></a><span data-ttu-id="4e318-136">Примечания</span><span class="sxs-lookup"><span data-stu-id="4e318-136">Remarks</span></span>

<span data-ttu-id="4e318-137">Пользовательский объект **Свойства** можно создать только в коллекции **[свойств](properties-collection-dao.md)** сохраняемого объекта.</span><span class="sxs-lookup"><span data-stu-id="4e318-137">You can create a user-defined **Property** object only in the **[Properties](properties-collection-dao.md)** collection of an object that is persistent.</span></span>

<span data-ttu-id="4e318-138">Если опустить одну или несколько дополнительных частей при использовании **CreateProperty**, можно использовать соответствующий оператор присвоения для установки или сброса соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="4e318-138">If you omit one or more of the optional parts when you use **CreateProperty**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="4e318-139">После добавления объекта можно изменить не все параметры его свойств.</span><span class="sxs-lookup"><span data-stu-id="4e318-139">After you append the object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="4e318-140">Для получения дополнительных сведений ознакомьтесь с разделами свойства " **имя**", " **Тип**" и " **значение** ".</span><span class="sxs-lookup"><span data-stu-id="4e318-140">See the **Name**, **Type**, and **Value** property topics for more details.</span></span>

<span data-ttu-id="4e318-141">Если имя ссылается на объект, который уже является членом коллекции, при использовании метода **[append](fields-append-method-dao.md)** возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="4e318-141">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="4e318-142">Чтобы удалить объект определяемого пользователем **Свойства** из коллекции, используйте метод **[Delete](fields-delete-method-dao.md)** в коллекции **свойств** .</span><span class="sxs-lookup"><span data-stu-id="4e318-142">To remove a user-defined **Property** object from the collection, use the **[Delete](fields-delete-method-dao.md)** method on the **Properties** collection.</span></span> <span data-ttu-id="4e318-143">Невозможно удалить встроенные свойства.</span><span class="sxs-lookup"><span data-stu-id="4e318-143">You can't delete built-in properties.</span></span>


> [!NOTE]
> <span data-ttu-id="4e318-144">Если опустить аргумент DDL, по умолчанию используется значение false (не для DDL).</span><span class="sxs-lookup"><span data-stu-id="4e318-144">If you omit the DDL argument, it defaults to False (non-DDL).</span></span> <span data-ttu-id="4e318-145">Так как соответствующее свойство DDL не предоставлено, необходимо удалить и повторно создать объект **Свойства** , который нужно изменить с DDL на non-DDL.</span><span class="sxs-lookup"><span data-stu-id="4e318-145">Because no corresponding DDL property is exposed, you must delete and re-create a **Property** object you want to change from DDL to non-DDL.</span></span>


