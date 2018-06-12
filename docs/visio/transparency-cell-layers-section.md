---
title: Прозрачность ячейки (слои раздел)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Определяет уровень прозрачности цвета слоя.
ms.openlocfilehash: 7c205612436e7731f268e17c851616beebf809dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815059"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="7f7dd-103">Прозрачность ячейки (слои раздел)</span><span class="sxs-lookup"><span data-stu-id="7f7dd-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="7f7dd-104">Определяет уровень прозрачности цвета слоя.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="7f7dd-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="7f7dd-105">**Value**</span></span>|<span data-ttu-id="7f7dd-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7f7dd-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7f7dd-107">0 — 100</span><span class="sxs-lookup"><span data-stu-id="7f7dd-107">0 - 100</span></span>  <br/> |<span data-ttu-id="7f7dd-108">Представляет собой процентную долю прозрачность.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="7f7dd-109">Значение по умолчанию — 0% (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="7f7dd-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7f7dd-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="7f7dd-110">Remarks</span></span>

<span data-ttu-id="7f7dd-111">Значения округляются до ближайшего большего половины процентов.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="7f7dd-112">Значение 100% является полностью прозрачным.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="7f7dd-113">Несмотря на то, что уровень полностью прозрачным цвета появится на странице документа как уровень не цвета, взаимодействия с других объектов на странице так же, как как если бы его прозрачность 0%.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="7f7dd-114">Также можно задать это значение с помощью элемента управления ползунок в диалоговом окне **Свойства слоя** (на вкладке **Главная** в группе **Редактирование** щелкните **слои**и выберите пункт **Свойства Layer**).</span><span class="sxs-lookup"><span data-stu-id="7f7dd-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="7f7dd-115">Чтобы получить ссылку на ячейку прозрачность по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="7f7dd-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f7dd-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="7f7dd-116">Cell name:</span></span>  <br/> |<span data-ttu-id="7f7dd-117">Layers.ColorTrans [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7f7dd-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7f7dd-118">Для получения ссылки на ячейки прозрачность по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="7f7dd-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7f7dd-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7f7dd-119">Section index:</span></span>  <br/> |<span data-ttu-id="7f7dd-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="7f7dd-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="7f7dd-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7f7dd-121">Row index:</span></span>  <br/> |<span data-ttu-id="7f7dd-122">**visRowLayer** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7f7dd-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7f7dd-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7f7dd-123">Cell index:</span></span>  <br/> |<span data-ttu-id="7f7dd-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="7f7dd-124">**visLayerColorTrans**</span></span> <br/> |
   

