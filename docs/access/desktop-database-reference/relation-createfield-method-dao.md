---
title: Relation.CreateField Method (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d86230f99afb95d121ea683ed4324d361b77757
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25602897"
---
# <a name="relationcreatefield-method-dao"></a><span data-ttu-id="b859c-102">Relation.CreateField Method (DAO)</span><span class="sxs-lookup"><span data-stu-id="b859c-102">Relation.CreateField Method (DAO)</span></span>


<span data-ttu-id="b859c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="b859c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="b859c-104">Создает новый объект **[поля](field-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="b859c-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="b859c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b859c-105">Syntax</span></span>

<span data-ttu-id="b859c-106">*выражение* . CreateField (***имя***, ***Тип***, ***размер***)</span><span class="sxs-lookup"><span data-stu-id="b859c-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="b859c-107">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="b859c-107">*expression* A variable that represents a **Relation** object.</span></span>

### <a name="parameters"></a><span data-ttu-id="b859c-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b859c-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="b859c-109">Имя</span><span class="sxs-lookup"><span data-stu-id="b859c-109">Name</span></span></p></th>
<th><p><span data-ttu-id="b859c-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="b859c-110">Required/Optional</span></span></p></th>
<th><p><span data-ttu-id="b859c-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b859c-111">Data Type</span></span></p></th>
<th><p><span data-ttu-id="b859c-112">Описание</span><span class="sxs-lookup"><span data-stu-id="b859c-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b859c-113">Имя</span><span class="sxs-lookup"><span data-stu-id="b859c-113">Name</span></span></p></td>
<td><p><span data-ttu-id="b859c-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b859c-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="b859c-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b859c-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b859c-116">Строка, уникальным образом новый объект <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="b859c-116">A String that uniquely names the new <strong>Field</strong> object.</span></span> <span data-ttu-id="b859c-117">Свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см на допустимый имена <strong>полей</strong> .</span><span class="sxs-lookup"><span data-stu-id="b859c-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b859c-118">Тип</span><span class="sxs-lookup"><span data-stu-id="b859c-118">Type</span></span></p></td>
<td><p><span data-ttu-id="b859c-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b859c-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="b859c-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b859c-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b859c-121">Аргумент не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="b859c-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b859c-122">Size</span><span class="sxs-lookup"><span data-stu-id="b859c-122">Size</span></span></p></td>
<td><p><span data-ttu-id="b859c-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="b859c-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="b859c-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="b859c-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="b859c-125">Аргумент не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="b859c-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b859c-126"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="b859c-126"><<<<<<< HEAD</span></span>
### <a name="return-value"></a><span data-ttu-id="b859c-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b859c-127">Return Value</span></span>
=======
### <a name="return-value"></a><span data-ttu-id="b859c-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b859c-128">Return value</span></span>
>>>>>>> <span data-ttu-id="b859c-129">master</span><span class="sxs-lookup"><span data-stu-id="b859c-129">master</span></span>

<span data-ttu-id="b859c-130">Поле</span><span class="sxs-lookup"><span data-stu-id="b859c-130">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="b859c-131">Замечания</span><span class="sxs-lookup"><span data-stu-id="b859c-131">Remarks</span></span>

<span data-ttu-id="b859c-132">Чтобы создать новое поле, а также указать имя, тип данных и размер поля можно использовать метод **CreateField** .</span><span class="sxs-lookup"><span data-stu-id="b859c-132">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field.</span></span> <span data-ttu-id="b859c-133">Если опустить одно или несколько частей необязательно при использовании **CreateField**, можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="b859c-133">If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="b859c-134">После добавления нового объекта, можно изменить некоторые, но не для всех параметров его свойств.</span><span class="sxs-lookup"><span data-stu-id="b859c-134">After you append the new object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="b859c-135">Обратитесь к соответствующим разделам отдельных свойств для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="b859c-135">See the individual property topics for more details.</span></span>

<span data-ttu-id="b859c-136">Аргументы типа и размера, применяются только к объектам **поля** в объекте **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="b859c-136">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="b859c-137">Пропускать следующие аргументы объекта **поля** связан с объектом **индекса** или **связи** .</span><span class="sxs-lookup"><span data-stu-id="b859c-137">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="b859c-138">Если имя ссылается на объект, который уже входит в коллекции, то во время выполнения возникает ошибка при использовании метода **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="b859c-138">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="b859c-139">Чтобы удалить объект **поля** из коллекции **полей** , используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="b859c-139">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span> <span data-ttu-id="b859c-140">Невозможно удалить объект **поля** из коллекции **полей** объектов **TableDef** после создания индекса, которая ссылается на поле.</span><span class="sxs-lookup"><span data-stu-id="b859c-140">You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

