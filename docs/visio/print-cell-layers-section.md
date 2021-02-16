---
title: Print Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm825
localization_priority: Normal
ms.assetid: 9c76bf02-7269-65bb-2fd2-920243d962ef
description: Указывает, можно ли печатать фигуры, принадлежащие слои.
ms.openlocfilehash: f9a1dca6d45b53c02ff0ed29f921c352fc947630
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435217"
---
# <a name="print-cell-layers-section"></a><span data-ttu-id="4c414-103">Print Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="4c414-103">Print Cell (Layers Section)</span></span>

<span data-ttu-id="4c414-104">Указывает, можно ли печатать фигуры, принадлежащие слои.</span><span class="sxs-lookup"><span data-stu-id="4c414-104">Specifies whether shapes belonging to the layer can be printed.</span></span>
  
|<span data-ttu-id="4c414-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="4c414-105">**Value**</span></span>|<span data-ttu-id="4c414-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="4c414-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4c414-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="4c414-107">TRUE</span></span>  <br/> |<span data-ttu-id="4c414-108">Фигуры можно печатать.</span><span class="sxs-lookup"><span data-stu-id="4c414-108">Shapes can be printed.</span></span>  <br/> |
|<span data-ttu-id="4c414-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="4c414-109">FALSE</span></span>  <br/> |<span data-ttu-id="4c414-110">Фигуры невозможно печатать.</span><span class="sxs-lookup"><span data-stu-id="4c414-110">Shapes cannot be printed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c414-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="4c414-111">Remarks</span></span>

<span data-ttu-id="4c414-112">Это значение также можно установить  с помощью параметра "Печать" в  диалоговом  **окне** "Свойства слоя" (на вкладке "Главная" в группе редактирования щелкните "Слои" и выберите "Свойства уровня"). </span><span class="sxs-lookup"><span data-stu-id="4c414-112">You can also set this value by using the **Print** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="4c414-113">Чтобы получить ссылку на ячейку Print по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="4c414-113">To get a reference to the Print cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c414-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="4c414-114">Cell name:</span></span>  <br/> |<span data-ttu-id="4c414-115">Layers.Print[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4c414-115">Layers.Print[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4c414-116">Чтобы получить ссылку на ячейку Print по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="4c414-116">To get a reference to the Print cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c414-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="4c414-117">Section index:</span></span>  <br/> |<span data-ttu-id="4c414-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="4c414-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="4c414-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="4c414-119">Row index:</span></span>  <br/> |<span data-ttu-id="4c414-120">**visRowLayer**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4c414-120">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4c414-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="4c414-121">Cell index:</span></span>  <br/> |<span data-ttu-id="4c414-122">**visDocPreviewScope**</span><span class="sxs-lookup"><span data-stu-id="4c414-122">**visDocPreviewScope**</span></span> <br/> |
   

