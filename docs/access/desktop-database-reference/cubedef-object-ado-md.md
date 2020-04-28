---
title: Объект CubeDef (ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c82c95a430da76694fe26300e877e86f86a2eb4b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295312"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="440a5-102">Объект CubeDef (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="440a5-102">CubeDef object (ADO MD)</span></span>


<span data-ttu-id="440a5-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="440a5-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="440a5-104">Представляет куб из многомерной схемы, содержащий набор связанных измерений.</span><span class="sxs-lookup"><span data-stu-id="440a5-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="440a5-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="440a5-105">Remarks</span></span>

<span data-ttu-id="440a5-106">С помощью коллекций и свойств объекта **CubeDef** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="440a5-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="440a5-107">Определите **CubeDef** со свойством [Name](name-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="440a5-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="440a5-108">Возвращает строку, описывающую куб, с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="440a5-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="440a5-109">Возвращает измерения, составляющие куб, с коллекцией [измерений](dimensions-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="440a5-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="440a5-110">Получите дополнительные сведения о **CubeDef** с помощью стандартной коллекции [свойств](properties-collection-ado.md) ADO.</span><span class="sxs-lookup"><span data-stu-id="440a5-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="440a5-111">Коллекция **Properties** содержит свойства, предоставляемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="440a5-111">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="440a5-112">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="440a5-112">The following table lists properties that might be available.</span></span> <span data-ttu-id="440a5-113">Фактический список свойств может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="440a5-113">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="440a5-114">Просмотрите документацию для своего поставщика, чтобы получить полный список доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="440a5-114">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="440a5-115">Имя</span><span class="sxs-lookup"><span data-stu-id="440a5-115">Name</span></span></p></th>
<th><p><span data-ttu-id="440a5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="440a5-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="440a5-117">каталогнаме</span><span class="sxs-lookup"><span data-stu-id="440a5-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="440a5-118">Имя каталога, к которому принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="440a5-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="440a5-119">креатедон</span><span class="sxs-lookup"><span data-stu-id="440a5-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="440a5-120">Дата и время создания куба.</span><span class="sxs-lookup"><span data-stu-id="440a5-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="440a5-121">кубегуид</span><span class="sxs-lookup"><span data-stu-id="440a5-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="440a5-122">GUID Куба.</span><span class="sxs-lookup"><span data-stu-id="440a5-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="440a5-123">кубенаме</span><span class="sxs-lookup"><span data-stu-id="440a5-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="440a5-124">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="440a5-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="440a5-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="440a5-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="440a5-126">Тип куба.</span><span class="sxs-lookup"><span data-stu-id="440a5-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="440a5-127">датаупдатедби</span><span class="sxs-lookup"><span data-stu-id="440a5-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="440a5-128">Идентификатор пользователя, который выполняет Последнее обновление данных.</span><span class="sxs-lookup"><span data-stu-id="440a5-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="440a5-129">Описание</span><span class="sxs-lookup"><span data-stu-id="440a5-129">Description</span></span></p></td>
<td><p><span data-ttu-id="440a5-130">Понятное описание Куба.</span><span class="sxs-lookup"><span data-stu-id="440a5-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="440a5-131">ластсчемаупдате</span><span class="sxs-lookup"><span data-stu-id="440a5-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="440a5-132">Дата и время последнего обновления схемы.</span><span class="sxs-lookup"><span data-stu-id="440a5-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="440a5-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="440a5-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="440a5-134">Имя схемы, к которой принадлежит куб.</span><span class="sxs-lookup"><span data-stu-id="440a5-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="440a5-135">счемаупдатедби</span><span class="sxs-lookup"><span data-stu-id="440a5-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="440a5-136">Идентификатор пользователя, выполняющего Последнее обновление схемы.</span><span class="sxs-lookup"><span data-stu-id="440a5-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

