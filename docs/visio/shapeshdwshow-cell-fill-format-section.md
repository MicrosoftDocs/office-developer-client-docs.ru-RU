---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Определяет, отображается ли в фигуре тень как целое число от 0 до 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349149"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="57772-103">ShapeShdwShow Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="57772-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="57772-104">Определяет, отображается ли в фигуре тень как целое число от 0 до 2.</span><span class="sxs-lookup"><span data-stu-id="57772-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="57772-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="57772-105">**Value**</span></span>|<span data-ttu-id="57772-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="57772-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="57772-107">нуль</span><span class="sxs-lookup"><span data-stu-id="57772-107">0</span></span>  <br/> |<span data-ttu-id="57772-108">Всегда отображать тень, если указана теневая копия.</span><span class="sxs-lookup"><span data-stu-id="57772-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="57772-109">Тени для дочерних фигур не отображаются.</span><span class="sxs-lookup"><span data-stu-id="57772-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="57772-110">1,1</span><span class="sxs-lookup"><span data-stu-id="57772-110">1</span></span>  <br/> |<span data-ttu-id="57772-111">Не выводите тень, если у фигуры нет родительского объекта.</span><span class="sxs-lookup"><span data-stu-id="57772-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="57772-112">Используйте тени вложенных фигур, если они сгруппированы вместе.</span><span class="sxs-lookup"><span data-stu-id="57772-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="57772-113">2</span><span class="sxs-lookup"><span data-stu-id="57772-113">2</span></span>  <br/> |<span data-ttu-id="57772-114">Всегда отображать тень, если указана тень.</span><span class="sxs-lookup"><span data-stu-id="57772-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="57772-115">Отображаются тени для дочерних фигур.</span><span class="sxs-lookup"><span data-stu-id="57772-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57772-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="57772-116">Remarks</span></span>

<span data-ttu-id="57772-117">Чтобы получить ссылку на ячейку **ShapeShdwShow** по имени из другой формулы, по значению атрибута **N** элемента **ячейки** или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="57772-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="57772-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="57772-118">Cell name:</span></span>  <br/> | <span data-ttu-id="57772-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="57772-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="57772-120">Чтобы получить ссылку на ячейку **ShapeShdwShow** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="57772-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="57772-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="57772-121">Section index:</span></span>  <br/> |<span data-ttu-id="57772-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="57772-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="57772-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="57772-123">Row index:</span></span>  <br/> |<span data-ttu-id="57772-124">**Висровфилл**</span><span class="sxs-lookup"><span data-stu-id="57772-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="57772-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="57772-125">Cell index:</span></span>  <br/> |<span data-ttu-id="57772-126">**Висфиллшдвшов**</span><span class="sxs-lookup"><span data-stu-id="57772-126">**visFillShdwShow**</span></span> <br/> |
   

