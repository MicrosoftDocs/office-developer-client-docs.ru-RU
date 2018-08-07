---
title: Ячейка SoftEdgesSize (раздел "Дополнительные свойства эффекта")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a5cde2ca-f343-4a6e-b5d9-a1b78b3cd240
description: Определяет размер эффекта программных пограничного сервера в пунктах от 0,00 для 100,00. Если ячейка SoftEdgesSize имеет значение 0, фигура не имеет сглаживание.
ms.openlocfilehash: 3b301ae2e8c82867be2a486f2e93c2275fbf3914
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814915"
---
# <a name="softedgessize-cell-additional-effect-properties-section"></a><span data-ttu-id="27215-104">Ячейка SoftEdgesSize (раздел "Дополнительные свойства эффекта")</span><span class="sxs-lookup"><span data-stu-id="27215-104">SoftEdgesSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="27215-105">Определяет размер эффекта программных пограничного сервера в пунктах от 0,00 для 100,00.</span><span class="sxs-lookup"><span data-stu-id="27215-105">Determines the size of a soft edge effect, in points from 0.00 to 100.00.</span></span> <span data-ttu-id="27215-106">Если ячейка **SoftEdgesSize** имеет значение 0, фигура не имеет сглаживание.</span><span class="sxs-lookup"><span data-stu-id="27215-106">If the **SoftEdgesSize** cell has a value of 0, the shape does not have soft edges.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="27215-107">Замечания</span><span class="sxs-lookup"><span data-stu-id="27215-107">Remarks</span></span>

<span data-ttu-id="27215-108">Для получения ссылки на ячейки **SoftEdgesSize** по имени из другой формулы, по значению атрибута **N** элемент **ячейки** и программы, с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="27215-108">To get a reference to the **SoftEdgesSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27215-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="27215-109">Cell name:</span></span>  <br/> | <span data-ttu-id="27215-110">SoftEdgesSize</span><span class="sxs-lookup"><span data-stu-id="27215-110">SoftEdgesSize</span></span>  <br/> |
   
<span data-ttu-id="27215-111">Для получения ссылки на ячейки **SoftEdgesSize** по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="27215-111">To get a reference to the **SoftEdgesSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="27215-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="27215-112">Section index:</span></span>  <br/> |<span data-ttu-id="27215-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="27215-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="27215-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="27215-114">Row index:</span></span>  <br/> |<span data-ttu-id="27215-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="27215-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="27215-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="27215-116">Cell index:</span></span>  <br/> |<span data-ttu-id="27215-117">**visSoftEdgesSize**</span><span class="sxs-lookup"><span data-stu-id="27215-117">**visSoftEdgesSize**</span></span> <br/> |
   

