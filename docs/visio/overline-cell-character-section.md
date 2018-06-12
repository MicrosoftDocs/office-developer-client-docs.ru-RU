---
title: Надчеркивание ячейки (раздел знаков)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251728
localization_priority: Normal
ms.assetid: 102cce17-43ee-e313-3412-a72d6ee18fe6
description: Определяет, есть ли текст линия над текстом.
ms.openlocfilehash: 3ceb0f5bcb6f66098938e49ea5f176921d0c9808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814323"
---
# <a name="overline-cell-character-section"></a><span data-ttu-id="964f0-103">Надчеркивание ячейки (раздел знаков)</span><span class="sxs-lookup"><span data-stu-id="964f0-103">Overline Cell (Character Section)</span></span>

<span data-ttu-id="964f0-104">Определяет, есть ли текст линия над текстом.</span><span class="sxs-lookup"><span data-stu-id="964f0-104">Determines whether the text has a line above it.</span></span>
  
|<span data-ttu-id="964f0-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="964f0-105">**Value**</span></span>|<span data-ttu-id="964f0-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="964f0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="964f0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="964f0-107">TRUE</span></span>  <br/> |<span data-ttu-id="964f0-108">Текст имеет линия над текстом.</span><span class="sxs-lookup"><span data-stu-id="964f0-108">Text has a line above it.</span></span>  <br/> |
|<span data-ttu-id="964f0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="964f0-109">FALSE</span></span>  <br/> |<span data-ttu-id="964f0-110">Текст не имеет линия над текстом.</span><span class="sxs-lookup"><span data-stu-id="964f0-110">Text does not have a line above it.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="964f0-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="964f0-111">Remarks</span></span>

<span data-ttu-id="964f0-112">Можно также задать значение ячейки, используя диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ).</span><span class="sxs-lookup"><span data-stu-id="964f0-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="964f0-113">Для получения ссылки на ячейки надчеркивание по имени, из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="964f0-113">To get a reference to the Overline cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="964f0-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="964f0-114">Cell name:</span></span>  <br/> |<span data-ttu-id="964f0-115">Char.Overline [ *i* ] где *i* < 1 > = 2.</span><span class="sxs-lookup"><span data-stu-id="964f0-115">Char.Overline[ *i*  ] where  *i*  = <1>, 2.</span></span> <span data-ttu-id="964f0-116">3...</span><span class="sxs-lookup"><span data-stu-id="964f0-116">3...</span></span>  <br/> |
   
<span data-ttu-id="964f0-117">Для получения ссылки на ячейки надчеркивание по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="964f0-117">To get a reference to the Overline cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="964f0-118">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="964f0-118">Section index:</span></span>  <br/> |<span data-ttu-id="964f0-119">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="964f0-119">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="964f0-120">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="964f0-120">Row index:</span></span>  <br/> |<span data-ttu-id="964f0-121">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="964f0-121">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="964f0-122">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="964f0-122">Cell index:</span></span>  <br/> |<span data-ttu-id="964f0-123">**visCharacterOverline**</span><span class="sxs-lookup"><span data-stu-id="964f0-123">**visCharacterOverline**</span></span> <br/> |
   

