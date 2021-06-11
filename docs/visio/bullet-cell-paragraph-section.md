---
title: Bullet Cell (Paragraph Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Определяет стиль пули.
ms.openlocfilehash: 03b7d046cd42458b614313c19b2100259730539c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422770"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="e8fb7-103">Bullet Cell (Paragraph Section)</span><span class="sxs-lookup"><span data-stu-id="e8fb7-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="e8fb7-104">Определяет стиль пули.</span><span class="sxs-lookup"><span data-stu-id="e8fb7-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="e8fb7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e8fb7-105">**Value**</span></span>|<span data-ttu-id="e8fb7-106">**Стиль пули**</span><span class="sxs-lookup"><span data-stu-id="e8fb7-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8fb7-107">0</span><span class="sxs-lookup"><span data-stu-id="e8fb7-107">0</span></span>  <br/> |<span data-ttu-id="e8fb7-108">Нет</span><span class="sxs-lookup"><span data-stu-id="e8fb7-108">None</span></span>  <br/> |
|<span data-ttu-id="e8fb7-109">1</span><span class="sxs-lookup"><span data-stu-id="e8fb7-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="e8fb7-110">2</span><span class="sxs-lookup"><span data-stu-id="e8fb7-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="e8fb7-111">3</span><span class="sxs-lookup"><span data-stu-id="e8fb7-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="e8fb7-112">4 </span><span class="sxs-lookup"><span data-stu-id="e8fb7-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="e8fb7-113">5 </span><span class="sxs-lookup"><span data-stu-id="e8fb7-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="e8fb7-114">6 </span><span class="sxs-lookup"><span data-stu-id="e8fb7-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="e8fb7-115">7 </span><span class="sxs-lookup"><span data-stu-id="e8fb7-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="e8fb7-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e8fb7-116">Section index:</span></span>  <br/> |<span data-ttu-id="e8fb7-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="e8fb7-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="e8fb7-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e8fb7-118">Row index:</span></span>  <br/> |<span data-ttu-id="e8fb7-119">**visRowParagraph**  +   *i,* *где i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="e8fb7-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="e8fb7-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8fb7-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e8fb7-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="e8fb7-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8fb7-122">Примечания</span><span class="sxs-lookup"><span data-stu-id="e8fb7-122">Remarks</span></span>

<span data-ttu-id="e8fb7-123">Вы также можете установить значение этой ячейки, щелкнув правой кнопкой мыши фигуру, указав на **формат,** щелкнув **текст,** а затем щелкнув вкладку **Bullets.**</span><span class="sxs-lookup"><span data-stu-id="e8fb7-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="e8fb7-124">Чтобы получить ссылку на ячейку Bullet по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e8fb7-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e8fb7-125">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e8fb7-125">Cell name:</span></span>  <br/> |<span data-ttu-id="e8fb7-126">Para.Bullet[ *i*  ] где  *i*  = <1>, 2, 3, ...</span><span class="sxs-lookup"><span data-stu-id="e8fb7-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="e8fb7-127">Чтобы получить ссылку на ячейку Bullet по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e8fb7-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

