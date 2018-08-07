---
title: Ячейка TextBkgndTrans (раздел "Формат текстового блока")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253240
localization_priority: Normal
ms.assetid: b2f9d317-cc42-bec5-66f9-f988bcbdcc24
description: Определяет уровень прозрачности цвета фона блока текста фигуры.
ms.openlocfilehash: d9fee430cb2ccd19e8d6069e7561a8fef409a62e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815005"
---
# <a name="textbkgndtrans-cell-text-block-format-section"></a><span data-ttu-id="40f65-103">Ячейка TextBkgndTrans (раздел "Формат текстового блока")</span><span class="sxs-lookup"><span data-stu-id="40f65-103">TextBkgndTrans Cell (Text Block Format Section)</span></span>

<span data-ttu-id="40f65-104">Определяет уровень прозрачности цвета фона блока текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="40f65-104">Determines the transparency level for the background color of the shape's text block.</span></span>
  
|<span data-ttu-id="40f65-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="40f65-105">**Value**</span></span>|<span data-ttu-id="40f65-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="40f65-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="40f65-107">0 — 100</span><span class="sxs-lookup"><span data-stu-id="40f65-107">0 - 100</span></span>  <br/> |<span data-ttu-id="40f65-108">Представляет собой процентную долю прозрачность.</span><span class="sxs-lookup"><span data-stu-id="40f65-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="40f65-109">Значение по умолчанию — 0% (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="40f65-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="40f65-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="40f65-110">Remarks</span></span>

<span data-ttu-id="40f65-111">Значения округляются до ближайшего большего половины процентов.</span><span class="sxs-lookup"><span data-stu-id="40f65-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="40f65-112">Значение 100% является полностью прозрачным.</span><span class="sxs-lookup"><span data-stu-id="40f65-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="40f65-113">Хотя фигуры, полностью прозрачным текст фон отображается на странице документа как фигуры, не содержит текст фона, взаимодействия с другие объекты на странице таким же образом, как если бы его прозрачность 0%.</span><span class="sxs-lookup"><span data-stu-id="40f65-113">Although a shape that has a completely transparent text background appears the same on the drawing page as a shape that has no text background, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="40f65-114">Также можно задать это значение, с помощью элемента управления ползунок на вкладке **Шрифт** диалоговое окно " **Text** " (на вкладке **Главная** щелкните стрелку **шрифтов** ).</span><span class="sxs-lookup"><span data-stu-id="40f65-114">You can also set this value using the slider control on the **Font** tab of the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="40f65-115">Чтобы получить ссылку на ячейку TextBkgndTrans по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="40f65-115">To get a reference to the TextBkgndTrans cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40f65-116">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="40f65-116">Cell name:</span></span>  <br/> |<span data-ttu-id="40f65-117">TextBkgndTrans</span><span class="sxs-lookup"><span data-stu-id="40f65-117">TextBkgndTrans</span></span>  <br/> |
   
<span data-ttu-id="40f65-118">Для получения ссылки на ячейки TextBkgndTrans по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="40f65-118">To get a reference to the TextBkgndTrans cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="40f65-119">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="40f65-119">Section index:</span></span>  <br/> |<span data-ttu-id="40f65-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="40f65-120">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="40f65-121">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="40f65-121">Row index:</span></span>  <br/> |<span data-ttu-id="40f65-122">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="40f65-122">**visRowText**</span></span> <br/> |
|<span data-ttu-id="40f65-123">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="40f65-123">Cell index:</span></span>  <br/> |<span data-ttu-id="40f65-124">**visTxtBlkBkgndTrans**</span><span class="sxs-lookup"><span data-stu-id="40f65-124">**visTxtBlkBkgndTrans**</span></span> <br/> |
   

