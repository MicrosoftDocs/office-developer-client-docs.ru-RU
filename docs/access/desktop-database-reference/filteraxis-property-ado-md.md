---
title: FilterAxis Property (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 912dfec595f718c2144e69b4fbd3af592f8b6d5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25480985"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="fdcef-102">FilterAxis Property (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="fdcef-102">FilterAxis Property (ADO MD)</span></span>


<span data-ttu-id="fdcef-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="fdcef-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="fdcef-104">Указывает фильтр сведений о текущем ячеек.</span><span class="sxs-lookup"><span data-stu-id="fdcef-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="fdcef-105">Return Values</span><span class="sxs-lookup"><span data-stu-id="fdcef-105">Return Values</span></span>

<span data-ttu-id="fdcef-106">Возвращает объект [ось](axis-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="fdcef-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdcef-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="fdcef-107">Remarks</span></span>

<span data-ttu-id="fdcef-108">Свойство **FilterAxis** используется для возвращения сведений о измерений, которые использовались для среза данных.</span><span class="sxs-lookup"><span data-stu-id="fdcef-108">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data.</span></span> <span data-ttu-id="fdcef-109">Свойство [DimensionCount](dimensioncount-property-ado-md.md) **ось** возвращает число измерений, срез.</span><span class="sxs-lookup"><span data-stu-id="fdcef-109">The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions.</span></span> <span data-ttu-id="fdcef-110">В этом ось обычно имеет только одну строку.</span><span class="sxs-lookup"><span data-stu-id="fdcef-110">This axis usually has just one row.</span></span>

<span data-ttu-id="fdcef-111">**Ось** , возвращаемые [FilterAxis](filteraxis-property-ado-md.md) не содержащихся в коллекции [осей](axes-collection-ado-md.md) для объекта [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="fdcef-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

