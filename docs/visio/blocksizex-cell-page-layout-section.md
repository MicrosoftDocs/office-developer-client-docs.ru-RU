---
title: Ячейка BlockSizeX (раздел "Макет страницы")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm105
localization_priority: Normal
ms.assetid: 253aac17-077e-48e0-39a8-a3abd5d4a257
description: Определяет размер горизонтального блока должна помещаться область, в которой каждый фигур на странице документа при расположении фигур с помощью диалогового окна "Настройка макета" (на вкладке конструктор в группе макет нажмите кнопку Изменить расположение и нажмите кнопку Дополнительные параметры расположения).
ms.openlocfilehash: 68ed13b85583326c25635049d7e85babe62d5eb5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813286"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="2342c-103">Ячейка BlockSizeX (раздел "Макет страницы")</span><span class="sxs-lookup"><span data-stu-id="2342c-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="2342c-104">Определяет размер горизонтального блока должна помещаться область, в которой каждый фигур на странице документа при расположении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **Конструктор** в группе **Макет** выберите **Изменение макета страницы **и нажмите кнопку **Дополнительные параметры расположения**).</span><span class="sxs-lookup"><span data-stu-id="2342c-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2342c-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="2342c-105">Remarks</span></span>

<span data-ttu-id="2342c-106">Также можно задать это значение в диалоговом окне **Макет и маршрутизация интервалы** (на вкладку **Конструктор** , щелкните стрелку в группе **Параметры страницы** , перейдите на вкладку **Макет и маршрутизации** и нажмите кнопку **интервала**).</span><span class="sxs-lookup"><span data-stu-id="2342c-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="2342c-107">Чтобы получить ссылку на ячейку BlockSizeX по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="2342c-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2342c-108">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="2342c-108">Cell name:</span></span>  <br/> |<span data-ttu-id="2342c-109">BlockSizeX</span><span class="sxs-lookup"><span data-stu-id="2342c-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="2342c-110">Для получения ссылки на ячейки BlockSizeX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="2342c-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2342c-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2342c-111">Section index:</span></span>  <br/> |<span data-ttu-id="2342c-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2342c-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2342c-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2342c-113">Row index:</span></span>  <br/> |<span data-ttu-id="2342c-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="2342c-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="2342c-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2342c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="2342c-116">**visPLOBlockSizeX**</span><span class="sxs-lookup"><span data-stu-id="2342c-116">**visPLOBlockSizeX**</span></span> <br/> |
   

