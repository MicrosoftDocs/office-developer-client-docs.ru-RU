---
title: Ячейка LineToNodeX (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: Определяет горизонтальную свободное пространство между все соединители и фигур на странице документа.
ms.openlocfilehash: 75f7e8150711421138a01175be34003d124e88ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814095"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="a0c3a-103">Ячейка LineToNodeX (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="a0c3a-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="a0c3a-104">Определяет горизонтальную свободное пространство между все соединители и фигур на странице документа.</span><span class="sxs-lookup"><span data-stu-id="a0c3a-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a0c3a-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="a0c3a-105">Remarks</span></span>

<span data-ttu-id="a0c3a-106">Также можно задать значение данной ячейки в диалоговом окне **Макет и интервал по маршрутизации** .</span><span class="sxs-lookup"><span data-stu-id="a0c3a-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="a0c3a-107">(На вкладке **Конструктор** щелкните стрелку **Параметры страницы** , нажмите кнопку **Макет и маршрутизации**и нажмите кнопку **интервалы**.)</span><span class="sxs-lookup"><span data-stu-id="a0c3a-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="a0c3a-108">Чтобы получить ссылку на ячейку LineToNodeY по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="a0c3a-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0c3a-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="a0c3a-109">Cell name:</span></span>  <br/> |<span data-ttu-id="a0c3a-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="a0c3a-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="a0c3a-111">Для получения ссылки на ячейки LineToNodeX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="a0c3a-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a0c3a-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="a0c3a-112">Section index:</span></span>  <br/> |<span data-ttu-id="a0c3a-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a0c3a-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="a0c3a-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="a0c3a-114">Row index:</span></span>  <br/> |<span data-ttu-id="a0c3a-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="a0c3a-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="a0c3a-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="a0c3a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="a0c3a-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="a0c3a-117">**visPLOLineToNodeX**</span></span> <br/> |
   

