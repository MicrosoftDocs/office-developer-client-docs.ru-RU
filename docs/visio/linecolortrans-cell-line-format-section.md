---
title: LineColorTrans Cell (Line Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50120
localization_priority: Normal
ms.assetid: b68054b5-7efd-1156-9dc1-5ec94e18d227
description: Определяет уровень прозрачности цвета строки фигуры.
ms.openlocfilehash: 555ea15de0279a37bcf67de7374d922b8692ce02
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414440"
---
# <a name="linecolortrans-cell-line-format-section"></a><span data-ttu-id="71830-103">LineColorTrans Cell (Line Format Section)</span><span class="sxs-lookup"><span data-stu-id="71830-103">LineColorTrans Cell (Line Format Section)</span></span>

<span data-ttu-id="71830-104">Определяет уровень прозрачности цвета строки фигуры.</span><span class="sxs-lookup"><span data-stu-id="71830-104">Determines the transparency level of a shape's line color.</span></span>
  
|<span data-ttu-id="71830-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="71830-105">**Value**</span></span>|<span data-ttu-id="71830-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="71830-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="71830-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="71830-107">0 - 100</span></span>  <br/> |<span data-ttu-id="71830-108">Представляет процент прозрачности.</span><span class="sxs-lookup"><span data-stu-id="71830-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="71830-109">По умолчанию — 0% (совершенно непрозрачной).</span><span class="sxs-lookup"><span data-stu-id="71830-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="71830-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="71830-110">Remarks</span></span>

<span data-ttu-id="71830-111">Значения округлились до ближайшей половины процента.</span><span class="sxs-lookup"><span data-stu-id="71830-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="71830-112">Значение 100% полностью прозрачно.</span><span class="sxs-lookup"><span data-stu-id="71830-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="71830-113">Хотя фигура с полностью прозрачным цветом строки выглядит так же, как фигура без линий на странице рисования, она будет взаимодействовать с другими объектами на странице так же, как если бы ее прозрачность составляет 0%.</span><span class="sxs-lookup"><span data-stu-id="71830-113">Although a shape with a completely transparent line color appears the same as a shape with no lines on the drawing page, it will interact with other objects on the page in the same ways as if its transparency is 0%.</span></span> 
  
<span data-ttu-id="71830-114">Это значение можно также задать с помощью управления ползунок в диалоговом окне **Line** (на вкладке **Главная,** в группе **Shape** щелкните Строка, указать на **вес,** а затем нажмите кнопку **Дополнительные строки).**</span><span class="sxs-lookup"><span data-stu-id="71830-114">You can also set this value by using the slider control in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="71830-115">Чтобы получить ссылку на ячейку LineColorTrans по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="71830-115">To get a reference to the LineColorTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71830-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="71830-116">Cell name:</span></span>  <br/> |<span data-ttu-id="71830-117">LineColorTrans</span><span class="sxs-lookup"><span data-stu-id="71830-117">LineColorTrans</span></span>  <br/> |
   
<span data-ttu-id="71830-118">Чтобы получить ссылку на ячейку LineColorTrans по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="71830-118">To get a reference to the LineColorTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="71830-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="71830-119">Section index:</span></span>  <br/> |<span data-ttu-id="71830-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="71830-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="71830-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="71830-121">Row index:</span></span>  <br/> |<span data-ttu-id="71830-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="71830-122">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="71830-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="71830-123">Cell index:</span></span>  <br/> |<span data-ttu-id="71830-124">**visLineColorTrans**</span><span class="sxs-lookup"><span data-stu-id="71830-124">**visLineColorTrans**</span></span> <br/> |
   

