---
title: Свойство FilterAxis (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32292456"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="f0294-102">Свойство FilterAxis (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f0294-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="f0294-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="f0294-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f0294-104">Показывает данные фильтра о текущем наборе ячеек.</span><span class="sxs-lookup"><span data-stu-id="f0294-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="f0294-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="f0294-105">Return values</span></span>

<span data-ttu-id="f0294-106">Возвращает объект [Axis](axis-object-ado-md.md) и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="f0294-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="f0294-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="f0294-107">Remarks</span></span>

<span data-ttu-id="f0294-108">Используйте свойство **FilterAxis** , чтобы получить сведения об измерениях, использованных для среза данных.</span><span class="sxs-lookup"><span data-stu-id="f0294-108">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data.</span></span> <span data-ttu-id="f0294-109">Свойство [DimensionCount](dimensioncount-property-ado-md.md) **оси** возвращает число измерений среза.</span><span class="sxs-lookup"><span data-stu-id="f0294-109">The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions.</span></span> <span data-ttu-id="f0294-110">Эта ось обычно содержит только одну строку.</span><span class="sxs-lookup"><span data-stu-id="f0294-110">This axis usually has just one row.</span></span>

<span data-ttu-id="f0294-111">**Ось** , возвращаемая методом [FilterAxis](filteraxis-property-ado-md.md) , не входит в коллекцию [осей](axes-collection-ado-md.md) для объекта набора [ячеек](cellset-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="f0294-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

