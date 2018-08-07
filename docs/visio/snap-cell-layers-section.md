---
title: Ячейка Snap (раздел "Слои")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251355
localization_priority: Normal
ms.assetid: c1b24e45-6f08-686b-b53d-e85fb9087a50
description: Определяет, могут привязываются ли другие элементы для фигур, назначенных на уровень. Фигур, назначенных на уровень можно привязать к другим фигурам, но другие фигуры невозможно привязать к ним.
ms.openlocfilehash: 7fc684afb67d0454ea5907c08f4f7644d97c7f74
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814891"
---
# <a name="snap-cell-layers-section"></a><span data-ttu-id="c686e-104">Ячейка Snap (раздел "Слои")</span><span class="sxs-lookup"><span data-stu-id="c686e-104">Snap Cell (Layers Section)</span></span>

<span data-ttu-id="c686e-105">Определяет, могут привязываются ли другие элементы для фигур, назначенных на уровень.</span><span class="sxs-lookup"><span data-stu-id="c686e-105">Determines whether other shapes can snap to shapes assigned to the layer.</span></span> <span data-ttu-id="c686e-106">Фигур, назначенных на уровень можно привязать к другим фигурам, но другие фигуры невозможно привязать к ним.</span><span class="sxs-lookup"><span data-stu-id="c686e-106">Shapes assigned to the layer can snap to other shapes, but other shapes can't snap to them.</span></span>
  
|<span data-ttu-id="c686e-107">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c686e-107">**Value**</span></span>|<span data-ttu-id="c686e-108">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c686e-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c686e-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="c686e-109">TRUE</span></span>  <br/> |<span data-ttu-id="c686e-110">Другие фигуры можно привязать к фигурам в слое.</span><span class="sxs-lookup"><span data-stu-id="c686e-110">Other shapes can snap to shapes on the layer.</span></span>  <br/> |
|<span data-ttu-id="c686e-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="c686e-111">FALSE</span></span>  <br/> |<span data-ttu-id="c686e-112">Другие фигуры невозможно привязать к фигур на уровне.</span><span class="sxs-lookup"><span data-stu-id="c686e-112">Other shapes cannot snap to shapes on the layer.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c686e-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="c686e-113">Remarks</span></span>

<span data-ttu-id="c686e-114">Также можно задать значение ячейки с помощью режим **привязки** в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer**).</span><span class="sxs-lookup"><span data-stu-id="c686e-114">You can also set the value of this cell using the **Snap** option in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="c686e-115">Для получения ссылки на ячейки привязки по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c686e-115">To get a reference to the Snap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c686e-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c686e-116">Cell name:</span></span>  <br/> |<span data-ttu-id="c686e-117">Layers.Snap [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="c686e-117">Layers.Snap[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="c686e-118">Для получения ссылки на ячейки привязки по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c686e-118">To get a reference to the Snap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c686e-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c686e-119">Section index:</span></span>  <br/> |<span data-ttu-id="c686e-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="c686e-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="c686e-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c686e-121">Row index:</span></span>  <br/> |<span data-ttu-id="c686e-122">**visRowLayer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c686e-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c686e-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c686e-123">Cell index:</span></span>  <br/> |<span data-ttu-id="c686e-124">**visLayerSnap**</span><span class="sxs-lookup"><span data-stu-id="c686e-124">**visLayerSnap**</span></span> <br/> |
   

