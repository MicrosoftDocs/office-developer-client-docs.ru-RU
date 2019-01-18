---
title: Свойство LevelDepth (ADO MD)
TOCTitle: LevelDepth property (ADO MD)
ms:assetid: ba680f1e-2731-ad6b-4cee-cd3d8d114788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249894(v=office.15)
ms:contentKeyID: 48547366
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 664a21f8b642c8db27580993089268e5d7b6f4ae
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ru-RU
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708566"
---
# <a name="leveldepth-property-ado-md"></a><span data-ttu-id="752ed-102">Свойство LevelDepth (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="752ed-102">LevelDepth property (ADO MD)</span></span>


<span data-ttu-id="752ed-103">**Применимо к**: Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="752ed-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="752ed-104">Показывает, сколько уровней между корень иерархии и участником.</span><span class="sxs-lookup"><span data-stu-id="752ed-104">Indicates the number of levels between the root of the hierarchy and a member.</span></span>

## <a name="return-values"></a><span data-ttu-id="752ed-105">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="752ed-105">Return values</span></span>

<span data-ttu-id="752ed-106">Возвращает **длинное** целое и доступен только для чтения.</span><span class="sxs-lookup"><span data-stu-id="752ed-106">Returns a **Long** integer, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="752ed-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="752ed-107">Remarks</span></span>

<span data-ttu-id="752ed-108">Свойство **LevelDepth** используется для определения расстояния объект [члена](member-object-ado-md.md) на корневом уровне иерархии.</span><span class="sxs-lookup"><span data-stu-id="752ed-108">Use the **LevelDepth** property to determine the distance of the [Member](member-object-ado-md.md) object from the root level of the hierarchy.</span></span> <span data-ttu-id="752ed-109">**LevelDepth** элемента на корневом уровне равно 0.</span><span class="sxs-lookup"><span data-stu-id="752ed-109">The **LevelDepth** of a member at the root level is 0.</span></span> <span data-ttu-id="752ed-110">Это соответствует свойству [глубину](depth-property-ado-md.md) объекта [уровень](level-object-ado-md.md) .</span><span class="sxs-lookup"><span data-stu-id="752ed-110">This corresponds to the [Depth](depth-property-ado-md.md) property of a [Level](level-object-ado-md.md) object.</span></span>

