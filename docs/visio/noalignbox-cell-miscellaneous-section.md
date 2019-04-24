---
title: NoAlignBox Cell (Miscellaneous Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm700
localization_priority: Normal
ms.assetid: b2d51f4b-d64e-fd14-4ff1-ed67c69213bc
description: Включает и выключает отображение прямоугольника выделения для выбранной фигуры.
ms.openlocfilehash: 2ff9f051df54f4d424589332b9fbaea973552edc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319861"
---
# <a name="noalignbox-cell-miscellaneous-section"></a><span data-ttu-id="ebc17-103">NoAlignBox Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="ebc17-103">NoAlignBox Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="ebc17-104">Включает и выключает отображение прямоугольника выделения для выбранной фигуры.</span><span class="sxs-lookup"><span data-stu-id="ebc17-104">Switches the display of the selection rectangle on and off for the selected shape.</span></span>
  
|<span data-ttu-id="ebc17-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="ebc17-105">**Value**</span></span>|<span data-ttu-id="ebc17-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ebc17-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ebc17-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ebc17-107">TRUE</span></span>  <br/> | <span data-ttu-id="ebc17-108">При выборе фигуры прямоугольник выделения не отображается.</span><span class="sxs-lookup"><span data-stu-id="ebc17-108">Selection rectangle is not displayed when the shape is selected.</span></span>  <br/> |
| <span data-ttu-id="ebc17-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ebc17-109">FALSE</span></span>  <br/> | <span data-ttu-id="ebc17-110">Если выбрана фигура, отображается прямоугольник выделения.</span><span class="sxs-lookup"><span data-stu-id="ebc17-110">Selection rectangle is displayed when the shape is selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ebc17-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="ebc17-111">Remarks</span></span>

<span data-ttu-id="ebc17-112">Чтобы получить ссылку на ячейку NoAlignBox по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="ebc17-112">To get a reference to the NoAlignBox cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ebc17-113">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="ebc17-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ebc17-114">NoAlignBox</span><span class="sxs-lookup"><span data-stu-id="ebc17-114">NoAlignBox</span></span>  <br/> |
   
<span data-ttu-id="ebc17-115">Чтобы получить ссылку на ячейку NoAlignBox по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="ebc17-115">To get a reference to the NoAlignBox cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ebc17-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="ebc17-116">Section index:</span></span>  <br/> |<span data-ttu-id="ebc17-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ebc17-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ebc17-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="ebc17-118">Row index:</span></span>  <br/> |<span data-ttu-id="ebc17-119">**Висровмиск**</span><span class="sxs-lookup"><span data-stu-id="ebc17-119">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="ebc17-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="ebc17-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ebc17-121">**Висноалигнбокс**</span><span class="sxs-lookup"><span data-stu-id="ebc17-121">**visNoAlignBox**</span></span> <br/> |
   

