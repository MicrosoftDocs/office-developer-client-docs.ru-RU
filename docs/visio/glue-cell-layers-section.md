---
title: Glue Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm415
localization_priority: Normal
ms.assetid: 75f2ea45-52ac-ddfa-14ea-402933ae2449
description: Указывает, можно ли приклеить фигуры, принадлежащие к слой.
ms.openlocfilehash: 55886a7e96bd2c08966cb85f5edad6a7174e30cd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408518"
---
# <a name="glue-cell-layers-section"></a><span data-ttu-id="4cad8-103">Glue Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="4cad8-103">Glue Cell (Layers Section)</span></span>

<span data-ttu-id="4cad8-104">Указывает, можно ли приклеить фигуры, принадлежащие к слой.</span><span class="sxs-lookup"><span data-stu-id="4cad8-104">Specifies whether shapes belonging to the layer can be glued.</span></span>
  
|<span data-ttu-id="4cad8-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4cad8-105">**Value**</span></span>|<span data-ttu-id="4cad8-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4cad8-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cad8-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4cad8-107">TRUE</span></span>  <br/> |<span data-ttu-id="4cad8-108">Приклейка включена.</span><span class="sxs-lookup"><span data-stu-id="4cad8-108">Glue is enabled.</span></span>  <br/> |
|<span data-ttu-id="4cad8-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4cad8-109">FALSE</span></span>  <br/> |<span data-ttu-id="4cad8-110">Приклейка отключена.</span><span class="sxs-lookup"><span data-stu-id="4cad8-110">Glue is disabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cad8-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="4cad8-111">Remarks</span></span>

<span data-ttu-id="4cad8-112">Эта ячейка соответствует параметру **Glue** в диалоговом **окне** "Свойства  слоя" (на вкладке "Главная" в группе редактирования щелкните "Слои" и выберите "Свойства **уровня").**  </span><span class="sxs-lookup"><span data-stu-id="4cad8-112">This cell corresponds to the **Glue** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties** ).</span></span> 
  
<span data-ttu-id="4cad8-113">Чтобы получить ссылку на ячейку Glue по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4cad8-113">To get a reference to the Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cad8-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4cad8-114">Cell name:</span></span>  <br/> |<span data-ttu-id="4cad8-115">Layers.Glue[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4cad8-115">Layers.Glue[  *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4cad8-116">Чтобы получить ссылку на ячейку Glue по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4cad8-116">To get a reference to the Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cad8-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4cad8-117">Section index:</span></span>  <br/> |<span data-ttu-id="4cad8-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="4cad8-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="4cad8-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4cad8-119">Row index:</span></span>  <br/> |<span data-ttu-id="4cad8-120">**visRowLayer**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4cad8-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4cad8-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4cad8-121">Cell index:</span></span>  <br/> |<span data-ttu-id="4cad8-122">**visLayerGlue**</span><span class="sxs-lookup"><span data-stu-id="4cad8-122">**visLayerGlue**</span></span> <br/> |
   

