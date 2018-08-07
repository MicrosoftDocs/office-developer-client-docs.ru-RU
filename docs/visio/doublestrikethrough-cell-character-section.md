---
title: Ячейка DoubleStrikethrough (раздел "Символ")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Определяет, является ли текст Двойное зачеркивание.
ms.openlocfilehash: dcd7c7769da8298c1f6ab474d2b63fc982f479b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813655"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="1d019-103">Ячейка DoubleStrikethrough (раздел "Символ")</span><span class="sxs-lookup"><span data-stu-id="1d019-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="1d019-104">Определяет, является ли текст Двойное зачеркивание.</span><span class="sxs-lookup"><span data-stu-id="1d019-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1d019-105">Замечания</span><span class="sxs-lookup"><span data-stu-id="1d019-105">Remarks</span></span>

<span data-ttu-id="1d019-106">Чтобы получить ссылку на ячейку DoubleStrikethrough по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="1d019-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1d019-107">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="1d019-107">Cell name:</span></span>  <br/> | <span data-ttu-id="1d019-108">Char.DoubleStrikethrough [ *i* ] где *i* = < 1 > 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1d019-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1d019-109">Для получения ссылки на ячейки DoubleStrikethrough по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="1d019-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1d019-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="1d019-110">Section index:</span></span>  <br/> |<span data-ttu-id="1d019-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="1d019-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="1d019-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="1d019-112">Row index:</span></span>  <br/> |<span data-ttu-id="1d019-113">**visRowCharacter** +  *i* где *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1d019-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1d019-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="1d019-114">Cell index:</span></span>  <br/> |<span data-ttu-id="1d019-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="1d019-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

