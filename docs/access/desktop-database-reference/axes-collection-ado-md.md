---
title: Коллекция осей (ADO MD)
TOCTitle: Axes Collection (ADO MD)
ms:assetid: 7c719197-45f1-a5b9-665d-25cb693b1eb0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249520(v=office.15)
ms:contentKeyID: 48545836
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 612a78d8ac99a070f133fd3804f5b69c8093d47c
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/31/2018
ms.locfileid: "25862603"
---
# <a name="axes-collection-ado-md"></a><span data-ttu-id="91fbe-102">Коллекция осей (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="91fbe-102">Axes Collection (ADO MD)</span></span>


<span data-ttu-id="91fbe-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="91fbe-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="91fbe-104">Содержит объекты [ось](axis-object-ado-md.md) , определяющие набора ячеек.</span><span class="sxs-lookup"><span data-stu-id="91fbe-104">Contains the [Axis](axis-object-ado-md.md) objects that define a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="91fbe-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="91fbe-105">Remarks</span></span>

<span data-ttu-id="91fbe-106">Объект [ячеек](cellset-object-ado-md.md) содержит коллекцию **осей** .</span><span class="sxs-lookup"><span data-stu-id="91fbe-106">A [Cellset](cellset-object-ado-md.md) object contains an **Axes** collection.</span></span> <span data-ttu-id="91fbe-107">После запуска **ячеек** этой коллекции будет содержать по крайней мере один **оси**.</span><span class="sxs-lookup"><span data-stu-id="91fbe-107">Once the **Cellset** is opened, this collection will contain at least one **Axis**.</span></span> <span data-ttu-id="91fbe-108">В разделе [ось](axis-object-ado-md.md) объект для подробное объяснение того, как использовать объекты **оси** .</span><span class="sxs-lookup"><span data-stu-id="91fbe-108">See the [Axis](axis-object-ado-md.md) object for a more detailed explanation of how to use **Axis** objects.</span></span>


> [!NOTE]
> <span data-ttu-id="91fbe-109">Оси фильтра набора **ячеек** не содержащихся в коллекции **осей** .</span><span class="sxs-lookup"><span data-stu-id="91fbe-109">The filter axis of a **Cellset** is not contained in the **Axes** collection.</span></span> <span data-ttu-id="91fbe-110">Свойству [FilterAxis](filteraxis-property-ado-md.md) для получения дополнительных сведений см.</span><span class="sxs-lookup"><span data-stu-id="91fbe-110">See the [FilterAxis](filteraxis-property-ado-md.md) property for more information.</span></span>



<span data-ttu-id="91fbe-111">**Осей** — это обычная коллекция ADO.</span><span class="sxs-lookup"><span data-stu-id="91fbe-111">**Axes** is a standard ADO collection.</span></span> <span data-ttu-id="91fbe-112">С помощью свойства и методы коллекции сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="91fbe-112">With the properties and methods of a collection, you can do the following:</span></span>

  - <span data-ttu-id="91fbe-113">Получите число объектов в коллекции со свойством [Count](count-property-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="91fbe-113">Obtain the number of objects in the collection with the [Count](count-property-ado.md) property.</span></span>

  - <span data-ttu-id="91fbe-114">Возвращает объект из коллекции с помощью свойства [элемента](item-property-ado.md) по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="91fbe-114">Return an object from the collection with the default [Item](item-property-ado.md) property.</span></span>

  - <span data-ttu-id="91fbe-115">Обновление объектов в коллекции от поставщика с помощью метода [обновления](refresh-method-ado.md) .</span><span class="sxs-lookup"><span data-stu-id="91fbe-115">Update the objects in the collection from the provider with the [Refresh](refresh-method-ado.md) method.</span></span>

