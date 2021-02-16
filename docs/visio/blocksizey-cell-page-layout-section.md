---
title: BlockSizeY Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm110
localization_priority: Normal
ms.assetid: be51e18e-ea49-0788-1a17-866090afb9f4
description: Определяет размер вертикального блока, область, в которой каждая фигура должна умещаться на странице рисования при разметке фигур с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout "Страница" и выберите "Дополнительные параметры макета").
ms.openlocfilehash: 08f2012bb027267810c21ef253a0073bb42d3a96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427404"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="8b469-103">BlockSizeY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="8b469-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="8b469-104">Определяет размер вертикального блока, область, в которой каждая фигура должна умещаться на  странице рисования при разметке фигур  с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните "Страница повторного макета" **и** выберите "Дополнительные параметры  макета"). </span><span class="sxs-lookup"><span data-stu-id="8b469-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="8b469-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="8b469-105">Remarks</span></span>

<span data-ttu-id="8b469-106">Это значение также можно  установить в диалоговом окне "Макет" и "Интервал маршрутов" (на  вкладке "Конструктор" щелкните стрелку в группе "Настройка страницы", выберите вкладку "Макет" и "Маршрут" и щелкните   "Интервал"). </span><span class="sxs-lookup"><span data-stu-id="8b469-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="8b469-107">Чтобы получить ссылку на ячейку BlockSizeY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="8b469-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b469-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="8b469-108">Cell name:</span></span>  <br/> | <span data-ttu-id="8b469-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="8b469-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="8b469-110">Чтобы получить ссылку на ячейку BlockSizeY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="8b469-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="8b469-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="8b469-111">Section index:</span></span>  <br/> |<span data-ttu-id="8b469-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8b469-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="8b469-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="8b469-113">Row index:</span></span>  <br/> |<span data-ttu-id="8b469-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8b469-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="8b469-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="8b469-115">Cell index:</span></span>  <br/> |<span data-ttu-id="8b469-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="8b469-116">**visPLOBlockSizeY**</span></span> <br/> |
   

