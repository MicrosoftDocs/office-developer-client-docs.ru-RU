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
description: Определяет размер вертикального блока, область, в которой все фигуры должны размещаться на странице документа при разметке фигур с помощью диалогового окна Настройка макета (на вкладке Конструктор в группе Макет выберите пункт изменить макет страницы, а затем щелкните Дополнительные параметры макета).
ms.openlocfilehash: 08f2012bb027267810c21ef253a0073bb42d3a96
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297349"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="dad90-103">BlockSizeY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="dad90-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="dad90-104">Определяет размер вертикального блока, область, в которой каждая из фигур должна размещаться на странице документа при размещении фигур с помощью диалогового окна " **Настройка макета** " (на вкладке **конструктор** в группе **Макет** выберите пункт **изменить макет страницы**). а затем выберите **Дополнительные параметры макета**.</span><span class="sxs-lookup"><span data-stu-id="dad90-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dad90-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="dad90-105">Remarks</span></span>

<span data-ttu-id="dad90-106">Вы также можете задать это значение в диалоговом окне **Макет и интервалы маршрутизации** (на вкладке **конструктор** щелкните стрелку в группе **Параметры страницы** , перейдите на вкладку **Макет и маршрутизация** , а затем выберите **интервал**).</span><span class="sxs-lookup"><span data-stu-id="dad90-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="dad90-107">Чтобы получить ссылку на ячейку BlockSizeY по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="dad90-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dad90-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="dad90-108">Cell name:</span></span>  <br/> | <span data-ttu-id="dad90-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="dad90-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="dad90-110">Чтобы получить ссылку на ячейку BlockSizeY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="dad90-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dad90-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="dad90-111">Section index:</span></span>  <br/> |<span data-ttu-id="dad90-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dad90-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dad90-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="dad90-113">Row index:</span></span>  <br/> |<span data-ttu-id="dad90-114">**Висровпажелайаут**</span><span class="sxs-lookup"><span data-stu-id="dad90-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="dad90-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="dad90-115">Cell index:</span></span>  <br/> |<span data-ttu-id="dad90-116">**Висплоблокксизэй**</span><span class="sxs-lookup"><span data-stu-id="dad90-116">**visPLOBlockSizeY**</span></span> <br/> |
   

