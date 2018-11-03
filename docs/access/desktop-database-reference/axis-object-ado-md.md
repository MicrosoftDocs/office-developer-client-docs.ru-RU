---
title: Объект Axis (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ba1e32c3d2638589675a45c7cbc5a3e722651358
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928434"
---
# <a name="axis-object-ado-md"></a><span data-ttu-id="cffc7-102">Объект Axis (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="cffc7-102">Axis object (ADO MD)</span></span>


<span data-ttu-id="cffc7-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="cffc7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="cffc7-104">Представляет позиционные или оси фильтра набора ячеек, содержащий выбранные элементы из одного или нескольких измерений.</span><span class="sxs-lookup"><span data-stu-id="cffc7-104">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="cffc7-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="cffc7-105">Remarks</span></span>

<span data-ttu-id="cffc7-106">Объект **оси** можно заключенный в коллекцию [осей](axes-collection-ado-md.md) или возвращается свойством [FilterAxis](filteraxis-property-ado-md.md) [ячеек](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="cffc7-106">An **Axis** object can be contained by an [Axes](axes-collection-ado-md.md) collection, or returned by the [FilterAxis](filteraxis-property-ado-md.md) property of a [Cellset](cellset-object-ado-md.md).</span></span>

<span data-ttu-id="cffc7-107">С помощью семейств сайтов и свойствам объекта **ось** сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="cffc7-107">With the collections and properties of an **Axis** object, you can do the following:</span></span>

  - <span data-ttu-id="cffc7-108">Определение **оси** с помощью свойства [Name](name-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="cffc7-108">Identify the **Axis** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="cffc7-109">Выполните итерацию по каждой позиции по **оси** с использованием [положения](positions-collection-ado-md.md) коллекции.</span><span class="sxs-lookup"><span data-stu-id="cffc7-109">Iterate through each position along an **Axis** using the [Positions](positions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="cffc7-110">Получите число измерений на **оси** со свойством [DimensionCount](dimensioncount-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="cffc7-110">Obtain the number of dimensions on the **Axis** with the [DimensionCount](dimensioncount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="cffc7-111">Получение атрибутов поставщика **ось** , коллекции стандартных ADO [Свойства](properties-collection-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="cffc7-111">Obtain provider-specific attributes of the **Axis** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

