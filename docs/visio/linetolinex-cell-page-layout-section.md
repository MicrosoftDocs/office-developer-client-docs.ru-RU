---
title: LineToLineX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm565
localization_priority: Normal
ms.assetid: f6b461fe-56ac-4c0e-31cd-6b3c1075db6e
description: Определяет горизонтальный зазор между всеми соединителями на странице документа.
ms.openlocfilehash: f3dbf43c737fef1fa1156fb4dc8d0f23449328c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416330"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="f2d04-103">LineToLineX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="f2d04-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="f2d04-104">Определяет горизонтальный зазор между всеми соединителями на странице документа.</span><span class="sxs-lookup"><span data-stu-id="f2d04-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f2d04-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="f2d04-105">Remarks</span></span>

<span data-ttu-id="f2d04-106">Значение этой ячейки также можно задать в диалоговом окне **Макет и интервалы маршрутизации** .</span><span class="sxs-lookup"><span data-stu-id="f2d04-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="f2d04-107">На вкладке **конструктор** щелкните стрелку **Параметры страницы** , выберите **Макет и маршрутизация**, а затем щелкните **интервалы**.</span><span class="sxs-lookup"><span data-stu-id="f2d04-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="f2d04-108">Чтобы получить ссылку на ячейку LineToLineX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="f2d04-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2d04-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f2d04-109">Cell name:</span></span>  <br/> |<span data-ttu-id="f2d04-110">LineToLineX</span><span class="sxs-lookup"><span data-stu-id="f2d04-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="f2d04-111">Чтобы получить ссылку на ячейку LineToLineX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f2d04-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f2d04-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f2d04-112">Section index:</span></span>  <br/> |<span data-ttu-id="f2d04-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f2d04-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f2d04-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f2d04-114">Row index:</span></span>  <br/> |<span data-ttu-id="f2d04-115">**висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="f2d04-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="f2d04-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f2d04-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f2d04-117">**висплолинетолинекс**</span><span class="sxs-lookup"><span data-stu-id="f2d04-117">**visPLOLineToLineX**</span></span> <br/> |
   

