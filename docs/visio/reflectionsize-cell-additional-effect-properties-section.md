---
title: ReflectionSize Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: Определяет размер отражения относительно фигуры в процентах от 0,0 до 100,0%. Фигура со значением 0% в ячейке ReflectionSize не имеет отражения; значение 100% отображает полное зеркальное изображение фигуры.
ms.openlocfilehash: 60fcb315ec1b6187082bdcdbbdcfaa4b80bbcfb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409078"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a><span data-ttu-id="85cb0-104">ReflectionSize Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="85cb0-104">ReflectionSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="85cb0-105">Определяет размер отражения относительно фигуры в процентах от 0,0 до 100,0%.</span><span class="sxs-lookup"><span data-stu-id="85cb0-105">Determines the size of the reflection relative to the shape, as a percentage from 0.0 to 100.0%.</span></span> <span data-ttu-id="85cb0-106">Фигура со значением 0% в ячейке **ReflectionSize** не имеет отражения; значение 100% отображает полное зеркальное изображение фигуры.</span><span class="sxs-lookup"><span data-stu-id="85cb0-106">A shape with a value of 0% in the **ReflectionSize** cell does not have a reflection; a value of 100% displays a complete mirror image of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="85cb0-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="85cb0-107">Remarks</span></span>

<span data-ttu-id="85cb0-108">Чтобы получить ссылку на ячейку **ReflectionSize** по имени из другой формулы, по значению атрибута **N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="85cb0-108">To get a reference to the **ReflectionSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85cb0-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="85cb0-109">Cell name:</span></span>  <br/> | <span data-ttu-id="85cb0-110">ReflectionSize</span><span class="sxs-lookup"><span data-stu-id="85cb0-110">ReflectionSize</span></span>  <br/> |
   
<span data-ttu-id="85cb0-111">Чтобы получить ссылку на **ячейку ReflectionSize** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="85cb0-111">To get a reference to the **ReflectionSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="85cb0-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="85cb0-112">Section index:</span></span>  <br/> |<span data-ttu-id="85cb0-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="85cb0-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="85cb0-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="85cb0-114">Row index:</span></span>  <br/> |<span data-ttu-id="85cb0-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="85cb0-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="85cb0-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="85cb0-116">Cell index:</span></span>  <br/> |<span data-ttu-id="85cb0-117">**visReflectionSize**</span><span class="sxs-lookup"><span data-stu-id="85cb0-117">**visReflectionSize**</span></span> <br/> |
   

