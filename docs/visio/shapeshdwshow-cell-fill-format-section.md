---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Определяет, отображает ли фигура тень в виде integer от 0 до 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422119"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="0e067-103">ShapeShdwShow Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="0e067-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="0e067-104">Определяет, отображает ли фигура тень в виде integer от 0 до 2.</span><span class="sxs-lookup"><span data-stu-id="0e067-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="0e067-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0e067-105">**Value**</span></span>|<span data-ttu-id="0e067-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e067-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e067-107">0</span><span class="sxs-lookup"><span data-stu-id="0e067-107">0</span></span>  <br/> |<span data-ttu-id="0e067-108">Всегда отобразить тень, если задана тень.</span><span class="sxs-lookup"><span data-stu-id="0e067-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="0e067-109">Тени для под фигур не отображаются.</span><span class="sxs-lookup"><span data-stu-id="0e067-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="0e067-110">1</span><span class="sxs-lookup"><span data-stu-id="0e067-110">1</span></span>  <br/> |<span data-ttu-id="0e067-111">Не отрисуй тень, если у фигуры нет родительского.</span><span class="sxs-lookup"><span data-stu-id="0e067-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="0e067-112">Используйте тени sub-shape если сгруппировали совместно.</span><span class="sxs-lookup"><span data-stu-id="0e067-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="0e067-113">2</span><span class="sxs-lookup"><span data-stu-id="0e067-113">2</span></span>  <br/> |<span data-ttu-id="0e067-114">Всегда отобразить тень, если задана тень.</span><span class="sxs-lookup"><span data-stu-id="0e067-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="0e067-115">Отображаются тени для под-фигур.</span><span class="sxs-lookup"><span data-stu-id="0e067-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e067-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e067-116">Remarks</span></span>

<span data-ttu-id="0e067-117">Чтобы получить ссылку на **ячейку ShapeShdwShow** по имени из другой формулы, по значению **атрибута N** элемента **Cell** или из программы с использованием свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0e067-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e067-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e067-118">Cell name:</span></span>  <br/> | <span data-ttu-id="0e067-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="0e067-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="0e067-120">Чтобы получить ссылку на **ячейку ShapeShdwShow** по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0e067-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0e067-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0e067-121">Section index:</span></span>  <br/> |<span data-ttu-id="0e067-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0e067-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0e067-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0e067-123">Row index:</span></span>  <br/> |<span data-ttu-id="0e067-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="0e067-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="0e067-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e067-125">Cell index:</span></span>  <br/> |<span data-ttu-id="0e067-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="0e067-126">**visFillShdwShow**</span></span> <br/> |
   

