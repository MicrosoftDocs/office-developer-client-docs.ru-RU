---
title: Ячейка TextPosAfterBullet (раздел абзаца)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: Представляет расстояние между первой строкой абзаца и маркером.
ms.openlocfilehash: fe22b81113ab6537922ad4627aa53f34f2e62c48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815008"
---
# <a name="textposafterbullet-cell-paragraph-section"></a><span data-ttu-id="7445c-103">Ячейка TextPosAfterBullet (раздел абзаца)</span><span class="sxs-lookup"><span data-stu-id="7445c-103">TextPosAfterBullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="7445c-104">Представляет расстояние между первой строкой абзаца и маркером.</span><span class="sxs-lookup"><span data-stu-id="7445c-104">Represents the distance between the first line of the paragraph and the bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="7445c-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="7445c-105">Remarks</span></span>

<span data-ttu-id="7445c-106">Это расстояние добавляется расстояние, содержащихся в ячейке IndFirst, который является отступа по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7445c-106">This distance is added to the distance contained in the IndFirst cell, which is the default left indent.</span></span> <span data-ttu-id="7445c-107">Это значение не зависит от масштаба документа.</span><span class="sxs-lookup"><span data-stu-id="7445c-107">This value is independent of the scale of the drawing.</span></span> 
  
<span data-ttu-id="7445c-108">Чтобы получить ссылку на ячейку TextPosAfterBullet по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="7445c-108">To get a reference to the TextPosAfterBullet cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7445c-109">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="7445c-109">Cell name:</span></span>  <br/> | <span data-ttu-id="7445c-110">Para.TextPosAfterBullet [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="7445c-110">Para.TextPosAfterBullet[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7445c-111">Для получения ссылки на ячейки TextPosAfterBullet по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="7445c-111">To get a reference to the TextPosAfterBullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7445c-112">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="7445c-112">Section index:</span></span>  <br/> |<span data-ttu-id="7445c-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="7445c-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="7445c-114">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="7445c-114">Row index:</span></span>  <br/> |<span data-ttu-id="7445c-115">**visRowParagraph** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7445c-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7445c-116">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="7445c-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7445c-117">**visTextPosAfterBullet**</span><span class="sxs-lookup"><span data-stu-id="7445c-117">**visTextPosAfterBullet**</span></span> <br/> |
   

