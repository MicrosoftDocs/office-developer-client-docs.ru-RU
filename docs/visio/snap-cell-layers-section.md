---
title: Snap Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Определяет, могут ли другие фигуры привязываться к фигурам, назначенным для слоя. Фигуры, назначенные слою, могут быть привязаны к другим фигурам, но не могут привязываться к ним.
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359810"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="15945-104">Snap Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="15945-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="15945-105">Определяет, могут ли другие фигуры привязываться к фигурам, назначенным для слоя.</span><span class="sxs-lookup"><span data-stu-id="15945-105">Determines whether other shapes can snap to shapes assigned to the layer.</span></span> <span data-ttu-id="15945-106">Фигуры, назначенные слою, могут быть привязаны к другим фигурам, но не могут привязываться к ним.</span><span class="sxs-lookup"><span data-stu-id="15945-106">Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="15945-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="15945-107">**Value**</span></span>|<span data-ttu-id="15945-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="15945-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="15945-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="15945-109">TRUE</span></span>  <br/> |<span data-ttu-id="15945-110">Другие фигуры могут привязываться к фигурам в слое.</span><span class="sxs-lookup"><span data-stu-id="15945-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="15945-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="15945-111">FALSE</span></span>  <br/> |<span data-ttu-id="15945-112">Другие фигуры не могут быть привязаны к фигурам в слое.</span><span class="sxs-lookup"><span data-stu-id="15945-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="15945-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="15945-113">Remarks</span></span>

<span data-ttu-id="15945-114">Значение этой ячейки также можно задать с помощью параметра " **привязать** " в диалоговом окне **Свойства слоя** (на вкладке **Главная** , в группе **Правка** щелкните **слои**, а затем выберите **Свойства слоя**).</span><span class="sxs-lookup"><span data-stu-id="15945-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="15945-115">Чтобы получить ссылку на ячейку привязки по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="15945-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15945-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="15945-116">Cell name:</span></span>  <br/> |<span data-ttu-id="15945-117">Слои. Snapin [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="15945-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="15945-118">Чтобы получить ссылку на ячейку привязки по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="15945-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="15945-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="15945-119">Section index:</span></span>  <br/> |<span data-ttu-id="15945-120">**Виссектионлайер**</span><span class="sxs-lookup"><span data-stu-id="15945-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="15945-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="15945-121">Row index:</span></span>  <br/> |<span data-ttu-id="15945-122">**висровлайер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="15945-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="15945-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="15945-123">Cell index:</span></span>  <br/> |<span data-ttu-id="15945-124">**Вислайерснап**</span><span class="sxs-lookup"><span data-stu-id="15945-124">**visLayerSnap**</span></span> <br/> |
   

