---
title: Метод Relation.CreateField (DAO)
TOCTitle: CreateField Method
ms:assetid: bc60c91e-acef-1c90-7303-12f77cce15b8
ms:mtpsurl: https://msdn.microsoft.com/library/Ff822717(v=office.15)
ms:contentKeyID: 48547411
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: ae322277dd1d357aceb3f9129110dded705f9eca
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28716287"
---
# <a name="relationcreatefield-method-dao"></a><span data-ttu-id="7bdd5-102">Метод Relation.CreateField (DAO)</span><span class="sxs-lookup"><span data-stu-id="7bdd5-102">Relation.CreateField method (DAO)</span></span>

<span data-ttu-id="7bdd5-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="7bdd5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="7bdd5-104">Создает новый объект **[поля](field-object-dao.md)** (только для рабочих областей Microsoft Access).</span><span class="sxs-lookup"><span data-stu-id="7bdd5-104">Creates a new **[Field](field-object-dao.md)** object (Microsoft Access workspaces only).</span></span>

## <a name="syntax"></a><span data-ttu-id="7bdd5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7bdd5-105">Syntax</span></span>

<span data-ttu-id="7bdd5-106">*выражение* . CreateField (***имя***, ***Тип***, ***размер***)</span><span class="sxs-lookup"><span data-stu-id="7bdd5-106">*expression* .CreateField(***Name***, ***Type***, ***Size***)</span></span>

<span data-ttu-id="7bdd5-107">*выражение* Переменная, которая представляет собой объект- **связи** .</span><span class="sxs-lookup"><span data-stu-id="7bdd5-107">*expression* A variable that represents a **Relation** object.</span></span>

## <a name="parameters"></a><span data-ttu-id="7bdd5-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="7bdd5-108">Parameters</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7bdd5-109">Имя</span><span class="sxs-lookup"><span data-stu-id="7bdd5-109">Name</span></span></p></th>
<th><p><span data-ttu-id="7bdd5-110">Обязательный или необязательный</span><span class="sxs-lookup"><span data-stu-id="7bdd5-110">Required/optional</span></span></p></th>
<th><p><span data-ttu-id="7bdd5-111">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7bdd5-111">Data type</span></span></p></th>
<th><p><span data-ttu-id="7bdd5-112">Описание</span><span class="sxs-lookup"><span data-stu-id="7bdd5-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7bdd5-113"><em>Name</em></span><span class="sxs-lookup"><span data-stu-id="7bdd5-113"><em>Name</em></span></span></p></td>
<td><p><span data-ttu-id="7bdd5-114">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7bdd5-114">Optional</span></span></p></td>
<td><p><span data-ttu-id="7bdd5-115"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7bdd5-115"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7bdd5-116">Строка, уникальным образом новый объект <strong>поля</strong> .</span><span class="sxs-lookup"><span data-stu-id="7bdd5-116">A String that uniquely names the new <strong>Field</strong> object.</span></span> <span data-ttu-id="7bdd5-117">Свойство <strong><a href="connection-name-property-dao.md">Name</a></strong> для получения дополнительных сведений см на допустимый имена <strong>полей</strong> .</span><span class="sxs-lookup"><span data-stu-id="7bdd5-117">See the <strong><a href="connection-name-property-dao.md">Name</a></strong> property for details on valid <strong>Field</strong> names.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7bdd5-118"><em>Type</em></span><span class="sxs-lookup"><span data-stu-id="7bdd5-118"><em>Type</em></span></span></p></td>
<td><p><span data-ttu-id="7bdd5-119">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7bdd5-119">Optional</span></span></p></td>
<td><p><span data-ttu-id="7bdd5-120"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7bdd5-120"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7bdd5-121">Аргумент не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="7bdd5-121">Argument not supported for this object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7bdd5-122"><em>Size</em></span><span class="sxs-lookup"><span data-stu-id="7bdd5-122"><em>Size</em></span></span></p></td>
<td><p><span data-ttu-id="7bdd5-123">Необязательный</span><span class="sxs-lookup"><span data-stu-id="7bdd5-123">Optional</span></span></p></td>
<td><p><span data-ttu-id="7bdd5-124"><strong>Variant</strong></span><span class="sxs-lookup"><span data-stu-id="7bdd5-124"><strong>Variant</strong></span></span></p></td>
<td><p><span data-ttu-id="7bdd5-125">Аргумент не поддерживается для этого объекта.</span><span class="sxs-lookup"><span data-stu-id="7bdd5-125">Argument not supported for this object.</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="return-value"></a><span data-ttu-id="7bdd5-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7bdd5-126">Return value</span></span>

