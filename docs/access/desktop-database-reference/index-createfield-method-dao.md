---
title: Метод index. CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: fc82b785-8768-b144-a2a4-c1f1798865a6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff837208(v=office.15)
ms:contentKeyID: 48548892
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aedda14273446ff6823776e535eb7995aa127fa5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32291833"
---
# <a name="indexcreatefield-method-dao"></a><span data-ttu-id="42b4a-102">Метод index. CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="42b4a-102">Index.CreateField method (DAO)</span></span>

<span data-ttu-id="42b4a-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="42b4a-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="42b4a-104">Создает новый объект **[Field](field-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="42b4a-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="42b4a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="42b4a-105">Syntax</span></span>

<span data-ttu-id="42b4a-106">*Expression* . CreateField (***имя***, ***тип***, ***Размер***)</span><span class="sxs-lookup"><span data-stu-id="42b4a-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="42b4a-107">*Expression (выражение* ) Переменная, представляющая объект **индекса** .</span><span class="sxs-lookup"><span data-stu-id="42b4a-107">*expression* A variable that represents an **Index** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="42b4a-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="42b4a-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="42b4a-109">Имя</span><span class="sxs-lookup"><span data-stu-id="42b4a-109">Name</span></span></p></th>
<th><p><span data-ttu-id="42b4a-110">Обязательный/необязательный</span><span class="sxs-lookup"><span data-stu-id="42b4a-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="42b4a-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="42b4a-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="42b4a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="42b4a-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="42b4a-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="42b4a-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="42b4a-114">Необязательно заполнять.</span><span class="sxs-lookup"><span data-stu-id="42b4a-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="42b4a-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="42b4a-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="42b4a-116">Строка, присваивающая уникальное имя новому объекту <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="42b4a-116">A String that uniquely names the new <strong>Field</strong> object.</span></span> <span data-ttu-id="42b4a-117">См. свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения более подробных сведений о допустимых именах <strong>Field</strong>.</span><span class="sxs-lookup"><span data-stu-id="42b4a-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="42b4a-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="42b4a-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="42b4a-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="42b4a-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="42b4a-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="42b4a-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="42b4a-121">Аргумент не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="42b4a-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="42b4a-122"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="42b4a-122"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="42b4a-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="42b4a-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="42b4a-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="42b4a-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="42b4a-125">Аргумент не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="42b4a-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="42b4a-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42b4a-126">Return value</span></span>

<span data-ttu-id="42b4a-127">Поле</span><span class="sxs-lookup"><span data-stu-id="42b4a-127">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="42b4a-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="42b4a-128">Remarks</span></span>

<span data-ttu-id="42b4a-129">Можно использовать метод **CreateField**, чтобы создать новое поле, а также указать имя, тип данных и размер поля.</span><span class="sxs-lookup"><span data-stu-id="42b4a-129">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field.</span></span> <span data-ttu-id="42b4a-130">Если опустить одну или несколько необязательных частей при использовании метода **CreateField**, вы можете воспользоваться соответствующим оператором присваивания, чтобы задать или сбросить соответствующее свойство перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="42b4a-130">If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="42b4a-131">После добавления нового объекта вы можете изменять некоторые, но не все параметры его свойств.</span><span class="sxs-lookup"><span data-stu-id="42b4a-131">After you append the new object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="42b4a-132">См. разделы для отдельных свойств для получения дополнительных данных.</span><span class="sxs-lookup"><span data-stu-id="42b4a-132">See the individual property topics for more details.</span></span>

<span data-ttu-id="42b4a-133">Аргументы Type и size применяются только к объектам **field** в объекте **tabledef** .</span><span class="sxs-lookup"><span data-stu-id="42b4a-133">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="42b4a-134">Эти аргументы игнорируются, если объект **Field** связан с объектом **Index** или **Relation**.</span><span class="sxs-lookup"><span data-stu-id="42b4a-134">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="42b4a-135">Если имя ссылается на объект, который уже является членом коллекции, при использовании метода **[append](fields-append-method-dao.md)** возникает ошибка во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="42b4a-135">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="42b4a-136">Чтобы удалить объект **Field** из коллекции **Fields**, используйте метод **[Delete](fields-delete-method-dao.md)** для коллекции.</span><span class="sxs-lookup"><span data-stu-id="42b4a-136">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span> <span data-ttu-id="42b4a-137">Вы не можете удалить объект **Field** из коллекции **Fields** объекта **TableDef** после создания индекса, ссылающегося на поле.</span><span class="sxs-lookup"><span data-stu-id="42b4a-137">You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

