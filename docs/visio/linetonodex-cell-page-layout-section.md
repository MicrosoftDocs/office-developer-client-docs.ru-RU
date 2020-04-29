---
title: LineToNodeX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: Определяет горизонтальный зазор между всеми соединительными линиями и фигурами на странице документа.
ms.openlocfilehash: c5a27edb25ce7b1449ad6e2988027b474bd79fdb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439711"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="0ab50-103">LineToNodeX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="0ab50-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="0ab50-104">Определяет горизонтальный зазор между всеми соединительными линиями и фигурами на странице документа.</span><span class="sxs-lookup"><span data-stu-id="0ab50-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0ab50-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="0ab50-105">Remarks</span></span>

<span data-ttu-id="0ab50-106">Значение этой ячейки также можно задать в диалоговом окне **Макет и интервалы маршрутизации** .</span><span class="sxs-lookup"><span data-stu-id="0ab50-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="0ab50-107">На вкладке **конструктор** щелкните стрелку **Параметры страницы** , выберите **Макет и маршрутизация**, а затем щелкните **интервалы**.</span><span class="sxs-lookup"><span data-stu-id="0ab50-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="0ab50-108">Чтобы получить ссылку на ячейку LineToNodeY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="0ab50-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ab50-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0ab50-109">Cell name:</span></span>  <br/> |<span data-ttu-id="0ab50-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="0ab50-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="0ab50-111">Чтобы получить ссылку на ячейку LineToNodeX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0ab50-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0ab50-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0ab50-112">Section index:</span></span>  <br/> |<span data-ttu-id="0ab50-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0ab50-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0ab50-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0ab50-114">Row index:</span></span>  <br/> |<span data-ttu-id="0ab50-115">**висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="0ab50-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="0ab50-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0ab50-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0ab50-117">**висплолинетонодекс**</span><span class="sxs-lookup"><span data-stu-id="0ab50-117">**visPLOLineToNodeX**</span></span> <br/> |
   

