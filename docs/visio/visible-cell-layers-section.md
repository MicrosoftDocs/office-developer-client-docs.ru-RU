---
title: Ячейка Visible (раздел "Слои")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1110
localization_priority: Normal
ms.assetid: 02048012-a814-410b-f26e-56fcfbe106e6
description: Указывает, отображаются на странице документа ли фигур, относящегося к слою.
ms.openlocfilehash: 9a025403b1f5b46d2f439805a15954eaeeab2686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815140"
---
# <a name="visible-cell-layers-section"></a><span data-ttu-id="257cb-103">Ячейка Visible (раздел "Слои")</span><span class="sxs-lookup"><span data-stu-id="257cb-103">Visible Cell (Layers Section)</span></span>

<span data-ttu-id="257cb-104">Указывает, отображаются на странице документа ли фигур, относящегося к слою.</span><span class="sxs-lookup"><span data-stu-id="257cb-104">Specifies whether shapes belonging to the layer are visible on the drawing page.</span></span>
  
|<span data-ttu-id="257cb-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="257cb-105">**Value**</span></span>|<span data-ttu-id="257cb-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="257cb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="257cb-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="257cb-107">TRUE</span></span>  <br/> |<span data-ttu-id="257cb-108">Видны фигур.</span><span class="sxs-lookup"><span data-stu-id="257cb-108">Shapes are visible.</span></span>  <br/> |
|<span data-ttu-id="257cb-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="257cb-109">FALSE</span></span>  <br/> |<span data-ttu-id="257cb-110">Фигуры являются скрытыми.</span><span class="sxs-lookup"><span data-stu-id="257cb-110">Shapes are hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="257cb-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="257cb-111">Remarks</span></span>

<span data-ttu-id="257cb-112">В этой ячейке соответствует параметру **Visible** в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer** ).</span><span class="sxs-lookup"><span data-stu-id="257cb-112">This cell corresponds to the **Visible** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="257cb-113">Для получения ссылки на ячейки видимым по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="257cb-113">To get a reference to the Visible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="257cb-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="257cb-114">Cell name:</span></span>  <br/> |<span data-ttu-id="257cb-115">Layers.Visible [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="257cb-115">Layers.Visible[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="257cb-116">Для получения ссылки на ячейки видимым по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="257cb-116">To get a reference to the Visible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="257cb-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="257cb-117">Section index:</span></span>  <br/> |<span data-ttu-id="257cb-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="257cb-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="257cb-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="257cb-119">Row index:</span></span>  <br/> |<span data-ttu-id="257cb-120">**visRowLayer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="257cb-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="257cb-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="257cb-121">Cell index:</span></span>  <br/> |<span data-ttu-id="257cb-122">**visLayerVisible**</span><span class="sxs-lookup"><span data-stu-id="257cb-122">**visLayerVisible**</span></span> <br/> |
   

