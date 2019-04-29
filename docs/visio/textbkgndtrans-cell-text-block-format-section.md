---
title: TextBkgndTrans Cell (Text Block Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Определяет уровень прозрачности для цвета фона блока текста фигуры.
ms.openlocfilehash: f4c4dc7700c553bd4c9bee337220e357c4c5538a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408693"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a><span data-ttu-id="07eeb-103">TextBkgndTrans Cell (Text Block Format Section)</span><span class="sxs-lookup"><span data-stu-id="07eeb-103">TextBkgndTrans Cell (Text Block Format Section)</span></span>

<span data-ttu-id="07eeb-104">Определяет уровень прозрачности для цвета фона блока текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="07eeb-104">Determines the transparency level for the background color of the shape's text block.</span></span>
  
|<span data-ttu-id="07eeb-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="07eeb-105">**Value**</span></span>|<span data-ttu-id="07eeb-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="07eeb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="07eeb-107">0-100</span><span class="sxs-lookup"><span data-stu-id="07eeb-107">0 - 100</span></span>  <br/> |<span data-ttu-id="07eeb-108">Представляет процент прозрачности.</span><span class="sxs-lookup"><span data-stu-id="07eeb-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="07eeb-109">Значение по умолчанию: 0% (полностью непрозрачно).</span><span class="sxs-lookup"><span data-stu-id="07eeb-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="07eeb-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="07eeb-110">Remarks</span></span>

<span data-ttu-id="07eeb-111">Значения округляются до ближайшей половины процентов.</span><span class="sxs-lookup"><span data-stu-id="07eeb-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="07eeb-112">Значение 100% полностью прозрачно.</span><span class="sxs-lookup"><span data-stu-id="07eeb-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="07eeb-113">Несмотря на то, что фигура с полностью прозрачным текстовым фоном отображается на странице документа как фигура без текста, она взаимодействует с другими объектами на странице так же, как если бы ее прозрачность была равна 0%.</span><span class="sxs-lookup"><span data-stu-id="07eeb-113">Although a shape that has a completely transparent text background appears the same on the drawing page as a shape that has no text background, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="07eeb-114">Это значение также можно задать с помощью ползунка на вкладке **Шрифт** диалогового окна **текст** (на вкладке **Главная** щелкните значок со стрелкой **шрифта** ).</span><span class="sxs-lookup"><span data-stu-id="07eeb-114">You can also set this value using the slider control on the **Font** tab of the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="07eeb-115">Чтобы получить ссылку на ячейку TextBkgndTrans по имени из другой формулы или из программы с помощью свойства **CellsU** , используйте следующее:</span><span class="sxs-lookup"><span data-stu-id="07eeb-115">To get a reference to the TextBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07eeb-116">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="07eeb-116">Cell name:</span></span>  <br/> |<span data-ttu-id="07eeb-117">TextBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="07eeb-117">TextBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="07eeb-118">Чтобы получить ссылку на ячейку TextBkgndTrans по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="07eeb-118">To get a reference to the TextBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07eeb-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="07eeb-119">Section index:</span></span>  <br/> |<span data-ttu-id="07eeb-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="07eeb-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="07eeb-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="07eeb-121">Row index:</span></span>  <br/> |<span data-ttu-id="07eeb-122">**Висровтекст**</span><span class="sxs-lookup"><span data-stu-id="07eeb-122">**visRowText**</span></span> <br/> |
|<span data-ttu-id="07eeb-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="07eeb-123">Cell index:</span></span>  <br/> |<span data-ttu-id="07eeb-124">**Висткстблкбкгндтранс**</span><span class="sxs-lookup"><span data-stu-id="07eeb-124">**visTxtBlkBkgndTrans**</span></span> <br/> |
   

