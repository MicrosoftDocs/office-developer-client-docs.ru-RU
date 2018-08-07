---
title: Ячейка Bullet (раздел "Абзац")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm130
localization_priority: Normal
ms.assetid: 124a5ee1-6dd1-d17d-6f0e-dbaa5d95d9cd
description: Определяет стиль маркеров.
ms.openlocfilehash: d3ecdd8e0f3780490f92766351b5ac94e875ae28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813318"
---
# <a name="bullet-cell-paragraph-section"></a><span data-ttu-id="15b82-103">Ячейка Bullet (раздел "Абзац")</span><span class="sxs-lookup"><span data-stu-id="15b82-103">Bullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="15b82-104">Определяет стиль маркеров.</span><span class="sxs-lookup"><span data-stu-id="15b82-104">Determines the bullet style.</span></span>
  
|<span data-ttu-id="15b82-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="15b82-105">**Value**</span></span>|<span data-ttu-id="15b82-106">**Стиль маркированного списка**</span><span class="sxs-lookup"><span data-stu-id="15b82-106">**Bullet style**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15b82-107">0</span><span class="sxs-lookup"><span data-stu-id="15b82-107">0</span></span>  <br/> |<span data-ttu-id="15b82-108">Нет</span><span class="sxs-lookup"><span data-stu-id="15b82-108">None</span></span>  <br/> |
|<span data-ttu-id="15b82-109">1</span><span class="sxs-lookup"><span data-stu-id="15b82-109">1</span></span>  <br/> |![](media/IC_Bullet1_ZA07645847.gif)           <br/> |
|<span data-ttu-id="15b82-110">2</span><span class="sxs-lookup"><span data-stu-id="15b82-110">2</span></span>  <br/> |![](media/IC_Bullet2_ZA07645848.gif)           <br/> |
|<span data-ttu-id="15b82-111">3</span><span class="sxs-lookup"><span data-stu-id="15b82-111">3</span></span>  <br/> |![](media/IC_Bullet3_ZA07645849.gif)           <br/> |
|<span data-ttu-id="15b82-112">4</span><span class="sxs-lookup"><span data-stu-id="15b82-112">4</span></span>  <br/> |![](media/IC_Bullet4_ZA07645851.gif)           <br/> |
|<span data-ttu-id="15b82-113">5</span><span class="sxs-lookup"><span data-stu-id="15b82-113">5</span></span>  <br/> |![](media/IC_Bullet5_ZA07645852.gif)           <br/> |
|<span data-ttu-id="15b82-114">6</span><span class="sxs-lookup"><span data-stu-id="15b82-114">6</span></span>  <br/> |![](media/IC_Bullet6_ZA07645853.gif)           <br/> |
|<span data-ttu-id="15b82-115">7</span><span class="sxs-lookup"><span data-stu-id="15b82-115">7</span></span>  <br/> |![](media/IC_Bullet7_ZA07645854.gif)           <br/> |
   
|||
|:-----|:-----|
|<span data-ttu-id="15b82-116">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="15b82-116">Section index:</span></span>  <br/> |<span data-ttu-id="15b82-117">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="15b82-117">**visSectionParagraph**</span></span> <br/> |
|<span data-ttu-id="15b82-118">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="15b82-118">Row index:</span></span>  <br/> |<span data-ttu-id="15b82-119">**visRowParagraph** +  *i* где *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="15b82-119">**visRowParagraph** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="15b82-120">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="15b82-120">Cell index:</span></span>  <br/> |<span data-ttu-id="15b82-121">**visBulletIndex**</span><span class="sxs-lookup"><span data-stu-id="15b82-121">**visBulletIndex**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15b82-122">Замечания</span><span class="sxs-lookup"><span data-stu-id="15b82-122">Remarks</span></span>

<span data-ttu-id="15b82-123">Вы может также необходимо задать значение ячейки, щелкнув правой кнопкой мыши фигуру, с указанием **формате**, нажав кнопку **текст**и затем выбрав вкладку **маркеры** .</span><span class="sxs-lookup"><span data-stu-id="15b82-123">You can also set the value of this cell by right-clicking a shape, pointing to **Format**, clicking **Text**, and then clicking the **Bullets** tab.</span></span> 
  
<span data-ttu-id="15b82-124">Для получения ссылки на ячейку маркера по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="15b82-124">To get a reference to the Bullet cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15b82-125">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="15b82-125">Cell name:</span></span>  <br/> |<span data-ttu-id="15b82-126">Para.Bullet [ *i* ] где *i* = < 1 > 2, 3,...</span><span class="sxs-lookup"><span data-stu-id="15b82-126">Para.Bullet[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="15b82-127">Для получения ссылки на ячейки маркера по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="15b82-127">To get a reference to the Bullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  

