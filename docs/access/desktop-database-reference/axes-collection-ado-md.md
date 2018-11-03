---
title: Коллекция Axes (ADO MD)
TOCTitle: Axes collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: b7e7c9b82a1613f9f3d17a1da3e637f9f9382693
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944342"
---
# <a name="axes-collection-ado-md"></a><span data-ttu-id="2c779-102">Коллекция Axes (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="2c779-102">Axes collection (ADO MD)</span></span>


<span data-ttu-id="2c779-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="2c779-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2c779-104">Содержит объекты [ось](axis-object-ado-md.md) , определяющие набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="2c779-104">Contains the [Axis](axis-object-ado-md.md) objects that define a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="2c779-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="2c779-105">Remarks</span></span>

<span data-ttu-id="2c779-106">Объект [ячеек](cellset-object-ado-md.md) содержит коллекцию **осей** .</span><span class="sxs-lookup"><span data-stu-id="2c779-106">A [Cellset](cellset-object-ado-md.md) object contains an **Axes** collection.</span></span> <span data-ttu-id="2c779-107">После запуска **ячеек** этой коллекции будет содержать по крайней мере один **оси**.</span><span class="sxs-lookup"><span data-stu-id="2c779-107">Once the **Cellset** is opened, this collection will contain at least one **Axis**.</span></span> <span data-ttu-id="2c779-108">В разделе [ось](axis-object-ado-md.md) объект для подробное объяснение того, как использовать объекты **оси** .</span><span class="sxs-lookup"><span data-stu-id="2c779-108">See the [Axis](axis-object-ado-md.md) object for a more detailed explanation of how to use **Axis** objects.</span></span>


> [!NOTE]
> <span data-ttu-id="2c779-109">Оси фильтра набора **ячеек** не содержащихся в коллекции **осей** .</span><span class="sxs-lookup"><span data-stu-id="2c779-109">The filter axis of a **Cellset** is not contained in the **Axes** collection.</span></span> <span data-ttu-id="2c779-110">Свойству [FilterAxis](filteraxis-property-ado-md.md) для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="2c779-110">See the [FilterAxis](filteraxis-property-ado-md.md) property for more information.</span></span>



<span data-ttu-id="2c779-111">**Осей** — это обычная коллекция ADO.</span><span class="sxs-lookup"><span data-stu-id="2c779-111">**Axes** is a standard ADO collection.</span></span> <span data-ttu-id="2c779-112">С помощью свойства и методы коллекции сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="2c779-112">With the properties and methods of a collection, you can do the following:</span></span>

- <span data-ttu-id="2c779-113">Получите число объектов в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2c779-113">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

- <span data-ttu-id="2c779-114">Возвращает объект из коллекции с помощью свойства [элемента](item-property-ado.md) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2c779-114">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

- <span data-ttu-id="2c779-115">Обновление объектов в коллекции от поставщика с помощью метода [обновления](refresh-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="2c779-115">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

