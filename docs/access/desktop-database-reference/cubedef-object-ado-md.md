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
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719906"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="8c34e-102">Объект CubeDef (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="8c34e-102">CubeDef object (ADO MD)</span></span>


<span data-ttu-id="8c34e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="8c34e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="8c34e-104">Представляет куб из многомерных схемы, содержащая набор связанных измерений.</span><span class="sxs-lookup"><span data-stu-id="8c34e-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c34e-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="8c34e-105">Remarks</span></span>

<span data-ttu-id="8c34e-106">Со свойствами объекта **CubeDef** и семейств сайтов выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="8c34e-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="8c34e-107">Определение **CubeDef** с помощью свойства [Name](name-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8c34e-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="8c34e-108">Возвращает строку, которая описывает куба с помощью свойства [Description](description-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8c34e-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="8c34e-109">Возвращает измерения, которые будут включены в куб с коллекцией [измерения](dimensions-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="8c34e-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="8c34e-110">Получение дополнительных сведений о **CubeDef** с помощью стандартных ADO [Свойства](properties-collection-ado.md) коллекции.</span><span class="sxs-lookup"><span data-stu-id="8c34e-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="8c34e-111">Коллекции **свойств** содержит свойства, предоставленных поставщиком.</span><span class="sxs-lookup"><span data-stu-id="8c34e-111">The **Properties** collection contains provider-supplied properties.</span></span> <span data-ttu-id="8c34e-112">В следующей таблице перечислены свойства, которые могут быть недоступны.</span><span class="sxs-lookup"><span data-stu-id="8c34e-112">The following table lists properties that might be available.</span></span> <span data-ttu-id="8c34e-113">Список свойств фактический может различаться в зависимости от реализации поставщика.</span><span class="sxs-lookup"><span data-stu-id="8c34e-113">The actual property list may differ depending upon the implementation of the provider.</span></span> <span data-ttu-id="8c34e-114">Обратитесь к документации вашего поставщика для получения более полного списка доступных свойств.</span><span class="sxs-lookup"><span data-stu-id="8c34e-114">See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="8c34e-115">Имя</span><span class="sxs-lookup"><span data-stu-id="8c34e-115">Name</span></span></p></th>
<th><p><span data-ttu-id="8c34e-116">Описание</span><span class="sxs-lookup"><span data-stu-id="8c34e-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c34e-117">ИмяКаталога</span><span class="sxs-lookup"><span data-stu-id="8c34e-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="8c34e-118">Имя каталога, к которому принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="8c34e-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c34e-119">CreatedOn</span><span class="sxs-lookup"><span data-stu-id="8c34e-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="8c34e-120">Дата и время создания куба.</span><span class="sxs-lookup"><span data-stu-id="8c34e-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c34e-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="8c34e-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="8c34e-122">Куб GUID.</span><span class="sxs-lookup"><span data-stu-id="8c34e-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c34e-123">Имя куба</span><span class="sxs-lookup"><span data-stu-id="8c34e-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="8c34e-124">Имя куба.</span><span class="sxs-lookup"><span data-stu-id="8c34e-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c34e-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="8c34e-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="8c34e-126">Тип куба.</span><span class="sxs-lookup"><span data-stu-id="8c34e-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c34e-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="8c34e-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="8c34e-128">Идентификатор пользователя пользователь, выполняющий последнего обновления данных.</span><span class="sxs-lookup"><span data-stu-id="8c34e-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c34e-129">Описание</span><span class="sxs-lookup"><span data-stu-id="8c34e-129">Description</span></span></p></td>
<td><p><span data-ttu-id="8c34e-130">Понятное описание куба.</span><span class="sxs-lookup"><span data-stu-id="8c34e-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c34e-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="8c34e-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="8c34e-132">Дата и время последнего обновления схемы.</span><span class="sxs-lookup"><span data-stu-id="8c34e-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c34e-133">SchemaName</span><span class="sxs-lookup"><span data-stu-id="8c34e-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="8c34e-134">Имя схемы, к которой принадлежит этот куб.</span><span class="sxs-lookup"><span data-stu-id="8c34e-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c34e-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="8c34e-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="8c34e-136">Идентификатор пользователя пользователь, выполняющий последнее обновление схемы.</span><span class="sxs-lookup"><span data-stu-id="8c34e-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

