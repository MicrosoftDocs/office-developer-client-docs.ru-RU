---
title: ShdwOffsetX Cell (Page Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Определяет расстояние в единицах страниц, на которое тень фигуры смещена горизонтально от фигуры.
ms.openlocfilehash: fbc7d37fc8ba45f3219af6a4350301102954f23d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431654"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="5add5-103">ShdwOffsetX Cell (Page Properties Section)</span><span class="sxs-lookup"><span data-stu-id="5add5-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="5add5-104">Определяет расстояние в единицах страниц, на которое тень фигуры смещена горизонтально от фигуры.</span><span class="sxs-lookup"><span data-stu-id="5add5-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5add5-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="5add5-105">Remarks</span></span>

<span data-ttu-id="5add5-106">Это значение заданной в диалоговом **окне Настройка** страницы (на вкладке **Дизайн** щелкните стрелку **установки страницы).**</span><span class="sxs-lookup"><span data-stu-id="5add5-106">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> <span data-ttu-id="5add5-107">Это значение не зависит от масштаба рисунка.</span><span class="sxs-lookup"><span data-stu-id="5add5-107">This value is independent of the scale of the drawing.</span></span> <span data-ttu-id="5add5-108">Если рисунок масштабирован, смещение теней остается тем же.</span><span class="sxs-lookup"><span data-stu-id="5add5-108">If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="5add5-109">Чтобы получить ссылку на ячейку ShdwOffsetX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="5add5-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5add5-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="5add5-110">Cell name:</span></span>  <br/> | <span data-ttu-id="5add5-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="5add5-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="5add5-112">Чтобы получить ссылку на ячейку ShdwOffsetX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="5add5-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5add5-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="5add5-113">Section index:</span></span>  <br/> |<span data-ttu-id="5add5-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5add5-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5add5-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="5add5-115">Row index:</span></span>  <br/> |<span data-ttu-id="5add5-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="5add5-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="5add5-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="5add5-117">Cell index:</span></span>  <br/> |<span data-ttu-id="5add5-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="5add5-118">**visPageShdwOffsetX**</span></span> <br/> |
   

