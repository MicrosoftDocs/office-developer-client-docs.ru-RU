---
title: Свойство Count (ADO)
TOCTitle: Count property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: e2a341a82e5cdc9ed5a55ca9f4b80ba80c6875bf
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713536"
---
# <a name="count-property-ado"></a><span data-ttu-id="dcacb-102">Свойство Count (ADO)</span><span class="sxs-lookup"><span data-stu-id="dcacb-102">Count property (ADO)</span></span>


<span data-ttu-id="dcacb-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="dcacb-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dcacb-104">Указывает число объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="dcacb-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcacb-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcacb-105">Return value</span></span>

<span data-ttu-id="dcacb-106">Возвращает значение типа **Long** .</span><span class="sxs-lookup"><span data-stu-id="dcacb-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcacb-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="dcacb-107">Remarks</span></span>

<span data-ttu-id="dcacb-108">Используйте свойство **Count** для определения количества объектов в данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="dcacb-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="dcacb-109">Поскольку нумерация для элементов коллекции начинается с нуля, всегда должны кода циклов, начиная с нуля элемента и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="dcacb-109">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="dcacb-110">Если используется Microsoft Visual Basic и хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , используйте **для** **каждого... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="dcacb-110">If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="dcacb-111">Если свойство **Count** равно нулю, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="dcacb-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

