---
title: Strikethru Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm975
localization_priority: Normal
ms.assetid: b03b4415-0b1a-eb03-2b5e-373b39a0f07a
description: Определяет, форматирован ли текст в виде strikethrough.
ms.openlocfilehash: 4a58123814a4782c279a36d202e1293ec222ef93
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412431"
---
# <a name="strikethru-cell-character-section"></a><span data-ttu-id="d0b9f-103">Strikethru Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="d0b9f-103">Strikethru Cell (Character Section)</span></span>

<span data-ttu-id="d0b9f-104">Определяет, форматирован ли текст в виде strikethrough.</span><span class="sxs-lookup"><span data-stu-id="d0b9f-104">Determines whether the text is formatted as strikethrough.</span></span>
  
|<span data-ttu-id="d0b9f-105">**Значение**</span><span class="sxs-lookup"><span data-stu-id="d0b9f-105">**Value**</span></span>|<span data-ttu-id="d0b9f-106">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d0b9f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d0b9f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d0b9f-107">TRUE</span></span>  <br/> |<span data-ttu-id="d0b9f-108">Текст форматирован как strikethrough.</span><span class="sxs-lookup"><span data-stu-id="d0b9f-108">Text is formatted as strikethrough.</span></span>  <br/> |
|<span data-ttu-id="d0b9f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d0b9f-109">FALSE</span></span>  <br/> |<span data-ttu-id="d0b9f-110">Текст не форматирован как strikethrough.</span><span class="sxs-lookup"><span data-stu-id="d0b9f-110">Text is not formatted as strikethrough.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0b9f-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="d0b9f-111">Remarks</span></span>

<span data-ttu-id="d0b9f-112">Вы также можете установить значение этой ячейки с помощью диалогового окна **Text** (на вкладке **Главная** щелкните **стрелку Шрифта).**</span><span class="sxs-lookup"><span data-stu-id="d0b9f-112">You can also set the value of this cell by using the **Text** dialog box (on the **Home** tab, click the **Font** arrow).</span></span> 
  
<span data-ttu-id="d0b9f-113">Чтобы получить ссылку на ячейку Strikethru по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="d0b9f-113">To get a reference to the Strikethru cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0b9f-114">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="d0b9f-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d0b9f-115">Char.Strikethru[ *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d0b9f-115">Char.Strikethru[ *i*  ] where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d0b9f-116">Чтобы получить ссылку на ячейку Strikethru по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="d0b9f-116">To get a reference to the Strikethru cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d0b9f-117">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="d0b9f-117">Section index:</span></span>  <br/> |<span data-ttu-id="d0b9f-118">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="d0b9f-118">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="d0b9f-119">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="d0b9f-119">Row index:</span></span>  <br/> |<span data-ttu-id="d0b9f-120">**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="d0b9f-120">**visRowCharacter** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d0b9f-121">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="d0b9f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d0b9f-122">**visCharacterStrikethru**</span><span class="sxs-lookup"><span data-stu-id="d0b9f-122">**visCharacterStrikethru**</span></span> <br/> |
   

