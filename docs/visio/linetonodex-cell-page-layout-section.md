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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358935"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="f954e-103">LineToNodeX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="f954e-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="f954e-104">Определяет горизонтальный зазор между всеми соединительными линиями и фигурами на странице документа.</span><span class="sxs-lookup"><span data-stu-id="f954e-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f954e-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="f954e-105">Remarks</span></span>

<span data-ttu-id="f954e-106">Значение этой ячейки также можно задать в диалоговом окне **Макет и интервалы маршрутизации** .</span><span class="sxs-lookup"><span data-stu-id="f954e-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="f954e-107">На вкладке **конструктор** щелкните стрелку **Параметры страницы** , выберите **Макет и маршрутизация**, а затем щелкните интервалы. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="f954e-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="f954e-108">Чтобы получить ссылку на ячейку LineToNodeY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="f954e-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f954e-109">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="f954e-109">Cell name:</span></span>  <br/> |<span data-ttu-id="f954e-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="f954e-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="f954e-111">Чтобы получить ссылку на ячейку LineToNodeX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="f954e-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f954e-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="f954e-112">Section index:</span></span>  <br/> |<span data-ttu-id="f954e-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f954e-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f954e-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="f954e-114">Row index:</span></span>  <br/> |<span data-ttu-id="f954e-115">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="f954e-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="f954e-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="f954e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f954e-117">**Висплолинетонодекс**</span><span class="sxs-lookup"><span data-stu-id="f954e-117">**visPLOLineToNodeX**</span></span> <br/> |
   

