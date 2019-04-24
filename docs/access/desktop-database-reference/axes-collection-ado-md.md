---
title: Коллекция осей (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 8183b0bad1dcbaba33088dffcf21959f5b9fd993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32296936"
---
# <a name="axes-collection-ado-md"></a><span data-ttu-id="d678f-102">Коллекция осей (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="d678f-102">Axes collection (ADO MD)</span></span>


<span data-ttu-id="d678f-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="d678f-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d678f-104">Содержит объекты [осей](axis-object-ado-md.md) , определяющие набор ячеек.</span><span class="sxs-lookup"><span data-stu-id="d678f-104">Contains the [Axis](axis-object-ado-md.md) objects that define a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="d678f-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="d678f-105">Remarks</span></span>

<span data-ttu-id="d678f-106">Объект набора [ячеек](cellset-object-ado-md.md) содержит коллекцию **осей** .</span><span class="sxs-lookup"><span data-stu-id="d678f-106">A [Cellset](cellset-object-ado-md.md) object contains an **Axes** collection.</span></span> <span data-ttu-id="d678f-107">После открытия набора **ячеек** эта коллекция будет содержать по крайней мере одну **ось**.</span><span class="sxs-lookup"><span data-stu-id="d678f-107">Once the **Cellset** is opened, this collection will contain at least one **Axis**.</span></span> <span data-ttu-id="d678f-108">Более подробное описание использования объектов **осей** показано на объекте [Axis](axis-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="d678f-108">See the [Axis](axis-object-ado-md.md) object for a more detailed explanation of how to use **Axis** objects.</span></span>


> [!NOTE]
> <span data-ttu-id="d678f-109">Ось фильтра для набора **ячеек** не находится в коллекции **осей** .</span><span class="sxs-lookup"><span data-stu-id="d678f-109">The filter axis of a **Cellset** is not contained in the **Axes** collection.</span></span> <span data-ttu-id="d678f-110">Дополнительные сведения см. в свойстве [FilterAxis](filteraxis-property-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="d678f-110">See the [FilterAxis](filteraxis-property-ado-md.md) property for more information.</span></span>



<span data-ttu-id="d678f-111">**Оси** — это стандартная коллекция ADO.</span><span class="sxs-lookup"><span data-stu-id="d678f-111">**Axes** is a standard ADO collection.</span></span> <span data-ttu-id="d678f-112">С помощью свойств и методов коллекции можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d678f-112">With the properties and methods of a collection, you can do the following:</span></span>

- <span data-ttu-id="d678f-113">Получите число объектов в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d678f-113">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="d678f-114">Возвращает объект из коллекции со свойством [Item](item-property-ado.md) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d678f-114">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="d678f-115">Обновление объектов в коллекции от поставщика с помощью метода [Refresh](refresh-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="d678f-115">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

