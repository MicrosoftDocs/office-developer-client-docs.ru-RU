---
title: Visible Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Указывает, видны ли фигуры уровня на странице рисования.
ms.openlocfilehash: 4266debc318c839bdd29fa818d11b5e1da669a9e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405452"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="07ebc-103">Visible Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="07ebc-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="07ebc-104">Указывает, видны ли фигуры уровня на странице рисования.</span><span class="sxs-lookup"><span data-stu-id="07ebc-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="07ebc-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="07ebc-105">**Value**</span></span>|<span data-ttu-id="07ebc-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="07ebc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07ebc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="07ebc-107">TRUE</span></span>  <br/> |<span data-ttu-id="07ebc-108">Фигуры видны.</span><span class="sxs-lookup"><span data-stu-id="07ebc-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="07ebc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="07ebc-109">FALSE</span></span>  <br/> |<span data-ttu-id="07ebc-110">Фигуры скрыты.</span><span class="sxs-lookup"><span data-stu-id="07ebc-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07ebc-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="07ebc-111">Remarks</span></span>

<span data-ttu-id="07ebc-112">Эта ячейка соответствует параметру **Visible** в диалоговом **окне** "Свойства  слоя" (на вкладке "Главная" в группе редактирования щелкните "Слои" и выберите "Свойства **уровня").**  </span><span class="sxs-lookup"><span data-stu-id="07ebc-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="07ebc-113">Чтобы получить ссылку на ячейку Visible по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="07ebc-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07ebc-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="07ebc-114">Cell name:</span></span>  <br/> |<span data-ttu-id="07ebc-115">Layers.Visible[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="07ebc-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="07ebc-116">Чтобы получить ссылку на ячейку Visible по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="07ebc-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07ebc-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="07ebc-117">Section index:</span></span>  <br/> |<span data-ttu-id="07ebc-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="07ebc-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="07ebc-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="07ebc-119">Row index:</span></span>  <br/> |<span data-ttu-id="07ebc-120">**visRowLayer**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="07ebc-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="07ebc-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="07ebc-121">Cell index:</span></span>  <br/> |<span data-ttu-id="07ebc-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="07ebc-122">**visLayerVisible**</span></span> <br/> |
   

