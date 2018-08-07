---
title: Ячейка Strikethru (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Определяет, является ли текст зачеркивание.
ms.openlocfilehash: 2b25d1d9b00d062214c02c3fc7b14569b43a5110
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19814962"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="d338b-103">Ячейка Strikethru (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="d338b-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="d338b-104">Определяет, является ли текст зачеркивание.</span><span class="sxs-lookup"><span data-stu-id="d338b-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="d338b-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d338b-105">**Value**</span></span>|<span data-ttu-id="d338b-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d338b-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d338b-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d338b-107">TRUE</span></span>  <br/> |<span data-ttu-id="d338b-108">Текст форматируется как зачеркивание.</span><span class="sxs-lookup"><span data-stu-id="d338b-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="d338b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d338b-109">FALSE</span></span>  <br/> |<span data-ttu-id="d338b-110">Текст не формате зачеркивание.</span><span class="sxs-lookup"><span data-stu-id="d338b-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d338b-111">Замечания</span><span class="sxs-lookup"><span data-stu-id="d338b-111">Remarks</span></span>

<span data-ttu-id="d338b-112">Можно также задать значение ячейки, используя диалоговое окно " **текст** " (на вкладке **Главная** щелкните стрелку **шрифтов** ).</span><span class="sxs-lookup"><span data-stu-id="d338b-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="d338b-113">Чтобы получить ссылку на ячейку Strikethru по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="d338b-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d338b-114">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="d338b-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d338b-115">Char.Strikethru [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d338b-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d338b-116">Для получения ссылки на ячейки Strikethru по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="d338b-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d338b-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d338b-117">Section index:</span></span>  <br/> |<span data-ttu-id="d338b-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d338b-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d338b-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d338b-119">Row index:</span></span>  <br/> |<span data-ttu-id="d338b-120">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d338b-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d338b-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d338b-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d338b-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="d338b-122">**visCharacterStrikethru**</span></span> <br/> |
   

