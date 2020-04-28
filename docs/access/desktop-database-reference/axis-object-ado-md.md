---
title: Объект Axis (ADO MD)
TOCTitle: Axis object (ADO MD)
ms:assetid: a4332b69-8900-08f1-a4e2-9395d005ed42
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249763(v=office.15)
ms:contentKeyID: 48546807
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 23fdb0d9ba636ae58fa19b42d5a8a47cb01d4ab2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296901"
---
# <a name="axis-object-ado-md"></a><span data-ttu-id="ab49e-102">Объект Axis (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="ab49e-102">Axis object (ADO MD)</span></span>


<span data-ttu-id="ab49e-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="ab49e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="ab49e-104">Представляет положение или ось фильтра для набора ячеек, содержащего выбранные элементы одного или нескольких измерений.</span><span class="sxs-lookup"><span data-stu-id="ab49e-104">Represents a positional or filter axis of a cellset, containing selected members of one or more dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab49e-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab49e-105">Remarks</span></span>

<span data-ttu-id="ab49e-106">Объект **Axis** может содержаться в коллекции [осей](axes-collection-ado-md.md) или возвращен свойством [FilterAxis](filteraxis-property-ado-md.md) набора [ячеек](cellset-object-ado-md.md).</span><span class="sxs-lookup"><span data-stu-id="ab49e-106">An **Axis** object can be contained by an [Axes](axes-collection-ado-md.md) collection, or returned by the [FilterAxis](filteraxis-property-ado-md.md) property of a [Cellset](cellset-object-ado-md.md).</span></span>

<span data-ttu-id="ab49e-107">С помощью коллекций и свойств объекта **Axis** можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ab49e-107">With the collections and properties of an **Axis** object, you can do the following:</span></span>

- <span data-ttu-id="ab49e-108">Определите **ось** со свойством [Name](name-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="ab49e-108">Identify the **Axis** with the [Name](name-property-ado-md.md) property.</span></span>

- <span data-ttu-id="ab49e-109">Выполните итерацию по каждой позиции вдоль **оси** с помощью коллекции [Positions](positions-collection-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="ab49e-109">Iterate through each position along an **Axis** using the [Positions](positions-collection-ado-md.md) collection.</span></span>

- <span data-ttu-id="ab49e-110">Получите количество измерений на **оси** со свойством [DimensionCount](dimensioncount-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="ab49e-110">Obtain the number of dimensions on the **Axis** with the [DimensionCount](dimensioncount-property-ado-md.md) property.</span></span>

- <span data-ttu-id="ab49e-111">Получите атрибуты **оси** , зависящие от поставщика, с помощью стандартной коллекции [свойств](properties-collection-ado.md) ADO.</span><span class="sxs-lookup"><span data-stu-id="ab49e-111">Obtain provider-specific attributes of the **Axis** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