<span data-ttu-id="7bdd5-127">Поле</span><span class="sxs-lookup"><span data-stu-id="7bdd5-127">Field</span></span>

## <a name="remarks"></a><span data-ttu-id="7bdd5-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="7bdd5-128">Remarks</span></span>

<span data-ttu-id="7bdd5-129">Чтобы создать новое поле, а также указать имя, тип данных и размер поля можно использовать метод **CreateField** .</span><span class="sxs-lookup"><span data-stu-id="7bdd5-129">You can use the **CreateField** method to create a new field, as well as specify the name, data type, and size of the field.</span></span> <span data-ttu-id="7bdd5-130">Если опустить одно или несколько частей необязательно при использовании **CreateField**, можно использовать соответствующие присваивания установить или сбросить соответствующего свойства перед добавлением нового объекта в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="7bdd5-130">If you omit one or more of the optional parts when you use **CreateField**, you can use an appropriate assignment statement to set or reset the corresponding property before you append the new object to a collection.</span></span> <span data-ttu-id="7bdd5-131">После добавления нового объекта, можно изменить некоторые, но не для всех параметров его свойств.</span><span class="sxs-lookup"><span data-stu-id="7bdd5-131">After you append the new object, you can alter some but not all of its property settings.</span></span> <span data-ttu-id="7bdd5-132">Обратитесь к соответствующим разделам отдельных свойств для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="7bdd5-132">See the individual property topics for more details.</span></span>

<span data-ttu-id="7bdd5-133">Аргументы типа и размера, применяются только к объектам **поля** в объекте **TableDef** .</span><span class="sxs-lookup"><span data-stu-id="7bdd5-133">The type and size arguments apply only to **Field** objects in a **TableDef** object.</span></span> <span data-ttu-id="7bdd5-134">Пропускать следующие аргументы объекта **поля** связан с объектом **индекса** или **связи** .</span><span class="sxs-lookup"><span data-stu-id="7bdd5-134">These arguments are ignored when a **Field** object is associated with an **Index** or **Relation** object.</span></span>

<span data-ttu-id="7bdd5-135">Если имя ссылается на объект, который уже входит в коллекции, то во время выполнения возникает ошибка при использовании метода **[Append](fields-append-method-dao.md)** .</span><span class="sxs-lookup"><span data-stu-id="7bdd5-135">If name refers to an object that is already a member of the collection, a run-time error occurs when you use the **[Append](fields-append-method-dao.md)** method.</span></span>

<span data-ttu-id="7bdd5-136">Чтобы удалить объект **поля** из коллекции **полей** , используйте метод **[Delete](fields-delete-method-dao.md)** в семействе сайтов.</span><span class="sxs-lookup"><span data-stu-id="7bdd5-136">To remove a **Field** object from a **Fields** collection, use the **[Delete](fields-delete-method-dao.md)** method on the collection.</span></span> <span data-ttu-id="7bdd5-137">Невозможно удалить объект **поля** из коллекции **полей** объектов **TableDef** после создания индекса, которая ссылается на поле.</span><span class="sxs-lookup"><span data-stu-id="7bdd5-137">You can't delete a **Field** object from a **TableDef** object's **Fields** collection after you create an index that references the field.</span></span>

