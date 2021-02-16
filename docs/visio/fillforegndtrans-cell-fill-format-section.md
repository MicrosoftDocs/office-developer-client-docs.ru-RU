---
title: FillForegndTrans Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: Определяет уровень прозрачности для цвета переднего плана (заливки) шаблона заливки фигуры.
ms.openlocfilehash: d05a83f83ea3d95ac3d42a2bfb3996917119f580
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427852"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a><span data-ttu-id="11aff-103">FillForegndTrans Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="11aff-103">FillForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="11aff-104">Определяет уровень прозрачности для цвета переднего плана (заливки) шаблона заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="11aff-104">Determines the transparency level for the foreground (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="11aff-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="11aff-105">**Value**</span></span>|<span data-ttu-id="11aff-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="11aff-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="11aff-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="11aff-107">0 - 100</span></span>  <br/> |<span data-ttu-id="11aff-108">Представляет процент прозрачности.</span><span class="sxs-lookup"><span data-stu-id="11aff-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="11aff-109">Значение по умолчанию — 0 % (полностью непрозрачной).</span><span class="sxs-lookup"><span data-stu-id="11aff-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="11aff-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="11aff-110">Remarks</span></span>

<span data-ttu-id="11aff-111">Значения округлются до ближайшей половины процента.</span><span class="sxs-lookup"><span data-stu-id="11aff-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="11aff-112">Значение 100% полностью прозрачно.</span><span class="sxs-lookup"><span data-stu-id="11aff-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="11aff-113">Хотя фигура с полностью прозрачной заливки выглядит так же, как фигура без заливки на странице рисования, она будет взаимодействовать с другими объектами на странице так же, как если бы ее прозрачность составляет 0 %.</span><span class="sxs-lookup"><span data-stu-id="11aff-113">Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="11aff-114">Это значение также можно установить с помощью  ползунок в  диалоговом окне "Заливка" (на вкладке "Главная" в группе фигур щелкните "Заполнить" и выберите "Параметры  заливки"). </span><span class="sxs-lookup"><span data-stu-id="11aff-114">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span> <span data-ttu-id="11aff-115">Это значение управляет значением прозрачности заливки фона и переднего плана.</span><span class="sxs-lookup"><span data-stu-id="11aff-115">This value controls the value of both the background and foreground fill transparencies.</span></span> <span data-ttu-id="11aff-116">Чтобы установить эти значения независимо друг от друга, необходимо ввести их в окне Таблицы фигур.</span><span class="sxs-lookup"><span data-stu-id="11aff-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="11aff-117">Чтобы получить ссылку на ячейку FillForegndTrans по имени из другой формулы или из программы, использующей свойство **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="11aff-117">To get a reference to the FillForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11aff-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="11aff-118">Cell name:</span></span>  <br/> |<span data-ttu-id="11aff-119">FillForegndTrans</span><span class="sxs-lookup"><span data-stu-id="11aff-119">FillForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="11aff-120">Чтобы получить ссылку на ячейку FillForegndTrans по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="11aff-120">To get a reference to the FillForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11aff-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="11aff-121">Section index:</span></span>  <br/> |<span data-ttu-id="11aff-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="11aff-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="11aff-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="11aff-123">Row index:</span></span>  <br/> |<span data-ttu-id="11aff-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="11aff-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="11aff-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="11aff-125">Cell index:</span></span>  <br/> |<span data-ttu-id="11aff-126">**visFillForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="11aff-126">**visFillForegndTrans**</span></span> <br/> |
   

