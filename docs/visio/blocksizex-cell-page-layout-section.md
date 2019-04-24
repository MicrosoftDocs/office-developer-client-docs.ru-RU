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
description: Определяет размер горизонтального блока, область, в которой все фигуры должны размещаться на странице документа при разметке фигур с помощью диалогового окна Настройка макета (на вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета).
ms.openlocfilehash: 8e4cee4b2059d9b8f2fe77c2d4902e67246eac2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309480"
---
# <a name="blocksizex-cell-page-layout-section"></a><span data-ttu-id="b56bb-103">BlockSizeX Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="b56bb-103">BlockSizeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="b56bb-104">Определяет размер горизонтального блока, область, в которой все фигуры должны размещаться на странице документа при размещении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **конструктор** в группе **Макет** нажмите кнопку \*\*изменить макет страницы). \*\*, а затем выберите **Дополнительные параметры макета**.</span><span class="sxs-lookup"><span data-stu-id="b56bb-104">Determines the horizontal block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b56bb-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="b56bb-105">Remarks</span></span>

<span data-ttu-id="b56bb-106">Вы также можете задать это значение в диалоговом окне **Макет и интервалы маршрутизации** (на вкладке **конструктор** щелкните стрелку в группе **Параметры страницы** , перейдите на вкладку **Макет и маршрутизация** , а затем выберите **интервал**).</span><span class="sxs-lookup"><span data-stu-id="b56bb-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="b56bb-107">Чтобы получить ссылку на ячейку BlockSizeX по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="b56bb-107">To get a reference to the BlockSizeX cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b56bb-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="b56bb-108">Cell name:</span></span>  <br/> |<span data-ttu-id="b56bb-109">BlockSizeX</span><span class="sxs-lookup"><span data-stu-id="b56bb-109">BlockSizeX</span></span>  <br/> |
   
<span data-ttu-id="b56bb-110">Чтобы получить ссылку на ячейку BlockSizeX по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="b56bb-110">To get a reference to the BlockSizeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b56bb-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b56bb-111">Section index:</span></span>  <br/> |<span data-ttu-id="b56bb-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b56bb-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b56bb-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b56bb-113">Row index:</span></span>  <br/> |<span data-ttu-id="b56bb-114">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="b56bb-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="b56bb-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b56bb-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b56bb-116">**Висплоблокксизекс**</span><span class="sxs-lookup"><span data-stu-id="b56bb-116">**visPLOBlockSizeX**</span></span> <br/> |
   

