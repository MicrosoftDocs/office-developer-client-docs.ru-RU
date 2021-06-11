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
description: Определяет, могут ли другие фигуры привязаться к фигурам, назначенным на этот слой. Фигуры, присвоенные слою, могут привязаться к другим фигурам, но другие фигуры не могут привязаться к ним.
ms.openlocfilehash: 87e7e7500469fb7f8c7fdd4771a0225d0e4fc993
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434846"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="0e312-104">Snap Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="0e312-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="0e312-105">Определяет, могут ли другие фигуры привязаться к фигурам, назначенным на этот слой.</span><span class="sxs-lookup"><span data-stu-id="0e312-105">Determines whether other shapes can snap to shapes assigned to the layer.</span></span> <span data-ttu-id="0e312-106">Фигуры, присвоенные слою, могут привязаться к другим фигурам, но другие фигуры не могут привязаться к ним.</span><span class="sxs-lookup"><span data-stu-id="0e312-106">Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="0e312-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="0e312-107">**Value**</span></span>|<span data-ttu-id="0e312-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0e312-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0e312-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="0e312-109">TRUE</span></span>  <br/> |<span data-ttu-id="0e312-110">Другие фигуры могут привязаться к фигурам на уровне.</span><span class="sxs-lookup"><span data-stu-id="0e312-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="0e312-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="0e312-111">FALSE</span></span>  <br/> |<span data-ttu-id="0e312-112">Другие фигуры не могут привязаться к фигурам на уровне.</span><span class="sxs-lookup"><span data-stu-id="0e312-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0e312-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="0e312-113">Remarks</span></span>

<span data-ttu-id="0e312-114">Вы также можете установить значение этой ячейки с помощью параметра **прикрепление** в диалоговом окне **Layer Properties** (на вкладке **Главная,** в группе редактирования щелкните Слои **и** нажмите кнопку **Layer Properties).** </span><span class="sxs-lookup"><span data-stu-id="0e312-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="0e312-115">Чтобы получить ссылку на ячейку прикрепление по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="0e312-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e312-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e312-116">Cell name:</span></span>  <br/> |<span data-ttu-id="0e312-117">Слои. прикрепление, *где* *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0e312-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0e312-118">Чтобы получить ссылку на ячейку прикрепление по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="0e312-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0e312-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="0e312-119">Section index:</span></span>  <br/> |<span data-ttu-id="0e312-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="0e312-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="0e312-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="0e312-121">Row index:</span></span>  <br/> |<span data-ttu-id="0e312-122">**visRowLayer**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="0e312-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="0e312-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="0e312-123">Cell index:</span></span>  <br/> |<span data-ttu-id="0e312-124">**visLayerSnap**</span><span class="sxs-lookup"><span data-stu-id="0e312-124">**visLayerSnap**</span></span> <br/> |
   

