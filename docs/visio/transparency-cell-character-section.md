---
title: Transparency Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Определяет уровень прозрачности для диапазона цвета текста фигуры.
ms.openlocfilehash: 8619ec25372ae163fff1759aca36ff6693820e39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427838"
---
# <a name="transparency-cell-character-section"></a><span data-ttu-id="23bdd-103">Transparency Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="23bdd-103">Transparency Cell (Character Section)</span></span>

<span data-ttu-id="23bdd-104">Определяет уровень прозрачности для диапазона цвета текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="23bdd-104">Determines the transparency level for a range of a shape's text color.</span></span>
  
|<span data-ttu-id="23bdd-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="23bdd-105">**Value**</span></span>|<span data-ttu-id="23bdd-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="23bdd-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="23bdd-107">0 - 100</span><span class="sxs-lookup"><span data-stu-id="23bdd-107">0 - 100</span></span>  <br/> |<span data-ttu-id="23bdd-108">Представляет процент прозрачности.</span><span class="sxs-lookup"><span data-stu-id="23bdd-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="23bdd-109">Значение по умолчанию — 0 % (полностью непрозрачной).</span><span class="sxs-lookup"><span data-stu-id="23bdd-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23bdd-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="23bdd-110">Remarks</span></span>

<span data-ttu-id="23bdd-111">Значения округлются до ближайшей половины процента.</span><span class="sxs-lookup"><span data-stu-id="23bdd-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="23bdd-112">Значение 100% полностью прозрачно.</span><span class="sxs-lookup"><span data-stu-id="23bdd-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="23bdd-113">Хотя фигура с полностью прозрачным текстом отображается на странице документа так же, как фигура без текста, она взаимодействует с другими объектами на странице так же, как если бы ее прозрачность была 0%.</span><span class="sxs-lookup"><span data-stu-id="23bdd-113">Although a shape that has completely transparent text appears the same on the drawing page as a shape that has no text, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="23bdd-114">Это значение также можно установить с помощью ползунок  на вкладке **"Шрифт"** в диалоговом окне "Текст" (на вкладке "Главная" щелкните стрелку **шрифта).** </span><span class="sxs-lookup"><span data-stu-id="23bdd-114">You can also set this value by using the slider control on the **Font** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="23bdd-115">Если раздел "Символы" содержит несколько строк, ячейка Transparency содержит сведения о форматированиях, применяемые к поддиаплю текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="23bdd-115">If the Characters section contains multiple rows, the Transparency cell contains formatting information applied to a sub-range of a shape's text.</span></span> <span data-ttu-id="23bdd-116">В противном случае он содержит сведения о формате для всего текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="23bdd-116">Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="23bdd-117">Чтобы получить ссылку на ячейку Transparency по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="23bdd-117">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23bdd-118">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="23bdd-118">Cell name:</span></span>  <br/> |<span data-ttu-id="23bdd-119">Char.ColorTrans[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="23bdd-119">Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="23bdd-120">Чтобы получить ссылку на ячейку Transparency по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="23bdd-120">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23bdd-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="23bdd-121">Section index:</span></span>  <br/> |<span data-ttu-id="23bdd-122">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="23bdd-122">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="23bdd-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="23bdd-123">Row index:</span></span>  <br/> |<span data-ttu-id="23bdd-124">**visRowCharacter**  +   *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="23bdd-124">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="23bdd-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="23bdd-125">Cell index:</span></span>  <br/> |<span data-ttu-id="23bdd-126">**visCharacterColorTrans**</span><span class="sxs-lookup"><span data-stu-id="23bdd-126">**visCharacterColorTrans**</span></span> <br/> |
   

