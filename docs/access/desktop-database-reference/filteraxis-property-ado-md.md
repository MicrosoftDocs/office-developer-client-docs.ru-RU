---
title: Свойство FilterAxis (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 214de72e71a51c6b6b65bc2636a28e5650035c0a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926908"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="3433e-102">Свойство FilterAxis (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="3433e-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="3433e-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="3433e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="3433e-104">Указывает фильтр сведений о текущем ячеек.</span><span class="sxs-lookup"><span data-stu-id="3433e-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="3433e-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="3433e-105">Return values</span></span>

<span data-ttu-id="3433e-106">Возвращает объект [ось](axis-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3433e-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="3433e-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="3433e-107">Remarks</span></span>

<span data-ttu-id="3433e-108">Свойство **FilterAxis** используется для возвращения сведений о измерений, которые использовались для среза данных.</span><span class="sxs-lookup"><span data-stu-id="3433e-108">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data.</span></span> <span data-ttu-id="3433e-109">Свойство [DimensionCount](dimensioncount-property-ado-md.md) **ось** возвращает число измерений, срез.</span><span class="sxs-lookup"><span data-stu-id="3433e-109">The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions.</span></span> <span data-ttu-id="3433e-110">В этом ось обычно имеет только одну строку.</span><span class="sxs-lookup"><span data-stu-id="3433e-110">This axis usually has just one row.</span></span>

<span data-ttu-id="3433e-111">**Ось** , возвращаемые [FilterAxis](filteraxis-property-ado-md.md) не содержащихся в коллекции [осей](axes-collection-ado-md.md) для объекта [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="3433e-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

