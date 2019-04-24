---
title: FillBkgndTrans Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253230
localization_priority: Normal
ms.assetid: 87065350-ba9a-aae8-47f6-f263f6700d08
description: Определяет уровень прозрачности для цвета фона (заливки) узора заливки фигуры.
ms.openlocfilehash: 64c5d09fb18f089769e025893b9fac8b1878fca1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322486"
---
# <a name="fillbkgndtrans-cell-fill-format-section"></a><span data-ttu-id="9b6e0-103">FillBkgndTrans Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="9b6e0-103">FillBkgndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="9b6e0-104">Определяет уровень прозрачности для цвета фона (заливки) узора заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-104">Determines the transparency level for the background (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="9b6e0-105">**Value**</span><span class="sxs-lookup"><span data-stu-id="9b6e0-105">**Value**</span></span>|<span data-ttu-id="9b6e0-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9b6e0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9b6e0-107">0-100</span><span class="sxs-lookup"><span data-stu-id="9b6e0-107">0 - 100</span></span>  <br/> |<span data-ttu-id="9b6e0-108">Представляет процент прозрачности.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="9b6e0-109">Значение по умолчанию: 0% (полностью непрозрачно).</span><span class="sxs-lookup"><span data-stu-id="9b6e0-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9b6e0-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="9b6e0-110">Remarks</span></span>

<span data-ttu-id="9b6e0-111">Значения округляются до ближайшей половины процентов.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="9b6e0-112">Значение 100% полностью прозрачно.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="9b6e0-113">Несмотря на то, что фигура с полностью прозрачной заливкой отображается точно так же, как и фигура без заливки на странице документа, она будет взаимодействовать с другими объектами на странице тем же способом, что и прозрачность 0%.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-113">Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="9b6e0-114">Это значение также можно задать с помощью ползунка в диалоговом \*\*\*\* окне "Заливка" (на вкладке **Главная** , в группе **фигур** нажмите кнопку **Заливка**, а затем выберите команду **Параметры заливки**).</span><span class="sxs-lookup"><span data-stu-id="9b6e0-114">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span> <span data-ttu-id="9b6e0-115">Это значение управляет значениями прозрачности фона и фоновой заливки.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-115">This value controls the value of both the background and foreground fill transparencies.</span></span> <span data-ttu-id="9b6e0-116">Чтобы задать эти значения независимо друг от друга, необходимо ввести их в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="9b6e0-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="9b6e0-117">Чтобы получить ссылку на ячейку FillBkgndTrans по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="9b6e0-117">To get a reference to the FillBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b6e0-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="9b6e0-118">Cell name:</span></span>  <br/> |<span data-ttu-id="9b6e0-119">FillBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="9b6e0-119">FillBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="9b6e0-120">Чтобы получить ссылку на ячейку FillBkgndTrans по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="9b6e0-120">To get a reference to the FillBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9b6e0-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="9b6e0-121">Section index:</span></span>  <br/> |<span data-ttu-id="9b6e0-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9b6e0-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9b6e0-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="9b6e0-123">Row index:</span></span>  <br/> |<span data-ttu-id="9b6e0-124">**Висровфилл**</span><span class="sxs-lookup"><span data-stu-id="9b6e0-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="9b6e0-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="9b6e0-125">Cell index:</span></span>  <br/> |<span data-ttu-id="9b6e0-126">**Висфиллбкгндтранс**</span><span class="sxs-lookup"><span data-stu-id="9b6e0-126">**visFillBkgndTrans**</span></span> <br/> |
   

