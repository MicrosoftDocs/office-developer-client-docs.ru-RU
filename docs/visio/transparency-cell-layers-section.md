---
title: Transparency Cell (Layers Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50130
localization_priority: Normal
ms.assetid: 7382e2aa-5e18-19d2-88d8-c4a19a385106
description: Определяет уровень прозрачности цвета слоя.
ms.openlocfilehash: fe0aacf167b2400ca10e22a70c9086429f6059f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436379"
---
# <a name="transparency-cell-layers-section"></a><span data-ttu-id="526f7-103">Transparency Cell (Layers Section)</span><span class="sxs-lookup"><span data-stu-id="526f7-103">Transparency Cell (Layers Section)</span></span>

<span data-ttu-id="526f7-104">Определяет уровень прозрачности цвета слоя.</span><span class="sxs-lookup"><span data-stu-id="526f7-104">Determines the transparency level for a layer color.</span></span>
  
|<span data-ttu-id="526f7-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="526f7-105">**Value**</span></span>|<span data-ttu-id="526f7-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="526f7-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="526f7-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="526f7-107">0 - 100</span></span>  <br/> |<span data-ttu-id="526f7-108">Представляет процент прозрачности.</span><span class="sxs-lookup"><span data-stu-id="526f7-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="526f7-109">По умолчанию — 0% (совершенно непрозрачной).</span><span class="sxs-lookup"><span data-stu-id="526f7-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="526f7-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="526f7-110">Remarks</span></span>

<span data-ttu-id="526f7-111">Значения округлились до ближайшей половины процента.</span><span class="sxs-lookup"><span data-stu-id="526f7-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="526f7-112">Значение 100% полностью прозрачно.</span><span class="sxs-lookup"><span data-stu-id="526f7-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="526f7-113">Несмотря на то, что слой с полностью прозрачным цветом отображается на странице рисования так же, как и слой без цвета, он взаимодействует с другими объектами на странице так же, как если бы его прозрачность была 0%.</span><span class="sxs-lookup"><span data-stu-id="526f7-113">Although a layer that has completely transparent color appears the same on the drawing page as a layer that has no color, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span> <span data-ttu-id="526f7-114">Это значение можно также установить с помощью управления ползунок в диалоговом окне **Layer Properties** (на вкладке **Home,** в группе редактирования щелкните Слои **и** нажмите кнопку **Layer Properties).** </span><span class="sxs-lookup"><span data-stu-id="526f7-114">You can also set this value by using the slider control in the **Layer Properties** dialog box (on the **Home** tab, in the **Editing** group, click **Layers**, and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="526f7-115">Чтобы получить ссылку на ячейку Transparency по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="526f7-115">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="526f7-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="526f7-116">Cell name:</span></span>  <br/> |<span data-ttu-id="526f7-117">Layers.ColorTrans[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="526f7-117">Layers.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="526f7-118">Чтобы получить ссылку на ячейку Прозрачности по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="526f7-118">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="526f7-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="526f7-119">Section index:</span></span>  <br/> |<span data-ttu-id="526f7-120">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="526f7-120">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="526f7-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="526f7-121">Row index:</span></span>  <br/> |<span data-ttu-id="526f7-122">**visRowLayer**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="526f7-122">**visRowLayer** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="526f7-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="526f7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="526f7-124">**visLayerColorTrans**</span><span class="sxs-lookup"><span data-stu-id="526f7-124">**visLayerColorTrans**</span></span> <br/> |
   

