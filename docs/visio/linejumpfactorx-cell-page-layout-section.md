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
description: Определяет размер значков пересечения линий на горизонтальных динамических соединителях на странице относительно значения ячейки LineToLineX. Значение этой ячейки может находиться в диапазоне от 0 до 10, но в этом случае предлагаются дробные значения от 0 до 1.
ms.openlocfilehash: 8698d99021ca64415417de8e946cbd80b586e759
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424996"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a><span data-ttu-id="a1e8b-104">LineJumpFactorX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="a1e8b-104">LineJumpFactorX Cell (Page Layout Section)</span></span>

<span data-ttu-id="a1e8b-105">Определяет размер значков пересечения линий на горизонтальных динамических соединителях на странице относительно значения ячейки LineToLineX.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-105">Determines the size of line jumps on horizontal dynamic connectors on the page, relative to the value of the LineToLineX cell.</span></span> <span data-ttu-id="a1e8b-106">Значение этой ячейки может находиться в диапазоне от 0 до 10, но в этом случае предлагаются дробные значения от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="a1e8b-106">The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a1e8b-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="a1e8b-107">Remarks</span></span>

<span data-ttu-id="a1e8b-108">Значение этой ячейки также можно задать на вкладке **Макет и маршрутизация** в диалоговом окне **Параметры страницы** (на вкладке **конструктор** щелкните стрелку **Параметры страницы** , а затем выберите **Макет и маршрутизация**).</span><span class="sxs-lookup"><span data-stu-id="a1e8b-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="a1e8b-109">Чтобы получить ссылку на ячейку LineJumpFactorX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="a1e8b-109">To get a reference to the LineJumpFactorX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1e8b-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="a1e8b-110">Cell name:</span></span>  <br/> |<span data-ttu-id="a1e8b-111">LineJumpFactorX</span><span class="sxs-lookup"><span data-stu-id="a1e8b-111">LineJumpFactorX</span></span>  <br/> |
   
<span data-ttu-id="a1e8b-112">Чтобы получить ссылку на ячейку LineJumpFactorX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="a1e8b-112">To get a reference to the LineJumpFactorX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1e8b-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a1e8b-113">Section index:</span></span>  <br/> |<span data-ttu-id="a1e8b-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a1e8b-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a1e8b-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a1e8b-115">Row index:</span></span>  <br/> |<span data-ttu-id="a1e8b-116">**висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="a1e8b-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a1e8b-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a1e8b-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a1e8b-118">**виспложумпфакторкс**</span><span class="sxs-lookup"><span data-stu-id="a1e8b-118">**visPLOJumpFactorX**</span></span> <br/> |
   

