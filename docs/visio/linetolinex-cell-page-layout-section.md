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
description: Определяет горизонтальный зазор между всеми соединитетелями на странице рисования.
ms.openlocfilehash: f3dbf43c737fef1fa1156fb4dc8d0f23449328c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416330"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="78946-103">LineToLineX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="78946-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="78946-104">Определяет горизонтальный зазор между всеми соединитетелями на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="78946-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="78946-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="78946-105">Remarks</span></span>

<span data-ttu-id="78946-106">Вы также можете установить значение этой ячейки в диалоговом окне Макет и **Маршрутная** интервал.</span><span class="sxs-lookup"><span data-stu-id="78946-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="78946-107">(На **вкладке Дизайн** щелкните стрелку **установки** страницы, щелкните **Макет** и маршрутику, а затем щелкните **Интервал**.)</span><span class="sxs-lookup"><span data-stu-id="78946-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="78946-108">Чтобы получить ссылку на ячейку LineToLineX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="78946-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78946-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="78946-109">Cell name:</span></span>  <br/> |<span data-ttu-id="78946-110">LineToLineX</span><span class="sxs-lookup"><span data-stu-id="78946-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="78946-111">Чтобы получить ссылку на ячейку LineToLineX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="78946-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="78946-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="78946-112">Section index:</span></span>  <br/> |<span data-ttu-id="78946-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="78946-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="78946-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="78946-114">Row index:</span></span>  <br/> |<span data-ttu-id="78946-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="78946-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="78946-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="78946-116">Cell index:</span></span>  <br/> |<span data-ttu-id="78946-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="78946-117">**visPLOLineToLineX**</span></span> <br/> |
   

