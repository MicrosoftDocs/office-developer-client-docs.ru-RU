---
title: BlockSizeX Cell (Page Layout Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: Определяет горизонтальный размер блока, область, в которой каждая фигура должна умещаться на странице рисования при выкладывке фигур с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните Re-Layout "Страница" и выберите "Дополнительные параметры макета").
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424191"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="0b6b4-103">BlockSizeX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="0b6b4-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="0b6b4-104">Определяет горизонтальный размер блока, область, в которой каждая фигура должна умещаться на  странице рисования при отрисовке фигур  с помощью диалоговых окна "Настройка макета" (на вкладке "Конструктор" в группе "Макет" щелкните "Страница повторного макета" **и** выберите "Дополнительные параметры  макета"). </span><span class="sxs-lookup"><span data-stu-id="0b6b4-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0b6b4-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="0b6b4-105">Remarks</span></span>

<span data-ttu-id="0b6b4-106">Это значение также можно  установить в диалоговом окне "Макет" и "Интервал маршрутов" (на  вкладке "Конструктор" щелкните стрелку в группе "Настройка страницы", выберите вкладку "Макет" и "Маршрут" и щелкните   "Интервал"). </span><span class="sxs-lookup"><span data-stu-id="0b6b4-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="0b6b4-107">Чтобы получить ссылку на ячейку BlockSizeX по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0b6b4-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0b6b4-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0b6b4-108">Cell name:</span></span>  <br/> |<span data-ttu-id="0b6b4-109">BlockSizeX</span><span class="sxs-lookup"><span data-stu-id="0b6b4-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="0b6b4-110">Чтобы получить ссылку на ячейку BlockSizeX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0b6b4-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0b6b4-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0b6b4-111">Section index:</span></span>  <br/> |<span data-ttu-id="0b6b4-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0b6b4-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0b6b4-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0b6b4-113">Row index:</span></span>  <br/> |<span data-ttu-id="0b6b4-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="0b6b4-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="0b6b4-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0b6b4-115">Cell index:</span></span>  <br/> |<span data-ttu-id="0b6b4-116">**visPLOBlockSizeX**</span><span class="sxs-lookup"><span data-stu-id="0b6b4-116">**visPLOBlockSizeX**</span></span> <br/> |
   

