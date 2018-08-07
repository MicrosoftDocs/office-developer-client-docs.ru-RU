---
title: Ячейка TxtHeight (раздел "Преобразование текста")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: 'Определяет высоту блока текста. Формула по умолчанию имеет вид:'
ms.openlocfilehash: e9495eef837a61fa9b7ecb2b242fdabc5df30080
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815080"
---
# <a name="txtheight-cell-text-transform-section"></a><span data-ttu-id="43087-104">Ячейка TxtHeight (раздел "Преобразование текста")</span><span class="sxs-lookup"><span data-stu-id="43087-104">TxtHeight Cell (Text Transform Section)</span></span>

<span data-ttu-id="43087-105">Определяет высоту блока текста.</span><span class="sxs-lookup"><span data-stu-id="43087-105">Determines the height of the text block.</span></span> <span data-ttu-id="43087-106">Формула по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="43087-106">The default formula is:</span></span>
  
<span data-ttu-id="43087-107">= Высота \* 1</span><span class="sxs-lookup"><span data-stu-id="43087-107">= Height \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="43087-108">Замечания</span><span class="sxs-lookup"><span data-stu-id="43087-108">Remarks</span></span>

<span data-ttu-id="43087-109">Чтобы получить ссылку на ячейку ВысотаТекста по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="43087-109">To get a reference to the TxtHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="43087-110">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="43087-110">Cell name:</span></span>  <br/> | <span data-ttu-id="43087-111">ВысотаТекста</span><span class="sxs-lookup"><span data-stu-id="43087-111">TxtHeight</span></span>  <br/> |
   
<span data-ttu-id="43087-112">Для получения ссылки на ячейки ВысотаТекста по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="43087-112">To get a reference to the TxtHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="43087-113">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="43087-113">Section index:</span></span>  <br/> |<span data-ttu-id="43087-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="43087-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="43087-115">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="43087-115">Row index:</span></span>  <br/> |<span data-ttu-id="43087-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="43087-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="43087-117">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="43087-117">Cell index:</span></span>  <br/> |<span data-ttu-id="43087-118">**visXFormHeight**</span><span class="sxs-lookup"><span data-stu-id="43087-118">**visXFormHeight**</span></span> <br/> |
   

