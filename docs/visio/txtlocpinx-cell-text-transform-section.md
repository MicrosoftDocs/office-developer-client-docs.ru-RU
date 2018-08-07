---
title: Ячейка TxtLocPinX (раздел "Преобразование текста")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: 'Определяет значение x-координаты центра блок текста из ротации относительно начала блока текста. Формула по умолчанию имеет вид:'
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19815067"
---
# <a name="txtlocpinx-cell-text-transform-section"></a><span data-ttu-id="b3362-104">Ячейка TxtLocPinX (раздел "Преобразование текста")</span><span class="sxs-lookup"><span data-stu-id="b3362-104">TxtLocPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="b3362-105">Определяет значение *x* -координаты центра блок текста из ротации относительно начала блока текста.</span><span class="sxs-lookup"><span data-stu-id="b3362-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the text block.</span></span> <span data-ttu-id="b3362-106">Формула по умолчанию имеет вид:</span><span class="sxs-lookup"><span data-stu-id="b3362-106">The default formula is:</span></span> 
  
<span data-ttu-id="b3362-107">= ШиринаТекста \* 0,5</span><span class="sxs-lookup"><span data-stu-id="b3362-107">= TxtWidth \* 0.5</span></span>
  
<span data-ttu-id="b3362-108">Эту формулу вычисляется по горизонтали по центру блока текста.</span><span class="sxs-lookup"><span data-stu-id="b3362-108">This formula evaluates to the horizontal center of the text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b3362-109">Замечания</span><span class="sxs-lookup"><span data-stu-id="b3362-109">Remarks</span></span>

<span data-ttu-id="b3362-110">Чтобы получить ссылку на ячейку TxtLocPinX по имени из другой формулы, и программы, с помощью свойства **CellsU** , используйте следующую команду:</span><span class="sxs-lookup"><span data-stu-id="b3362-110">To get a reference to the TxtLocPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3362-111">Имя ячейки.</span><span class="sxs-lookup"><span data-stu-id="b3362-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b3362-112">TxtLocPinX</span><span class="sxs-lookup"><span data-stu-id="b3362-112">TxtLocPinX</span></span>  <br/> |
   
<span data-ttu-id="b3362-113">Для получения ссылки на ячейки TxtLocPinX по индексу из программы, используйте свойство **CellsSRC** с следующие аргументы:</span><span class="sxs-lookup"><span data-stu-id="b3362-113">To get a reference to the TxtLocPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b3362-114">Индекс раздела:</span><span class="sxs-lookup"><span data-stu-id="b3362-114">Section index:</span></span>  <br/> |<span data-ttu-id="b3362-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b3362-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b3362-116">Индекс строки:</span><span class="sxs-lookup"><span data-stu-id="b3362-116">Row index:</span></span>  <br/> |<span data-ttu-id="b3362-117">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="b3362-117">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="b3362-118">Индекс ячейки:</span><span class="sxs-lookup"><span data-stu-id="b3362-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b3362-119">**visXFormLocPinX**</span><span class="sxs-lookup"><span data-stu-id="b3362-119">**visXFormLocPinX**</span></span> <br/> |
   

