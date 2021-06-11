---
title: LineJumpFactorY Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Определяет размер прыжков строки на вертикальных динамических соединителях на странице относительно значения ячейки LineToLineY. Значение этой ячейки может варьироваться от 0 до 10, но предлагаются дробные значения от 0 до 1.
ms.openlocfilehash: 36712c1558ff2f50309dc31e8f918061180c8fa4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411962"
---
# <a name="linejumpfactory-cell-page-layout-section"></a><span data-ttu-id="46473-104">LineJumpFactorY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="46473-104">LineJumpFactorY Cell (Page Layout Section)</span></span>

<span data-ttu-id="46473-105">Определяет размер прыжков строки на вертикальных динамических соединителях на странице относительно значения ячейки LineToLineY.</span><span class="sxs-lookup"><span data-stu-id="46473-105">Determines the size of line jumps on vertical dynamic connectors on the page, relative to the value of the LineToLineY cell.</span></span> <span data-ttu-id="46473-106">Значение этой ячейки может варьироваться от 0 до 10, но предлагаются дробные значения от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="46473-106">The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="46473-107">Примечания</span><span class="sxs-lookup"><span data-stu-id="46473-107">Remarks</span></span>

<span data-ttu-id="46473-108">Вы также можете установить значение этой ячейки на вкладке  Layout и   **Routing** в диалоговом окне Настройка страницы (на вкладке Дизайн щелкните стрелку установки страницы, а затем нажмите макет и маршрутинг).</span><span class="sxs-lookup"><span data-stu-id="46473-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="46473-109">Чтобы получить ссылку на ячейку LineJumpFactorY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="46473-109">To get a reference to the LineJumpFactorY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46473-110">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="46473-110">Cell name:</span></span>  <br/> |<span data-ttu-id="46473-111">LineJumpFactorY</span><span class="sxs-lookup"><span data-stu-id="46473-111">LineJumpFactorY</span></span>  <br/> |
   
<span data-ttu-id="46473-112">Чтобы получить ссылку на ячейку LineJumpFactorY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="46473-112">To get a reference to the LineJumpFactorY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46473-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="46473-113">Section index:</span></span>  <br/> |<span data-ttu-id="46473-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="46473-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="46473-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="46473-115">Row index:</span></span>  <br/> |<span data-ttu-id="46473-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="46473-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="46473-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="46473-117">Cell index:</span></span>  <br/> |<span data-ttu-id="46473-118">**visPLOJumpFactorY**</span><span class="sxs-lookup"><span data-stu-id="46473-118">**visPLOJumpFactorY**</span></span> <br/> |
   

