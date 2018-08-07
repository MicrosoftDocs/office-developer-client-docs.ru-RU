---
title: Ячейка Active (раздел "Слои")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm10
localization_priority: Normal
ms.assetid: 4c8e366f-9e9b-30ea-a89f-57c8d7a1168e
description: Указывает, активна ли уровень. Фигуры без назначенный слои назначаются active слои при перетаскивании на страницу документа.
ms.openlocfilehash: 81d3ec083e207a927c46dda99e2b7f42c0a7bd8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813135"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="bd6c3-104">Ячейка Active (раздел "Слои")</span><span class="sxs-lookup"><span data-stu-id="bd6c3-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="bd6c3-105">Указывает, активна ли уровень.</span><span class="sxs-lookup"><span data-stu-id="bd6c3-105">Specifies whether the layer is active.</span></span> <span data-ttu-id="bd6c3-106">Фигуры без назначенный слои назначаются active слои при перетаскивании на страницу документа.</span><span class="sxs-lookup"><span data-stu-id="bd6c3-106">Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="bd6c3-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="bd6c3-107">**Value**</span></span>|<span data-ttu-id="bd6c3-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="bd6c3-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd6c3-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="bd6c3-109">TRUE</span></span>  <br/> |<span data-ttu-id="bd6c3-110">Слой активен.</span><span class="sxs-lookup"><span data-stu-id="bd6c3-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="bd6c3-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="bd6c3-111">FALSE</span></span>  <br/> |<span data-ttu-id="bd6c3-112">Уровень не является активным.</span><span class="sxs-lookup"><span data-stu-id="bd6c3-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd6c3-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="bd6c3-113">Remarks</span></span>

<span data-ttu-id="bd6c3-114">Значение в этой ячейке соответствует параметру **Active** в диалоговом окне **Свойства слоя** (в группе **Правка** на вкладке **Главная** нажмите кнопку **уровни**и выберите пункт **Свойства Layer**).</span><span class="sxs-lookup"><span data-stu-id="bd6c3-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="bd6c3-115">Чтобы получить ссылку на активную ячейку по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="bd6c3-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd6c3-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="bd6c3-116">Cell name:</span></span>  <br/> |<span data-ttu-id="bd6c3-117">Layers.Active [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bd6c3-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bd6c3-118">Для получения ссылки на активную ячейку по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="bd6c3-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bd6c3-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="bd6c3-119">Section index:</span></span>  <br/> |<span data-ttu-id="bd6c3-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="bd6c3-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="bd6c3-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="bd6c3-121">Row index:</span></span>  <br/> |<span data-ttu-id="bd6c3-122">**visRowLayer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bd6c3-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="bd6c3-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="bd6c3-123">Cell index:</span></span>  <br/> |<span data-ttu-id="bd6c3-124">**visLayerActive**</span><span class="sxs-lookup"><span data-stu-id="bd6c3-124">**visLayerActive**</span></span> <br/> |
   

