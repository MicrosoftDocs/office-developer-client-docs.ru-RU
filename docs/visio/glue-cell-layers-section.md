---
title: Ячейка связывающих (слои раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Указывает, может быть связан фигур, относящегося к слою.
ms.openlocfilehash: 81a54bebaa8ca68a8fbc8853c69f88efb34bbdb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813848"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="e3c5a-103">Ячейка связывающих (слои раздел)</span><span class="sxs-lookup"><span data-stu-id="e3c5a-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="e3c5a-104">Указывает, может быть связан фигур, относящегося к слою.</span><span class="sxs-lookup"><span data-stu-id="e3c5a-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="e3c5a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="e3c5a-105">**Value**</span></span>|<span data-ttu-id="e3c5a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="e3c5a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3c5a-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e3c5a-107">TRUE</span></span>  <br/> |<span data-ttu-id="e3c5a-108">Связывающих включена.</span><span class="sxs-lookup"><span data-stu-id="e3c5a-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="e3c5a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e3c5a-109">FALSE</span></span>  <br/> |<span data-ttu-id="e3c5a-110">Связывающих отключено.</span><span class="sxs-lookup"><span data-stu-id="e3c5a-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3c5a-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="e3c5a-111">Remarks</span></span>

<span data-ttu-id="e3c5a-112">В этой ячейке соответствует параметру **связывающих** в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer** ).</span><span class="sxs-lookup"><span data-stu-id="e3c5a-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="e3c5a-113">Для получения ссылки на ячейки связывающих по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="e3c5a-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3c5a-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="e3c5a-114">Cell name:</span></span>  <br/> |<span data-ttu-id="e3c5a-115">Layers.Glue [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e3c5a-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e3c5a-116">Для получения ссылки на ячейки связывающих по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="e3c5a-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3c5a-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="e3c5a-117">Section index:</span></span>  <br/> |<span data-ttu-id="e3c5a-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="e3c5a-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="e3c5a-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="e3c5a-119">Row index:</span></span>  <br/> |<span data-ttu-id="e3c5a-120">**visRowLayer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e3c5a-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e3c5a-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="e3c5a-121">Cell index:</span></span>  <br/> |<span data-ttu-id="e3c5a-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="e3c5a-122">**visLayerGlue**</span></span> <br/> |
   

