---
title: Count Property (ADO)
TOCTitle: Count Property (ADO)
ms:assetid: b59f9581-ffd1-471d-44fa-3c1bb812e140
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249871(v=office.15)
ms:contentKeyID: 48547253
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: ad02d854a560e3fa99bf7454c97083e88638c520
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2018
ms.locfileid: "25481376"
---
# <a name="count-property-ado"></a><span data-ttu-id="6563c-102">Count Property (ADO)</span><span class="sxs-lookup"><span data-stu-id="6563c-102">Count Property (ADO)</span></span>


<span data-ttu-id="6563c-103">**Применимо к**: Access 2013 | Office 2013</span><span class="sxs-lookup"><span data-stu-id="6563c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="6563c-104">Указывает число объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="6563c-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="6563c-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6563c-105">Return Value</span></span>

<span data-ttu-id="6563c-106">Возвращает значение типа **Long** .</span><span class="sxs-lookup"><span data-stu-id="6563c-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6563c-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="6563c-107">Remarks</span></span>

<span data-ttu-id="6563c-108">Используйте свойство **Count** для определения количества объектов в данной коллекции.</span><span class="sxs-lookup"><span data-stu-id="6563c-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="6563c-109">Поскольку нумерация для элементов коллекции начинается с нуля, всегда должны кода циклов, начиная с нуля элемента и заканчивая значение свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="6563c-109">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="6563c-110">Если используется Microsoft Visual Basic и хотите выполняют цикл по элементам коллекции без проверки свойство **Count** , используйте **для** **каждого... Далее** команды.</span><span class="sxs-lookup"><span data-stu-id="6563c-110">If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="6563c-111">Если свойство **Count** равно нулю, нет объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="6563c-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

