---
title: Ячейка FillForegndTrans (раздел "Формат заливки")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253231
localization_priority: Normal
ms.assetid: 8b1b3904-6635-3fd1-31a9-ff32c19394af
description: Определяет уровень прозрачности цвет переднего плана (заливки) узора заливки фигуры.
ms.openlocfilehash: f9b09d67bc8d9ae851e86eaaa2ce1d36a92b2da2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813756"
---
# <a name="fillforegndtrans-cell-fill-format-section"></a><span data-ttu-id="c7f9a-103">Ячейка FillForegndTrans (раздел "Формат заливки")</span><span class="sxs-lookup"><span data-stu-id="c7f9a-103">FillForegndTrans Cell (Fill Format Section)</span></span>

<span data-ttu-id="c7f9a-104">Определяет уровень прозрачности цвет переднего плана (заливки) узора заливки фигуры.</span><span class="sxs-lookup"><span data-stu-id="c7f9a-104">Determines the transparency level for the foreground (fill) color of the shape's fill pattern.</span></span>
  
|<span data-ttu-id="c7f9a-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c7f9a-105">**Value**</span></span>|<span data-ttu-id="c7f9a-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c7f9a-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c7f9a-107">0 — 100</span><span class="sxs-lookup"><span data-stu-id="c7f9a-107">0 - 100</span></span>  <br/> |<span data-ttu-id="c7f9a-108">Представляет собой процентную долю прозрачность.</span><span class="sxs-lookup"><span data-stu-id="c7f9a-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="c7f9a-109">Значение по умолчанию — 0% (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="c7f9a-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7f9a-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="c7f9a-110">Remarks</span></span>

<span data-ttu-id="c7f9a-111">Значения округляются до ближайшего большего половины процентов.</span><span class="sxs-lookup"><span data-stu-id="c7f9a-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="c7f9a-112">Значение 100% является полностью прозрачным.</span><span class="sxs-lookup"><span data-stu-id="c7f9a-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="c7f9a-113">Несмотря на то, что фигуры с полностью прозрачной заливкой отображается же, как фигуры без заливки на странице документа, он будет взаимодействовать с другими объектами на странице же образом как в случае его прозрачность 0%.</span><span class="sxs-lookup"><span data-stu-id="c7f9a-113">Although a shape with a completely transparent fill appears the same as a shape with no fill on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span>
  
<span data-ttu-id="c7f9a-114">Также можно задать это значение, с помощью элемента управления ползунок в диалоговом окне **заполнить** (на вкладке **Главная** в группе **фигуру** щелкните **заполните поля**и нажмите кнопку **Параметры заливки**).</span><span class="sxs-lookup"><span data-stu-id="c7f9a-114">You can also set this value using the slider control in the **Fill** dialog box (on the **Home** tab, in the **Shape** group, click **Fill**, and then click **Fill Options**).</span></span> <span data-ttu-id="c7f9a-115">Это значение определяет значение Прозрачность заливки фона и переднего плана.</span><span class="sxs-lookup"><span data-stu-id="c7f9a-115">This value controls the value of both the background and foreground fill transparencies.</span></span> <span data-ttu-id="c7f9a-116">Чтобы задать эти значения независимо друг от друга, необходимо ввести их в окне таблицы свойств фигуры.</span><span class="sxs-lookup"><span data-stu-id="c7f9a-116">To set these values independently, you must enter them in the ShapeSheet window.</span></span>
  
<span data-ttu-id="c7f9a-117">Чтобы получить ссылку на ячейку FillForegndTrans по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c7f9a-117">To get a reference to the FillForegndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7f9a-118">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c7f9a-118">Cell name:</span></span>  <br/> |<span data-ttu-id="c7f9a-119">FillForegndTrans</span><span class="sxs-lookup"><span data-stu-id="c7f9a-119">FillForegndTrans</span></span>  <br/> |
   
<span data-ttu-id="c7f9a-120">Для получения ссылки на ячейки FillForegndTrans по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c7f9a-120">To get a reference to the FillForegndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c7f9a-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c7f9a-121">Section index:</span></span>  <br/> |<span data-ttu-id="c7f9a-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c7f9a-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c7f9a-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c7f9a-123">Row index:</span></span>  <br/> |<span data-ttu-id="c7f9a-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="c7f9a-124">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="c7f9a-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c7f9a-125">Cell index:</span></span>  <br/> |<span data-ttu-id="c7f9a-126">**visFillForegndTrans**</span><span class="sxs-lookup"><span data-stu-id="c7f9a-126">**visFillForegndTrans**</span></span> <br/> |
   

