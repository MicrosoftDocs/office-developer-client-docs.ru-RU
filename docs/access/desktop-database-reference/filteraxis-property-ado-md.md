---
title: FilterAxis Property (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32ddf737ae0d6aa9a7b2daf8adc2a07707c91c0c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603058"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="3f862-102">FilterAxis Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3f862-102">FilterAxis Property (ADO MD)</span></span>


<span data-ttu-id="3f862-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="3f862-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="3f862-104">Указывает фильтр сведений о текущем ячеек.</span><span class="sxs-lookup"><span data-stu-id="3f862-104">Indicates filter information about the current cellset.</span></span>

<span data-ttu-id="3f862-105"><<<<<<< HEAD</span><span class="sxs-lookup"><span data-stu-id="3f862-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="3f862-106">Return Values</span><span class="sxs-lookup"><span data-stu-id="3f862-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="3f862-107">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3f862-107">Return values</span></span>
>>>>>>> <span data-ttu-id="3f862-108">master</span><span class="sxs-lookup"><span data-stu-id="3f862-108">master</span></span>

<span data-ttu-id="3f862-109">Возвращает объект [ось](axis-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3f862-109">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f862-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="3f862-110">Remarks</span></span>

<span data-ttu-id="3f862-111">Свойство **FilterAxis** используется для возвращения сведений о измерений, которые использовались для среза данных.</span><span class="sxs-lookup"><span data-stu-id="3f862-111">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data.</span></span> <span data-ttu-id="3f862-112">Свойство [DimensionCount](dimensioncount-property-ado-md.md) **ось** возвращает число измерений, срез.</span><span class="sxs-lookup"><span data-stu-id="3f862-112">The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions.</span></span> <span data-ttu-id="3f862-113">В этом ось обычно имеет только одну строку.</span><span class="sxs-lookup"><span data-stu-id="3f862-113">This axis usually has just one row.</span></span>

<span data-ttu-id="3f862-114">**Ось** , возвращаемые [FilterAxis](filteraxis-property-ado-md.md) не содержащихся в коллекции [осей](axes-collection-ado-md.md) для объекта [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="3f862-114">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

