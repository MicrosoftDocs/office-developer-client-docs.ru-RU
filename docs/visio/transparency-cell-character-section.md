---
title: Ячейка Transparency (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm50135
localization_priority: Normal
ms.assetid: ab835a1a-9e90-126e-279f-463882c48e93
description: Определяет уровень прозрачности для диапазона цвет текста фигуры.
ms.openlocfilehash: 5914a061b1bba2173b338544b05abda8780ff164
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815049"
---
# <a name="transparency-cell-character-section"></a><span data-ttu-id="2d03b-103">Ячейка Transparency (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="2d03b-103">Transparency Cell (Character Section)</span></span>

<span data-ttu-id="2d03b-104">Определяет уровень прозрачности для диапазона цвет текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="2d03b-104">Determines the transparency level for a range of a shape's text color.</span></span>
  
|<span data-ttu-id="2d03b-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="2d03b-105">**Value**</span></span>|<span data-ttu-id="2d03b-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="2d03b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d03b-107">0 — 100</span><span class="sxs-lookup"><span data-stu-id="2d03b-107">0 - 100</span></span>  <br/> |<span data-ttu-id="2d03b-108">Представляет собой процентную долю прозрачность.</span><span class="sxs-lookup"><span data-stu-id="2d03b-108">Represents the percentage of transparency.</span></span> <span data-ttu-id="2d03b-109">Значение по умолчанию — 0% (полностью непрозрачный).</span><span class="sxs-lookup"><span data-stu-id="2d03b-109">The default is 0% (completely opaque).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d03b-110">Замечания</span><span class="sxs-lookup"><span data-stu-id="2d03b-110">Remarks</span></span>

<span data-ttu-id="2d03b-111">Значения округляются до ближайшего большего половины процентов.</span><span class="sxs-lookup"><span data-stu-id="2d03b-111">Values are rounded to the nearest half percent.</span></span> <span data-ttu-id="2d03b-112">Значение 100% является полностью прозрачным.</span><span class="sxs-lookup"><span data-stu-id="2d03b-112">A value of 100% is completely transparent.</span></span> <span data-ttu-id="2d03b-113">Хотя фигуры, полностью прозрачным текст отображается на странице документа как фигуры, которая не содержит текста, взаимодействия с другие объекты на странице таким же образом, как если бы его прозрачность 0%.</span><span class="sxs-lookup"><span data-stu-id="2d03b-113">Although a shape that has completely transparent text appears the same on the drawing page as a shape that has no text, it interacts with other objects on the page in the same way as if its transparency were 0%.</span></span>
  
<span data-ttu-id="2d03b-114">Также можно задать это значение с помощью ползунка на вкладке « **Шрифт** » в диалоговое окно " **Text** " (на вкладке **Главная** щелкните стрелку **шрифтов** ).</span><span class="sxs-lookup"><span data-stu-id="2d03b-114">You can also set this value by using the slider control on the **Font** tab in the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="2d03b-115">Если раздел символов содержит несколько строк, ячейка прозрачность содержит сведения о форматировании, применяемые к поддиапазона текстом фигуры.</span><span class="sxs-lookup"><span data-stu-id="2d03b-115">If the Characters section contains multiple rows, the Transparency cell contains formatting information applied to a sub-range of a shape's text.</span></span> <span data-ttu-id="2d03b-116">В противном случае содержит сведения о форматировании для всех текста фигуры.</span><span class="sxs-lookup"><span data-stu-id="2d03b-116">Otherwise, it contains formatting information for all of the shape's text.</span></span>
  
<span data-ttu-id="2d03b-117">Чтобы получить ссылку на ячейку прозрачность по имени из другой формулы или из файла с помощью свойства **CellsU** , используйте:</span><span class="sxs-lookup"><span data-stu-id="2d03b-117">To get a reference to the Transparency cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d03b-118">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="2d03b-118">Cell name:</span></span>  <br/> |<span data-ttu-id="2d03b-119">Char.ColorTrans [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2d03b-119">Char.ColorTrans[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2d03b-120">Для получения ссылки на ячейки прозрачность по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="2d03b-120">To get a reference to the Transparency cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2d03b-121">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="2d03b-121">Section index:</span></span>  <br/> |<span data-ttu-id="2d03b-122">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="2d03b-122">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="2d03b-123">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="2d03b-123">Row index:</span></span>  <br/> |<span data-ttu-id="2d03b-124">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2d03b-124">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="2d03b-125">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="2d03b-125">Cell index:</span></span>  <br/> |<span data-ttu-id="2d03b-126">**visCharacterColorTrans**</span><span class="sxs-lookup"><span data-stu-id="2d03b-126">**visCharacterColorTrans**</span></span> <br/> |
   

