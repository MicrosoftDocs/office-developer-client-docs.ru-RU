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
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="3cd36-102">Объект CubeDef (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3cd36-102">CubeDef object (ADO MD)</span></span>


<span data-ttu-id="3cd36-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3cd36-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3cd36-104">Представляет куб из многомерной схемы, содержащей набор связанных измерений.</span><span class="sxs-lookup"><span data-stu-id="3cd36-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="3cd36-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="3cd36-105">Remarks</span></span>

<span data-ttu-id="3cd36-106">С коллекциями и свойствами объекта **CubeDef** можно сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="3cd36-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="3cd36-107">Определите **CubeDef с** [свойством Name.](name-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="3cd36-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="3cd36-108">Верни строку, описываемую кубом с [свойством Description.](description-property-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="3cd36-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="3cd36-109">Возвращайте размеры, которые составляют куб в коллекции [Dimensions.](dimensions-collection-ado-md.md)</span><span class="sxs-lookup"><span data-stu-id="3cd36-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="3cd36-110">Получение дополнительных сведений **о CubeDef в** стандартной коллекции свойств [ADO.](properties-collection-ado.md)</span><span class="sxs-lookup"><span data-stu-id="3cd36-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="3cd36-111">Коллекция **свойств** содержит свойства, предоставленные поставщиком.</span><span class="sxs-lookup"><span data-stu-id="3cd36-111">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="3cd36-112">В следующей таблице перечислены свойства, которые могут быть доступны.</span><span class="sxs-lookup"><span data-stu-id="3cd36-112">The following table lists properties that might be available.</span></span> <span data-ttu-id="3cd36-113">Фактический список свойств может отличаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="3cd36-113">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="3cd36-114">Дополнительный список доступных свойств см. в документации для поставщика.</span><span class="sxs-lookup"><span data-stu-id="3cd36-114">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3cd36-115">Имя</span><span class="sxs-lookup"><span data-stu-id="3cd36-115">Name</span></span></p></th>
<th><p><span data-ttu-id="3cd36-116">Описание</span><span class="sxs-lookup"><span data-stu-id="3cd36-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3cd36-117">CatalogName</span><span class="sxs-lookup"><span data-stu-id="3cd36-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="3cd36-118">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="3cd36-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd36-119">CreatedOn</span><span class="sxs-lookup"><span data-stu-id="3cd36-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="3cd36-120">Дата и время создания куба.</span><span class="sxs-lookup"><span data-stu-id="3cd36-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd36-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="3cd36-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="3cd36-122">GUID Cube.</span><span class="sxs-lookup"><span data-stu-id="3cd36-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd36-123">CubeName</span><span class="sxs-lookup"><span data-stu-id="3cd36-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="3cd36-124">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="3cd36-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd36-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="3cd36-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="3cd36-126">Тип куба.</span><span class="sxs-lookup"><span data-stu-id="3cd36-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd36-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="3cd36-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="3cd36-128">Пользовательский ID пользователя, который делает последнее обновление данных.</span><span class="sxs-lookup"><span data-stu-id="3cd36-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd36-129">Description</span><span class="sxs-lookup"><span data-stu-id="3cd36-129">Description</span></span></p></td>
<td><p><span data-ttu-id="3cd36-130">Содержательное описание куба.</span><span class="sxs-lookup"><span data-stu-id="3cd36-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd36-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="3cd36-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="3cd36-132">Дата и время последнего обновления схемы.</span><span class="sxs-lookup"><span data-stu-id="3cd36-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3cd36-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="3cd36-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="3cd36-134">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="3cd36-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3cd36-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="3cd36-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="3cd36-136">Пользовательский ID пользователя, который делает последнее обновление схемы.</span><span class="sxs-lookup"><span data-stu-id="3cd36-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

