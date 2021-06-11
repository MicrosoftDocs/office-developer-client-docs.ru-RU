---
title: DoubleStrikethrough Cell (Character Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033762
localization_priority: Normal
ms.assetid: c48a77e1-ea3c-7a6d-8c05-f9e0cb434cda
description: Определяет, форматирован ли текст в виде двойного забастовки.
ms.openlocfilehash: d8ef5bdb6e086be9657f51c66c10d578414e1deb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360594"
---
# <a name="doublestrikethrough-cell-character-section"></a><span data-ttu-id="eb643-103">DoubleStrikethrough Cell (Character Section)</span><span class="sxs-lookup"><span data-stu-id="eb643-103">DoubleStrikethrough Cell (Character Section)</span></span>

<span data-ttu-id="eb643-104">Определяет, форматирован ли текст в виде двойного забастовки.</span><span class="sxs-lookup"><span data-stu-id="eb643-104">Determines whether text is formatted as double strikethrough.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="eb643-105">Примечания</span><span class="sxs-lookup"><span data-stu-id="eb643-105">Remarks</span></span>

<span data-ttu-id="eb643-106">Чтобы получить ссылку на ячейку DoubleStrikethrough по имени из другой формулы или из программы с помощью свойства **CellsU,** используйте:</span><span class="sxs-lookup"><span data-stu-id="eb643-106">To get a reference to the DoubleStrikethrough cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb643-107">Имя ячейки:</span><span class="sxs-lookup"><span data-stu-id="eb643-107">Cell name:</span></span>  <br/> | <span data-ttu-id="eb643-108">Char.DoubleStrikethrough[  *i*  ] где  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="eb643-108">Char.DoubleStrikethrough[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="eb643-109">Чтобы получить ссылку на ячейку DoubleStrikethrough по индексу из программы, используйте свойство **CellsSRC** со следующими аргументами:</span><span class="sxs-lookup"><span data-stu-id="eb643-109">To get a reference to the DoubleStrikethrough cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="eb643-110">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="eb643-110">Section index:</span></span>  <br/> |<span data-ttu-id="eb643-111">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="eb643-111">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="eb643-112">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="eb643-112">Row index:</span></span>  <br/> |<span data-ttu-id="eb643-113">**visRowCharacter**  +   *i,* *где i* = 0, 1, 2 ...</span><span class="sxs-lookup"><span data-stu-id="eb643-113">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="eb643-114">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="eb643-114">Cell index:</span></span>  <br/> |<span data-ttu-id="eb643-115">**visCharacterDoubleStrikethrough**</span><span class="sxs-lookup"><span data-stu-id="eb643-115">**visCharacterDoubleStrikethrough**</span></span> <br/> |
   

