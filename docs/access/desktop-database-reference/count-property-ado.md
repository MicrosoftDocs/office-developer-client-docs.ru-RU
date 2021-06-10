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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295473"
---
# <a name="count-property-ado"></a><span data-ttu-id="b0d60-102">Свойство Count (ADO)</span><span class="sxs-lookup"><span data-stu-id="b0d60-102">Count property (ADO)</span></span>


<span data-ttu-id="b0d60-103">**Область применения**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="b0d60-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="b0d60-104">Указывает количество объектов в коллекции.</span><span class="sxs-lookup"><span data-stu-id="b0d60-104">Indicates the number of objects in a collection.</span></span>

## <a name="return-value"></a><span data-ttu-id="b0d60-105">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b0d60-105">Return value</span></span>

<span data-ttu-id="b0d60-106">Возвращает значение **Long.**</span><span class="sxs-lookup"><span data-stu-id="b0d60-106">Returns a **Long** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0d60-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="b0d60-107">Remarks</span></span>

<span data-ttu-id="b0d60-108">Используйте свойство **Count,** чтобы определить, сколько объектов находится в заданной коллекции.</span><span class="sxs-lookup"><span data-stu-id="b0d60-108">Use the **Count** property to determine how many objects are in a given collection.</span></span>

<span data-ttu-id="b0d60-109">Так как нуминг для членов коллекции начинается с нуля, всегда следует использовать циклы кода, начиная с нулевого члена и заканчивая значением свойства **Count** минус 1.</span><span class="sxs-lookup"><span data-stu-id="b0d60-109">Because numbering for members of a collection begins with zero, you should always code loops starting with the zero member and ending with the value of the **Count** property minus 1.</span></span> <span data-ttu-id="b0d60-110">Если вы используете microsoft Visual Basic и хотите проциклить членов коллекции без проверки свойства **Count,** используйте **для каждого...** **Следующая** команда.</span><span class="sxs-lookup"><span data-stu-id="b0d60-110">If you are using Microsoft Visual Basic and want to loop through the members of a collection without checking the **Count** property, use the **For** **Each...Next** command.</span></span>

<span data-ttu-id="b0d60-111">Если свойство **Count** нулевое, в коллекции нет объектов.</span><span class="sxs-lookup"><span data-stu-id="b0d60-111">If the **Count** property is zero, there are no objects in the collection.</span></span>

