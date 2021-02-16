---
title: Active Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Указывает, активен ли уровень. Фигуры без предварительно заранее назначены активным слоям при перетаскивания их на страницу рисования.
ms.openlocfilehash: f97f7dc09d1f882452ae2234882de45f06bd0da1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417436"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="e3b58-104">Active Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="e3b58-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="e3b58-105">Указывает, активен ли уровень.</span><span class="sxs-lookup"><span data-stu-id="e3b58-105">Specifies whether the layer is active.</span></span> <span data-ttu-id="e3b58-106">Фигуры без предварительно заранее назначены активным слоям при перетаскивания их на страницу рисования.</span><span class="sxs-lookup"><span data-stu-id="e3b58-106">Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="e3b58-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e3b58-107">**Value**</span></span>|<span data-ttu-id="e3b58-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3b58-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3b58-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="e3b58-109">TRUE</span></span>  <br/> |<span data-ttu-id="e3b58-110">Уровень активен.</span><span class="sxs-lookup"><span data-stu-id="e3b58-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="e3b58-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="e3b58-111">FALSE</span></span>  <br/> |<span data-ttu-id="e3b58-112">Слой не активен.</span><span class="sxs-lookup"><span data-stu-id="e3b58-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3b58-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3b58-113">Remarks</span></span>

<span data-ttu-id="e3b58-114">Значение в этой ячейке  соответствует активному параметру в диалоговом  **окне**  "Свойства слоя" (в группе редактирования на вкладке "Главная" щелкните "Слои" и выберите "Свойства **уровня").** </span><span class="sxs-lookup"><span data-stu-id="e3b58-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="e3b58-115">Чтобы получить ссылку на ячейку Active по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="e3b58-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3b58-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="e3b58-116">Cell name:</span></span>  <br/> |<span data-ttu-id="e3b58-117">Layers.Active[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e3b58-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e3b58-118">Чтобы получить ссылку на ячейку Active по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="e3b58-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3b58-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e3b58-119">Section index:</span></span>  <br/> |<span data-ttu-id="e3b58-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="e3b58-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="e3b58-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e3b58-121">Row index:</span></span>  <br/> |<span data-ttu-id="e3b58-122">**visRowLayer**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e3b58-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e3b58-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e3b58-123">Cell index:</span></span>  <br/> |<span data-ttu-id="e3b58-124">**visLayerActive**</span><span class="sxs-lookup"><span data-stu-id="e3b58-124">**visLayerActive**</span></span> <br/> |
   

