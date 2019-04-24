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
description: Указывает, активен ли слой. Фигуры без предварительно назначенных слоев назначаются активным слоям при их перетаскивании на страницу документа.
ms.openlocfilehash: f97f7dc09d1f882452ae2234882de45f06bd0da1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338782"
---
# <a name="active-cell-layers-section"></a><span data-ttu-id="173be-104">Active Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="173be-104">Active Cell (Layers Section)</span></span>

<span data-ttu-id="173be-105">Указывает, активен ли слой.</span><span class="sxs-lookup"><span data-stu-id="173be-105">Specifies whether the layer is active.</span></span> <span data-ttu-id="173be-106">Фигуры без предварительно назначенных слоев назначаются активным слоям при их перетаскивании на страницу документа.</span><span class="sxs-lookup"><span data-stu-id="173be-106">Shapes without pre-assigned layers are assigned to the active layer(s) when you drag them onto the drawing page.</span></span>
  
|<span data-ttu-id="173be-107">**Value**</span><span class="sxs-lookup"><span data-stu-id="173be-107">**Value**</span></span>|<span data-ttu-id="173be-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="173be-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="173be-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="173be-109">TRUE</span></span>  <br/> |<span data-ttu-id="173be-110">Слой активен.</span><span class="sxs-lookup"><span data-stu-id="173be-110">Layer is active.</span></span>  <br/> |
|<span data-ttu-id="173be-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="173be-111">FALSE</span></span>  <br/> |<span data-ttu-id="173be-112">Слой не активен.</span><span class="sxs-lookup"><span data-stu-id="173be-112">Layer is not active.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="173be-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="173be-113">Remarks</span></span>

<span data-ttu-id="173be-114">Значение в этой ячейке соответствует параметру **Активная** в диалоговом окне **Свойства слоя** (в группе **Правка** на вкладке **Главная** щелкните **слои**, а затем выберите **Свойства слоя**).</span><span class="sxs-lookup"><span data-stu-id="173be-114">The value in this cell corresponds to the **Active** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="173be-115">Чтобы получить ссылку на активную ячейку по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="173be-115">To get a reference to the Active cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="173be-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="173be-116">Cell name:</span></span>  <br/> |<span data-ttu-id="173be-117">Слои. Active [ *i* ], где *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="173be-117">Layers.Active[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="173be-118">Чтобы получить ссылку на активную ячейку по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="173be-118">To get a reference to the Active cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="173be-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="173be-119">Section index:</span></span>  <br/> |<span data-ttu-id="173be-120">**Виссектионлайер**</span><span class="sxs-lookup"><span data-stu-id="173be-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="173be-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="173be-121">Row index:</span></span>  <br/> |<span data-ttu-id="173be-122">**висровлайер** +  *i* , где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="173be-122">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="173be-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="173be-123">Cell index:</span></span>  <br/> |<span data-ttu-id="173be-124">**Вислайерактиве**</span><span class="sxs-lookup"><span data-stu-id="173be-124">**visLayerActive**</span></span> <br/> |
   

