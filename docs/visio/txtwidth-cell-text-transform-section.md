---
title: Ячейка ШиринаТекста (раздел Преобразование текст)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Определяет ширину блока текста. Формула по умолчанию имеет вид:'
ms.openlocfilehash: ecba66aaf1f7eeb6d16c6b0d4c6569aed051910f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815100"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="c20e4-104">Ячейка ШиринаТекста (раздел Преобразование текст)</span><span class="sxs-lookup"><span data-stu-id="c20e4-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="c20e4-105">Определяет ширину блока текста.</span><span class="sxs-lookup"><span data-stu-id="c20e4-105">Determines the width of the text block.</span></span> <span data-ttu-id="c20e4-106">Формула по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="c20e4-106">The default formula is:</span></span>
  
<span data-ttu-id="c20e4-107">= Ширина \* 1</span><span class="sxs-lookup"><span data-stu-id="c20e4-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c20e4-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="c20e4-108">Remarks</span></span>

<span data-ttu-id="c20e4-109">Чтобы получить ссылку на ячейку ШиринаТекста по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="c20e4-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c20e4-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="c20e4-110">Cell name:</span></span>  <br/> | <span data-ttu-id="c20e4-111">ШиринаТекста</span><span class="sxs-lookup"><span data-stu-id="c20e4-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="c20e4-112">Для получения ссылки на ячейки ШиринаТекста по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="c20e4-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c20e4-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="c20e4-113">Section index:</span></span>  <br/> |<span data-ttu-id="c20e4-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c20e4-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c20e4-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="c20e4-115">Row index:</span></span>  <br/> |<span data-ttu-id="c20e4-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="c20e4-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="c20e4-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="c20e4-117">Cell index:</span></span>  <br/> |<span data-ttu-id="c20e4-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="c20e4-118">**visXFormWidth**</span></span> <br/> |
   

