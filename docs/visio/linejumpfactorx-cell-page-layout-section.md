---
title: LineJumpFactorX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Определяет размер переходов по горизонтали динамических соединителю на странице относительно значения ячейки LineToLineX. Значение этой ячейки может варьироваться от 0 до 10, но предлагается дробное значение от 0 до 1.
ms.openlocfilehash: 8698d99021ca64415417de8e946cbd80b586e759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424996"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a><span data-ttu-id="d3ba4-104">LineJumpFactorX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="d3ba4-104">LineJumpFactorX Cell (Page Layout Section)</span></span>

<span data-ttu-id="d3ba4-105">Определяет размер переходов по горизонтали динамических соединителю на странице относительно значения ячейки LineToLineX.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-105">Determines the size of line jumps on horizontal dynamic connectors on the page, relative to the value of the LineToLineX cell.</span></span> <span data-ttu-id="d3ba4-106">Значение этой ячейки может варьироваться от 0 до 10, но предлагается дробное значение от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="d3ba4-106">The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d3ba4-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="d3ba4-107">Remarks</span></span>

<span data-ttu-id="d3ba4-108">Вы также можете установить значение этой  ячейки на вкладке "Макет и маршрут"  в диалоговом окне "Настройка страницы" (на вкладке "Конструктор", щелкните стрелку "Настройка страницы", а затем щелкните "Макет и **маршрут").**  </span><span class="sxs-lookup"><span data-stu-id="d3ba4-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="d3ba4-109">Чтобы получить ссылку на ячейку LineJumpFactorX по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="d3ba4-109">To get a reference to the LineJumpFactorX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3ba4-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d3ba4-110">Cell name:</span></span>  <br/> |<span data-ttu-id="d3ba4-111">LineJumpFactorX</span><span class="sxs-lookup"><span data-stu-id="d3ba4-111">LineJumpFactorX</span></span>  <br/> |
   
<span data-ttu-id="d3ba4-112">Чтобы получить ссылку на ячейку LineJumpFactorX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d3ba4-112">To get a reference to the LineJumpFactorX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3ba4-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d3ba4-113">Section index:</span></span>  <br/> |<span data-ttu-id="d3ba4-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d3ba4-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d3ba4-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d3ba4-115">Row index:</span></span>  <br/> |<span data-ttu-id="d3ba4-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="d3ba4-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="d3ba4-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d3ba4-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d3ba4-118">**visPLOJumpFactorX**</span><span class="sxs-lookup"><span data-stu-id="d3ba4-118">**visPLOJumpFactorX**</span></span> <br/> |
   

