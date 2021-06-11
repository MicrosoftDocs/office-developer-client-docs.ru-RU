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
description: Определяет размер вертикального блока, область, в которой каждая из фигур должна поместиться на странице рисования при раскладке фигур с помощью диалогового окна Configure Layout (на вкладке Дизайн в группе Макет нажмите кнопку Re-Layout Page, а затем нажмите кнопку Дополнительные параметры макета).
ms.openlocfilehash: 08f2012bb027267810c21ef253a0073bb42d3a96
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427404"
---
# <a name="blocksizey-cell-page-layout-section"></a><span data-ttu-id="e5c27-103">BlockSizeY Cell (Page Layout Section)</span><span class="sxs-lookup"><span data-stu-id="e5c27-103">BlockSizeY Cell (Page Layout Section)</span></span>

<span data-ttu-id="e5c27-104">Определяет размер вертикального блока, область, в которой каждая из фигур должна поместиться на странице рисования при раскладке фигур, используя диалоговое окно **Configure Layout** (на вкладке Design, в группе  **Макет,** щелкните страницу **повторного** макета, а затем нажмите кнопку Дополнительные параметры макета). </span><span class="sxs-lookup"><span data-stu-id="e5c27-104">Determines the vertical block size, the area in which each of your shapes must fit on the drawing page when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e5c27-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="e5c27-105">Remarks</span></span>

<span data-ttu-id="e5c27-106">Вы также можете установить  это значение в диалоговом окне  Макет и Маршрутинг интервалов (на вкладке Дизайн щелкните стрелку в группе установки страницы, щелкните вкладку Макет и маршрутизацию, а затем щелкните **Spacing).**  </span><span class="sxs-lookup"><span data-stu-id="e5c27-106">You can also set this value in the **Layout and Routing Spacing** dialog box (on the **Design** tab, click the arrow in the **Page Setup** group, click the **Layout and Routing** tab, and then click **Spacing**).</span></span>
  
<span data-ttu-id="e5c27-107">Чтобы получить ссылку на ячейку BlockSizeY по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e5c27-107">To get a reference to the BlockSizeY cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5c27-108">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e5c27-108">Cell name:</span></span>  <br/> | <span data-ttu-id="e5c27-109">BlockSizeY</span><span class="sxs-lookup"><span data-stu-id="e5c27-109">BlockSizeY</span></span>  <br/> |
   
<span data-ttu-id="e5c27-110">Чтобы получить ссылку на ячейку BlockSizeY по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e5c27-110">To get a reference to the BlockSizeY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e5c27-111">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e5c27-111">Section index:</span></span>  <br/> |<span data-ttu-id="e5c27-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e5c27-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e5c27-113">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e5c27-113">Row index:</span></span>  <br/> |<span data-ttu-id="e5c27-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="e5c27-114">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="e5c27-115">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e5c27-115">Cell index:</span></span>  <br/> |<span data-ttu-id="e5c27-116">**visPLOBlockSizeY**</span><span class="sxs-lookup"><span data-stu-id="e5c27-116">**visPLOBlockSizeY**</span></span> <br/> |
   

