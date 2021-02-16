---
title: ShdwForegndTrans Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253253
localization_priority: Normal
ms.assetid: c42d4d2e-f8f0-bc5b-6018-4bb4ffa81b64
description: Определяет уровень прозрачности для цвета, используемого для переднего плана (росчерка) шаблона заливки тени для отпадения фигуры.
ms.openlocfilehash: 0ef3ce525edcce4ccd61f36649ead512545eef58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435042"
---
# <a name="shdwforegndtrans-cell-fill-format-section"></a><span data-ttu-id="225c4-103">ShdwForegndTrans Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="225c4-103">ShdwForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="225c4-104">Определяет уровень прозрачности для цвета, используемого для переднего плана (росчерка) шаблона заливки тени для отпадения фигуры.</span><span class="sxs-lookup"><span data-stu-id="225c4-104">Determines the transparency level for the color used for the foreground (stroke) of the shape's drop shadow fill pattern.</span></span>
  
|<span data-ttu-id="225c4-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="225c4-105">**Value**</span></span>|<span data-ttu-id="225c4-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="225c4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="225c4-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="225c4-107">0 - 100</span></span>  <br/> |<span data-ttu-id="225c4-108">Представляет процент прозрачности.</span><span class="sxs-lookup"><span data-stu-id="225c4-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="225c4-109">Значение по умолчанию — 0 % (полностью непрозрачной).</span><span class="sxs-lookup"><span data-stu-id="225c4-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="225c4-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="225c4-110">Remarks</span></span>

<span data-ttu-id="225c4-111">Значения округлются до ближайшей половины процента.</span><span class="sxs-lookup"><span data-stu-id="225c4-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="225c4-112">Значение 100% полностью прозрачно.</span><span class="sxs-lookup"><span data-stu-id="225c4-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="225c4-113">Хотя тень с полностью прозрачной заливки отображается на странице рисования так же, как и тени без заливки, она взаимодействует с другими объектами на странице так же, как если бы ее прозрачность была 0%.</span><span class="sxs-lookup"><span data-stu-id="225c4-113">Although a shadow that has a completely transparent fill appears the same on the drawing page as a shadow that has no fill, it interacts with other objects on the page in the same ways as if its transparency were 0%.</span></span>
  
<span data-ttu-id="225c4-114">Это значение также можно установить с помощью  ползунок в диалоговом окне "Тени" (на вкладке "Главная" в группе фигур щелкните "Тени" и выберите **"Параметры теней").**   </span><span class="sxs-lookup"><span data-stu-id="225c4-114">You can also set this value by using the slider control in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span> <span data-ttu-id="225c4-115">Это значение управляет значением как фоновой, так и передней теней.</span><span class="sxs-lookup"><span data-stu-id="225c4-115">This value controls the value of both the background and foreground shadow transparencies.</span></span> <span data-ttu-id="225c4-116">Чтобы установить эти значения независимо друг от друга, необходимо ввести их в окне ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="225c4-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="225c4-117">Чтобы получить ссылку на ячейку ShdwForegndTrans по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="225c4-117">To get a reference to the ShdwForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="225c4-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="225c4-118">Cell name:</span></span>  <br/> |<span data-ttu-id="225c4-119">ShdwForegndTrans</span><span class="sxs-lookup"><span data-stu-id="225c4-119">ShdwForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="225c4-120">Чтобы получить ссылку на ячейку ShdwForegndTrans по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="225c4-120">To get a reference to the ShdwForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="225c4-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="225c4-121">Section index:</span></span>  <br/> |<span data-ttu-id="225c4-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="225c4-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="225c4-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="225c4-123">Row index:</span></span>  <br/> |<span data-ttu-id="225c4-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="225c4-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="225c4-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="225c4-125">Cell index:</span></span>  <br/> |<span data-ttu-id="225c4-126">**visFillShdwForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="225c4-126">**visFillShdwForegndTrans**</span></span> <br/> |
   

